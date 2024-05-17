# The Rhino Pad Macro Pad by Kea Workshop

The Rhino Pad is a compact Macro Pad tailored for Computer-Aided Drawing, with 13 keys and an encoder that can be programmed for any macro in your program. It supports QMK or ZMK with either a Pro Micro or similar for QMK, or the Nice!Nano V2 for ZMK. 

The Keycap spacing is 19.05mm x 19.05mm, NOT the usual choc keycap spacing. You can find the 3D printed keycaps on printables https://www.printables.com/model/685983-kea-workshop-choc-v1-mx-spaced-keycaps. 

The Case is 3D printed and uses 3mm x 2mm x 1mm magnets to hold it together. This is included in the files.

https://www.keaworkshop.com/product/rhino-pad

If you have any questions or want to get in contact with me, my discord is klouder#3331 or my email is claude@keaworkshop.com.

# Seagull Macropad

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

Reinsert you microcontroller, install your switches and keycaps, and enjoy your new Macropad!

## Firmware

V2 Known Issues: 
- Unable to change function of push button encoder on VIAL as the button is not in a matrix, and when designing I did not know that you cannot map a direct button. Changing this must be done in the QMK code. V2 Code to modify can be found above. Default Keystroke for this is KC_MUTE. (FIXED IN V3)

V3 Known Issues: 
- NA

## Photos

![Finished Built Raw](https://github.com/klouderone/therhinopad/assets/136342173/7532a64a-21ee-4ed4-a29c-350c069533df)

![Rhino Pad PCB on Concrete Downsized](https://github.com/klouderone/therhinopad/assets/136342173/98acb469-6ab1-4682-90cb-9becd1a81c45)

![Rhino Pad In Sunlight Raw](https://github.com/klouderone/therhinopad/assets/136342173/616d3922-3b9c-4362-b5cb-f112fc74224c)

![1C0A9588](https://github.com/klouderone/therhinopad/assets/136342173/759a504e-d0ec-4d2b-a97f-19ea15972cc2)

![Rhino Macro Pad Case 3D Print](https://github.com/klouderone/therhinopad/assets/136342173/ae6c48cd-eaf5-4cdf-a334-ba2e1485ab1b)

https://github.com/klouderone/therhinopad/assets/136342173/4a9ca853-e027-4251-8eb0-e6747945bf2f

## Build Guide

Solder the diodes onto the PCB. Make sure that the orientation of the diode matches that on the PCB, the flat line on both the PCB and Diode should be pointing the same direction. It is reccommended that you tin one pad on each diode placement, and use tweezers to hold the diode in the correct position and quickly melt the solder to lock it in place. Then solder the other untinned side of the diode, and go back to solder the original side of the diode. Ideally, you can use solder paste and place all the diodes correctly and then heat the PCB so they all fall into place.

<img width="1157" alt="Screenshot 2024-03-26 010702" src="https://github.com/klouderone/therhinopad/assets/136342173/abd3ebe3-e6ec-456a-b4f3-d995a5001cb6">   


<br>

Then solder the button and switch onto the PCB. Take your time doing this and use tweezers and a steady hand. Ideally, you can use solder paste to do this also. The switch is not neccessary if you are using a Pro-Micro.

<img width="1293" alt="Screenshot 2024-03-26 010728" src="https://github.com/klouderone/therhinopad/assets/136342173/2b494b68-7a53-48db-b5c1-1824d192b3c5">   


<br>

Solder the Hotswap sockets onto the back of the PCB. This should be pretty straight forward.

<img width="1207" alt="Screenshot 2024-03-26 010850" src="https://github.com/klouderone/therhinopad/assets/136342173/9f2457d8-928e-4f71-a638-a3602788d785">    


<br>

Place the Mill Max sockets into the corresponding holes. If you are using a Nice!Nano, you want to have 13 sockets each side, and if you are using a Pro Micro or similar, you want 12 sockets per side. You can use some side cutters to trim this to length. The microcontroller wants to go as far down as possible, so that if you are using a Pro Micro, the VBAT - and + holes do not have any pins in them. From here, solder the Mill Max pins onto the microcontroller through holes. It is reccommended you do not heat the through holes for too long on this step, make sure your iron is in good condition to melt the solder. Be careful to make sure that the sockets are not bent and are both vertical when soldering the microcontroller to mill max pins, as this will impact how easy it is to remove the microcontroller and may cause damage to the pins when taking it out. You can ignore the holes in the middle of the microcontroller, these are not connected to anything.

<img width="1161" alt="Screenshot 2024-03-26 011222" src="https://github.com/klouderone/therhinopad/assets/136342173/45bff567-3fb6-4f12-94e3-533d3b0e5343">     


<br>

From here, you can then solder the sockets onto the PCB, also making sure that the sockets sit nicely on the PCB.

<img width="1021" alt="Screenshot 2024-03-26 011312" src="https://github.com/klouderone/therhinopad/assets/136342173/6e7e2c39-c4b9-48a0-8982-64bab3de7e8b">    


<br>

If you have an OLED or Nice!View display, you can solder these on here. If using an OLED display, make sure that it is socketed correctly. The VCC through hole is the middle hole. The Picture below shows the correct way. The socket should usually come with your display. The correct socket for the OLED is a 1x4p PH5 Box header socket https://www.aliexpress.com/item/4000147221999.html. You should be able to find this at your local electronics store.

<img width="1085" alt="Screenshot 2024-03-26 012811" src="https://github.com/klouderone/therhinopad/assets/136342173/2864f1aa-34e5-4a99-8793-9dee23dcb66e">     


<br>

You can now solder the encoder on. If you have an EC11 encoder, use side cutters to remove the two pins used for the press down button. 

<img width="1118" alt="image" src="https://github.com/klouderone/therhinopad/assets/136342173/85d91154-2910-4931-b9b8-96c9883e600a">
 

<br>

Before putting your keycaps on, you can now upload your firmware to the microcontroller. Basic firmware folders can be found in the github repo, and moved into your local machine for editing or flashing.

<img width="1204" alt="Screenshot 2024-03-26 011403" src="https://github.com/klouderone/therhinopad/assets/136342173/8b49ee2c-48aa-4b15-b982-8c639f651856">


Please refer to the abundance of youtube videos if you get stuck with QMK or ZMK! 

Thanks for reading and happy building!

