# Flaws, Mistakes, Improvements

## Bad usage of Onshape

For this project, I used one single "Part Studio" inside Onshape to design the entire printer. This means that the part studio have over 600 features and over 200 parts. This is making either my computer or the Onshape server lag, and probably making some Onshape staff question my sanity.

The proper way of designing a complex machine with moving parts is to use assemblies and sub-assemblies. For example, the sliding blocks should be a sub-assembly that can move within the main assembly. The bed assembly should be a sub-assembly that can move together up and down along the Z axis.

For [my Hephaestus 3D printer](https://eleccelerator.com/hephaestus-my-own-3d-printer/), I used SolidWorks to design it, so using nested assemblies was easy, and I could attain much more detail in my design since the assembly could contain imported 3D models directly from manufacturers. SolidWorks allows you to make constraints between parts from different assemblies, so this was easy.

In Onshape, at the time of this writing, I cannot make constraints between different assemblies, so I am forced to design using a single part studio.

Another bad thing I did is that I did not separate out operations that should stand alone. For example, I never used the holes tool, instead, I drew circles into the sketches. This reduced the number of features in the feature tree, which I knew would be huge. Doing things all in one sketch takes away from the ability to suppress individual features easily. This would've been more important in a professional setting where a part could have two variants, one with holes and one without.

Also, I just hate how "mate connectors" work in Onshape assemblies, it is really hard to get used to for a former SolidWorks user. My point is: if you are new to CAD and starting with Onshape, you might not be so stuck, so try using assemblies as much as possible, because technically that's more proper.

And sorry if I'm making your computer laggy with my massive model.

## Overconstraint

Some might comment that it's a bad design to secure all the rods so securely. All of the rods break the "two points make a line" rule because of the sliding bearings are technically a 3rd point. But honestly, this works, Hephaestus does the same thing but with aluminum fixtures instead of plastic, and the Ultimaker brand also has a similar design. If your assembly steps take this into account, and you're not getting crazy warping from extreme temperature changes, it's fine. Plus, the rods are slightly bendy, as we've discussed already, and the bearings will just take the additional preload.

## Sliding Blocks Improvement

The sliding blocks on Hephaestus are a two part design. The new sliding blocks on Bones is a three piece design, with a "cap" piece that clamps down on the cross linear rod. This third piece might not be needed if the two other pieces were made bigger with a slot, the cross linear rod will sit in the slot with a friction fit. This is how the Ultimaker 2 works.

## Less-than-optimal Print Volume

I didn't put in the effort to squeeze every last millimeter of build volume out of this design. As I've said in the first few lessons, I didn't account for the height of the bed assembly when planning out the vertical space usage. This height is variable by the springs used for the bed leveling and since I didn't know the compressed lengths of the springs, I just ignored this.

The extruder print head has the blower fan mounted on the bottom instead of on the side, this is due to lazy planning. If it was mounted to the side, we would lose some width in the available print space. This problem can be solved with better planning, technically the bed would need to be moved a bit to the left. But this would've made a lot of things more annoying to model. The good news is that the final more advanced fan duct design should be very high performance.

## Rear Bed Backstop

The backstop plates that sits behind the glass bed could be completely avoided if I knew where it would be safe to drill some holes into the heated bed. If I could drill some holes in the right places, I could include some permanently attached metal clips to secure the glass bed.
