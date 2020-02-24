# Mechanical Assembly (Continued)

## Extruder

Follow E3D's instructions on how to assemble the Hemera extruder and hot-end:

 * [01. Hemera Core Assembly Guide](https://e3d-online.dozuki.com/Guide/01+-+E3D+Hemera+Core+Assembly/122?lang=en)
 * [02. Hemera Direct Assembly Guide](https://e3d-online.dozuki.com/Guide/02+-++E3D+Hemera+Direct+Assembly/127?lang=en)

Attach the blower fan onto the 3D printed part that mounts to the Hemera extruder using small zip-ties.

![](../images/lesson10/ziptieblowerfan.png)

Attach the 3D printed mounts to the Hemera extruder, using the 6mm long M3 screws.

![](../images/lesson10/hemeramount.png)

If the screws are too long, then use some washers under them.

This is now the print head. Install this whole print head onto the gantry's cross linear rods. Slide the linear rods through the clamps first, then slide the linear ball bearings into the clamps.

![](../images/lesson10/extrudermountanimation/animation.gif)

Finally, tighten down the clamps using square nuts, 20mm long M3 screws, and here you **must use washers**.

When you are done this, then you can move the print head around by hand. All the rods will start spinning and the motors will start spinning. Check that, although you can move the print head, it doesn't wiggle around as if the bearings are loose.

## X and Y Axis Endstops

We actually have two different types of endstops: limit switch and shaft collar.

Move the bed up to the nozzle by hand. Move the nozzle to the left front of the glass bed where coordinate (X=0, Y=0) should be.

Now you can use the shaft collar on the side linear rods to set that point as the limit by butting up the collar against the sliding block. Tighten that set-screw.

Mount the limit switches in the correct position such that the switch will not be destroyed when the sliding block reaches the shaft collar. Use the 20mm long M3 screws to fasten it to the 3D printed gantry bearing mount. The screws should enter through the limit switch, and on the other side, use a washer (**required**) and nylon locking nut to fasten.

![](../images/lesson10/setlimits1.png)

Also do the same for the far right corner of the print bed. But this time, allow the nozzle to go past the edge of the glass by a few millimeters. This is because we want the shaft collars to act as a safety limit but the firmware will enforce the geometric limit.

![](../images/lesson10/setlimits2.png)

As a reminder, do not touch the shaft collars indicated in the next diagram, leave them tightened in place.

![](../images/lesson10/leavethesecollarslocked.png)

## Drag Chain

The drag chain can be disassembled and re-assembled to become different lengths. We chose a drag chain with an internal dimension of 10mm x 10mm, for this chain, each link is about 14mm long.

![](../images/lesson10/dragchainlinks.png)

At the end of every link, there's a small tab that stops it from bending the wrong way. Flipping the links allow the bend to go in another direction.

![](../images/lesson10/dragchainblockingtab.png)

The end links are wedge shaped with holes for screws, these can be flipped if we need to.

![](../images/lesson10/dragchainends.png)

Know all this now, have a look at the drag chain in our printer.

![](../images/lesson10/dragchainoverview.png)

Closer up, pay attention to the shape of the end pieces, and pay attention to where the bends change direction.

![](../images/lesson10/dragchainclosein.png)

Your job is to take the drag chain you've purchased and arrange it in this shape. I did some calculations and for this chain, you need 31 ordinary links in total, plus the 2 end links.

Do not mount the drag chain yet, you need to put wires through it first, then attach the bed heater to the forklift, only *then* you attach the drag chain to the frame.

## Print Bed

~~If the heated bed does not have countersunk holes, now is the time to use a drill and a countersink drill bit to make the holes countersunk. Make sure the M3 countersink head screws will sit in the hole with the head flush with the surface.~~ (my research indicates that the heated bed on the shopping list does have the holes already countersunk)

Now is the time to do the wiring for the heated bed, which is covered in [another page (click here)]().

Using the countersink M3 screws, a nylon locking nut, the bed springs, and the knob, fasten the bed heater plate to the bed forklift. Tighten the knobs until the springs are fully compressed first, then release each spring about 2mm.

![](../images/lesson6/bedassemblyoverviewlow.png)

Secure the wires to the 3D printed wire guide on the back of the forklift using zip-ties. This will allow us to work with the wires without worrying about breaking the solder joints.

![](../images/lesson10/bedrearwireguide.png)

Use binder clips to attach the glass sheet to the bed heater.

![](../images/lesson10/binderclipglassbed.png)

## Drag Chain Again

Now you screw the drag chain to the 3D printed drag chain anchors, and then you screw the drag chain anchors to the frame of the 3D printer.

![](../images/lesson6/dragchainanchors.png)

## Upper Wire Guide Tube

Install the teflon tube that keeps the wires from sagging on top of the printer. The tube should be cut to about 1000mm long.

Screw on the 3D printed wire guidance part to the printer's frame using M5 x 8mm flanged screws and T-slot nuts, then use zip-ties to attach the teflon tube.

The other end of the tube should be zip-tied to the back of the Hemera extruder, where there are holes on the 3D printed part. If you've install electronics to the Hemera extruder and hot-end already, then now is a good time to zip-tie their wires to the teflon tube.

![](../images/lesson10/uppercornercableguideziptie.png)

## The Rest

Everything else should be attached using M5 8mm long flanged screws and M5 T-slot nuts. Have fun!

You may want to complete all the electrical wiring before fastening the electronics.

## Next Lesson

 * [Lesson 11b](ordered_lessons/lesson11b.md): Electronics Bring-Up