---
layout: post
title:  "Model solar car racing"
date:   2016-10-16 00:00:00 +1100
categories: solarcar
tags: electronics machining solar vmsvc
thumbnail: "/assets/images/2016-solar-car.jpg"
---

For five years I designed, built and raced model solar cars. This was part of the [Victorian Model Solar Vehicle Challenge (VMSVC)](https://www.modelsolar.org.au/) held at Scienceworks and the [Australian-International Model Solar Vehicle Challenge (AIMSVC)](https://www.modelsolarchallenge.com.au/).

<!-- | Year  | Vehicle        |    Team Members    | Events competed at                                                  | Solar panel                                            |       Electronics (MPPT)       |     Motor      | Chassis                                                                                                                                        |
| :---: | :------------- | :----------------: | :------------------------------------------------------------------ | :----------------------------------------------------- | :----------------------------: | :------------: | :--------------------------------------------------------------------------------------------------------------------------------------------- |
| 2012  | Humpty 01      | Tyrell L, Jotham G | VMSVC Sheridan Kit Car                                              | Commercial                                             |              None              |    Brushed     | Monocoque folded plastic                                                                                                                       |
| 2013  | Humpty 02      |      Jotham G      | VMSVC, AIMSVC (held in Victoria)                                    | Homemade (1st had some shorted cells, second was good) |      Scorpio electronics       | Faulhaber 2232 | Monocoque balsawood                                                                                                                            |
| 2014  | Humpty 03      |      Jotham G      | VMSVC                                                               | Homemade (unreliable)                                  |      Scorpio electronics       | Faulhaber 2232 | Carbon fibre arrowshaft joined using epoxy coated thread, folded plastic body                                                                  |
| 2014  | Humpty 03 MkII |      Jotham G      | AIMSVC (held in NSW)                                                | Commercial (~10W, 16V)                                 |            Automax?            | Faulhaber 2232 | Carbon fibre arrowshaft joined using epoxy coated thread, folded plastic body                                                                  |
| 2015  | Humpty 04      |      Jotham G      | VMSVC, AIMSVC (held at the World Solar Challenge finish line in SA) | Commercial (~10W, 16V)                                 | Homemade, based on BHHS design | Faulhaber 2232 | Aluminium and carbon fibre arrowshaft composite joined using aluminium blocks with holes and grub screws, folded plastic body                  |
| 2016  | Humpty 05      |      Jotham G      | VMSVC, AIMSVC (held in Victoria)                                    | Commercial (~10W, 16V)                                 |            Automax             | Faulhaber 2232 | Aluminium and carbon fibre arrowshaft composite joined using aluminium blocks with holes and grub screws, folded plastic body, castor steering | -->

{%- include captioned-image.html src="/assets/images/2016-solar-car.jpg" alt="Humpty 05 (left) racing in the 2016 Victorian Model Solar Vehicle Challenge" -%}

## Humpy 01
Humpty 01 is a Sheridan kit car built from a kit of parts with provided instructions. A school friend and I built this car for and raced it in the 2012 Victorian Model Solar Vehicle Challenge. This was my first experience with solar panels and the concept of matching the power output of solar panels, motors and gearing for best performance.

The name "Humpty 01" is short for "Humpty Dumpty" and is named after the provision in the design for an egg to be carried as a "driver". This name stuck for all future model solar cars I built.

## Humpty 02
After experiencing the challenge with Humpty 01, I competed in the student designed cars category the following year. Humpty 02 used a monocoque body and chassis made predominantly from balsawood. It was a three wheeled car, with two wheels at the front and an angled drive wheel at the back that also doubled as one of the guide rollers.

The car had some significant stability issues in bright sunlight, but performance was alright from memory in the rare event that it completed a lap without crashing.

### Making solar panels
In an effort to keep costs down, Dad and I had several attempts at making our own solar panels instead of buying off the shelf ones. To do this, we built a miniature table saw to cut the thin silicon cells down to size before soldering them into strings. The strings were potted in resin with fibreglass sheets front and back for strength and for thermal expansion reasons.

A significant challenge when making solar panels that will be reliable is thermal expansion. Solar cells are easy to crack, which can do anything from reducing the performance of the panel to completely disabling it. When exposed to many thermal cycles as experienced when placed in and removed from sunlight, any difference in the expansion rate of the cells and surrounding materials may rip the cells apart. Fibreglass and silicon cells are both made of glass, so hopefully behave similarly enough to reduce this issue.

We found that for our home workshop, it is best for the cells to be cut so that there are multiple bus bars attached to each cell. This allows for improved redundancy in the event of a cell cracking or joing failing.

Potting the solar panels was another challenge. Our first panels used balsawood as a permenantly attached mould. This had the interesting side effect of causing the panel to curve like a bimetalic strip depending on the temperature and humidity. Our next panels were made by casting the cells into a tray of resin. This worked ok, although the resign was quite thick in spots. It would probably be better to brush the resin on or vacuum infuse it to reduce the amount of excess.

## Humpty 03
Humpty 03 went to a four wheeled ladder chassis design that aimed to keep the weight as low as possible. The car that raced at the Victorian event had issues with the breakover angle and left a bit to be desired in terms of optimisations and appearances. An entirely new chassis and body were built for the national event that incorporated lessons learnt from the Victorian event.

<object data="/assets/docs/2014-humpty-03-mk2-poster_small.pdf" width="100%" height="600px" type="application/pdf"></object>

## Humpty 04
In some ways, this ended up being the practice run for Humpty 05. This vehicle also used a ladder chassis with folded plastic body, however used aluminium blocks that could be easily adjusted and modified as needed instead of glueing the chassis beams together as in Humpty 03. This turned out to be quite a reliable and well performing car.

<object data="/assets/docs/2015-humpty-04-poster_small.pdf" width="100%" height="600px" type="application/pdf"></object>

## Humpty 05
This is the last model solar car that I have built for this competition. A major design feature of this oh ack ls through a differential instead of driving a signle wheel like most model solar cars. This has the advantage of reducing wheel slip on vehicle start without using "O" rings as tyres that increase rolling resistance.

<object data="/assets/docs/2016-humpty-05-poster_small.pdf" width="100%" height="600px" type="application/pdf"></object>

I designed the differential housing using [OpenSCAD](https://openscad.org/) and one of my school teachers and a friend 3D printed its parts. This was my first experience of using 3D CAD and 3D printing, so it was quite the learning curve. I wasss not sure over the accuracy of the printed parts, so designed them to be machined down later. The differential was a great success and the car often visibly accelerated faster than its competitors whilst still having a high top speed.

This vehicle won the Victorian event in 2016 and was awarded joint best engineered car alongside a two wheeled car. The poster submitted also received an award.

<iframe class="embedded-16by9" src="https://www.youtube.com/embed/vjSzcoZUqPQ?si=AvgMrF7kTpE8bvZo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Other events
I have volunteered with the Sheridan Kit Car division of the VMSVC several times since I finished racing and have taken vehicles I have built to several exhibition events including:
- 2013 Avalon air show with Humpty 01.
- An exhibition in Jeff's shed (can't remember precise details).
- [2017 VMSVC](https://youtu.be/q32cP7OWZos).
- [2018 EV Expo](https://youtu.be/__geP4_VqYg) with Humpty 04 and Humpty 05.
- 2018 Shepparton car show with Humpty 05.
- [2018 VMSVC](https://youtu.be/QLc6vT73KbU).
- 2022 VMSVC.
- 2023 VMSVC.