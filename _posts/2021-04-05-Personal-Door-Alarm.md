---
navigation: true
title: "Personal Door Alarm"
date: 2021-04-05
cover: assets/images/daprofile.jpg
class: post-template
---

This projects is the result of people entering my room unwanted or frequently. I am sure all of you have experienced family members who enter you room and don't close the door on their way out. Well, this is my solution. 

This alarm sounds a loud buzzer when the door is opened. 
Here is the schematic: 
![schematic](assets/images/dooralarm.jpg)

Here is how it works:
First you are going to need some sort of reflector on you door. This alarm was built on a breadboard and placed on the floor right next to my door. The relfector was a white paper square, side length of 1 in. That paper was on a L shaped cardboard mount, which was taped to the bottom right corner of my door \(my door swings open to the left, clockwise\). The photoresistor detects the light that bounces off the reflector from the L1 LED. That's how the circuit knows if the door was opened. If it was, the amount of light will decrease which will increase the resistance on the photoresistor. 

![](assets/images/da1.jpg)

When the door is closed, the light is high so the resistance of the pr \(from now on I will call this photoresistor\) is low which allows a sufficient amount of negative charge to flow into the base of T1, which turns it off. If T1 is off then T3 is also off, which then the buzzer is off. But, if the door was opened, then the resistance of the pr becomes high. This stops a sufficient amount of electrons flowing into the base of T1, which then turns it on. Then electrons flow throught the D1 diode and into the collector of T3 which turns it on. Thus the buzzer sounds. However, the base of T3 is connected to a capacitor. This starts to charge while T3 is on. Once charged it will now repel the electrons flowing from the base of T3, effectivly turning it off. Which turns the buzzer off. Now you can close the door again or whatever. But now for the next cycle, we have to discharge the capacitor. That's the purpose of T2. Once you've closed the door, you make the resistance of the pr low. Which turns T1 off. This allows C1 to discharge through T2 and through R2 and whatever resistor you put on the emitor of T2. I put a 10K resistor. This effectivly discharges C1 allowing it to opperate correclty 











*Again this was a long time ago so the date isn't exact.
