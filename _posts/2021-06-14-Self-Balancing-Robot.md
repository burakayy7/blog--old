---
navigation: true
title: "Self-Balancing Arduino Robot"
date: 2021-06-14
cover: 'assets/images/sbrCover.jpg'
class: post-template
---


I have been wanting to make this project for some time now. I have seen others do them with really expensive motors and devices and I wanted to test and see if I could build a functioning prototype with the $5 materials I had laying around my room.

I first, looked at other's robots and how they designed their's. I also looked at which devices I had. Now for the main controller, I just used a 5v Arduino Nano board. But the IMu sensor was the challenging part. I first thought I could use a complimentary filter with the MPU6050, but that prooved to cause some oscillations and false orientation data. The cheap accelerometers would read too much vibrations and the gyros drift would sustain it well for long self-balancing. EVEN with the complimentary filter. Look, the comlimentary filter is great. But I wanted to remove as many failure points as possible for the first version. So for the first prototype, I decided to go the easy route: getting quaternions from the BNO055 and converting those to Eular angles.

For the motors I had only geared DC motors. These are super cheap and shouldn't be used on robots like this! I wonder if this will cause me any pain in the future?

And to drive those motors I had a L298N motor driver. This for sure will cause me problems and I knew it. I was just too broke to buy a better solution. This driver draws a lot of current. In fact, there is a voltage drop, from the input battery terminal to the motor driving terminals, by more than 2 volts. This means, that if I were to hook up a 9v battery, the motors would only see about 7 volts. And I am not even talking about the loss in current!! 

So, this driver is inefficient. Oh well!

For the main power source, I needed a battery that could provide a lot of power. However, I didn't have a rechargable battery. I tried 9v batteris, 2 9v batteries. and even some cheap NiCds. But I eventually found that the best results are with 3 9v batteries in series. Producing a total of 27 volts. Now I don't exactly know what this did the the 6v rated motors, but it was enough to provide the current needed for the robot. But only for a short amount of time, like 5-10 tests and then it was done. 

For the main frame, I went to CAD... NOOO. I was broke back then and didn't have a 3D printer. So I built the frame from cardboard cut with my 5 dollar scissors and barbecue skewers. I wanted a 2 'story' build where the battery and IMU would go on the top. Ideally the most mass should go on the top, since this is essentially an inverted pendulum. And the more mass an object has, the more inertia it has. So, the robot would have more time to react and stabilize it's own weight, if most of the weight was on top. 

In the end, I sketch-up something like this:

![](assets/images/sbrSketch.jpg)

and the dimensions:

![](assets/images/sbrDim.jpg)

In order to control the robot, it needs to know it's orientation, more specifically it's tilt. So, we can use a sensor called an Inertial Measurment Unit (IMU for short). 6-axis IMUs have a 3 axis accelerometer and a 3 axis gyroscope. We can use these and some math to get our rotation in Eular angles. However, this is usually sensative to vibration and gimble lock. So instead we can use something called Quaternions. Quaternions are the numbers that extend the complex numbers and can define 3 dimensional rotations with 4 numbers. However, most IMU's don't have quaternions. So, I used the BNO055 IMU and I explain how to get these measurments in 

Once the Eular angles are achieved, we need a way to control this. After some research, I chose the PID controller to control my robot. I learned how to implement this in Paul McWhorter's [IMU class](https://www.youtube.com/watch?v=t7ImNDOQIzM&list=PLGs0VKk2DiYwEo-k0mjIkWXlkrJWAU4L9&index=26).

Here is how I implemented a PID controller:

First, you need to get your error. Like let's say an angle of 0 is the target, but we read 10 degrees. Then the error is 10 degrees. Here is the code for getting all the terms in PID, which I will explain later:

~~~cpp
rollErrorOld = rollError; //get the old rollError
rollError = rollTarget-rollActual; //get the current rollError
rollErrorChange = rollError-rollErrorOld; //get the change in the rollError; our newError minus the oldError = change in Error
rollErrorSlope = rollErrorChange/dt; //get the slope of our error; the change in error over the chaneg in time is the 'slope' of the error 'line' if the y-axis is error and the x-axis is time
rollErrorArea = rollErrorArea+rollError*dt; //the area under the curve between the error curve and the x-axis

~~~

And all of these should be the same for pitch, just the variable names change. 

But what is PID?

Well, I explained that in [this blog post](https://burakayy.com/blog/What-is-PID). You should go check it out, and come back here when you feel confident on PID controllers.

Now that we know what a PID controller is and how it works, let's see how this will help control our robot. 

