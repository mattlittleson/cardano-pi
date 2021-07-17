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
