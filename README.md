# Olympus Pen D2 Repair
Repairing a mechanically and electrically faulty Olympus Pen D2 film camera.

## Electrical Repairs

***AKA: Repairing an Olympus Pen D2/D3 light meter and converting it to 1.55V SR44 batteries.***

See [my post about this repair](https://www.reddit.com/r/AnalogCommunity/comments/x2htal/designing_a_cds_light_meter_circuit/) on Reddit.

I have sucessfully repaired the meter and converted it to run on *SR44 (1.55 volt)* batteries. Here's the notes I took.

I have attached a new simpler schematic that better illustrates how the meter circuit works. The CdS LDR is actually two seperate LDRs merged into one. The meter runs off two parallel circuits that work together to give a final reading. From what I can gather... The *high resistance* LDR plus resistor ***S*** control the high end of the EV range, and the *low resistance* LDR plus resistors ***S*** and ***P*** control the low end of the EV range. *(See color coded schematic and image of wired up LDR.)*

I used trim-pots to calibrate the meter for *1.55 volts*, and I arrived at ***S*** *= 9.1 kΩ* and ***P*** *= 18 kΩ*. (Actually *9.5 kΩ* but the closest resistor value I could buy was *9.1 kΩ*. This is acceptable.)

I measured less than *100 μA* of current draw while metering moderate light. The theoretical maximum power consumption is less than *300 μW*, so a single *SR44* battery will last years.

The circuit is not voltage regulated, so **silver oxide** batteries must be used as they maintain consistent voltage across their lifetime. Under extremely low power applications, *SR44* cells typically start at *1.60 V* and settle around *1.55 V* until depletion.

I tested the calibrated meter with near depleted cells at *\~1.50 V*. Compared to brand new cells at *\~1.60 V* the meter read roughly half a stop lower *(e.g. EV 10.5 instead of EV 11)*. Totally acceptable.

The LDR had three layers of ND filters over it and a spot of black marker drawn over the central terminal of the LDR, probably to recalibrate the meter without having to change the resistors. I removed these. *If anyone else pulls apart their Pen and notices a spot of marker, let me know... It might have been put there at the factory.*

My calibrated meter has been tested accurate between *EV 10* to *EV 15*, but reads nearly half a stop lower between *EV 3* to *EV 7*. The spot of marker might have been to fix this difference between the high and low scales... I didn't draw the spot back on to test it.

Worst case I'd say it's accurate to ±1 stop, which is probably factory spec/tolerance.

Finally, I can confirm the solid metal body conducts the positive voltage from battery to the galvenometer (similar to how a car is wired).

![Reverse engineered schematic for Olympus Pen D2 light meter.](https://preview.redd.it/weybmhyfl2l91.jpg?width=4000&format=pjpg&auto=webp&s=afee574fb5b303a4237c27c2924f3639ef4dae9a)

![Simplified light meter schematic showing dual LDR split into distinct elements.](https://preview.redd.it/x33qtgq9wul91.jpg?width=2722&format=pjpg&auto=webp&s=6da070e1678e34289f012645039d4f519c8109d9)

![CdS cell \(LDR\) used in Olympus Pen D2 light meter.](https://preview.redd.it/ztua4cwgr2l91.png?width=2936&format=png&auto=webp&s=024c76a39e0dffcc03e8a3f36e85ab3fd368ec9b)

**Update:** After all this, the meter readings started jumping around erratically. I discovered that the button was not closing it's contacts properly, and was not only bouncing, but also introducing additonal resistance.

To fix this, I carefully deconstructed the button by unscrewing the golden top and removing the push-needle-rod-thing and the rubber bumper underneath the spring. You do not need to desolder the spring, just gently move it up and out of the tube so that the bumper can slide out.

The contact plate below the bumper had a deep indent in it made by the needle, so I cut up a tiny metal shim and placed it above the existing contact place. The needle will now make contact with the flat shim.

As a consequence, the button is now activated without depressing it as far. If you use a shim that is too thick, when it is reinstalled in the Pen's body, the button can be activated without being touched.

To avoid this, use a thin shim *(I cut off a fragment of a 9V battery terminal which is about 0.5mm thick)*, and set the button as far back as possible when you screw it in place *(this meant the button was slightly off axis, pointing to the side, but it still functions perfectly and is within spec)*.

**Update:** I also think that there isn't propper shielding between the circuit and the metal body; My meter frequently jumps between two readings (as if it were switching between high and low sensitivity settings). My best guess is the case is adding a parallel circuit to the loop occasionally.

## Mechanical Repairs

The camera required a complete and full dissassembly. Each individual part from the light meter to the shutter was removed and ultrasonically cleaned, before being reconstructed and lubricated.

The shutter was slow as the shutter blades required cleaning.
The aperture blades were in fine condition, and did not need to be bothered about as the aperture is manually stopped down always.

The winding function does not cock the shutter and allows the film to be wound infinitely, _but only_ when the top plate of the camera is attached; otherwise it works correctly while naked. This is a new problem I do not know how to fix.

![temp images here](IMAGE URL)

## Flash Unit

Custom designed flash unit for the **Olympus Pen** series.
Fitted to attach to the base of the **Pen D2** and synchronised with a PC socket at all speeds.

This section also includes designs to fabricate the same flash but for a **Canon P (Populaire)** instead.

![temp images here](IMAGE URL)
