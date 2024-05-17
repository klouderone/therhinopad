# The Rhino Pad Macro Pad by Kea Workshop

![Finished Built Raw](https://github.com/klouderone/therhinopad/assets/136342173/7532a64a-21ee-4ed4-a29c-350c069533df)

The Rhino Pad is a compact Macro Pad tailored for Computer-Aided Drawing, with 13 keys and an encoder that can be programmed for any macro in your program. It supports QMK or ZMK with either a Pro Micro or similar for QMK, or the Nice!Nano V2 for ZMK. The Keycap spacing is 19.05mm x 19.05mm, NOT the usual choc keycap spacing. You can find the 3D printed keycaps on printables https://www.printables.com/model/685983-kea-workshop-choc-v1-mx-spaced-keycaps. 

**Features:**

- 13 Switches, 1 Encoder
- Pro Micro / Elite C footprint
- Supports MX and Choc Hotswap Switches
- Supports wireless Microcontrollers (nice!nano); built in battery pads and battery switch pads
- Magnetic Sandwich Case

## Build Guide

This build is a medium-hard build. It is recommended that you use solder paste for the diodes, as it takes patience and a steady hand to solder them using an Iron.

**PLEASE MAKE SURE TO READ THE WHOLE GUIDE BEFORE COMMENCING BUILD.**

**Parts Needed:**
- 1x Rhino Macropad PCB
- 13x Kailh Choc Hot Swap Sockets
- 2x B3U-1000P Tactile Button (extra for mistake)
- 26x Mill-Max Pins
- 2x 13 Pin Mill-Max Sockets
- 20x 1N4148 SOD-123 Diodes (extra for mistakes)
- 1x EC11 Encoder
- 1x 3 Pin Toggle Switch (MSK-12C02 & PCM12SMTR)
- 13x Choc switches
- 13x Choc keycaps
- 1x Microcontroller (Elite C/Pro Micro/Nice!Nano V2)
- 1x OLED Display with matching header (optional)

### STEP ZERO: Flash Microcontroller with Known Firmware

First thing to do is to flash the microcontroller with the given firmware. This is to ensure that the Microcontroller works properly, and if it doesn't, is returnable/refundable to the vendor you bought it from. If you are using QMK, download the QMK toolbox and the VIAL firmware for your microcontroller, .uf2 for Elite-C RP2040 controllers, or .hex for Pro-Micro ATMega32U4 controllers. A google will be able to show you how to flash for your microcontroller. 

### STEP ONE: Soldering the Reset Button

Soldering the reset button is the most difficult due to its small contacts, though it is not required for the board to work. If you do not want to solder the reset button, you just need to bridge the pads on the back of the board with tweezers to put it into bootloader mode. Carefully and steadily use tweezers to correctly align the button, heat up the tinned pad and place the button onto the pad, remove the heat and let the solder solidify. Then solder the other pad to secure, and possibly add a touch more solder on the first pad.

### STEP TWO: Soldering the Battery Switch (wireless version only)

Soldering the battery switch is a little more complex than the reset button. I reccommend solder paste for this. If you do not use solder paste, tin one pad first. Place the switch onto the pad and hold it steady using tweezers, heat it up, and push it into the solder and let it solidify. Carefully solder all other pads to the PCB.

### STEP THREE: Soldering the diodes 

There are two ways to do this, both require tweezers;

Option One: using solder paste and a heat gun (hairdryer may work)

Apply solder paste into all the diode pads. Use your tweezers to carefully place the diodes in the correct orientation on top of the pads. Gently apply heat using a hot plate or a heat gun, and watch the diodes pull themselves into place.

Option Two: using, a clean soldering iron, a steady hand, and patience.

Tin the top pad of all the diode pads. Carefully and steadily use tweezers hold and correctly align the diode, heat up the tinned pad, and place the diode onto the pad. Then, solder the other pad to secure. 

### STEP FOUR: Solder Hotswap Sockets

Tin one of the Hotswap pads. Place your hotswap socket into the holes, and heat up the tinned pad side while adding solder. Make sure to touch the pad or the contact of the hotswap socket that is on the pad. After a good connection, remove heat and solder other side. Repeat for all. I recommend pushing the hotswap socket in while soldering to get a good solder joint.

### STEP FIVE: Soldering Mill-Max sockets to PCB

To do this correctly, you want to put the sockets into the PCB holes (see photo below for placement depending on microcontroller), and put the Microcontroller on top to align them perpendicular to the PCB. Use putty or your finger to keep the sockets aligned and solder them into place.

If you are using a nice!nano or similar, you need a 13 pin socket, as the top pins are used as the battery pins, so that you can switch off and on the battery. If you are not using a nice!nano or similar, you only need a 12 pin socket, so simply snip off the extra socket and solder.  

![how to solder](https://github.com/klouderone/therhinopad/assets/136342173/18f9f7d3-a00d-4d5b-a83f-5d993afe8ea4)

### STEP SIX: Soldering Microcontroller to the Mill-Max Pins

Place the microcontroller onto the sockets, aligning the pins with the through-holes as shown, and carefully solder. Make sure you do not leave the iron on the pins/through-holes for too long, as you risk burning the traces of the microcontoller. Be sure to not use too much solder, as if you use too much it can flow down through the hole and join the socket and microcontroller. It is better to do too little and go back after later. Carefully remove the microcontroller to confirm that the joints are good. When removing, pull uniformly from both the USB side and the bottom side. Failure to do this can result in bending the Mill-Max pins. I have found using a switch puller to be handy doing this.

### STEP SEVEN: Soldering Display Pins

On the PCB, the display pins are noted of their output. If you are using an OLED display, disregard the CS pin (this is used for e-paper displays like the nice!view). If you are using Mill-Max sockets, you want a PH5 (plastic height 5) box header.  You can then solder the box header. 

### STEP EIGHT: Soldering the Encoder

Make sure the Encoder is flat up against the PCB when soldering. First solder the signal pins (as they require less heat than the locking pins) to hold the encoder in place, and then solder the locking pins. 

### STEP NINE: Soldering the Battery (wireless version only)

With the microcontroller out of the Mill-Max sockets, carefully solder the positive lead of the battery to the positive pad, and the negative lead to the negative pad. DO NOT LET THESE TWO LEADS TOUCH! 

### STEP TEN: 

Reinsert your microcontroller, install your switches and keycaps, and enjoy your new Macropad!

## Photos


![Rhino Pad PCB on Concrete Downsized](https://github.com/klouderone/therhinopad/assets/136342173/98acb469-6ab1-4682-90cb-9becd1a81c45)

![Rhino Pad In Sunlight Raw](https://github.com/klouderone/therhinopad/assets/136342173/616d3922-3b9c-4362-b5cb-f112fc74224c)

![1C0A9588](https://github.com/klouderone/therhinopad/assets/136342173/759a504e-d0ec-4d2b-a97f-19ea15972cc2)

![Rhino Macro Pad Case 3D Print](https://github.com/klouderone/therhinopad/assets/136342173/ae6c48cd-eaf5-4cdf-a334-ba2e1485ab1b)


