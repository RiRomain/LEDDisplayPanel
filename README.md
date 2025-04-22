**LED Display Panel**
Led art installation - 2D matrix display panel - 3D printed and easy to assemble

### Introduction

This repository contains instruction on how to assemble a 9*28 led display matrix. The display uses WS2812B LED strips (60 led/meters) and an ESP8266 flashed with WLED.

### Assembly

Start by printing the part available on maker lab. You will need at least the back connection plate as well as the 2 back plate to start the assembly.

1. Cutting the led strip.
Cut the led strip to length, you need 9 strip with each 28 leds. You can use the 2 back plates to quickly measure the led strips.
   ![Alt text](images/BackPanel_LedStripMeasurement.JPG?raw=true "StripMeasurement")

2. Connect the 2 back plate via the connection plate.
Use 4 M3*8mm screws to connect the connection plate to the 2 back plates.
3. Stick the led strip to the back plates.
The data in (marked Din on the strip) side of all the strip need to be on the left, while the data out (marked DO on the strip) side need to be on the right. Most strips also comes with an arrow on them, make sure if points to the right for all the strips.
4. Connect the entry data line.
You need a thin cable to fit into the data line slots, around 1mm in diameter. I've used a sacriphicial ethernet cable.
Lay the data line cable in the top left chanel, to start on Din, and go through its dedicated chanel to the connection plate, leave enough cable out the back to later connect the ESP to it (about 10cm extra).
Strip a mm off of the cable, and solder it to Din.
5. Connect the other data line.
Next connect the DO pin of the first line with the Din of the second, using the dedicated chanel on the back plate. Repeat this until all Din of your strips are connected.
6. Connect the positive and negative of each strip with the strip above and under using some 18AWG wires. 
7. Next add longer 18AWG wires that will be used to power the strips, those need to be long enough to connect from the strips to the wago holder on the connection plate.
8. Add a sacriphisial LED to the wemos D1 mini.
In order to control the led strip, a 5V signal is needed. One WS2812b can be used to boost the signal from 3.3V to 5V.
Cut one LED and stick it to the back of the ESP. Add one resistor (200 to 500Ω) on pin RX (GPIO3). Connect the other end of the resistor to Din on the single LED.
Connect the 5V of the wemos to the 5V of the single LED, do the same with ground (marked G on the wemos).
9. Connect the wemos to power.
Connect 2 wires to the 5V and ground pin of the single LED, making sure they are long enough to reach the wago holder on the connection plate.
//TODO: Check if led out 5v and gnd need connection.


![](https://pandao.github.io/editor.md/images/logos/editormd-logo-180x180.png)


H1 Header (Underline)
=============

H2 Header (Underline)
-------------
