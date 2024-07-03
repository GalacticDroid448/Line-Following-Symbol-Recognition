As detailed below the programs that involve Computer Vision for Line Following and Symbol Recognition are written in C++, whereas the program that is responsible for Line Following 
using the outputs of photodiodes is written in C. 

In reference to Computer Vision these programs use a Raspberry Pi camera with a resolution of 320,240. The Pi is mounted upon an autonomous bot that moves like a car. In this senario the pi sends its outputs via I2C to an ESP32 which is responsible for motor speeds and changing the steering angle of the bot. 

The PID Line Following Solution - Photodiodes however uses a collection of 5 photodiodes that each fed through a seperate transimpedance amplifier circuitand then their different voltage levels between 0-3.3V are fed to the upstairs ESP32 which uses this to determine how much of the black line each photodiode observes, from this a new steering angle can be caluclated. Here two ESP32 are used the upstairs EPS32 is responsible for calcualting the new steering angle based on photodiode's outputs and sends this value via I2C to downstairs ESP32 which uses this data to actually implement the changes. 

All of the follwing programs use the PID control algorithim to Line Follow [RGBYK Line Following Solution; Computer Vision approach to Line Following; PID Line Following Solution - Photodiodes ]

The OpenCV is also used in the Computer Vision programs to turn the line colour they are trying to detect to a greyscale image as this reduces processing power. An example of how openCV extracts the main colour from an image is shown in :Extracting the main colour form an image. 

Extracting the main colour form an image : C++
RGBYK Line Following Solution : C++
Symbol Recognition with a Raspberry Pi: C++
Computer Vision approach to Line Following: C++

PID Line Following Solution - Photodiodes : C
