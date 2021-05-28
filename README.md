# Electrocardiogram

This tutorial will take you through the steps of building a 3-point electrocardiogram using an Arduino.

Before you begin, here’s a little info about ECGs:  <br /><br />
An ECG detects your heart's electrical rhythm and graphs them out. This graph is called a tracing and it consists of several waves that recur with each heartbeat, about 60 to 100 times per minute. The wave pattern is used to diagnose various heart conditions. Ideally, the wave pattern should be a recurring one (sample output attached later). A typical ECG machine is bulky and expensive. For developing countries like India which have a high incidence of cardio-vascular diseases, a low-cost portable ECG machine is a boon to make medical facilities accessible in far flung rural areas.


## Supplies
- Arduino Uno / Nano
- Male to female jumper wires (5)
- AD8232 module
- 3 electrodes (pad with cable to attach to AD8232 module)


## Building the Circuit
Solder pins/wires into the 6 holes (GND to SDN) of the AD8232 IC
Make the following connections:

Arduino Connection | AD8232
-------------------|-------
GND | GND
3.3V | 3.3V
A0 | OUTPUT
~11 | LO-
~10 | LO+

Note:
- ~ denotes a PWM/analog pin <br />
- The SDN pin is not used in this tutorial. Connecting this pin to ground or "LOW" on a digital pin will power down the chip. This is useful for low power applications.
### Setup:
![setup](https://user-images.githubusercontent.com/44669235/119943555-cf6b5800-bfb0-11eb-86e4-523f9a46c27a.png)
### Circuit Diagram:
![circuitDiagram](https://user-images.githubusercontent.com/44669235/119943508-c24e6900-bfb0-11eb-9676-12d6bc219744.jpg)


## Placement of Sensor Pads/Electrodes
Placement of sensor pads:

Cable Color | Signal
------------|-------
Red | Right Arm (RA)
Yellow | Left Arm (LA)
Green | Right Leg (RL)

- Make sure you clean your skin (with sanitiser perhaps) before attaching the sensor pads.
- Also, the closer to the heart the pads are, the better the measurement. Two methods of connecting the pads are:
![sensorPlacement](https://user-images.githubusercontent.com/44669235/119943465-b5317a00-bfb0-11eb-9130-90e48e3dd33c.png)


## Program - Arduino IDE

[ecg_ver1.ino](ecg_ver1.io)


## Uploading the Program to Your Arduino
![setting1](https://user-images.githubusercontent.com/44669235/119944098-7c45d500-bfb1-11eb-8279-7638c3d470ec.png)
![setting2](https://user-images.githubusercontent.com/44669235/119944111-8071f280-bfb1-11eb-9d8e-3b2672f85375.png)
- Connect your Arduino to your laptop/computer
- Choose your Arduino board (Tools —> Board)
- Choose device port where you’ve attached the Arduino (Tools —> Port)
- Compile and upload the code. Then open up the serial plotter (Tools —> Serial Plotter)


## Sample Output
![output](https://user-images.githubusercontent.com/44669235/119944153-8bc51e00-bfb1-11eb-9d5c-9665659b1e05.png)
Notice the graph is consistent in the image (the waveform is repeating). This means we’re all good.

Thank you.


## Social: <br />
Do share your comments. I'd love to hear about your experience while trying out the project! I'll try to reply to all queries within 24 hours.
1. YouTube: <br />
    a. [Scientify Inc](https://www.youtube.com/c/scientifyinc) <br />
    b. [Scientify Hindi](https://www.youtube.com/c/scientifyhindi) <br />
2. [Linkedin](https://www.linkedin.com/in/arhangoyal/) <br />
3. [Instagram](https://www.instagram.com/scientifyinc_/) <br />
4. [Instructables](https://www.instructables.com/member/Scientify%20Inc/instructables/) <br />
