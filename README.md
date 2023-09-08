# Raspberry-Pi-Adafruit-Motor-Shield-Interface
Raspberry Pi interfacing with L293D Adafruit Motor Shield Driver
-
As many of you know that the Adafruit Motor Shield is one of the most widely available and affordable motor driver which has multiple expansion ports and dual L293D motor driver with a half H driver, the reason for its popularity also lies in the fact that it is designed specifically for Arduino Uno and is compatible with other Arduino's as well. However, the story isn't the same for Raspberry Pi's as it is not compatible with them out of the box, you have to map out the pins and make your own connections. I searched the entire internet and didn't find anything that would help me build a interface between the two of them, that was until I found this article https://lastminuteengineers.com/l293d-motor-driver-shield-arduino-tutorial/ here the author states that 

"D9 and D10 are used to control the servo motors. D10 is connected to Servo 1, while D9 is connected to Servo 2."

They also stated the pins used by DC motors however, I tried building an interface for them and it didn't work. So, instead I built an interface to control Servo's.

