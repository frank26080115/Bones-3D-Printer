# 3D Printer Electronics

This lesson will be a little bit of general overview, and a lot of math! I will focus less on what things do (which the other lessons cover), and focus more on how to check for safety and pick components.

I am an electrical engineer, who can design every circuit board being used in a 3D printer. But if I wrote down absolutely everything I know, you'll get bored and miss the safety information. So I will keep it short and stick with important stuff.

## The building blocks

The major electrical components are:

 * Power Supply Unit (ie. PSU)
 * Control Circuit
 * Bed Heater (and temperature sensor)
 * Nozzle Heater (and temperature sensor)
 * Limit Switches
 * Hot-end Heatsink Fan
 * Part Cooling Fan
 * Maybe a LCD screen

### Power Input and PSU

The power that arrives at your home is 120VAC (in North America), AC meaning alternating current. This is quite high and quite dangerous for a computerized device like a 3D printer. We will use a power supply unit (PSU) to convert the 120VAC down to 12VDC so that our sensitive components can work properly, and not die when we make a mistake.

When shopping for a PSU, you'll need to look for:

 * rated for a 120VAC input
 * provides a 12VDC output
 * can output enough power (watts) to power the printer

#### Total Power Used

We'll very roughly add up the power consumption in our 3D printer:

 * 120W for the heated bed
 * 20W to 40W for the nozzle heater
 * 3 stepper motors, 5W each

The supporting electronics, such as the microcontroller, won't draw much, it should be drawing current in only milliamperes.

We have 175W total, and if we give it some safety margin, we can look for a 200W or better power supply. You can find one higher if you plan on doing upgrades.

If we are using 178W at 12V, then we can calculate the current consumption at this power consumption:

<nobr> 175W &divide; 12V = 14.6A </nobr> (we might round this to 15A later)

