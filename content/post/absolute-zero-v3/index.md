---
title: Absolute Zero V3
summary: 3lb Beetleweight Combat Robot
date: 2023-10-26
tags:
  - Hugo
  - Wowchemy
  - Markdown
image:
  caption: ''
---

Absolute Zero is a four-wheel-drive beetleweight combat robot which utilizes a "vertical spinner" weapon to damage opponents. It was my first beetleweight design, which has now been iterated upon numerous times and is still actively competing to this day. This post will go into detail on all of the components of the robot and why things are the way they are, give a brief top-level overview of the robot, and describe any important design decisions or changes I made along the way.

## Top-Level Overview

Colloquially, Absolute Zero (AZ) is considered a "4WD Vertical Spinner." Kinetic weapons are usually referred to by the direction they spin, with vertical spinners spinning upwards and horizontal spinners spinning sideways. I'll avoid going into too much robot detail here given that everything is explained further down in this post, so to go over some of the important features:

Power: 4S 1100mAh Li-HV Battery (16.8V)

Electronics: 50A Weapon ESC, 25A Drive ESCs, Fingertech Power Switch, Radiomaster R84 V2 Receiver 

Drive: 4WD, 1.875" Urethane Wheels

Chassis: 95A TPU, 3/8" UHMW, 2mm Carbon Fiber, 0.0625" 6061-Aluminum

Weapon: AR500 Vertical Drisk (Dual Disk), 350 MPH Theoretical Tip Speed

Front-End: Grade 5 Titanium Flaps

Absolute Zero V3 was designed in Onshape using a series of master sketches and a Multi-Part Part Studio which controls all of the critical geometry of the robot, and allowed me to easily have all of the robot's components reference geometry either from the master sketches using the Derive Tool, or reference geometry on other parts of the robot.


## Material Selection and Design Philosophy

Material selection depended on both desired properties and desired failure modes. For example, when it comes to outer armor, choosing a more brittle filament such as PLA would result in the armor shattering on impacts, which is not a desireable outcome. On the other hand, metals like steel are extremely strong at the cost of being very heavy for a 3lb weight class, and would be difficult to reasonably get in-weight.

The answer to this problem is TPU, a flexible thermoplastic. It is one of the most prevalent printed materials in combat robotics (outside of plastic antweights, which typically ban it) due to its strong layer adhesion, durability, strength, and tendency to be cut/scraped instead of shatter when hit. Being able to print the majority of the robot also allows for rapid prototyping of components and geometries that would typically not be machineable through methods like milling or waterjetting. As shown below, my outer armor held up extremely well in practice, only taking damage in the form of some scrapes and cuts.

[Insert those images here]

I would experience a lot of problems if the entire robot was made out of TPU, however. Given that there are multiple belt runs from motors to driven components, the entire robot flexing would causes a lot of issues with friction and inconsistent center-to-center distances between the components. For this reason, the robot's structure is primarily held together by two parallel 2mm carbon fiber plates. These plates screw into the major chassis components from both top and bottom, including the weapon rails, drive rails, outer armor, and weapon divider separating the weapon motor from the robot's internals. These plates allow the robot to maintain a rigid chassis in spite of the numerous TPU chassis components.

[Insert CF Pictures]

The drive and weapon rails used to be TPU with titanium inserts for rigidity, but I have since switched to use 3/8" UHMW. These UHMW rails are lightweight, strong, and can't fail along layer lines like a printed component. 3/8" cuts it close in terms of "what will bend and what wont" in competitions, but I have only so far experienced bending on the thinner "ears" of the robot that stick up past the weapon and allow me to drive while inverted.

[Insert Rail Pictures]

In some special cases, I chose to use CF-Nylon filament, nylon reinforced with carbon fiber. While a pain to print (and typically needs active drying), it is an extremely strong filament when properly printed. On this iteration of the robot, the cf-nylon components are the pulley bolted to the weapon motor and the weapon divider. I have used the same weapon pulley across more than one event without having to change out the print, and it is resistant to melting unlike a TPU pulley, which I once had fuse to the weapon rail across from it due to heat.

[Insert CF-Nylon Picture]

There are a few instances where I use thin aluminum plates to add rigidity, or in the case of my drive system to facemount the drive motors to the drive rails. Across the back of my weapon rails is a 0.0625" 6061 aluminum plate which I refer to as a "stiffener plate." The plate connects the two rails across the back to add rigidity to the weapon system and make sure it does not flex excessively on big hits. Given the low clearance between my weapon motor pulley and the inner wall of the weapon rail, excess flexing could potentially cause the motor to stop spinning.

[Insert Stiffener Plate Picture]

On the weapon itself, the impactors (or disks, blades, etc.) are made out of AR500 steel. Given that they are the parts actually dealing damage to my opponent, I want them to be as hard as possible without risking shattering. If the blades were softer than the material I was hitting, the blade would get chipped away more than it would be damaging other people. Numerous competitiors have started implementing AR600 instead, an even harder alternative.

[Insert Disk Picture]

Now, we can take a closer look at each of the different components of the robot, why I chose to design them the way they are, and how they work.


## Chassis

Save your spreadsheet as a CSV file in your page's folder and then render it by adding the _Table_ shortcode to your page:

```go
{{</* table path="results.csv" header="true" caption="Table 1: My results" */>}}
```

renders as

{{< table path="results.csv" header="true" caption="Table 1: My results" >}}

## Weapon System

## Drive System

## Electronics

## Front-End Configurations
