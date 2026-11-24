# Progress Check In Part 1

## Updates




### Power Supply and Speed
Like I guessed in my proposal video, the _____ was the issue that kept the servo from running correctly. The _____ was able to move (albeit completely randomly) the motor when the ground of the ____ was only connected to the motor and not also connected to the Arduino. In order for control of the motor to work correctly, they must share the ground with the Arduino. When shared the ground, nothing would happen. I believe one possible issue is that the ____ was slightly broken a bit from a drop from before, however, that wouldn't explain how it worked when not sharing the ground (this same exact non-sharing effect happened with the new power supply). 


Furthermore, some spec sheets for the SG90 stated that the absolute max voltage for the servo was about 6V and not 5V. Since, I already have two servos and Micro Center sells the same motor for dirt cheap, I thought I would try risking a motor and running it at 6V instead of 5V to try and crank out as much speed and torque as possible. The reason I decided on this is that I need to allow the indicator to be as long as possibly to allow it to be easily viewable as I get closer to the car (which will be seen in the video). The problem is that as the flag increases in length and mass, so does the torque. From there, as torque increases, speed will decrease. Speed is the key to this project working in a reliable matter. Having to go at 1 mph or less while parking just so the motor can keep up is greatly inconvenient and unsafe if some one none the wiser goes way too fast. This means I need to try to maximize how fast the servo rotates to allow normal parking speeds. While it may not make a significant increase, raising the voltage to 6V will help a ton.

So, what sort of power supply should I look for? Well, in case the 6V is not a great idea, I need to make sure that it can change voltages so that I do not have to waste money on another supply. Additionally I need to be able to connect it to the circuit. Most importantly, I need to make sure it can allow the current to only supply what is needed has enough amperage to power the servo correctly. I needed to stop by Micro Center anyway, so I decided to scour their website to see if they had what I needed. 

After looking through their website, I found this [CyberPower Systems Universal Power Adapter](https://www.microcenter.com/product/710639/CPUAC1U1300_Universal_Power_Adapter?iitt=Rf8_RMhWhyULaeighM_-xFYDOFxlOF_7&MccGuid=4DB231AC-D731-446A-8E25-7CC67683918C). This was exactly what I needed be cause it 


### Testing
After reattaching and rewiring eveything. I ran a test with the new power supply 


### Stick Flag
So now that the servo now runs its code correctly, the only thing left is the indicator for the driver to know how close they are to 

I was going to test several different sticks with varying widths, however, I was pleasantly surprised to find that the quarter inch I tested first worked perfectly fine with no major issues. Instead of wasting 


### The Project is Essentially Done
I already 3D printed all components prior to the project proposal as seen in that submission. Additionally, essentially the same code was used in that video as well, however, the motor was simply not 


<iframe width="560" height="315" src="https://www.youtube.com/embed/K9nsScTuK84?si=NyPmnC0JZcS0tolc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


## What next?
Really the only thing left to do is just clean up the code for further efficiency.  Right now the code still has everything I need for testing (distance calculations, distance and angle 

Further more, I found some thin sticks 



## Other Projects like Mine
Something to note is that I only really combined the 
