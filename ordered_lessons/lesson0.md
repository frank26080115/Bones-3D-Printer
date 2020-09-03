# How does this 3D printer work?

First, please use Onshape and explorer the 3D model of the 3D printer a bit: [https://cad.onshape.com/documents/359ba....150f](https://cad.onshape.com/documents/359baba3de4f085c967fb5a9/w/62a7ef2a4414462a5d8bf3e1/e/208ce2426916e4fde5ad150f)

![](../images/3dmodeloverview.png)

Poke around, the parts are named. You might be able to guess how it works.

If you are unfamiliar with how a 3D printer works:

There's a print head that moves horizontally. This print head carries the extruder and nozzle. The extruder is the part of the printer that pushes a thin strand of plastic through a very hot nozzle. When the plastic is melted by and pushed out the nozzle, it will land on something and solidify. At the beginning of a print, it will first land on the bed, and make a thin layer of plastic as the print head moves around. Then the bed will move down very slightly so the print head can extrude the next layer on top of the first layer. The computer determines the shape of each layer, and thus, the movement of the print head, using software called a slicer. The slicer makes files that contain gcode commands, and the printer's circuitry reads those gcode commands and tells each motor what to do.

## X and Y motion

Have a look at this video below, it will show:

 * rods that are spinning
 * those spinning rods are spinning some pulleys
 * the pulleys pull on the belts
 * the belts pull on the grey sliding blocks
 * the rods in the middle are attached to the sliding blocks move with the sliding blocks
 * the print head moves along with those rods in the middle

<video controls="controls" loop="loop" preload="none" id="vid_0" poster="../images/filmanimation.gif" style="width: 100%;"><source src="../videos/hephaestuscircles.mp4" type="video/mp4"><a href="../videos/hephaestuscircles.mp4"><img src="../images/filmanimation.gif" width="100%"></a></video>

## Z bed movement

The bed moves on the vertical Z axis. It is driven by a leadscrew, which is a rod with a helix grove that goes into a nut, a lead-nut, that has a matching grove. As the rod spins, the nut will move up and down. The bed is attached to this lead-nut so the bed moves up and down as the rod spins.

<video controls="controls" loop="loop" preload="none" id="vid_0" poster="../images/filmanimation.gif" style="width: 100%;"><source src="../videos/zleadscrew.mp4" type="video/mp4"><a href="../videos/zleadscrew.mp4"><img src="../images/filmanimation.gif" width="100%"></a></video>

## Extruder

We will be using the Hemera extruder, which uses a stepper motor and some gears to drive the plastic filament into the nozzle. The system of parts that melts the plastic filament is known as a "hot end".

<div class="youtube_container"><iframe src="https://www.youtube.com/embed/yV4bd_d5FAI" frameborder="0" allowfullscreen=""></iframe></div>

Read more about the [Hemera extruder on the E3D-Online website](https://e3d-online.com/e3d-hemera-feature)

## More Detailed Explanation

There's a much more in-depth look at all of the 3D printer motion components in [lesson number 5](lesson5).

## Get Started

Let's go to [lesson 1, designing the frame](lesson1)!
