# The Rhino Pad Macro Pad by Kea Workshop

The Rhino Pad is a compact Macro Pad tailored for Computer-Aided Drawing, with 13 keys and an encoder that can be programmed for any macro in your program. It supports QMK or ZMK with either a Pro Micro or similar for QMK, or the Nice!Nano V2 for ZMK. 

The Keycap spacing is 19.05mm x 19.05mm, NOT the usual choc keycap spacing. You can find the 3D printed keycaps on printables https://www.printables.com/model/685983-kea-workshop-choc-v1-mx-spaced-keycaps. 

The Case is 3D printed and uses 3mm x 2mm x 1mm magnets to hold it together. This is included in the files.

https://www.keaworkshop.com/product/rhino-pad

If you have any questions or want to get in contact with me, my discord is klouder#3331 or my email is claude@keaworkshop.com.
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

Then solder the button and switch onto the PCB. Take your time doing this and use tweezers and a steady hand. Ideally, you can use solder paste to do this also. 

<img width="1293" alt="Screenshot 2024-03-26 010728" src="https://github.com/klouderone/therhinopad/assets/136342173/2b494b68-7a53-48db-b5c1-1824d192b3c5">   


<br>

Solder the Hotswap sockets onto the back of the PCB. This should be pretty straight forward.

<img width="1207" alt="Screenshot 2024-03-26 010850" src="https://github.com/klouderone/therhinopad/assets/136342173/9f2457d8-928e-4f71-a638-a3602788d785">    


<br>

Place the Mill Max sockets into the corresponding holes. If you are using a Nice!Nano, you want to have 13 sockets each side, and if you are using a Pro Micro or similar, you want 12 sockets per side. You can use some side cutters to trim this to length. The microcontroller wants to go as far down as possible, so that if you are using a Pro Micro, the VBAT - and + holes do not have any pins in them. From here, solder the Mill Max pins onto the microcontroller through holes. It is reccommended you do not heat the through holes for too long on this step, make sure your iron is in good condition to melt the solder. Be careful to make sure that the sockets are not bent and are both vertical when soldering the microcontroller to mill max pins, as this will impact how easy it is to remove the microcontroller and may cause damage to the pins when taking it out. 

<img width="1161" alt="Screenshot 2024-03-26 011222" src="https://github.com/klouderone/therhinopad/assets/136342173/45bff567-3fb6-4f12-94e3-533d3b0e5343">     


<br>

From here, you can then solder the sockets onto the PCB, also making sure that the sockets sit nicely on the PCB.

<img width="1021" alt="Screenshot 2024-03-26 011312" src="https://github.com/klouderone/therhinopad/assets/136342173/6e7e2c39-c4b9-48a0-8982-64bab3de7e8b">    


<br>

If you have an OLED or Nice!View display, you can solder these on here. If using an OLED display, make sure that it is socketed correctly. The VCC through hole is the middle hole. The Picture below shows the correct way.

<img width="1085" alt="Screenshot 2024-03-26 012811" src="https://github.com/klouderone/therhinopad/assets/136342173/2864f1aa-34e5-4a99-8793-9dee23dcb66e">     


<br>

You can now solder the encoder on. If you have an EC11 encoder, use side cutters to remove the two pins used for the press down button. 

<img width="1118" alt="image" src="https://github.com/klouderone/therhinopad/assets/136342173/85d91154-2910-4931-b9b8-96c9883e600a">
 

<br>

Before putting your keycaps on, you can now upload your firmware to the microcontroller. Basic firmware folders can be found in the github repo, and moved into your local machine for editing or flashing.

<img width="1204" alt="Screenshot 2024-03-26 011403" src="https://github.com/klouderone/therhinopad/assets/136342173/8b49ee2c-48aa-4b15-b982-8c639f651856">


Please refer to the abundance of youtube videos if you get stuck with QMK or ZMK! 

Thanks for reading and happy building!

