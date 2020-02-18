# Assembly Preparation

## Shopping List

This page will attempt to list everything you need to buy. You can try shopping around for the best deal but for certain parts, I will insist on a particular model from a particular store. In the end, feel free to ask me to check an item on your list.

The main source will be Amazon Prime and McMaster-Carr. If you wish to shop on Aliexpress, eBay, Banggood, etc, that's up to you.

### Fasteners

There are about 400 screws being used in this design! That's not even counting the nuts and washers.

I've figured out that it's not cheaper to buy them from Amazon, plus, there are some that cannot be found easily on Amazon. So the source for all the screws shall be from McMaster-Carr. I have optimized a shopping list for every screw, nut, and washer you need from McMaster-Carr:

| Qty | Sku                                             | Name | 
|-----|-------------------------------------------------|------|
| 120 | [90909A721](https://www.mcmaster.com/90909A721) | M5 x 8mm flanged button head screw |
| 100 | [93475A240](https://www.mcmaster.com/93475A240) | M5 washer |
| 30  | [92832A229](https://www.mcmaster.com/92832A229) | M3 x 20mm button head screw |
| 30  | [92095A168](https://www.mcmaster.com/92095A168) | M3 x 14mm button head screw |
| 30  | [92832A215](https://www.mcmaster.com/92832A215) | M3 x  6mm button head screw |
| 12  | [91290A137](https://www.mcmaster.com/91290A137) | M3 x 50mm button head screw |
| 100 | [90576A102](https://www.mcmaster.com/90576A102) | M3 nylon locking nut |
| 100 | [97259A101](https://www.mcmaster.com/97259A101) | M3 square nut 5.5mm wide |
| 100 | [93475A210](https://www.mcmaster.com/93475A210) | M3 washer |
| 8   | [95947A008](https://www.mcmaster.com/95947A008) | M3 x 12mm standoff |
| 8   | [90304A215](https://www.mcmaster.com/90304A215) | M4 x 8mm screw |
| 8   | [93475A230](https://www.mcmaster.com/93475A230) | M4 washer      |

(some of the quantities are 100 because the pack size is 100 and I don't actually know how many you need)

The above list is optimized to an extreme extent, including the usage of [cost-saving alternate versions of 3D printed parts](../other_pages/optional3dprintedparts). If you want your life to be easier, also purchase the following: (warning - I don't guarantee that these will get utilized)

| Sku                                             | Name                             | Why? |
|-------------------------------------------------|----------------------------------|------|
| [90991A113](https://www.mcmaster.com/90991A113) | M3 x  8mm button head screw      | just in case 6mm is too short  |
| [92832A225](https://www.mcmaster.com/92832A225) | M3 x 16mm button head screw      | just in case 14mm is too short |
| [90991A115](https://www.mcmaster.com/90991A115) | M3 x 12mm button head screw      | just in case 14mm is too long  |
| [92703A151](https://www.mcmaster.com/92703A151) | M3 x 12mm countersink head screw | original lead-nut mount design |
| [95947A012](https://www.mcmaster.com/95947A012) | M3 x 16mm standoff               | higher circuit board mounting  |

McMaster-Carr doesn't tell you what the shipping costs are, but in the end, it should still be cheaper than Amazon. (warning - if McMaster-Carr ships from two different warehouses, you pay extra shipping)

McMaster-Carr does NOT stock T-slot-nuts for M5 screws, or at least... they do but they cost like $2 each and we'd need like 180 of them. So this one we have to buy from Amazon. They cost about $10 for a pack of 100. (specs: 2020 series T-slot nut for M5 screws)

### Frame Brackets

 * 10x T shaped frame brackets
 * 18x L shaped frame brackets
 * 26x corner frame brackets

Buy extras, I may have miscounted.

If the frame brackets do not come with screws already, then you will need to purchase an additional 180x ["M5 x 8mm flanged button head screw" (SKU 90909A721) from McMaster-Carr](https://www.mcmaster.com/90909A721).

These should also have come with T-slot-nuts

### Bed Leveling Springs

Amazon sells bed leveling springs in packs of 4 which includes the knob as well. I have not tried these, and I question just how good those springs are.

I do have some suggestions that are from McMaster-Carr that are much stronger. Stronger is good, it'll make the bed more stable. My suggestion is this set of parts:

 * [spring SKU 94125K204](https://www.mcmaster.com/94125K204), which comes in a pack of 5, and works great with our design
 * [screw SKU 92125A150](https://www.mcmaster.com/92125A150), M3 screw with countersink head, very long
 * [nut SKU 94300A120](https://www.mcmaster.com/94300A120), M3 wing nut, use as the knob

### Z Axis Leadscrew and Lead-Nut

This one must be a 380mm long leadscrew integrated into a NEMA stepper motor.

 * [Pololu product number 2690:](https://www.pololu.com/product/2690) "Stepper Motor with 38cm Lead Screw: Bipolar, 200 Steps/Rev, 42×38mm, 2.8V, 1.7 A/Phase"

Seemingly equivalent products from overseas costs about half the price. Make sure the leadscrew is TR8x8, and 380mm long. Make sure the physical and electrical specifications are similar. 

Make sure you get at least two lead-nuts! One should come with the motor, get a spare!

### Motion Components

#### X and Y Axis Stepper Motors

Buy 2 of them. NEMA 17 sized stepper motor with 5mm D shaped output shaft. 200 steps per rotation, phase current rating of about 1.5 amps or more, bipolar.

This [17HS15-1504S-X1 from OMC](https://www.omc-stepperonline.com/nema-17-bipolar-45ncm-6374ozin-15a-42x42x39mm-4-wires-w--1m-pin-connector.html) is absolutely perfectly suitable for a 3D printer like ours, and comes with a 1m cable. Should be about $9 each. Another option is [17HS15-1684S from OMC](https://www.omc-stepperonline.com/nema-17-stepper-motor/nema-17-bipolar-1-8deg-36ncm-51oz-in-1-68a-2-8v-42x42x39mm-4-wires.html), which doesn't have a connector but still have a cable.

#### 8mm diameter linear rods

Buy 6 of them. 8mm diameter, 440mm long, hardened steel, chrome plated.

For comparison, getting the best quality possible from MiSUMi, they'll cost about $20 each. On Amazon, something that might work costs $8 each, in a pack of 2.

If you want to buy from MiSUMi, you can get each rod custom cut-to-length.

#### 16mm diameter linear rods

Buy 2 of them. 16mm diameter, 400mm long, hardened steel, chrome plated.

So far I've not found a good deal for these. They are $15.50 each on MiSUMi ([part number PSFJ16-400](https://us.misumi-ec.com/vona2/detail/110302634310/?PNSearch=PSFJ16-400)).

If you want to buy from MiSUMi, you can get each rod custom cut-to-length.

#### LM8UU linear ball bearings

Buy 4 of them. 8mm inner diameter, 15mm outer diameter, 25mm long.

The standard LM8UU on MiSUMi costs $6.50 each ([part number LMU8](https://us.misumi-ec.com/vona2/detail/110300026540/?HissuCode=LMU8)). Amazon has them for about $2 each if you get a pack of 4.

#### LM16UU linear ball bearings

Buy 4 of them. 16mm inner diameter, 28mm outer diameter, 37mm long.

The standard LM8UU on MiSUMi costs $8.13 each ([part number LMU16](https://us.misumi-ec.com/vona2/detail/110300026540/?HissuCode=LMU16)). Amazon has them for about $3 each if you get a pack of 4.

We may need to upgrade to LM16LUU if the bed vibrates. This is highly unlikely though.

#### brass bushing

These must be "oil free" or "oil-less" or "self-lubricating graphite" brass bushings!

Buy 4 of them. 8mm inner diameter, 12mm outer diameter, 24mm or 25mm long. You can try putting two together that are 12mm to act as one piece.

MiSUMI has these for about $13.50 each ([part number MPBZ8-25](https://us.misumi-ec.com/vona2/detail/110300032230/?HissuCode=MPBZ8-25)). This might be a better deal than Amazon or eBay.

#### F608ZZ rotary ball bearing

Buy 8 of them. 8mm inner diameter, 22mm outer diameter, with flange, 6mm or 7mm overall thickness.

The standard F608ZZ on MiSUMi costs $12.28 each ([part number F608ZZ](https://us.misumi-ec.com/vona2/detail/221000058301/?PNSearch=F608ZZ&HissuCode=F608ZZ)). Amazon has them for about $2 each or lower, in large packs.

Another 4 more is needed for the spool holder but the spool holder do not need high quality ones.

#### Timing Belt

2GT profile 6mm wide timing belt, with some sort of fiber cord inside for reinforcement.

You need 4 chunks, each chunk should be about 760mm long, so you can also buy a roll that's longer than 3040mm long.

MiSUMi has these for about $7.85 per chunk ([part number GBN7602GT-60](https://us.misumi-ec.com/vona2/detail/110302652060/?HissuCode=GBN7602GT-60)). [Filastruder has the Gates branded 2GT belt](https://www.filastruder.com/products/gates-2gt-belts), it'll cost $31 for all the belt we need. Amazon lists 5 meters worth for $7.

#### Timing Belt Pulley

Buy 8 of them. 20 teeth, 8mm bore, 2GT profile, 6mm wide or slightly wider.

MiSUMi and Filastruder actually doesn't have a product that matches what we need, and no acceptable substitutes. The Ultimaker reseller [fbrc8 has some](https://fbrc8.com/products/pulley-8mm-assembly) that are $8.40 each. Otherwise, they are on Amazon for about $2.50 each, in packs of 5.

#### Timing Belt Tension Spring

Buy 4 of them. Torsion springs designed specifically to tighten up 6mm wide belts. These cost pennies!

#### Shaft Collar

Buy at least 10 of them, 20 is better. 8mm bore, about 7mm wide, about 14mm outer diameter, using set-screws for locking. Try getting ones that have two set-screws instead of just one if possible.

There's no reason to get high quality versions of these. They are dirt cheap. I'm not even going to research them.

#### Shaft Coupling

Buy at least 2 of them. 8mm bore to 5mm bore, 25mm long, 18mm outer diameter, flexible aluminum.

There's no reason for these to be high quality. About $3 or less is a fine price.

### Extruder

We've talked about the [E3D Hemera extruder](https://e3d-online.com/e3d-hemera) many times. This is what we must use. Get the full package with 12V electronics. It comes packaged with a lot of stuff so make sure you are not buying anything duplicated.

### Hot-End Components

The heat-block should be an [aluminum heat-block](https://e3d-online.com/v6-heater-block-for-sensor-cartridges) from E3D-Online.

The heater cartidge must be a 12V 30W [heater cartidge](https://e3d-online.com/standard-heater-cartridge) from E3D-Online. Knock-offs may have problems fitting properly into the heat-block, which is a potential hazard and lowers efficiency.

The temperature sensor should be a [thermistor cartridge](https://e3d-online.com/thermistor-cartridge) designed specifically for the heat-block.

### Cooling Fan

The extruder should've already included a [12V cooling fan](https://e3d-online.com/e3d-hemera-fan). You should get another one to cool the control circuit board. Should be 40mm x 40mm square shape and 10mm thick.

Get a Noctua NF-A4x10 if you are willing to spend $15 on just a cooling fan. It's super quiet. Otherwise, shop around, they are cheap.

### Blower Fan

You will need a small centrifugal blower fan, 40mm x 40mm square shape, 10mm thich, running on 12V.

These usually cost about $6 on Amazon, usually in packs of 2 or 4.

# Aside

#### E3D-Online

E3D-Online is a company in the UK who has many American [resellers](https://e3d-online.com/resellers) that you can trust, I typically use [Filastruder](https://www.filastruder.com/), who also resells parts from Duet and Gates.

#### Stainless Steel

None of this machine is meant to work outdoors or in a wet environment. You can choose steel or stainless steel according to price. Black oxide is also fine.

#### Torx

Use torx screws whenever possible. They will save you so many headaches because they are impossible to strip. Their wrenches and drivers do not have metric or imperial versions, it's always just a "T number", so it's impossible to strip the screw head by using the wrong tool.

Hex is the next preferred type, at least it's better than philips, because a wrench can apply more torque to the screw.

#### Lock Nuts, Lock Washers

Using square nuts and flat washers is fine in this 3D printer. The vibrations expected isn't strong enough to shake the screws loose. Use a thread-locker if you wish.

The Ultimaker brand of 3D printers use mostly square nuts for their frame assembly and nylon locking nuts for everything else. They rarely even use washers. Their printers will last several years of continued abuse.

My own Hephaestus 3D printer used locking nuts and locking washers everywhere because the printer itself was a present to myself. Plus, some of the screws were literally impossible to tighten once they have been installed. This new design is different from Hephaestus, every screw can be tightened without much trouble.
