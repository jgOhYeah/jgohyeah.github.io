---
layout: post
title:  "Model solar car racing"
date:   2016-10-16 00:00:00 +1100
categories: solarcar
tags: electronics machining solar vmsvc microcontrollers
thumbnail: "/assets/images/2016-solar-car.jpg"
---

For five years I designed, built and raced model solar cars. This was part of the [Victorian Model Solar Vehicle Challenge (VMSVC)](https://www.modelsolar.org.au/) held at Scienceworks and the [Australian-International Model Solar Vehicle Challenge (AIMSVC)](https://www.modelsolarchallenge.com.au/).

{%- include captioned-image.html src="/assets/images/2016-solar-car.jpg" alt="Humpty 05 (left) racing in the 2016 Victorian Model Solar Vehicle Challenge" -%}

## Vehicles summary
<style>
    .table-centre {
        text-align: center;
    }

    .table-right {
        text-align: right;
    }
</style>

<table class="table-sideways">
    <thead>
        <tr>
            <th class="table-centre">Year</th>
            <th class="table-centre">Car</th>
            <th>Events competed at</th>
            <th>Solar panel</th>
            <th>Electronics (MPPT)</th>
            <th>Chassis</th>
            <th>Awards</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="table-centre">2012</td>
            <td class="table-centre">
                <a href="#humpty-01">Humpty 01</a>
            </td>
            <td>VMSVC Sheridan Kit Car</td>
            <td>Commercial</td>
            <td>None</td>
            <td>Monocoque folded plastic</td>
            <td>
                <ul>
                    <li>VMSVC kit car 1st place</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td class="table-centre">2013</td>
            <td class="table-centre">
                <a href="#humpty-02">Humpty 02</a>
            </td>
            <td>VMSVC, AIMSVC (held in Victoria)</td>
            <td>Homemade (1st had some shorted cells, second was good)</td>
            <td>Scorpio electronics</td>
            <td>Monocoque balsawood</td>
            <td>
                <ul>
                    <li>VMSVC best engineered car</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td class="table-centre">2014</td>
            <td class="table-centre">
                <a href="#humpty-03">Humpty 03</a>
            </td>
            <td>VMSVC</td>
            <td>Homemade (unreliable)</td>
            <td>Scorpio electronics</td>
            <td>Carbon fibre arrowshaft joined using epoxy coated thread, folded plastic body</td>
            <td>
                <ul>
                    <li>VMSVC best team effort</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td class="table-centre">2014</td>
            <td class="table-centre">
                <a href="#humpty-03">Humpty 03 MkII</a>
            </td>
            <td>AIMSVC (held in NSW)</td>
            <td>Commercial (~10W, 16V)</td>
            <td>Automax</td>
            <td>Carbon fibre arrowshaft joined using epoxy coated thread, folded plastic body</td>
            <td>
                <ul>
                    <li>AIMSVC best poster</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td class="table-centre">2015</td>
            <td class="table-centre">
                <a href="#humpty-04">Humpty 04</a>
            </td>
            <td>VMSVC, AIMSVC (held at the World Solar Challenge finish line in SA)</td>
            <td>Commercial</td>
            <td>Homemade, based on BHHS design</td>
            <td>Aluminium and carbon fibre arrowshaft composite joined using aluminium blocks with holes and grub
                screws,
                folded plastic body</td>
            <td>
                <ul>
                    <li>AIMSVC best poster</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td class="table-centre">2016</td>
            <td class="table-centre">
                <a href="#humpty-05">Humpty 05</a>
            </td>
            <td>VMSVC, AIMSVC (held in Victoria)</td>
            <td>Commercial (~10W, 16V)</td>
            <td>Automax</td>
            <td>Aluminium and carbon fibre arrowshaft composite joined using aluminium blocks with holes and grub
                screws,
                folded plastic body, castor steering</td>
            <td>
                <ul>
                    <li>VMSVC student designed car 1st place</li>
                    <li>VMSVC joint best engineered car</li>
                    <li>VMSVC best poster</li>
                </ul>
            </td>
        </tr>
    </tbody>
</table>

## Humpty 01
Humpty 01 is a Sheridan kit car built from a kit of parts with provided instructions. A school friend and I built this car for and raced it in the 2012 Victorian Model Solar Vehicle Challenge. This was my first experience with solar panels and the concept of matching the power output of solar panels, motors and gearing for best performance.

The name "Humpty 01" is short for "Humpty Dumpty" and is named after the provision in the design for an egg to be carried as a "driver". This name stuck for all future model solar cars I built.

## Humpty 02
After experiencing the challenge with Humpty 01, I competed in the student designed cars category the following year. Humpty 02 used a monocoque body and chassis made predominantly from balsawood. It was a three wheeled car, with two wheels at the front and an angled drive wheel at the back that also doubled as one of the guide rollers.

The car had some significant stability issues in bright sunlight, but performance was alright from memory in the rare event that it completed a lap without crashing.

### Making solar panels
In an effort to keep costs down, Dad and I had several attempts at making our own solar panels instead of buying off the shelf ones. To do this, we built a miniature table saw to cut the thin silicon cells down to size before soldering them into strings. The strings were potted in resin with fibreglass sheets front and back for strength and for thermal expansion reasons.

A significant challenge when making solar panels that will be reliable is thermal expansion. Solar cells are easy to crack, which can do anything from reducing the performance of the panel to completely disabling it. When exposed to many thermal cycles as experienced when placed in and removed from sunlight, any difference in the expansion rate of the cells and surrounding materials may rip the cells apart. Fibreglass and silicon cells are both made of glass, so hopefully behave similarly enough to reduce this issue.

We found that for our home workshop, it is best for the cells to be cut so that there are multiple bus bars attached to each cell. This allows for improved redundancy in the event of a cell cracking or join failing.

Potting the solar panels was another challenge. Our first panels used balsawood as a permanently attached mould. This had the interesting side effect of causing the panel to curve like a bimetallic strip depending on the temperature and humidity. Our next panels were made by casting the cells into a tray of resin. This worked ok, although the resin was quite thick in spots. It would probably be better to brush the resin on or vacuum infuse it to reduce the amount of excess.

## Humpty 03
Humpty 03 went to a four wheeled ladder chassis design that aimed to keep the weight as low as possible. The car that raced at the Victorian event had issues with the break over angle and left a bit to be desired in terms of optimisations and appearances. An entirely new chassis and body were built for the national event that incorporated lessons learnt from the Victorian event.

<object data="/assets/docs/2014-humpty-03-mk2-poster_small.pdf" class="pdf-document" type="application/pdf"></object>

## Humpty 04
In some ways, this ended up being the practice run for Humpty 05. This vehicle also used a ladder chassis with folded plastic body, however used aluminium blocks that could be easily adjusted and modified as needed instead of gluing the chassis beams together as in Humpty 03. This turned out to be quite a reliable and well performing car.

<object data="/assets/docs/2015-humpty-04-poster_small.pdf" class="pdf-document" type="application/pdf"></object>

## Humpty 05
This is the last model solar car that I have built for this competition. A major design feature of this driving the back wheels through a differential instead of driving a single wheel like most model solar cars. This has the advantage of reducing wheel slip on vehicle start without using "O" rings as tyres that increase rolling resistance.

<object data="/assets/docs/2016-humpty-05-poster_small.pdf" class="pdf-document" type="application/pdf"></object>

I designed the differential housing using [OpenSCAD](https://openscad.org/) and one of my school teachers and a friend 3D printed its parts. This was my first experience of using 3D CAD and 3D printing, so it was quite the learning curve. I was not sure of the dimensional accuracy of the printed parts, so designed them to be machined later. The differential was a great success and the car often visibly accelerated faster than its competitors whilst still having a high top speed.

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