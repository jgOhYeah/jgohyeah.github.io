---
layout: post
title: "Farm sensor network"
date: 2023-11-05 00:00:00 +1100
categories: farm
tags: farm pjon lora picaxe arduino esp32 "raspberry pi" thingsboard IOT university microcontrollers
thumbnail: "https://github.com/jgOhYeah/Farm-PJON-LoRa-network/blob/main/Pictures/BatteryMonitor.jpg?raw=true"
---

On our family farm I have set up a network of remote sensors to assist with the monitoring of various pieces of equipment and to be on the lookout for any potential issues or ways to improve productivity. This sensor network uses the [PJON](https://github.com/gioblu/PJON) protocol over LoRa radio to communicate. Back at the house, a base station receives messages from the sensors and passes them on to a [Thingsboard](https://thingsboard.io/) dashboard where the data is displayed and managed. The base station can also transmit commands back to the sensors as required.

The current sensors and devices include:
- Battery voltage monitoring and remote control of a solar electric fence.
- Monitoring the time that the main pressure pump spends running and how often it starts to detect water leaks.
- A "water baby" that sends alerts when water has reached particular points in the paddock when irrigating.

Planned additions include:
- Remote monitoring of the [tractor used to power the irrigation pump]({% link _posts/2023-11-06-farm-tractor-watchdog.md %}).

{%- include captioned-image.html src="/assets/images/2023-06-27-thingsboard.png" alt="Screenshots from the Thinsboard dashboard." -%}

## Current (ESP32 based) base station
I snuck this in as part of a FIT3146 assignment at uni and have added a bit to it since. Doxygen documentation is available [here](https://jgohyeah.github.io/FarmBaseStation/).

{%- include github-bookmark.html name="FarmBaseStation" description="Base station for connecting remote sensors to Thingsboard." url="https://github.com/jgOhYeah/FarmBaseStation"-%}

{%- include captioned-image.html src="https://github.com/jgOhYeah/FarmBaseStation/blob/main/Photos/Completed.jpg?raw=true" alt="The base station disguised." -%}

### Demonstation
A short demonstration video of the base station:
<iframe class="embedded-16by9" src="https://www.youtube-nocookie.com/embed/4jaKtZgRFBU?si=QCZzqgoIEKC1PZCp&amp;start=39" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Sensors and original base station
These sensors mainly use [PICAXE](https://picaxe.com/) microcontrollers as they were what I had on hand to build them. They are programmed using BASIC and I had to translate the drivers for the LoRa radios and PJON from their respective Arduino libraries.

{%- include github-bookmark.html name="Farm-PJON-LoRa-network" description="Code relating to a small LoRa network for remote monitoring and control. This is a work in progress." url="https://github.com/jgOhYeah/Farm-PJON-LoRa-network"-%}

{%- include captioned-image.html src="https://github.com/jgOhYeah/Farm-PJON-LoRa-network/blob/main/Pictures/BatteryMonitor.jpg?raw=true" alt="The battery voltage monitor and remote control that I built for the solar electric fence." -%}

{%- include captioned-image.html src="https://github.com/jgOhYeah/Farm-PJON-LoRa-network/blob/main/Pictures/PumpMonitorTesting.jpg?raw=true" alt="Debugging code when installing the pressure pump monitor." -%}