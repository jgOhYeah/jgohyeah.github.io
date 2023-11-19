---
layout: post
title: "Tractor watchdog"
date: 2023-11-06 00:00:00 +1100
categories: farm
tags: farm pjon lora arduino university
thumbnail: "/assets/images/2023-10-14-tractor-watchdog.jpg"
---

We use an early 1960s Fordson Dexta tractor to run the irrigation pump. During a day when we are irrigating, the tractor can often be left running for extended periods of time between checks. If something were to go wrong such as a loss of oil or the engine overheating, then the system should be shut down as quickly as possible to minimise damage.

{%- include captioned-image.html src="/assets/images/2023-10-14-tractor-watchdog.jpg" alt="Tractor tractor that the unit is designed for." -%}

I have designed and built an engine watchdog for this tractor that monitors various engine parameters and shuts it down if something is wrong. I snuck this project in as part of FIT3146 (Makerlab) in semester 2 2023.

## Code and design files
{%- include github-bookmark.html name="TractorWatchdog" description="Engine watchdog for a Fordson Dexta tractor. Should work with other tractors as well." url="https://github.com/jgOhYeah/TractorWatchdog"-%}

## Documentation
Doxygen documentation is available [here](https://jgohyeah.github.io/TractorWatchdog/).

<!-- ## Demonstration

## Video explaining how I built this -->