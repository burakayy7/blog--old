---
navigation: true
title: "What is PID?"
date: 2021-06-15
class: post-template
---

This is a quick post on what PID is and how to implement it.

For startes, PID stands for Proportional-Integral-Derivative. And PID is a closed-loop feedback controller. That means that when the controller outputs a value, that output will change the input, which will result in another different output to be produced. And this systems goes on and on until the main program is terminated. 

When are PID Controllers used?

Well, in almost any application that needs to be actively controlled. Such as: autopilot UAVs, self-balancing robots, drones, battery chargers, etc.

So what **exactly** are PID controllers?

Well, let's start off with the proportional part:

As you might of thought, this part produces a value **proportional** to the error. For example: let's assume we are making a drone. And the orientation sensor detects that we are tilting by 20 degrees. And let's say that the P Value (or the Proportional Value) is 0.5. Then the output of the P part will be 20*0.5 which is 10 degrees. If our error was 90 degrees, then the P Value would be 45 degrees. Essentially, the output is proportional to the error with respect to the P Value. However, this alone isn't very affective in the real world. Because in the real world there is momentum. Which means our system will overshoot, which causes oscillations in the system. 

Next, what does the Integral Part mean. And to better understand why this is important, let's first know why the Derivative term is there.

The D term, or the Derivative:

If you have noticed, the I and D parts are names commonly used in Calculus. This is because we actually are using concepts from Calculus. The Derivative term looks at our error 'curve' over time. Actually, it's not over time but this is what I mean: Imagine our error values are being plotted on an x-y plane, where the x-axis is time and the y-axis is the error. Now this will form some sort of 'curve' (I just mean a plot or graph). And by definition, the Derivative term is looking at the slope of our curve. Or basically, how fast are we going away or to our target value (in most systems this will be 0 or the x-axis)? And the D term changes accordingly to that value. Let's go through an example: Now let's assume our D Value is say 10. And the slope of the error curve is -2. Then the output of the D function is (D Value * slope) or (10) * (-2) = -20. So we will be adding a negative value to the output of the P function which will reduce our 'speed' to the target line. And will result in **NO OVERSHOOTING**! And again, if the slope was positive, then we would be getting closer to the x-axis, which is our target. And the slope  Now, this alone is a pretty good system. However, there are some scenarios where the error is not at the target but the specific P and D terms aren't affective at getting it back to the target. This is when the Intergal term comes in.

Finally, the Integral term:

This looks at the area under our curve relative to our target value, the line y=targetVal. 


