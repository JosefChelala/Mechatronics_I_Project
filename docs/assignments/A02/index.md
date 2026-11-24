# Progress Check In Part 1

## Updates




### Power Supply and Speed
Like I guessed in my proposal video, the MB V2 Power Supply included in the Arduino kit was the issue that kept the servo from running correctly. The MB V2 was able to move (albeit completely randomly) the motor when the ground of the Supply was only connected to the motor and not connected to the Arduino. In order for the Arduino's control of the motor to work correctly, they must share the ground with the Arduino. When shared, nothing would happen. I believe one possible issue is that the MB V2 was slightly broken a bit from a drop from before, however, that wouldn't explain how it worked when not sharing the ground (this same exact non-sharing effect happened with the new power supply). 

<img width="3000" height="4000" alt="20261124_012233" src="https://github.com/user-attachments/assets/7b28879b-2191-493d-bbae-676e2607e770" />


Furthermore, some spec sheets for the SG90 stated that the absolute max voltage for the servo was about 6V and not 5V. Since, I already have two servos and Micro Center sells the same motor for dirt cheap, I thought I would try risking a motor and running it at 6V instead of 5V to try and crank out as much speed and torque as possible. The reason I decided on this is that I need to allow the indicator to be as long as possibly to allow it to be easily viewable as I get closer to the car (which will be seen in the video). The problem is that as the flag increases in length and mass, so does the torque. From there, as torque increases, speed will decrease. Speed is the key to this project working in a reliable matter. Having to go at 1 mph or less while parking just so the motor can keep up is greatly inconvenient and unsafe if some one none the wiser goes way too fast. This means I need to try to maximize how fast the servo rotates to allow normal parking speeds. While it may not make a significant increase, raising the voltage to 6V will help a ton.

So, what sort of power supply should I look for? Well, in case the 6V is not a great idea, I need to make sure that it can change voltages so that I do not have to waste money on another supply. Additionally I need to be able to connect it to the circuit. Most importantly, I need to make sure it can allow the current to only supply what is needed has enough amperage to power the servo correctly. I needed to stop by Micro Center anyway, so I decided to scour their website to see if they had what I needed. 

After looking through their website, I found this [CyberPower Systems Universal Power Adapter](https://www.microcenter.com/product/710639/CPUAC1U1300_Universal_Power_Adapter?iitt=Rf8_RMhWhyULaeighM_-xFYDOFxlOF_7&MccGuid=4DB231AC-D731-446A-8E25-7CC67683918C). This was exactly what I needed and fit everything I wanted. The problem is that it required me to cut the head to work, so I did it and stripped the wire. Then I plugged it into separate rows (not the 4 columns for space). Lastly, I marked off which line was ground and the other as the voltage to not cause possible damage to the motor. 


<img width="1000" height="1000" alt="image" src="https://github.com/user-attachments/assets/722f69cf-f9e4-4f67-8dad-a4022eb75d20" />



<img width="4000" height="3000" alt="20261124_013351" src="https://github.com/user-attachments/assets/a9a0d6de-673a-4cba-a9ec-f57b080f72c6" />




### Testing
After reattaching and rewiring everything. I ran a test with the new power supply. As seen below, it worked perfectly.

<iframe width="560" height="315" src="https://www.youtube.com/embed/jCkTxEsWlgU?si=FocyBU2ucfGbkM28" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


### Stick Flag
So now that the servo runs with the code correctly, the only thing left is the indicator for the driver to know how close they are to the where they need to stop. Since it needs to have a combination of low mass and an geometry with a low moment of inertia to reduce the torque, I decided to just create a thin strip of plywood with a flag attached to the end of it. 

To create the thin strip of plywood, I found a replica cross arm attachment (found in our kit) for the servo motor and created plywood stick around it in SolidWorks. Essentially, I made a little kite at the base to surround it and secure its attachment to the arm. If the mass was too much, I could just slice up the kite a little bit if need be, but the affect it has is very little due to being at the center of rotation. Then I extended the arm out. from one of the long sides. Afterwards, I went to the fab lab and cut it out using their laser cutters. Lastly, I would cut a piece of a old, ripped up shirt I had and glue it to the stick.


<img width="3000" height="4000" alt="20261123_223044" src="https://github.com/user-attachments/assets/f41e8868-30dd-4218-9b42-ebeb5a28cf0e" />



I was going to test several different sticks with varying widths, however, I was pleasantly surprised to find that the quarter inch I tested first worked perfectly fine with no major issues. Instead of wasting a bunch of the fab lab resources, I decided to just "stick" (get it) with it.


<iframe width="560" height="315" src="https://www.youtube.com/embed/6W-l8zJQge0?si=SqP-kUWjT8saUuDo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


### The Project is Essentially Done
I already 3D printed all components prior to the project proposal as seen in that submission. Additionally, essentially the same code was used in that video as well, however, the motor was simply not working. Now, by using the new power supply and creating then attaching the arm, I basically finished the project. Below is the video of it working. It works fine, albeit it was working at a longer distance prior to this video. Additionally, the person driving didn't stop at the moment the flag reached the stop, but that is something that can be learned with practice. I would have rerecorded the video, but they had to leave so I will have a better video for the final submission.


<iframe width="560" height="315" src="https://www.youtube.com/embed/K9nsScTuK84?si=NyPmnC0JZcS0tolc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


## What next?
Really the only thing left to do is just clean up the code for further efficiency. Right now the code still has everything I need for testing (distance calculations, distance and angle, etc...). By removing all this excessive code, I believe that I could reduce any latency further.

Further more, I found some thin sticks that could possible keep the flag straight. However, this could add further torque that will reduce the functionality and safety of the project, although it did seem to move rather quickly even at the load so it is something that can be further checked out.



## Other Projects like Mine
Something to note is that I only really combined two pieces of example code (with some help from AI) to make this code for the project. The rest was my idea, inspired by my Dad's frustration. I had to build everything for my specific setup from scratch.



After looking through some other projects online, I found that a lot of people used essentially the same components I did, albeit for slightly different purposes. One project I found was this [Object Detection Servo Control using Arduino](https://github.com/Marahalshebel/Object-Detection-Servo-Control-using-Arduino) on GitHub, which uses the same Arduino Uno, HC-SR04 ultrasonic sensor, and SG90 servo motor that I used. The main difference is that their motor only rotates to 90 degrees when an object gets within 10 cm of the sensor, then moves back to 0 degrees when the object is no longer within that distance. As for commercial products, there are already a bunch of parking indicators that do essentially what I am trying to do, however, most of them use either lights or some sort of audible indicator to let the driver know how close they are. The reason I decided to go with a physical indicator instead is that the driver can actively see how much further they need to go without having to interpret different colored lights or listen for a sound. Rather than having the servo rotate between two set positions like the project I found, I have it rotate proportionally from 170 to 0 degrees as the car goes from 13 ft to 3 ft away from the sensor. Additionally, by using relatively cheap components and fabricating the rest of the parts myself, I was able to make something that works for my specific parking setup without having to spend a bunch of money.
