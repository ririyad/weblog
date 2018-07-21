---
author: rimonmostafiz
comments: true
date: 2017-09-09 10:58:00+00:00
layout: post
link: http://www.rimonmostafiz.com/electronics-project-2/
slug: electronics-project-2
title: Obstacle Sensor Using Arduino and Ultrasonic Sensor HC-SR04
wordpress_id: 693
categories:
- electronics
tags:
- arduino
- microcontroller
- project
- sencor
---

**Companion Video:**

https://www.youtube.com/watch?v=HOt-lHT-Nms

Objective for this project is to make an obstacle sensor which will detect some object in front of it and send some signal.

The operation of the project is simple. When we approach an object sensor LEDs light up according to the distance of the object. The green LED switches on if you are away, yellow if in the middle distance and red if it is close. The sensing distances LEDs are programmable, if we want to change we can just change the source code of the project.

**Components required for this project:**




 	
  * Arduino UNO

 	
  * One breadboard

 	
  * HC-SR04 ultrasonic range finder module

 	
  * Jumper wires

 	
  * LEDs of different colors

 	
  * Resistors of 220 ohms


**Description about the components:** **HC-SRO4**
[![](http://www.rimonmostafiz.com/wp-content/uploads/2016/01/HCSR04-300x177.jpg)](http://2.bp.blogspot.com/-7OeGrQpFRbc/VpDmbQI4aUI/AAAAAAAAAxg/dmpffccSpm0/s1600/HCSR04.jpg)

HC-SRO4 is an ultrasonic sensor which uses sonar to detect objects at a distance of 2 cm to 4 meters.  This sensor is widely used in robotics to build robots that move and should divert or avoid obstacles.



 	
  * It is easy to control it through the Arduino, because it only has 4 pins described below

 	
  * VCC – 5V (ranging from 4.5 V to 5.5 V)

 	
  * Trig – Sensor input (trigger)

 	
  * Echo – Output Sensor (Echo)

 	
  * GND – Ground




**Description about the components: ArduinoUNO**






[![](http://www.rimonmostafiz.com/wp-content/uploads/2016/01/Arduino_Uno_-_R3-300x300.jpg)](http://1.bp.blogspot.com/-KRQ7zDcbkGU/VpDmbruFxTI/AAAAAAAAAxk/Rw1KQTrOMQ8/s1600/Arduino_Uno_-_R3.jpg)



 	
  * The Uno is a microcontroller board based on the ATmega328P

 	
  * It has 14 digital input/output pins (of which 6 can be used as PWM outputs), 6 analog inputs, a 16 MHz quartz crystal, a USB connection, a power jack, an ICSP header and a reset button

 	
  * It contains everything needed to support the microcontroller; simply connect it to a computer with a USB cable or power it with a AC-to-DC adapter or battery to get started




**Assembly of the project:**









Digital ports 11, 12 and 13 of the resistors connected Arduino, which in turn are connected the legs of the LEDs positive;[![](http://www.rimonmostafiz.com/wp-content/uploads/2016/01/hc-sro4_esq-300x230.jpg)](http://3.bp.blogspot.com/-sHmweH8_hm4/VpDm1gc-5lI/AAAAAAAAAxs/cl5-tGDoy4A/s1600/hc-sro4_esq.jpg)



 	
  * Cathode pin of the LED in the GND (ground) of the Arduino

 	
  * VCC pin of the ultrasonic sensor HC-SRO4 in

 	
  * Arduino 5V

 	
  * TRIG pin sensor HC-SRO4 digital port on the

 	
  * Arduino 6

 	
  * ECHO pin sensor HC-SRO4 the

 	
  * digital port 7 of the Arduino

 	
  * GND pin HC-sensor SRO4 in Arduino GND








Now to install the library HC-SRO4 for your program to work. [Download this library](http://www.comofazerascoisas.com.br/posts/arq-dld/HCSR04Ultrasonic.rar) on your computer, then unzip the file. After unzipping a folder called HCSR04 Ultrasonic will be created on your computer. Copy this folder to the libraries of the Arduino IDE and it’s ready, you can now use the library resources into their programs.





Copy the code of the Arduino from this [link](https://github.com/rimonmostafiz/mix_repo/blob/master/ultra.ino) and upload it in Arduino. Done!!!




 




**Uses of the project:**











 	
  * This sensor is widely used in robotics to build robots that move and should divert or avoid obstacles.

 	
  * With this we can make a car parking sensor. we can monitor the distance while parking.



