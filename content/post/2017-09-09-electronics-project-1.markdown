---
author: rimonmostafiz
comments: true
date: 2017-09-09 11:34:00+00:00
layout: post
link: http://www.rimonmostafiz.com/electronics-project-1/
slug: electronics-project-1
title: Automatic Staircase Light Using Arduino, PIR Sensor & Relay
wordpress_id: 692
categories:
- electronics
tags:
- arduino
- microcontroller
- project
- sencor
---

**Companion Video: **

https://www.youtube.com/watch?v=OZECTbhp9dU

This automatic staircase light circuit switch on the staircase lights automatically when someone enters on the stairs and gets off after some time.




  * There are three important components in this circuit


    * PIR Sensor (Passive Infrared Sensor)


    * Relay


    * Arduino UNO







**Components required for this project:**









  * Arduino UNO


  * One breadboard


  * PIR Sencor


  * Relay Module


  * 1N4007 rectifier Diode


  * Jumper wires


  * Power Plug and Bulb


  * Battery


  * 220v AC supply




**Description about the components: PIR**












[![](http://www.rimonmostafiz.com/wp-content/uploads/2016/01/555-28027_1-300x300.png)](http://www.rimonmostafiz.com/wp-content/uploads/2016/01/555-28027_1.png)[![](http://www.rimonmostafiz.com/wp-content/uploads/2016/01/proximity_PIRbackLabeled-300x225.jpg)](http://www.rimonmostafiz.com/wp-content/uploads/2016/01/proximity_PIRbackLabeled.jpg)















PIR sensor is used here to detect the Human body movement, whenever there is any body movement the voltage at output pin changes.

Basically it detects the Change in Heat, and produce output whenever such detection occurs.









**Description about the components: Relay**









[![](http://www.rimonmostafiz.com/wp-content/uploads/2016/01/SPDT-Relay-Working-300x121.gif)](http://www.rimonmostafiz.com/wp-content/uploads/2016/01/SPDT-Relay-Working.gif)




  * Relay is an electromagnetic switch, which is controlled by small current, and used to switch ON and OFF relatively much larger current


  * By applying small current we can switch ON the relay which allow much larger current to flow


  * Relay is configured by using a small Driver circuit which consist a Transistor, Diode and a resistor


  * Transistor is used to amplify the current so that full current (from the DC source – 9v battery) can flow through coil to fully energies it













**Little Description about the components: Relay Module**






[![](http://www.rimonmostafiz.com/wp-content/uploads/2016/01/DSC03886-Copya-300x130.jpg)](http://www.rimonmostafiz.com/wp-content/uploads/2016/01/DSC03886-Copya.jpg)







  * Relay is configured by using a small Driver circuit which consist a Transistor, Diode and a resistor


  * Transistor is used to amplify the current so that full current (from the DC source – 9v battery) can flow through coil to fully energies it


  * Resistor is used to provide biasing to transistor


  * And Diode is used to prevent reverse current flow, when the transistor is switched OFF













** **




** **




**Little Description about the components: UNO**






[![](http://www.rimonmostafiz.com/wp-content/uploads/2016/01/Arduino_Uno_-_R3-300x300.jpg)](http://www.rimonmostafiz.com/wp-content/uploads/2016/01/Arduino_Uno_-_R3.jpg)










  * The Uno is a microcontroller board based on the ATmega328P.


  * It has 14 digital input/output pins (of which 6 can be used as PWM outputs), 6 analog inputs, a 16 MHz quartz crystal, a USB connection, a power jack, an ICSP header and a reset button


  * It contains everything needed to support the micro controller, simply connect it to a computer with a USB cable or power it with a AC-to-DC adapter or battery to get started













**Assembly of the project:**









  * PIR sensor out to Pin 4 and the Relay input to Pin 8 of Arduino.


  * The light bulb has one of the 120V wire spliced to connect the end connected to the power plug to the COM(Common) Pin of the Relay module and the one going to the lamp is connected to the NC(Normally Closed) Pin.


  * We use a bread board to connect the VCC and Ground to both modules from our UNO, but we connect a 1N4007 rectifier Diode to the VCC line of the Relay Module to allow the current to go only one way.











[![](http://www.rimonmostafiz.com/wp-content/uploads/2016/01/Schematic-Ir-Motion-300x229.png)](http://www.rimonmostafiz.com/wp-content/uploads/2016/01/Schematic-Ir-Motion.png)





Copy the code of the Arduino from this [link](https://github.com/rimonmostafiz/mix_repo/blob/master/relay.ino) and upload it in Arduino. Done!!!




**Uses of the project:**












  * This project is easy to made and fun to use.


  * Can also use in corridor.


  * We can save some electricity bill with it
