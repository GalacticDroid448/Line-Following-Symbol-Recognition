As detailed below the programs that involve Computer Vision for Line Following and Symbol Recognition are written in C++, whereas the program that is responsible for Line Following 
using the outputs of photodiodes is written in C. 

In reference to Computer Vision these programs use a Raspberry Pi camera with a resolution of 320,240. The Pi is mounted upon an autonomous bot that moves like a car. In this senario 
the pi sends its outputs via I2C to an ESP32 which is responsible for motor speeds and changing the steering angle of the bot. 

Extracting the main colour form an image
