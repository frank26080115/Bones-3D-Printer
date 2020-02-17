# Part CAD Design Walkthrough

I haven't given you homework in a while... there will be a bunch at the end. To warm you up, I will walk you through the design process of one of the more complex 3D printed parts of this 3D printer design.

Recall in [lesson 2], we talked about how the upper gantry was planned out with the size of the extruder in mind. This was how we figured out where the nozzle was vertically. We will start from there in order to design the 3D printed mount for the Hemera extruder.

![](../images/lesson2/beltplanningtohemeramount.png)

Remember that you can always follow along by forking and editing the 3D model yourself. Since it's a cloud based CAD tool, you can just fork it over to your own account, and edit the sketches and features to see what I am showing you. The link to the Onshape model: [https://cad.onshape.com/documents/359b...150f](https://cad.onshape.com/documents/359baba3de4f085c967fb5a9/w/62a7ef2a4414462a5d8bf3e1/e/208ce2426916e4fde5ad150f)

On this webpage, some images may be opened in full view (so you can zoom in) when you click on them. Not all of them, but some.

### How do we start?

First, we examine the Hemera extruder's datasheet where it has some mechanical drawings. The link to the file: [https://e3d-online.dozuki.com/Document/UBaWiCkBAAlCkZBG/Hemera-Datasheet-%28Edition-1%29.pdf](https://e3d-online.dozuki.com/Document/UBaWiCkBAAlCkZBG/Hemera-Datasheet-%28Edition-1%29.pdf)

Inside we see these drawings:

![](../images/lesson7/hemeramechdrawing.png)

What I did was create a rough representation of the Hemera extruder first. Using a sketch started from a side view. I need the sketch to show the overall body size of the Hemera, where the placements of the screw holes are. The positioning is relative to the positions of the rods so the cross linear rods and linear ball bearings are represented by dotted lines (construction lines).

(note: the sizes of the linear ball bearings had to be reseached before doing this drawing, LM8UU bearings are 15mm outer diameter and 25mm long)

[![](../images/lesson7/hemerastartsketch.png)](../images/lesson7/hemerastartsketch.png)

There are some dimensions in there that you can match up with the Hemera extruder's datasheet drawings, or the dimensions of the LM8UU bearings. There are also some dimensions you may not understand, I will explain them:

 * The 5mm circle over the bottom right 3mm circle: this is used along with a few tangent constraints to ensure that even with the 8mm rod installed, I can get a screwdriver into the M3 screw there.
 * 0.05mm on the outer diameter of the linear ball bearing: this can be adjusted later if the 3D printed clamps are too tight around the linear ball bearings.
 * 0.1mm at the center of the top linear ball bearing: this can be adjusted later if the vertical distance between the cross linear rods require adjustments.

Breaking down some of the constraints used in this sketch:

[![](../images/lesson7/hemerastartsketchconstraints.png)](../images/lesson7/hemerastartsketchconstraints.png)

We can extrude out this sketch 44mm to get a blocky representation of the Hemera extruder.

![](../images/lesson7/hemerastartextrude.png)

