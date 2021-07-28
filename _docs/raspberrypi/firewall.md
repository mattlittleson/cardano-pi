---
parent: Raspberry Pi 4
layout: default
title: Firewall
nav_order: 5
---

1 - Enable UFW and allow SSH
{% highlight bash %}
sudo ufw app list
sudo ufw allow OpenSSH
sudo ufw enable
sudo ufw status
{% endhighlight %}



2 - allow connections from block -> relay node
{% highlight bash %}
sudo ufw allow from <relaynode ip address> proto tcp to any port 6000
{% endhighlight %}


3 - allow connections from relay node -> block
{% highlight bash %}
sudo ufw allow from <block ip address> proto tcp to any port 6000
{% endhighlight %}

