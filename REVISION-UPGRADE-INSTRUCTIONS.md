# How to turn your Adelheid Rev1.0 PCB into Rev2.0

## Goal

Revision 1.0 of the PCB uses the wrong pin for the backlight functionality which causes the LEDs to flicker. The pin that controls the backlighting has to support PWM. Pin F6 does not, however pins B7, D0, D7, B5, B6, C6, C7 do.

&rarr; **swap pin C6 with F6**

## Steps

1. Get 2 short wires and strip off the insulation on both ends and add solder.
2. Add a generous amount of flux to the MCU where you want to solder on the wires. Pin F6 and Pin C6.

![first step](https://gist.githubusercontent.com/floookay/7bf6511a8d84804d32de4d7bbe3bd0fb/raw/c87a478d297af8eb8f7ab86c3eeb79d1fd98e5e3/rev1_step1.jpg)

3. Solder one end of each wire to the MCU.
4. Cut the existing traces with a cutter or a pair of tweezers. Make sure to not damage other parts of the PCB. Good places to cut the trace are marked with blue circles in the image above.
5. Check with a Multimeter that the traces are truly disconnected and that the cables are properly attached to the correct MCU pins.
6. Make a updated version of the Adelheid firmware and flash it to the board.
7. Lastly solder on the other ends of the wires like in the picture below.

![second step](https://gist.githubusercontent.com/floookay/7bf6511a8d84804d32de4d7bbe3bd0fb/raw/c87a478d297af8eb8f7ab86c3eeb79d1fd98e5e3/rev1_step2.jpg)

8. Clean your PCB from solder sprinkles.
