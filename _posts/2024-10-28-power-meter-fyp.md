---
layout: post
title:  "Final year project - cycling power meter and crankset"
date:   2024-10-28 00:00:00 +1100
categories: university
tags: electronics HPV university machining project MHP teamwork engineering microcontrollers
thumbnail: "https://github.com/monash-human-power/power-meter/blob/master/documents/images/power-meter-photo.jpg?raw=true"
---

In 2024, I completed the final year project (FYP) for my degree, working with Oscar Varney to develop a power meter and crank-set for Human Powered Vehicles (HPVs).

{%- include captioned-image.html src="https://github.com/monash-human-power/power-meter/blob/master/documents/images/power-meter-photo.jpg?raw=true" alt="Photograph of the completed crank-set prototype configured for use in MHP's next generation bicycle chassis." -%}

The crank-set is the spinning device that connects the pedals (and rider’s legs) to the chain and rest of the drive-train. This crank-set is optimised for the unique geometry requirements of high performance HPVs and uses inbuilt strain gauges to measure torque and an accelerometer and gyroscope to measure the angular velocity of the cranks. A microcontroller processes and multiplies these values to calculate the instantaneous and average power produced by the rider. The entire system is powered from a battery located in the middle of the axle.

MQTT messages sent over Wi-Fi and Bluetooth Low Energy (BLE) are used to offload the data to customised data-logging systems or off the shelf bicycle computers.

{%- include captioned-image.html src="/assets/images/2024-power-meter-side.jpg" alt="Photograph of one side of the power meter fitted into MHP's rider, chassis and drivetrain testing system." -%}

The PCB design files and firmware have been made open source and are available on GitHub.
{%- include github-bookmark.html name="power-meter" description="This is the code repository for a Final Year Project (FYP) to develop a crank-set and power meter for Human Powered Vehicles (HPVs)." url="https://github.com/monash-human-power/power-meter" thumbnail="https://github.com/monash-human-power/power-meter/blob/master/documents/images/power-meter-photo.jpg?raw=true" -%}