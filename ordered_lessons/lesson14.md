# Printer Operation and First Printer

I can't write this section well, because I never actually built this printer or used Marlin myself. Everything should be pretty obvious from the LCD screen's menu system though. Good luck.

## Loading Filament

The LCD screen should have a menu option that allows you to load and unload filament. Use that, it will guide you. Also remember that the Hemera has a lever that releases the filament.

For loading filament, generally the printer will heat up the nozzle, and then spin the extruder motor slowly. You will insert the filament into the extruder and wait until it comes out the nozzle. The leftover colour in the nozzle will come out first, then the colour will change to whatever new colour of plastic you just put in. Then you tell the printer to stop.

For unloading filament, the printer will heat up the nozzle, and then spin the extruder motor backwards slowly. The filament should exit and you can stop the printer.

If you change the material of filament you are using, you must also change it in the Cura slicer and re-generate the file you want to print. This is because the commands to set the temperature is included in the file on the SD card.

## Leveling the Bed

There might be an item in the LCD screen's menu system to initiate bed leveling. It will have instructions on the screen. Basically it will put the bed close to the nozzle, and you turn the bed leveling knobs until the distance is just right. You will do this for 3 or 4 corners of the bed.

The other way is to simply start printing. Usually the print starts with a skirt or brim, which is an outer line of plastic that is not a part of the actual 3D model. You can see if this line is too thick or too thin while it is printing. Where it is too thick, it means you need to raise the bed level on that side, and vice versa, lower the bed level where the line seems too thin.

## Starting a Print

Put the microSD card into the printer. Use the LCD screen to select the file and start the print.

This will take a while...

Are you confident that the machine won't catch fire? Don't leave your machine alone for the first few hours. Continue to monitor it, monitor it's connectors. Watch for smoke and fires. Progressively do bigger and bigger prints until you're sure it can handle very long jobs without problems. Perform more stress tests if you wish.

## Troubleshooting

There's a billion things that could go wrong. Here are some resources to help you troubleshoot problems with 3D prints

 * Simplify3D: [Print Quality Troubleshooting Guide](https://www.simplify3d.com/support/print-quality-troubleshooting/)
 * rigid.ink: [The Ultimate 3D Print Quality Troubleshooting Guide 2019](https://rigid.ink/pages/ultimate-troubleshooting-guide)
 * MatterHackers: [3D Printer Troubleshooting Guide](https://www.matterhackers.com/articles/3d-printer-troubleshooting-guide)
 * Prusa3D: [3D Print Quality Troubleshooting Guide](https://www.prusa3d.com/print-quality-troubleshooting/)
 * All3DP: [Problem Solved - Troubleshooting Guide to Common 3D Printing Problems](https://all3dp.com/1/common-3d-printing-problems-troubleshooting-3d-printer-issues/)

#### Electromagnetic Interference

Does your print randomly stop and the printer shows an error? Perhaps a temperature related error or a limit switch related error? First, use a multimeter to double check your wiring. If the wiring is fine but these errors still happen, then perhaps the wires for the switches or sensors might be put too close to the wires for a stepper motor. The stepper motors are driven with a very strong and constantly changing signal, this kind of signal generates a ton of electromagnetic radiation. This could cause crosstalk ([Wikipedia article click here](https://en.wikipedia.org/wiki/Crosstalk)) into other wires with weak signals, just like our sensors and switches. To fix this, simply move the wires for the sensors and switches away from the wires of the stepper motors. Other ways of fixing this is to use shielded cables, but that would get really expensive.