(175W is the worst case scenario, typically your bed heater is only fully powered up during pre-heat, and doesn't use much power to maintain heat)

#### AC Input and Conversion

When converting between different voltages, remember the [Law of Conservation of Energy](https://en.wikipedia.org/wiki/Conservation_of_energy). ~~If you don't conserve power, the cops will come and arrest you.~~ Power in must always equal power out. There's no free ~~lunch~~ power in the universe.

We know our printer is using about 15A from the 12VDC output. Then using the same calculation, we can calculate how much current is going into the 120VAC input:

<nobr> 175W &divide; 120V = 1.46A </nobr> (we might round this to 1.5A later)

The conversion isn't perfect though. Remember that everything in the universe is a resistor, even copper. The components inside the PSU has some resistance that will waste some power as heat while it is doing the conversion. The efficiency is advertised as "up to 89% efficient". If we are using 175W from the 12VDC output, then how much power are we actually taking?

<nobr> 175W &divide; 0.89 = 196.6W </nobr>

We are using 196.6W from your wall outlet. Let's do that current consumption calculation using this more realistic power consumption value:

<nobr> 196.6W &divide; 120V = 1.64A </nobr>

#### What's the important takeaway?

Safety First! But don't worry, a typical desktop computer uses about 500W, a microwave uses much more than 1000W. Your house should be protected by many circuit breakers, typically 10A or 15A, and our 3D printer will not trip those circuit breakers.

On the AC power input side, you only need to handle 1.64A of current, this means you need to use wires that have an insulation rated for more than 120VAC, and copper thickness that can handle 1.64A of current. If you think about it, a iPad charging cable can handle 2A easily but doesn't have thick insulation. This isn't very scary.

You'll want to use a fuse on the AC power input side, rated anywhere between 1.8A and 5A would be fine.

On the DC power output side, you'll want wires that can handle 15A of current for the main bus wire, and insulated to handle 12VDC. You will need a 20A fuse, typically installed on the control circuit board.

#### What do fuses (and circuit breakers) do?

Accidents happen, and we all make mistakes. Pretend you were using a drill on a piece of metal, but you lost your grip and that piece of metal flies across the room and hits your 3D printer's power cable, causing a short circuit! This would cause current to flow much greater than just 15A, I would actually expect some sparks. Without a fuse, then some electrical components, wires, and connectors, will start getting very hot, potentially starting a fire.

[Wikipedia: Fuse](https://en.wikipedia.org/wiki/Fuse_(electrical))

[Wikipedia: Circuit Breaker](https://en.wikipedia.org/wiki/Circuit_breaker)

## Grounding (aka Earthing)

Have you ever wondered what this round hole in a power outlet actually does? That's the ground pin. Its job is to protect you from electrical shock.

Imagine that piece of metal hit the 120VAC wire, and also touched the aluminum frame of the 3D printer, while you were holding it. If the frame was not grounded, then there's a chance that you be electrically shocked with 120VAC. If the frame was grounded, then all that high voltage would go into the ground, and not hurt you, moments later, the fuse should blow, and everything would be totally safe.

Grounding also prevents build-up of static electricity, because the static charges would go directly into the ground.

You also want to ground the negative terminal of the DC output. This is because the conversion from AC to DC can still have a small bit of AC leaking into the DC side. It's most often not dangerous but you can still feel a small shock if you touched something with even a few millivolts of AC.

[Wikipedia: Grounding](https://en.wikipedia.org/wiki/Ground_(electricity))

### Voltage choices, and why it matters

Most inexpensive 3D printers use a 12V DC power source. This is mostly due to Arduinos having an input voltage rating lower than 24V. As a result, it is much easier for us to find printer bed heaters that are rated for 12V.

A typical bed heater for a print bed we've designed is capable of outputting about 120W. Voltage multiplied by current equals power.

<nobr> 120W &divide; 12V = 10A </nobr>

We now know the current, then we can find the resistance of the bed heater. Remember that any resistor is a heating element, any heating element is a resistor. For this calculation, we use Ohm's Law:

<nobr> 12V &divide; 10A = 1.2&Omega; </nobr>

What happens when you use a 24V power supply but a 1.2&Omega; heating element? Use Ohm's Law again:

<nobr> 24V &divide; 1.2&Omega; = 20A </nobr>

20A is quite a big jump from 10A. Of course this would also feed double the power into the heating element:

<nobr> 24V x 20A = 480W </nobr>

Whoa! Maybe you thought that you can get away with just upgrading the wires and fuses to be a bit beefier for just an extra $5, but now we are into spending an extra $50 on a more beefy power supply.

This particular 3D printer I've designed is meant to use a very specific power supply, the MEAN WELL LRS-350-12, which can output a maximum of 350W. I am very happy about this particular product, it is reliable, intelligent (it's quiet, it's very good at knowing when to kick the cooling fan on), and compact.

24V is useful though, if you were to use a heater that's rated for 24V and still outputs 120W, then it means you'll only need 5A of current, this means you could potentially save some money on cheaper wires. But this is NOT why people build 24V printers.

People do need 24V or even higher voltage when they want to use more powerful heating elements, and drive more powerful motors. You need more heating and bigger motors for larger printers.

## Stepper motor electrical ratings

When you purchase a stepper motor, you'll see that it has a current rating and a voltage rating. For example, commonly, a current rating of 1.68A and voltage rating of 2.8V

Whoa, 12V is much more than 2.8V, do we need a 2.8V power supply? No...

Stepper motors are driven by dedicated stepper motor driver chips. These chips will have a feature called "current limiting".

Remember that the stepper motors are really just coils on the inside, and any conductor, even if it's copper, still has a resistance. That coil has a resistance and it obeys Ohm's Law

<nobr> 2.8V &divide; 1.68A = 1.67&Omega; </nobr>

(reading the datasheet, the coil resistance is measured at 1.65&Omega; so we are pretty close)

Pretend we've told the steppper motor driver to limit the current at 1.5A, then, since the coil has a resistance of 1.65&Omega;, we use Ohm's Law

<nobr> 1.5A x 1.65&Omega; = 2.475V </nobr>

Which would be fine. It's not about how much voltage is going into the stepper motor driver chip, it's all about how much current that chip is outputting.

Remember how I guessed that each stepper motor uses 5W? I simply multiplied 1.7A by 2.9V which gave me 4.9W

## Temperature Sensors

The most common type of temperature sensors for 3D printers are NTC thermistors and thermocouples.

A thermistor is a resistor that changes resistance according to temperature. They are easy for a microcontroller to read, using analog to digital conversion, and another resistor to provide a voltage divider. If you use poor tolerance resistor and a poor performing analog converter, then the accuracy will be poor. Thermistors are also limited to about 250 degrees C, you can go higher, especially ones designed for cheap 3D printers, but probably not a great choice for higher temperature 3D printed materials.

A thermocouple is much more accurate and responsive, but it is expensive and requires an amplifier to work, adding to the overall costs. The amplifier will actually output the temperature in degrees, very accurately. They also handle much higher temperatures.

Also, annoyingly... you cannot cut a thermocouple's wires! You must use one continuous piece of wire that the thermocouple was manufactured with. No cutting, no soldering, no connectors allowed, it will stop working. They are very difficult to use correctly. It's quite an engineering challenge to plan out your wiring when you want to use thermocouple.

We will be using thermistors for both the bed heater and the nozzle heater. The bed heater usually has a thermistor built-in already. The Hemera extruder kit will include both the nozzle heater and the nozzle thermistor as well.

[Wikipedia: Thermistor](https://en.wikipedia.org/wiki/Thermistor)

[Wikipedia: Thermocouple](https://en.wikipedia.org/wiki/Thermocouple)

## Cooling Fans

There are three cooling fans in our design:

 * one mounted to the Hemera extruder's heatsink
 * one that blows air under the nozzle
 * one that cools the control circuit board

None of these fans are safety critical.

The heatsink fan is there so that the filament doesn't jam in the hot-end, it helps the heat-break maintain a sharp temperature transition, meaning we want it to be hot on one side, and cold on the other side, and not warm in between. Unwanted large warm areas inside a hot-end is where filament jams happen.

The fan that blows air under the nozzle is there to cool the plastic after it has exited the hot nozzle. It will make the print look nicer for some types of plastic. (not all types, the firmware will turn it off according to the type of plastic)

The circuit board may need some cooling, as the stepper motor drivers, and heater MOSFETs, will get very hot.

## Control Circuitry

The control circuit can be broken down into more detail:

 * Microcontroller
 * Interfaces (eg. USB port, LCD screen, Networking)
 * Storage Device (eg. SD card)
 * Temperature Sensor Inputs
 * Fan Control Outputs
 * Bed Heater Outputs
 * Nozzle Heater Outputs
 * Stepper Motor Drivers

We are building a 3D printer that's very similar to other 3D printers on the market, this makes it easy for us to find a suitable 3D printer control circuit to purchase. They all generally have the same features.

The microcontroller is the brain that will execute the firmware code. It is connected to all the sensor inputs and is able to give control signals to all the outputs. It can control the stepper motors by giving instructions to the stepper motor drivers. It controls the heaters with the help from the temperature sensors. It can read files from the SD card to perform print jobs.

When shopping for a control circuit, we are checking the following specifications:

 * What type of microcontroller is it using, 8-bit or 32-bit?
 * How many stepper motors can it drive, and what stepper motor driver chips are used? What are their ratings?
 * What's the maximum power it can provide to the heaters?
 * Does it have the inputs and outputs we need? Does it support our sensors and our cooling fans?
 * How does the user interact with it? LCD screen? SD card? USB port?
