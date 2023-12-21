---
layout: post
title: "Tractor watchdog"
date: 2023-11-06 00:00:00 +1100
categories: farm
tags: farm pjon lora arduino university
thumbnail: "/assets/images/2023-10-14-tractor-watchdog.jpg"
---

We use an early 1960s Fordson Dexta tractor to run the irrigation pump. During a day when we are irrigating, the tractor can often be left running for extended periods of time between checks. If something were to go wrong such as a loss of oil or the engine overheating, then the system should be shut down as quickly as possible to minimise damage. I have designed and built an engine watchdog for this tractor that monitors various engine parameters and shuts it down if something is wrong. I snuck this project in as part of FIT3146 (Makerlab) in semester 2 2023.

## Demonstration video
<iframe class="embedded-16by9" src="https://www.youtube-nocookie.com/embed/NTL6U3gAmHQ?si=nD8ARRDJ-Tivxx8_" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


## Video on designing and making the unit
<iframe class="embedded-16by9" src="https://www.youtube-nocookie.com/embed/SbZSf4CfQ8M?si=eo8Zgq8k14I8ks1J" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Code and design files
{%- include github-bookmark.html name="TractorWatchdog" description="Engine watchdog for a Fordson Dexta tractor. Should work with other tractors as well." url="https://github.com/jgOhYeah/TractorWatchdog"-%}

## Documentation
Doxygen documentation is available [here](https://jgohyeah.github.io/TractorWatchdog/).

<!-- ## Demonstration

## Video explaining how I built this -->