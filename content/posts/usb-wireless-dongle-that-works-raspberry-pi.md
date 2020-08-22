--- 
date: 2020-08-23T17:08:13+08:00
title: "USB Wireless Dongle that Works in Raspberry Pi"
tags: [wifi, raspberry-pi, wifi-dongle, linux]
draft: false
--- 

I had my first raspberry pi way back 2015 but I never get to use it. Back then, that single-board computer doesn't have a built-in wireless interface.
Past forward 2020 and I bought a new PI on Lazada without checking on the specs...so I got a wifi dongle as well.

My pi arrived first and after thoroughly reading the specs, I laughed at myself for buying something that I may never need. 
Well, I can no longer cancel the order so I nothing more I can do. It's costs PHP 299.00 including shipping.

When the dongle arrived, I had no expectations. Included in the item was a little cd which I assume is the driver. 
<insert_here_dongle_item_pic>
![Boxed USB Wireless Dongle Item](/static/image/usb_wireless_dongle_boxed.jpg)
![Close-up Look of the USB Wireless Dongle](/static/image/usb_wireless_dongle_closeup.png)


I never used the CD as I don't think it would come with a Linux driver. So I plugged it in the raspberry pi and saw this:
```
root@raspberrypi:/home/pi# lsusb
Bus 002 Device 001: ID 1d6b:0003 Linux Foundation 3.0 root hub
Bus 001 Device 003: ID 148f:7601 Ralink Technology, Corp. MT7601U Wireless Adapter
Bus 001 Device 002: ID 2109:3431 VIA Labs, Inc. Hub
Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
```
2nd row of the output is the wireless adaptor:
```
Bus 001 Device 003: ID 148f:7601 Ralink Technology, Corp. MT7601U Wireless Adapter
```
Checked from LanScan and it's detected:
<insert_here_lanscan_pic>

Checking from CLI, I'm getting IP addressess assigned to two wireless interfaces: wlan0 which is the one that comes with the Rasperry pi and wlan1 which is the external wireless dongle.
<insert_ifconfig_pic>
<insert_connected_to_wifi_router>

<TBD>

