---
navigation: true
tite: "IMU Measurments"
date: 2021-06-06
class: post-template
---

For a long time I have always wanted to build robots that know their orientation. And to do that I will first need to learn how Inertial Measurment 
Units, IMU for short, work. I currently only have an MPU6050 which has both a 3-axis accelerometer and a 3-axis gyroscope. But, keep in mind that these 
are made with MEMS \(Micro-electromechanical systems\), or cell-phone grade sensors. They will have inperfections. 

I first started on a bunch of online tutorials on how to use this and I got the accelerometer to measure angles. 

Here is a short piece of code that will do the basic readings from the MPU6050:

```#include <MPU6050.h>


// MPU-6050 Short Example Sketch
//www.elegoo.com
//2016.12.9

#include<Wire.h>
const int MPU_addr=0x68;  // I2C address of the MPU-6050
int16_t AcX,ACY,AcY,AcZ,Tmp,GyX, GYX,GyY,GyZ;



void setup(){
  Wire.begin();
  Wire.beginTransmission(MPU_addr);
  Wire.write(0x6B);  // PWR_MGMT_1 register
  Wire.write(0);     // set to zero (wakes up the MPU-6050)
  Wire.endTransmission(true);
  Serial.begin(9600);
  pinMode(2, OUTPUT);
  
}
void loop(){
  Wire.beginTransmission(MPU_addr);
  Wire.write(0x3B);  // starting with register 0x3B (ACCEL_XOUT_H)
  Wire.endTransmission(false);
  Wire.requestFrom(MPU_addr,14,true);  // request a total of 14 registers
  AcX=Wire.read()<<8|Wire.read();  // 0x3B (ACCEL_XOUT_H) & 0x3C (ACCEL_XOUT_L)    
  AcY=Wire.read()<<8|Wire.read();  // 0x3D (ACCEL_YOUT_H) & 0x3E (ACCEL_YOUT_L)
  AcZ=Wire.read()<<8|Wire.read();  // 0x3F (ACCEL_ZOUT_H) & 0x40 (ACCEL_ZOUT_L)
  Tmp=Wire.read()<<8|Wire.read();  // 0x41 (TEMP_OUT_H) & 0x42 (TEMP_OUT_L)
  GyX=Wire.read()<<8|Wire.read();  // 0x43 (GYRO_XOUT_H) & 0x44 (GYRO_XOUT_L)
  GyY=Wire.read()<<8|Wire.read();  // 0x45 (GYRO_YOUT_H) & 0x46 (GYRO_YOUT_L)
  GyZ=Wire.read()<<8|Wire.read();  // 0x47 (GYRO_ZOUT_H) & 0x48 (GYRO_ZOUT_L)
 //Serial.print(" | AcX = "); Serial.println(AcX);
 //Serial.print(" | AcY = "); Serial.println(AcY);
 Serial.print(" | AcZ = "); Serial.println(AcZ);  //Serial.print(" | Tmp = "); Serial.print(Tmp/340.00+36.53);  //From the datasheet of MPU6050, we can know the temperature formula
delay(200);
}

```

But how do you convert these accelerometer measurments to angles?

Well, you use math. Specifically, trig.

People say that you don't need to know math if you want to be a programmer. And that's mostly true: if you want to be a low level coder.
But if you want the be a real programmer, then you will need to master the fundamentals of math!

![here is the explanation on paper](assets/images/imuaccel.jpg)

If you'd like a more detailed explanation: [click here](https://toptechboy.com/9-axis-imu-lesson-6-determine-tilt-from-3-axis-accelerometer/)

And you could probably put this in your Arduino code by using the Math library.

Later, my immature brain, thought it was a good idea to control a foam glider with these measurments.

It didn't work at all!!

Why?

Because the accelerometer measures accelerations on the sensor. So it is sensative to vibrations, which are very common on a plane.
