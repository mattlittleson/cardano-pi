---
parent: Raspberry Pi 4
layout: default
title: Users (optional)
nav_order: 2
---

# Additional information on Users
The default user is `ubuntu`  
If you want to rename or change the user, use the following guides:

## Adding a new user
1. Log in as the root user.
{% highlight bash %}
sudo su
{% endhighlight %}

2. Add a new user
{% highlight bash %}
adduser username
{% endhighlight %}
- Set a strong password
- Fill in user data (or just accept defaults)

3. Add "username" to the sudo group with usermod
{% highlight bash %}
usermod -aG sudo username
{% endhighlight %}

4. (optional) - Test sudo access
- Switch to the new user account
  {% highlight bash %}su - username{% endhighlight %}
- Run a command usually only accessible to the root user
  {% highlight bash %}sudo ls -la /root{% endhighlight %}

## Renaming a user
{% highlight bash %}
usermod -l login-name old-name
{% endhighlight %}
(This will not rename `/home/old-name`)

## Deleting a user
{% highlight bash %}
sudo deluser --remove-home newuser
{% endhighlight %}
