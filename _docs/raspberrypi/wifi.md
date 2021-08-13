---
parent: Raspberry Pi 4
layout: default
title: Wifi
nav_order: 3
---

1 - Identify the wifi card name, for this example it's `wlan0`

{% highlight bash %}
ls /sys/class/net
{% endhighlight %}

{% highlight bash %}
eth0 lo wlan0
{% endhighlight %}

2 - Add the wifi network to the netplan config

{% highlight bash %}
sudo nano /etc/netplan/50-cloud-init.yaml
{% endhighlight %}

Fill in `SSID` and `password` with your own credentials

{% highlight yaml %}

```
# example /etc/netplan/50-cloud-init.yaml
network:
    ethernets:
        eth0:
            dhcp4: true
            optional: true
    version: 2
    wifis:
        wlan0:
            optional: true
            access-points:
                "SSID":
                    password: "password"
            dhcp4: true
# end
```

{% endhighlight %}


3 - Test the config file for syntax errors
{% highlight bash %}
netplan apply
{% endhighlight %}

- If you get a permission denied error, great! The file was parsed correctly.


4 - Changes to `/etc/netplan/50-cloud-init.yaml` will not persist across an instance reboot. To disable cloud-init's network configuration capabilities

{% highlight bash %}
sudo nano /etc/cloud/cloud.cfg.d/99-disable-network-config.cfg
{% endhighlight %}
and write the following:
{% highlight cfg %}
network: {config: disabled}
{% endhighlight %}

5 - Reboot
{% highlight bash %}
sudo shutdown -r now
{% endhighlight %}
