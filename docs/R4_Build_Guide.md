---
title: Root 4 Assembly Guide
description: Root 4 Assembly Guide 
published: true
date: 2022-06-28T21:37:30.411Z
tags: root 4, r4, guide
editor: markdown
dateCreated: 2022-05-24T19:30:47.756Z
---

# Root 4 CNC Build Guide

## Before you get building/printing

## Key info
1.  Build area and machine size is all dependent on the size of ball screws and box section. Please see this file: [Here](https://github.com/RootCNC/Root-4-CNC/blob/master/Working%20Area.xlsx)
2.  North American builders should see the gotchas below
3.  Ballpark price is dependent on your build size and upgrade/quality-of-life choices you make, but expect somewhere in the realm of £900-1200 GBP, $1200-1500 USD, $1500-2000 AUD

## Gotchas before starting
1. Make sure you have access to metric box section in your country before you start printing parts.
2. If you need Imperial, then there is a [branch of files for 1.5 inch box section to print instead](https://github.com/RootCNC/Root-4-CNC/tree/38mm-Dev/Source/STL_Files/38.1x38.1mm%20Box%20Section%20%281.5x1.5%20inch%29)


## Printing parts

### Printing considerations
1. If you have access to a 0.6mm nozzle, this will significantly decrease the time needed to print, while also strengthening the parts due to the line widths. **Worth buying one just for this project alone.**
2. Similarly, larger layer heights afforded by the 0.6mm nozzle will give you more strength and speed up the print
3. Rigidity of material matters as much as strength for a number of parts. Consider using a modified PLA blend (commonly known as PLA+, pro PLA etc.) for parts where rigidity is paramount (see table below) and PETG for parts where sheer strength is more important.
4. More walls is better than more infill if you want strong parts
5. Use supports really carefully - some models have quite complex segments for nestling hex nuts, and you don't want to be pulling supports out of those spots. Use support blockers to ensure those channels are kept clear.
6. Tune your printer to give you accurate hole diameters. Check every hole after printing before moving on to print a duplicate part.

### Recommended print settings
1. 2-3 walls/perimeters of 0.6mm width
2. 0.3+ layer heights - this can be achieved with a 0.4mm nozzle, but better with a 0.6mm nozzle. Adaptive layers not recommended.
3. 3-4 bottom/top layers - whether you choose 3 or 4 will depend on whether there are mounting holes pushing against the top/bottom.
4. 30-40% infill. The more a piece is likely to be compressed, the more infill. If approaching 40% infill, consider if you'd be better off adding an additional wall instead.
5. None of these parts need to be pretty, so feel free to print as fast as you can, just ensure that your holes are accurate. Use hole horizontal expansion to your advantage to perfect your hole sizes.

## Planning your build
- Use the [working area file](https://github.com/RootCNC/Root-4-CNC/blob/master/Working%20Area.xlsx) to determine what size ball screws and box section you need to order.
- What do you intend to cut on your CNC? Consider whether a square build is most suitable, or whether a wider X axis with a shallower Y axis will mean your CNC takes up a smaller footprint, but can allow larger stock to be fed through from front to back for the occasional larger project.
- Going wider in the X axis is cheaper than going longer in the Y axis, as you only have a single ball screw on the X axis, but the amount of square box section is the same.
- Do you want the lightness and stiffness of aluminium square hollow section (will tend to cost more) or the beefy weight of steel (tends to be cheaper if not shipped). Steel's density will absorb more vibrations from the machine than aluminium will, and it's weight will go a small way to minimising deflection.

## Building your platform
- Decide what base/platform you're going to build your CNC upon. The Root 4 is different to the previous Root machines in that the machine isn't necessarily designed to be portable and doesn't rest on feet. This means you can really make the most of having a rigid platform.
- Keeping the platform square and flat over the life of the machine is essential. There are a few ways to do this:
  - You can follow the method in the videos of welding a metal frame to mount plywood to. This is the simplest and likely most cost effective method. The metal frame will stop the plywood from warping over time and also give you a frame for mounting controls/enclosure on.
  - If you intend to make a timber frame, then you will be best served building a 'torsion box' table to keep the surface as flat as possible. This can be done with an MDF core and two sheets of plywood - just make sure you have solid corners to be able to countersink mount holes for your Y axis mounts.
- Make sure your platform is deep enough to accommodate your stepper motors on their standoffs without hanging over the back of your CNC.
- Make sure your platform is wide enough to accommodate mounting your cable chain outside the path/width of the Y carriage.
- Do you want to use alcohol/alcohol-based cutting fluid for milling metals? Make sure any finish you put on your wood is not going to break down with alcohol or other solvents.

## High level overview - Order of construction
1. Carriages - build them up according to the video, slide them onto the tubes, ensure they have no play.
2. Mount Y axis ball screw mount and aluminium ball screw nut housing onto the Y axis side panels (not essential to do now, but does make things easier)
3. Mount Y axis side panels onto Y carriages (far easier to do now than trying to get in under already mounted square tubes)
4. Mark out and drill your Y axis mount holes. Screw down the rear mount.
5. Slide your hollow box section into the Y axis mount (ensuring the carriages are already on) and screw in the front Y axis mount
6. Prepare the Z axis front panel with rivnuts and threaded inserts, screw on your linear rails, leave everything else off
7. Mount X axis ball screw mount and aluminium ball screw nut housing onto the rear face of the Z axis front panel
8. Slide X axis mounts onto hollow box section (ensuring the carriages are already on) and lay it down on your table
9. Mount the Z axis front panel onto the X carriages
10. Wind the X axis ball screw nut into the centre of the screw. Position the X axis ball screw in place between the box section, ensuring the ball screw nut is on the correct side to nest inside the aluminium housing, but also ensuring the end machined for the fixed ball screw mount (FF) is on the left. Screw the ball screw nut into the housing
11. Flip the X axis setup over and mount the Z axis rear panel
12. Resting your X axis bottom carriage on a box or something of suitable height for support, screw the X axis mounts in place on your side panels
13. Attach your X axis ball screw mounts
14. TBC

## License

This project is licensed under the Creative Commons 4.0 license with 
Attribution-NonCommerial-ShareAlike see `LICENSE.txt` for details


<img src="https://raw.githubusercontent.com/RootCNC/Root-4-CNC/master/Media/ex_20200530_225621.jpg" width="600">