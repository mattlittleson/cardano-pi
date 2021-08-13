---
parent: Raspberry Pi 4
layout: default
title: Install Ubuntu 21.04
nav_order: 1
---

# Installing Ubuntu 21.04 arm64

## Raspberry Pi Imager

### Enable USB Boot

If booting from an external USB device, flash the Raspberry Pi bootloader to boot from USB's.

Format your micro SD card with [Raspberry Pi Imager][raspi-imager]

`Misc utility images > Bootloader > USB Boot`

Load the SD card into the pi and boot, 
wait for a solid green color on the monitor 
OR until the green led indicator on the Pi is a steady flash. 

### Get Ubuntu

Format your micro SD card with [Raspberry Pi Imager][raspi-imager]

`OS > Other general purpose OS > Ubuntu >`

```
Ubuntu Server 21.04
64bit server OS for arm64 architectures
```

## Manual Download

Download the image at [Ubuntu 64bit for arm64 architectures][raspi-ubuntu]

## Default Login

Username: `ubuntu`  
Password: `ubuntu`

[raspi-imager]: https://www.raspberrypi.org/software/
[raspi-ubuntu]: https://ubuntu.com/download/raspberry-pi
