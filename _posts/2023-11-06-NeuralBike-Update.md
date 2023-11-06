---
navigation: true
cover: 'assets/images/mainUnit1.jpg'
title: NeuralBike Update
date: 2023-11-06
class: post-template
---

Today I finally found the time to finish the pcb of the main controller for the Crash detection project. I have been working on this in the background for the past few weeks and it's finally complete today! 

The design is somewhat simple. On the top there's the Particle Boron LTE (which will be running inference) and there's also the MPU6050 (the IMU used to collect acceleromter data). But we also need to store that data so on the bottom there's a SD Card Module. This module runs on 5 volts but the Particle Boron runs on 3.3 volts, so to make them compatible, I shorted the input and the output of the voltage converter on the module so that it can run on 3.3 volts. 

Here is a picture if you want to see how the final product turned out:

![The main pcb]("assets/images/mainUnit2.jpg")


