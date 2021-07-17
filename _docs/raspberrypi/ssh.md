---
parent: Raspberry Pi 4
layout: default
title: SSH
nav_order: 4
---

1 - Generate ssh keys on your local machine with
{% highlight bash %}
ssh-keygen
{% endhighlight %}

2 - Copy your public key into remote
{% highlight bash %}
cat ~/.ssh/id_rsa.pub | ssh username@remote_host "mkdir -p ~/.ssh && cat >> ~/.ssh/authorized_keys"
{% endhighlight %}

3 - Disable password login & root login

{% highlight bash %}
sudo nano /etc/ssh/sshd_config
{% endhighlight %}

Change all these fields to no

{% highlight bash %}
ChallengeResponseAuthentication no
PasswordAuthentication no
UsePAM no
PermitRootLogin no
{% endhighlight %}

4 - Apply changes
{% highlight bash %}
sudo systemctl reload ssh
{% endhighlight %}
