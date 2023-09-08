# Raspberry-Pi-Adafruit-Motor-Shield-Interface
Raspberry Pi interfacing with L293D Adafruit Motor Shield Driver
-
As many of you know that the Adafruit Motor Shield is one of the most widely available and affordable motor driver which has multiple expansion ports and dual L293D motor driver with a half H driver, the reason for its popularity also lies in the fact that it is designed specifically for Arduino Uno and is compatible with other Arduino's as well. However, the story isn't the same for Raspberry Pi's as it is not compatible with them out of the box, you have to map out the pins and make your own connections. I searched the entire internet and didn't find anything that would help me build a interface between the two of them, that was until I found this article https://lastminuteengineers.com/l293d-motor-driver-shield-arduino-tutorial/ here the author states that 

"D9 and D10 are used to control the servo motors. D10 is connected to Servo 1, while D9 is connected to Servo 2."

They also stated the pins used by DC motors however, I tried building an interface for them and it didn't work. So, instead I built an interface to control Servo's.

![AFM Servo Connection Pins](https://github.com/lonewolf24/Raspberry-Pi-Adafruit-Motor-Shield-Interface/assets/68584884/13efb123-e3e7-4a20-a665-ce91bef60a21)

Here as you can see I have connected Servo's directly to the AFM and orange wire is connected to pin D9 and red wire to pin D10 which would recieve PWM signal from Raspberry Pi.

![AFM Power Pins](https://github.com/lonewolf24/Raspberry-Pi-Adafruit-Motor-Shield-Interface/assets/68584884/b6f9af67-a887-4f92-a9da-262b5b51b97c)

On the other side of AFM I have connected another red wite to 5V pin and brown wire to Ground pin. (*This part is not necessary if you are supplying power directly to the AFM, and if you are supplying power direclty to the AFM please make sure to take out the power jumper.)

![RPi](https://github.com/lonewolf24/Raspberry-Pi-Adafruit-Motor-Shield-Interface/assets/68584884/319bcf94-3af4-4905-a4ff-2d94fb9e516f)

Now connect the Servo control D9 and D10 pins to any GPIO pins on the Raspberry Pi.
Here I have chosen GPIO 12 (Physical board pin 32) and GPIO 13 (Physical board pin 33) for a reason, that is they output PWM signal which is what Servo's need.

![raspberry-pi-pinout](https://github.com/lonewolf24/Raspberry-Pi-Adafruit-Motor-Shield-Interface/assets/68584884/a66c5d6f-1797-4a53-a325-5ede309552b7)

Here is the pin layout for your convinience (Image courtesy- https://pinout.xyz/ )

The code I used to test this is provided in the repository (Code belongs to Christopher Barnatt who runs ExplainingComputers YouTube channel). To run the code you need to use Thonny on Raspberry Pi.

As of now only Servo's can be controlled using this method when I figure out how to use DC motors or Stepper moters with AFM on Raspberry Pi I will make a commit on this repository.

Till then this is as far as I could go.
