---
parent: Raspberry Pi 4
layout: default
title: Hostname (recommended)
nav_order: 2
---

# Changing the hostname

The default hostname is `ubuntu`,
to make things less confusing while `ssh`ing into each pi, lets change the hostnames

## Change a new user

1 - Edit hostname file

{% highlight bash %}
sudo nano /etc/hostname
{% endhighlight %}

- replace `ubuntu` with your prefered hostname
- I use `relay1` and `block` for the relay and block nodes

2 - Edit hosts file

{% highlight bash %}
sudo nano /etc/hosts
{% endhighlight %}

- replace `ubuntu` with the same prefered hostname
- there shouldn't be any instances of `ubuntu` in this file, however check just in case

3 - Reboot

{% highlight bash %}
sudo shutdown -r now
{% endhighlight %}
