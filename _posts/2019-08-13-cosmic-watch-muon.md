---
layout: post
title:  "Cosmic watch muon detectors"
date:   2019-08-13 00:00:00 +1100
categories: electronics
tags: arduino electronics project school microcontrollers
thumbnail: /assets/images/2018-07-31-muon-detector.jpg
---

In year 11, my physics teacher asked if I could build a [Cosmic Watch muon detector](http://www.cosmicwatch.lns.mit.edu/) to assist with proving the effects of special relativity.

The official github repository:
{%- include github-bookmark.html name="CosmicWatch-Desktop-Muon-Detector" description="This repository if for the supplementary material used to build the CosmicWatch Desktop Muon Detectors V2" url="https://github.com/spenceraxani/CosmicWatch-Desktop-Muon-Detector-v2" -%}

Muons are created when cosmic rays interact with the Earth's atmosphere. Whilst these subatomic particles travel extremely quickly, they are unstable and have an extremely short half life. This half life is so short that statistically muons should not be able to reach the surface of the Earth if relativitstic effects did not apply. Due to time dilation, it is much more likely for muons to reach the Earth's surface and be counted by a detector.

{%- include captioned-image.html src="/assets/images/2018-07-31-muon-detector.jpg" alt="Muon detectors showing their counts." -%}

I ended up building two detectors due to the relative costs of the silicon photomultiplier and its postage. This had the advantage that multiple detectors can be linked together for improved rejection of detections caused by things other than muons. This was my first significant experience with surface mount technology. In the end, both detectors were successfully built and last I heard, were still being used.

An Arduino Nano is used as the brains of each unit. Due to the limited amount of flash memory and RAM, the original firmware could only use one of the OLED display or SD card reader at a time. The microcontroller needed to be reprogrammed to swap between these. I managed to significantly modify the firware to cram in support for both using the display and SD card at the same time.

The modified firmware I made that supports using the display and SD card at the same time:
{%- include github-bookmark.html name="NonOfficial-StuffForCosmicWatchMuonDetectors" description="Extra code and stuff I (Jotham Gates) have made/adapted for Spencer Axiani's Cosmic Watch Desktop Muon Detector V2" url="https://github.com/jgOhYeah/NonOfficial-StuffForCosmicWatchMuonDetectors" -%}