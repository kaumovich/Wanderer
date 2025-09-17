# Wanderer
Wanderer is a wireless ultra low profile unibody 40% keyboard.  

![Preview]
---

## Main Features:  
* ultra low profile switches
* 3x6+3 unibody layout
* Bluetooth support
* 4 status LEDs
* Large battery capacity (pcb degsined for 402040 400mah battery)
* [ZMK firmware]

---

## ZMK Firmware  
ZMK firmware [here](https://github.com/Kaumovich/zmk-wanderer).  

P.S. firmwire fully based on KABARGA keyboard firmwire because it works really cool and i'm lazy

---


# Assembly Order:

Before starting assembly, read everything on this page. Since Kabarga supports a vast number of build variations, many details need to be explained for each component. Additionally, note that both the plate and bottom case have two sides with different designs—you can choose either during assembly. 

* Solder the diodes.
* Solder the reset button.
* Solder the power switch.
* Solder the resistors.
* Solder the MCU.
* If using hot-swap sockets, solder them at this stage.
* If using SMD LEDs, solder them at this stage.
* Clean the PCB from flux residue.
* Attach the standoffs to the plate. If desired, you can use silicone flat gaskets.
* If using through-hole LEDs, insert them into the PCB but do not solder them yet.
* Connect the plate, standoffs, and PCB together.
* Install the switches into the plate, starting from the corners.
* If not using hot-swap sockets, solder the switches.
* If using through-hole LEDs, press them against the plate, solder them, and trim the leads.
* Attach the battery to the plate using double-sided tape, then solder its leads to the PCB.
* Screw on the bottom case. If desired, you can use silicone flat gaskets.
* Attach the rubber feet.
* Press the reset button twice and flash the bootloader.
* Press the reset button twice again and flash the firmware.

---

## BOM:  
### Electronic components:
| Component          | Kabarga                    | 
| ------------------ | -------------------------- | 
| Reset              | EVQP7C01K                  | 
| MCU                | nice!nano v2               | 
| Diodes             | 1N4148WS T4 sod-32  42 pcs | 
| Power switch       | MSK-12C02                  | 
| Battery            | 402040 recomended          | 
| LEDs               | 0603                 4 pcs | 
| Resistors          | 0603 1-10k           4 pcs | 
| Keyboard switches  | Kailh pg1316        42 pcs | 


### MCU:
You can use any ProMicro-compatible MCU. Currently, ZMK firmware is available, but you can port QMK yourself if needed.


### Diodes:
![Preview](pics/diodes.png)  

Any SOD-323 diodes can be used. You can solder diodes on either side of the PCB, just make sure to follow the polarity shown in the diagram. However, the distance from the plate to the PCB in KS-27/33 is 1.2 mm, while the height of the diodes is 0.9 mm. This means you need to solder very carefully or place the diodes on the underside of the PCB. If you are not using hot-swap sockets and want to build the thinnest possible version by cutting all leads flush, you will likely prefer to solder the diodes under the plate.

### LEDs:
![Preview](pics/LED1_8mm.webp)  

The first three LEDs from the left indicate the battery level and the current BT profile. The rightmost LED signals a lost BT connection. In reality, the LED indicators can show much more, but this will be detailed later. You can use LEDs of the same or different colors, but keep in mind that different colors require different resistors, so balancing brightness across colors may be challenging.

![Preview](pics/led_footprint.png)

Through-hole LEDs (red on pic) should be soldered so that the rounded part of their casing aligns with the round pad on the PCB. On an SMD LED (blue on pic) , the stripe on the top of the casing should align with the square pad on the PCB.

### Resistors:
Resistors should be 1kΩ or higher, with the exact value depending on the color of the LEDs you are using. The maximum brightness of indicator LEDs can be adjusted in the firmware configuration file.


### case:

coming soon...
