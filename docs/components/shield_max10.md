---
id: shield_max10
title: VHDPlus Shield MAX10
sidebar_label:  Shield MAX10
---

> :warning: Coming Soon

<video muted autoPlay loop><source src="/img/vhdpshield/Shield.mp4" type="video/mp4"/>Your browser does not support the video tag. You can download the video anyway.</video>

The shield for the Core MAX10 features a powersupply, so you can power the board with a battery or power adapter, and more CRUVI connectors, so you can connect camera, motors and ultrasonic sensors at once while you're powering the FPGA with the same supply as the motors.

## Shield Overview
![Shield M Overview](/img/vhdpshield/Items3.png)

You have the choise between 3 CRUVI LS connectors and 3 PMOD connectors. Together with the PMOD connectors, you get the 8 I/Os that are also ADC inputs and 5V power.
With the CRUVI connectors, you can connect the most VHDPlus Extensions (Motor, Audio, Levelshifter ...) and with the PMOD connectors, you have a variety of extensions from Digilent or you can just use the 0.1" pins with the hardware you have at hand.

## Powersupply
<video muted autoPlay><source src="/img/vhdpshield/Zoom_Power.mp4" type="video/mp4"/>Your browser does not support the video tag. You can download the video anyway.</video>

The Shield features a 8.5 - 28V to 5V Step-Down Converter and a 5V to 3.3V Step-Down Converter, that can power the Core MAX10 and all extensions. 
The 5V Converter can deliver 5A continuous to even power servo motors or a small LED stripe.
The 3.3V Conerter is separated from the Core and only powers the extensions with a maximum of 2A. This should be enought to power the maximum of 3 CRUVI extensions and 6 PMOD extensions at the same time.