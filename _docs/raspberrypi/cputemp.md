---
parent: Raspberry Pi 4
layout: default
title: CPU Temp
nav_order: 4
---

# Getting the CPU temp
[Thanks to this Forum Post][forum]{:target="_blank"}

a - Make a bash script
{% highlight bash %}
#!/bin/bash

temp=$(</sys/class/thermal/thermal_zone0/temp)

temp_f=`echo "$temp/1000" | bc -l`
printf "CPU Temp: %.3f°C\n"  $temp_f
{% endhighlight %}

b - Compile c program
{% highlight c %}
# temp.c
#include <stdio.h>
int main() {
 FILE *fp;

   int temp = 0;
   fp = fopen("/sys/class/thermal/thermal_zone0/temp", "r");
   fscanf(fp, "%d", &temp);
   printf(">> CPU Temp: %.2f°C\n", temp / 1000.0);
   fclose(fp);

   return 0;
}
{% endhighlight %}

{% highlight bash %}
gcc temp.c -o temp
{% endhighlight %}

{% highlight bash %}
sudo mv ./temp /usr/local/bin/
{% endhighlight %}

[forum]: https://www.coincashew.com/coins/overview-ada/guide-how-to-build-a-haskell-stakepool-node



