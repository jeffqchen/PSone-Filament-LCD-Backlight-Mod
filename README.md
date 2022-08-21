# PSone Filament LCD Backlight Mod

The official PSone LCD screen has a fragile backlight system. The inverter and the CCFL tube could kick the bucket on itself. Sometimes you can't even figure out what went wrong with the backlight system. It's also nearly impossible to find the exact replacement parts at a reasonable price, even if you managed to figure it out.

<img src="./Pics/faulty_backlight.jpg" width=500>

Previously, there were multiple attempts of similar mods. But they all used singular LEDs, and resulted in uneven backlight that's difficult to look at. This new type of flexible filament LED provides the evenness as good as the CCFL tube, and is very easy to manipulate. More importantly, they are very affordable.

<img src="./Pics/filament_led.jpg" width=500>

So here is my solution, just in case you are facing the dilemma (however, by all means, please try to diagnose and fix the original system if possible).

<img src="./Pics/project_cover.jpg" width=500>

This design takes the 7.5V from the power input, runs it through an NPN amplifier, to feed two 3.3V flexible filament LED strips and some current-limiting resistors, controlled by the 5V_CON signal from the console.

<img src="./Pics/schematic.jpg" width=600>

Please note these values were fine tuned and do not match the perfect calculations. Somehow these filament LED strips do not drop the claimed voltage and I had to reduce the value of the current-limiting resistors to make them emit enough light. I did let the system run for an extended period of time to make sure it would last. The operation temperature was still much lower than the original design.

----------
## Parts

- [PCB](https://oshpark.com/shared_projects/M3fZRLg5)

- BSR14 NPN Amplifier

- [2x] flexible filament LED strips, 130mm, 3V, cold white 6500K

- Right-angle pin header

**All resistors are 1/4W through hole resistors.**

- R1-3: 48 Ohm
- R4, R5: 1.2K Ohm

----------
## PCB Assembly

Nothing is special about populating the parts.

<img src="./Pics/soldering_02.jpg" width=500>

Make sure the right-angled pin headers are on the invisible side of the PCB.

<img src="./Pics/pcb_populated_front.jpg" width=300> <img src="./Pics/pcb_populated_back.jpg" width=300>

Only two pins are necessary on each side of the PCB.

Cut and remove the black spacer after the pins are soldered in place.

<img src="./Pics/soldering_01.jpg" width=500>

Trim the legs somewhat so they don't reach too far into the main PCB when installed.

<img src="./Pics/trim_pins.jpg" width=500>

----------
## PCone Screen Motherboard Modding

<img src="./Pics/.jpg" width=600>

Remove component C114, C116, C117, T1. Cut the thick trace next to CN3 marked with a cross.

<img src="./Pics/remove_component.jpg" width=600>

----------
## Installing Mod PCB

Solder the pin headers to the inside of the mother board as shown in the photo. Note you need 3 pins in a row but have to skip the middle one. You might want to cut off the middle one before hand.

Solder two jumper wires as shown in the photo.

<img src="./Pics/installed_inside.jpg" width=600>

Solder a wire to the DC_CON test point on the motherboard, and solder the other end to the DC_CON on the mod board, as indicated in the photo.

<img src="./Pics/installed_outside.jpg" width=600>


----------
## Modding Backlight Assembly

Solder TWO flexible filament LEDs in series with a 60mm wire. The polarity of the LED strips does matter.

<img src="./Pics/led.jpg" width=600>

Disassemble the screen, and open up the backlight box assembly.

<img src="./Pics/backlight_01.jpg" width=600>

**VERY CAREFULLY** remove the CCFL tube.

Desolder the plug from the tube. Store the CCFL in a rigid environment so it doesn't have the chance to break.

<img src="./Pics/backlight_02.jpg" width=600>

Solder the red wire to the positive end of the LED filament in series, and the white end to the negative end on the other.

Fit the new LED assembly back into the backlight box like the original, then reassemble the entire LCD screen assembly.

<img src="./Pics/backlight_03.jpg" width=600>

----------
## Reassembly

Reseat the screen into the shell, reseat the motherboard onto the back of the screen assembly, then plug in the screen ribbon cable and lock the tab. Plug back in the screen backlight header.

To safely test the machine, secure the motherboard with at least two screws so the screen doesn't fall apart and cause damage.

----------
## Result

The backlight should now work. The backlight will not turn on until the PSone is powered on, exactly like how the screen is supposed to work.

The evenness of the new backlight should be great - exactly like the original CCFL.

<img src="./Pics/result.jpg" width=600>

The color temperature of these filament LEDs is different from the original, as compared below. Personally I think the original CCFL was too blue and the LEDs look more natural.

<img src="./Pics/comparison.jpg" width=600>
