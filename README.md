# 2Pocket

![](https://github.com/ParksDevelopment/2Pocket/blob/main/Images/Cover.jpeg)

[Introduction](#Introduction)

[Info and Production](#Production)

[PCB](#PCB)

[Firmware](#Firmware)

[Case](#Case)

[Overview](#Overview)

## Introduciton

The PickPocket is a revamped version of my contest entry keyboard the [2Pocket](https://github.com/ParksDevelopment/2Pocket/tree/main). When I started making the list of changes I wanted to make it became clear to me I wanted to make a new project from the ground up, so despite thier similarities the PickPocket is a brand new project with the following features and changes from 2Pocket

Features
- 36 Kailh Choc V1 Low Profile Hot swap sockets (Using [Nocturnals](https://lowprokb.ca/collections/switches/products/ambients-silent-choc-switches) switches for all pictures)
- Bluetooth support between halves and computer
- Powered by 2 (XIAO nRF52840)[https://wiki.seeedstudio.com/XIAO_BLE/]
- 2 3.7V 1100 mAh batteries Charged through the USB C port on the back of each board
- ZMK and KMK compatability tested
- Single Reversable PCB for cheaper manufacturing
- PassThrough Charging through magnetic push pins. Plugging in the left half and connecting the boards will charge both of them.
- Still small enough for your pockets!

Changes from 2Pocket
- Removed the pedometer. This was adding a few dollars per board and made the wiring for a reversable pcb more than I wanted to deal with
- Removed the 2 additional buttons. they were for pedometer controls primarily 
- Increased size for better case design. From 190mm x 74.8mm x 22mm to 207mm x 79mm x 23.5mm

The main goal of all these changes was to make something I could bring into work, was sturdy enough to be moved around, and solved my biggest frusteration with split keyboards which is charging them.

## Production

This project is both not for a contest and much simpler so I will briefly touch on the production and related information. Below is the Item list

| Part Name  | Quantity   | Solder by hand   |
|------------|------------|------------|
| 1N4148 Diode | 38| NO|
| 2 pin Jst socket | 2| YES|
| Choc hotswap sockets | 36| YES|
| Xiao NRF52840 | 2| YES|
| EEMB Lithium Polymer Battery 3.7V 1100mAh | 2| DNA|
|Magnetic Connector - Right Angle Three Contact Pins | 2| YES|


## PCB

The PCB has a footprint of 95mm x 71.5mm x 1.6mm and is reversable so the cost of production is quite small. It also features 4 mounting holes that are small enough to fit between the keys and are intended for M2 screws. Some things to note if you plan on making one is that to accomadate for the small size the parts that are hand soldered will always be on the bottom of their respective side. This means that you will want to put the micro controller on the bottom of each board. The wiring will workm with it on the top but it will overlap with some of the keys. Same goes for the magnetic push pins.

![](https://github.com/ParksDevelopment/2Pocket/blob/main/Images/pcb.jpg)

## Firmware

Due to the lack of a ADXL345 there is not much need for any firmware changes. Anything that works with a Xiao NRF52840 will work with this as long at it has bluetooth support

There are 2 pins, 4 and 5, which are also the I2C pins that go unused, for now. if you want to add the pedometer back in there is room for it through these.
Row Pins: 0,1,2,3
Column Pins: 6,7,8,9,10

## Case

The Case isn't anything special but I am happy with how it came out. Because of the extra space I have not working in the constraints of the contest I was able to get something a lot more sturdy. It is reversable like the board so 2 pieces each, a plate and the bottom. It also requires some threaded inserts but those can be easily removed. As it stands only the left side has a reset button.

| Part Name  | Quantity   | Link  |
|------------|------------|------------|
| M2 threaded inserts| 4| [Link](https://www.amazon.com/dp/B0DGP6FH5H?ref=nb_sb_ss_w_as-reorder_k1_1_7&amp=&crid=1JJC55YT0N74J&amp=&sprefix=m2+thre)|
| M2 Standoff and screws| 4| [Link](https://www.amazon.com/M2-Motherboard-Standoffs-Male-Female-Electronic/dp/B0BP6MT7RP/ref=sr_1_3?crid=1B0X8RUAJV7TB&dib=eyJ2IjoiMSJ9.4QcWRysCtdMoG_QF6B69rSAXRWaxghfNGHqr93WRVa_WalsyknAQGVyIgvgC3SLtFW8_Aq9xT8osy7Ujw2-KMYpiWbzHui2ul46HTimVXeC-CCfGhvA7aWc0ZlMaRxAaAogIQ04qn7LB9O_VYWGMlC1Eg_iei4z6oBYtRa2EqjSfnEmVXzc36kRT-TCwqZwGNqwdKtOXMUKBzJf1T8QhFMsNmuDVL8JtqZQa6X_zp2WqCpqts0BBzoPuzOpg5VYAeIQQLHLcRWSujUVZSC_JGGASAf63wpMIx7f5A5T_ZYg.Ff2cLg3y5jFBp4E5X0YNq7dlbfJBQw7yKhNeuV5YwsQ&dib_tag=se&keywords=m2%2Bstandoff%2Bkit&qid=1744292483&s=industrial&sprefix=m2%2Bstand%2Cindustrial%2C129&sr=1-3&th=1)

Much happier with the case this time around and while it still has quirks I don't feel the need to change it that much. I am using the keyboard to go to work and I never have any concerns throwing it in a bag.

![](https://github.com/ParksDevelopment/2Pocket/blob/main/Images/model.jpg)

## Overview

I have been happy with this redesign, while it is sad to lose the ADXL345, since there is a lot I was hoping to do with it and it was one of the more unique parts of the first board, it definetly made the project more streamlined 

p.s. enjoy the [extra photos](https://photos.app.goo.gl/FVwNr18BBK3Yw1VW6) my wife took of the board on a hike

![](https://github.com/ParksDevelopment/2Pocket/blob/main/Images/handComparison.jpeg)
