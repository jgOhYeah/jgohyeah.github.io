---
layout: post
title:  "Dashcam hacking"
date:   2024-01-30 00:00:00 +1100
categories: electronics
tags: electronics angular hacking linux typescript webdevelopment
thumbnail: "/assets/images/2024-01-13-dashcam.jpg"
---

Like many IoT devices, Dad's dashcam is *highly customisable* in ways that the manufacturer may not have originally intended.

## GPS repairs
The GPS on Dad's dashcam never quite worked reliably. After some investigations, we found that the GPS module built into the power cable could not find enough satellites to gain a fix.

The camera is powered via a micro-USB connector. Instead of using USB signalling, the provided cable contains a GPS module that sends NMEA strings using the data wires as a UART serial port.

Because of the relatively standard interface and voltages for GPS modules, Dad and I were able to swap out the faulty module for a [ublox neo 6m module](https://www.u-blox.com/en/product/neo-6-series) on a breakout board with voltage regulator and level shifting built in.

{%- include captioned-image.html src="https://core-electronics.com.au/media/catalog/product/cache/d5cf359726a1656c2b36f3682d3bbc67/0/1/018-gy-gps6mv2-2.jpg" alt="A similar module to the new one we installed. Image source: Core Electronics" -%}

## Root access and automatic startup sounds
This camera runs a version of Linux. It doesn't have a screen and instead hosts its own Wi-Fi network that allows it to be controlled using a phone app. Because the camera is the access point of the network, it isn't configured to or expected to be connected to the internet. The manufacturer left in enough convenient debugging features that gaining a root shell is not hard. What's more is that the root file system is writable and has some free space! I found that the camera uses busy box for most of its commands and includes the ash shell and a version of AWK.

After some trial and error, I have ended up creating an AWK file that runs on boot. On specific days it will link the startup sound to relevant files (Happy Birthday, Christmas Carols...). For other days the camera checks its last known location and applies some simple rules to choose a sound based on this.

All file and link modification each boot is done in RAM to reduce wear on the flash memory. I eventually ended up with too many sound files to fit in the internal flash and had to place them on the SD card instead.

## Dashcam viewer webpage
After playing around with the dashcam on long trips with family, I found that the camera has an HTTP server that serves the root of the SD card. By default, the web server generates a directory listing for each folder. If a file named index.html is added, it will serve this instead.

The dashcam viewer is a web page written using angular that allows convenient browsing of the saved files on the camera. It runs entirely in the user's web browser and doesn't require any server side scripting. It requests and interprets the directory listings to obtain the videos, thumbnails and GPS records on the system.

{%- include github-bookmark.html name="Dashcam Viewer Webpage" description="This is a web interface for a dashcam (Kaiser Bass R50), written using Angular. It is designed to be hosted by the dashcam itself." url="https://github.com/jgOhYeah/dashcam-viewer/"-%}

A demonstration with scaled down videos is available [here](https://jgohyeah.github.io/dashcam-viewer/).

<iframe src="https://jgohyeah.github.io/dashcam-viewer/" class="webpage-iframe"></iframe>