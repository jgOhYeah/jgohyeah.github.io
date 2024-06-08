---
layout: post
title:  "Paddock plantation timelapse"
date:   2023-02-23 00:00:00 +1100
categories: farm
tags: timelapse photography farm
thumbnail: "/assets/images/pandemic-plantation-timelapse.jpg"
permalink: /PaddockPlantationTimelapse.html
---

Back in July 2020, I set up an old phone and an assortment of other parts in a
new tree plantation to watch the trees (and grass) grow. Over the following
three years it has taken well over 196,000 photos.

<iframe class="embedded-4by3" src="https://www.youtube-nocookie.com/embed/ho5LEKpndx4?si=HWdEe_XU5RMaQt0E" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Selected photographs have been combined into High Dynamic Range (HDR) images and
these used as frames to create a video. This page will be updated as I obtain
and process more photos.

I find it fairly fascinating to watch the trees shoot up out of nowhere and the
grass change colour and grow with the seasons, before disappearing again as it
is mown (generally takes a couple of watches to spot many details).

## Camera design
{%- include captioned-image.html src="/assets/images/pandemic-plantation-timelapse.jpg" alt="The camera freshly installed in its corner of the plantation." -%}

The camera is made from various parts lying around, mainly comprising an old android phone, car USB charger, cordless drill battery, very crude charge controller (constant current supply based on an LM317 and a few diodes) and solar panel.

The [Automate](https://llamalab.com/automate/) application is used to schedule when photos are taken. When it is time, this calls a shell script that simulates a button press to turn on the screen, launches the take photo activity of the [Open Camera](https://opencamera.org.uk/) app and waits for it to take 3 photos using exposure bracketing. Once this is done, the script closes the camera app and turns off the display again.

Logging is performed for analysis and prevention of issues. These logs include those from the Automate app, shell script and [Battery Log](https://play.google.com/store/apps/details?id=kr.hwangti.batterylog&hl=en&gl=US) app. Observations and notes during servicing are also written down.


## Processing workflow
Image processing is undertaken with various pieces of software manged by shell scripts and a Makefile. Seeing as this is an ongoing project, I have automated the process as much as possible to make it easier to generate videos more frequently.

- Once every couple of weeks to a couple of months I retrieve the photos and logs from the phone.
- A shell script is used to select the photos that are required based on the dates they were taken. All photos are used at the start and end, while only one per day is used for the rest of the time. For each photo selected, the exposure bracketed images are combined using [Luminance HDR](https://github.com/LuminanceHDR/LuminanceHDR). Combined images are cached between processing runs to improve performance.
- [ImageMagick](https://imagemagick.org/index.php) is used to generate the title and end slides based on the image selection parameters in the shell script.
- For each frame of the video, a symlink is made to provide consecutive frame numbers without having to rename the actual image files.
- [timelapse-deflicker](https://github.com/cyberang3l/timelapse-deflicker/tree/master) is used to reduce some flicker and exposure differences between frames.
- [FFmpeg](https://ffmpeg.org/) is used to combine each frame into a video. The `drawtext` filter is used to add the date of each frame's capture to the video. FFmpeg is also used to add audio from the YouTube Audio Library.

## All videos I have processed and uploaded so far
<ul>
  <li><b>23/12/2023:</b> <a href="https://youtu.be/ho5LEKpndx4">https://youtu.be/ho5LEKpndx4</a></li>
  <li><b>23/02/2023:</b> <a href="https://youtu.be/rbYAF5bh35Q">https://youtu.be/rbYAF5bh35Q</a></li>
  <li><b>19/07/2022:</b> <a href="https://youtu.be/OD4dWEGN-B4">https://youtu.be/OD4dWEGN-B4</a></li>
  <li><b>26/12/2021:</b> <a href="https://youtu.be/lajF1W_7d8U">https://youtu.be/lajF1W_7d8U</a></li>
</ul>