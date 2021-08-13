---
parent: Setting up Cardano
layout: default
title: LLVM
nav_order: 2
---

# LLVM

compilation requires `llvm-9`

{% highlight bash %}
sudo apt-get update -y
sudo apt-get upgrade -y
sudo apt-get install llvm llvm-9
{% endhighlight %}

Edit `.bashrc`
{% highlight bash %}
nano ~/.bashrc
{% endhighlight %}

Add this to the end of `.bashrc`

{% highlight bash %}
export PATH=/usr/lib/llvm-9/bin:$PATH
export CPLUS_INCLUDE_PATH=$(llvm-config --includedir):$CPLUS_INCLUDE_PATH
export LD_LIBRARY_PATH=$(llvm-config --libdir):$LD_LIBRARY_PATH
{% endhighlight %}
