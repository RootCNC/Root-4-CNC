<img align="right" width=175 src="https://github.com/RootCNC/Root-4-CNC/blob/master/Media/R_Logo.png" />

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
7. You may find that your motor spacers aren't quite long enough/short enough. Your printer didn't get it wrong, it's just the nature of the build. Estimate how much the part needs adjusting by to enable the motor and ballscrew to marry up nicely, and use the scale feature of your slicer in the Z dimension only to stretch/squish it as necessary.

### Recommended print settings
1. 2-3 walls/perimeters of 0.6mm width, or 3-4 of 0.4mm width
2. 0.3+ layer heights - this can be achieved with a 0.4mm nozzle, but better with a 0.6mm nozzle. Adaptive layers not recommended.
3. 3-4 bottom/top layers - whether you choose 3 or 4 will depend on whether there are mounting holes pushing against the top/bottom.
4. 30-40% infill. The more a piece is likely to be compressed, the more infill. If approaching 40% infill, consider if you'd be better off adding an additional wall instead.
5. None of these parts need to be pretty, so feel free to print as fast as you can, just ensure that your holes are accurate. Use hole horizontal expansion to your advantage to perfect your hole sizes.

### Recommended materials
| Part                               | Recommended filament type                                                   |
|------------------------------------|-----------------------------------------------------------------------------|
| XY_Axis_BallScrewMount.STL         | PLA+                                                                        |
| XY_Carriage.STL                    | PLA+                                                                        |
| X_Axis_DragChainBrace.STL          | PETG                                                                        |
| X_Axis_DragChainMountXCarriage.STL | PLA+ or PETG                                                                |
| X_Axis_Mount_FF.STL                | PLA+                                                                        |
| X_Axis_Mount_FK.STL                | PLA+                                                                        |
| X_Axis_NEMA23_50mmSpacerFK12.STL   | PLA+ (print with enough walls that there's nearly no infill anyway)         |
| Y_Axis_DragChainCarriageMount.STL  | PLA+                                                                        |
| Y_Axis_Mount_FF12.STL              | PLA+ or PETG                                                                |
| Y_Axis_Mount_FK12.STL              | PLA+ or PETG                                                                |
| Y_Axis_NEMA23_50mmMotorSpacer.STL  | PLA+ (print with enough walls that there's nearly no infill anyway)         |
| Z_Axis_MotorMount.STL              | PLA+ or PETG. PETG will hold better as there's some risk of cracking due to necessary orientation |
| Spindle_Mount_XXmm.STL             | Use PETG if fan cooled and smaller diameter. Use PLA+ if water-cooled 80mm  |
| All dust shoe parts                | PETG best, PLA+ good enough                                                 |
|                                    |                                                                             |

## Planning your build
- Use the [working area file](https://github.com/RootCNC/Root-4-CNC/blob/master/Working%20Area.xlsx) to determine what size ball screws and box section you need to order.
- What do you intend to cut on your CNC? Consider whether a square build is most suitable, or whether a wider X axis with a shallower Y axis will mean your CNC takes up a smaller footprint, but can allow larger stock to be fed through from front to back for the occasional larger project.
- Going wider in the X axis is cheaper than going longer in the Y axis, as you only have a single ball screw on the X axis, but the amount of square box section is the same.
- Do you want the lightness and stiffness of aluminium square hollow section (will tend to cost more) or the beefy weight of steel (tends to be cheaper if not shipped). Steel's density will absorb more vibrations from the machine than aluminium will, and it's weight will go a small way to minimising deflection.

## Building your platform
- Decide what base/platform you're going to build your CNC upon. The Root 4 is different to the previous Root machines in that the machine isn't necessarily designed to be portable and doesn't rest on feet. This means you can really make the most of having a rigid platform.
- Keeping the platform square and flat over the life of the machine is essential. There are a few ways to do this:
  - You can follow the method in the videos of welding a metal frame to mount plywood to. This is the simplest and likely most cost effective method. The metal frame will stop the plywood from warping over time and also give you a frame for mounting controls/enclosure on.
  - If you intend to make a timber frame, then you will be best served building a 'torsion box' table to keep the surface as flat as possible. This can be done with an MDF core and two sheets of plywood - just make sure you have solid corners to be able to countersink mount holes for your Y axis mounts. The simplest way to make the MDF core is by cutting strips with half-laps which you can slot together as a grid. [Example in the RootCNC discord here](https://discord.com/channels/795012056943296522/795012173708787723/862584303178088458)
- Make sure your platform is deep enough to accommodate your stepper motors on their standoffs without hanging over the back of your CNC.
- Make sure your platform is wide enough to accommodate mounting your cable chain outside the path/width of the Y carriage.
- Do you want to use alcohol/alcohol-based cutting fluid for milling metals? Make sure any finish you put on your wood is not going to break down with alcohol or other solvents.

## High level overview - Order of construction
1. Carriages - build them up according to the video, slide them onto the tubes, ensure they have no play and that the long bolts are as close to equal in tension as possible. This ensures their perpendicularity.
2. Mount Y axis ball screw mount and aluminium ball screw nut housing onto the Y axis side panels (not essential to do now, but does make things easier)
3. Loosely mount Y axis side panels onto Y carriages (far easier to do now than trying to get in under already mounted square tubes)
4. Mark out and drill your Y axis mount holes. Screw down the rear mount.
5. Slide your hollow box section into the Y axis mount (ensuring the carriages are already on) and screw in the front Y axis mount
6. Find a solid, non-compressible item to slide under the side panel at the appropriate height (around 4mm). Tighten one side panel down fully. Use the same object to support the second side panel and tighten that down too.
7. Prepare the Z axis front panel by drilling holes for your T slot to mount on the edge of the panel (but don't mount it now), insert your rivnuts and threaded inserts, screw on your linear rails, leave everything else off
8. Mount X axis ball screw mount and aluminium ball screw nut housing onto the rear face of the Z axis front panel
9. Slide X axis mounts onto hollow box section (ensuring the carriages are already on) and lay it down on your table
10. Mount the Z axis front panel onto the X carriages
11. Wind the X axis ball screw nut into the centre of the screw. Position the X axis ball screw in place between the box section, ensuring the ball screw nut is on the correct side to nest inside the aluminium housing, but also ensuring the end machined for the fixed ball screw mount (FF) is on the left. Screw the ball screw nut into the housing.
12. Flip the X axis setup over and mount the Z axis rear panel
13. Resting your X axis bottom carriage on a box or something of suitable height for support, screw the X axis mounts in place on your side panels, trying to ensure they are of equal height above your working surface.
14. Wind your ball screw out so it protrudes through the right hand side panel. Attach your fixed side ball screw mount first as it's on the inside of the left side panel. Once secured, then wind your ball screw into place. Next mount the floating ball screw mount on the outside of the other side panel.
15. Mount your Z axis motor mount, and mount the Z axis motor but don't tighten it down yet.
16. Slide your last ball screw block onto the Z axis ball screw, then mount the Z axis ball screw along with it's mounts. Check that the ball screw block can move freely from top to bottom.
17. Attach the T track to your front panel
18. Attach your spindle mount
19. Slide your Z axis belt through the holes on both Z panels, insert the pulleys into it, and then attach your pulleys to the motor/ball screw. Pull the Z motor back to make the belt tight, and tighten the motor screws down.

20. To be continued...

## License

This project is licensed under the Creative Commons 4.0 license with 
Attribution-NonCommerial-ShareAlike see `LICENSE.txt` for details




