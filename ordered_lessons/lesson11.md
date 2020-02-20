# Electronics Assembly Part 1

This page will have the stuff you need to do before you do mechanical assembly!

I will write this page assuming you already have the skills to solder, to crimp, and to use heat-shrink tubing. I will cover these skills in separate pages if you do not have these skills.

## Strategy

For the high current and high voltage connections on the power supply, we will be using screw terminals. They mate with spade connectors (aka fork connectors). They also technically accept bare wires but it's a lot more dangerous without using connectors.

For the high current connections on the control circuit board, there are some terminal blocks. Terminal blocks like these work best with proper wire ferrules, but also accept bare wires. We will avoid using bare wires.

For the low current connections, the control circuit board uses many JST-XH connectors. These have a 2.54mm pin pitch and are polarized.

Now here's some bad news. Spade connectors need a crimper, or even two crimpers. Wire ferrules need a special type of crimper. JST-XH also has its own type of crimper. One crimper is about $20, which doesn't sound bad for a tool that will keep you safe and your projects reliable for many years, but spending $60 on just crimpers for a 3D printer might be a bit daunting.

I know the promise is that the 3D printer is cheap to build. But I will be writing my instructions assuming you have access to the crimpers for the spade connectors and the wire ferrules. You are free to half-ass some of the wiring, but don't expect me to be happy about it if you ask me to inspect it in person.

The wires we'll be using are either 14 AWG or 24 AWG. To avoid using a crimper for the JST-XH connectors, we will buy a large pack of JST-XH pigtails.

## Shopping

 * soldering iron
    * 40W or more
    * with real temperature control
    * with a flared shape (the TS100 fails at this)
    * ideally compatible with Hakko tips or Weller tips
 * 63/37 solder with rosin core, 0.8mm diameter
 * flux, no-clean type preferred
 * desoldering braid (aka solder wick)
 * heat gun, hot air blower, or a cigarette lighter
 * wire stripper for 24 AWG
 * wire stripper for 14 AWG
 * crimper for insulated terminals (or get a crimper with a set of dies)
 * crimper for wire ferrules
 * variety pack of heat-shrink tubing in different sizes, all black, marine grade preferred but not required
 * variety pack of wire ferrules
 * pack of insulated spade terminals that fit 14 AWG wires and fits #8 screws
 * JST-XH pigtails, both male and female
 * cables for stepper motors, with connectors that work with the SKR Mini E3

Below is a massive image that shows all the things in the above list:

[![](../images/lesson11/shopping.png)](../images/lesson11/shopping.png)

## WARNING: JST-XH Polarity

If you have a keen eye, you'll notice that the JST-XH pigtails from Amazon may have different arrangements of red and black, and may even be backwards from common cooling fans and such. In fact, the one listing I wanted you to buy actually have a 17% one-star rating with people complaining about how it is backwards. We will keep this in mind but we will also solve this later.

Keep in mind that the limit switches and thermistors do not have polarity. Switches are dumb devices without polarity, current can flow through them in any direction. Thermistors are just resistors, so they also allow current to flow through both ways, so polarity for thermistors also does not matter.

## Limit Switches

There are three limit switches in our design, one for each axis of motion: X, Y, and Z.

These switches will have a very weak signal going through them so we will be using the 24 AWG wire.

You'll notice that the switches can be connected to 4.3mm wide quick disconnects, which you can use your crimpers for. But they don't make these connectors for wires as small as 24 AWG.

It's not dangerous to directly solder some wires directly to the terminals. Use heat-shrink tubing on the solder connection.

![](../images/lesson11/preplimitswitches.png)

Of course you need to do this 3 times.

We will be making extension cables for these switches later.

## Cooling Fans

The cooling fans come with wires and maybe a connector, but for the sake of making my job writing instructions easier... we'll prepare all the fans like so:

![](../images/lesson11/hemerafanpigtail.png)

![](../images/lesson11/boxfanpigtail.png)

![](../images/lesson11/blowerfanpigtail.png)

The choices for the connectors are made to make life easier later. The wire can be pretty thin because the fans are not power hungry. We will be making extension cables for these fans later.

## Heated Bed

This part you should do **after** the printer has been mostly assembled! You need to **prepare the drag chain, but not install it,** before wiring the heated bed!

![](../images/lesson11/heatedbedwireprep.png)

After you are done soldering, coat the entire area with "J-B Weld 31314 High Temperature RTV Silicone Gasket Maker and Sealant". This will protect the solder joints from debris causing short circuits. Wait for it to cure completely before continuing.

![](../images/lesson11/hightemprtvsealant.png)

![](../images/lesson11/hightemprtvsealantuse.png)

Be very careful not to break the solder joints while installing the heated bed to the 3D printer. After installing the bed with the springs and knobs, zip-tie the wires to the 3D printed bed cable anchor. This will keep the solder joints from breaking.

![](../images/lesson6/bedcableanchoroverview.png)

## Extension Cables

Make the following extension cables following the diagram.