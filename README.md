# microbit
Tasks for learning physical computing with the microbit
MicroBit <br>
![Microbit](https://az742082.vo.msecnd.net/pub/jcjojcrc)

# The Compass
Note that the magnetometer needs to be calibrated before use. This is done by tipping the micro:bit around to draw a circle on the LEDs. Be aware that sometimes the magnetometer calibration can be affected by the magnetic fields emanating from an electronic device, such as a computer.

Follow the instructions on this page to learn about the magnetometer, - http://microbit-challenges.readthedocs.io/en/latest/tutorials/compass.html 

# Challenge
Make your microbit display the letters "N', "E", "S" and "W" when the microbit is pointing North, East, South and West respectively.<br>
![north](north.png)

## Starter code ##
    from microbit import *

    compass.calibrate()

    while True:
    sleep(100)
    val = compass.heading()
    if (val < 10 or val > 350):
      display.show('N')
    else:
      display.show(Image.NO)
