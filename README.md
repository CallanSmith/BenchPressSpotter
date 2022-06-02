# BenchPressSpotter

## Description

Our goal for this project is to create a bench press spotting machine that allows someone to re rack a failed rep by assisting with 20+ lbs of load. The problem we are trying to solve is the danger of not having a spotter when going for a 1 rep max.

## Criteria

## Constraints

## Solutions
Solution #1: Two simple articulated arms that would pick up bar and rerack it. The advantages of this desgin are that it would be simple to make the arms able to move the bar in a way that it could rerack it, however, two arms could not handle the load of the bar and that is why we didn't do this idea.

Solution #2: Servo controlled pulley system. THis idea was to make a pulley system that could move the bar up. The advatages of this idea are that it would be able to handle the load of the bar, the disadvantages of this idea are that it can't retract when sucesfully completing a rep.


## Design sketches/images

## List of matierals

## Schedule and delegation of work

## Code

```python

import board
import time
import digitalio
led = digitalio.DigitalInOut(board.D3) # led is not a led by relay, code mirrored led code so that is why that is what the variable is called
led.direction = digitalio.Direction.OUTPUT

button = digitalio.DigitalInOut(board.D7) # creating button variable
button.direction = digitalio.Direction.INPUT
button.pull = digitalio.Pull.UP

while True:
    if button.value is False: # if button pressed, turn relay on 
        led.value = True
        print("engaged")
        time.sleep(0.1)
    else:
        led.value = False # if not then turn relay off 
        print("disengaged")
        time.sleep(0.1)
```

The code for this project was very simple compared to the mechanical side of it, all the code does is turn on the relay when button is pressed, and when button is not pressed relay is off.



https://user-images.githubusercontent.com/71349670/171199708-31514010-6b1a-464e-92c0-694f5d2c34ee.mp4

## Wiring

<img src="Keyes-SR1y-with-Arduino-LED-STRIP.jpg" alt="The Wiring" width="500">

## Reflection
