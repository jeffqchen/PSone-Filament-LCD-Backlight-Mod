# PSone Filament LCD Backlight Mod

The official PSone LCD screen has a fragile backlight system. The inverter and the CCFL tube could kick the bucket on itself. Sometimes you can't even figure out what went wrong with the backlight system. It's also nearly impossible to find the exact replacement parts at a reasonable price, even if you managed to figure it out.

So here is my solution, just in case you are facing the dilemma (however, by all means, try and fix the original if possible).

This design takes the 7.5V from the power input, runs it through an NPN amplifier, to feed two flexible filament LED strips and some current-limiting resistors, controlled by the 5V_CON signal from the console.
