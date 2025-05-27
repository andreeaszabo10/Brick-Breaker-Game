# Brick Breaker Game

## Introduction

This project is a Breakout-style game, controlled with an Arduino Uno, played on an I2C OLED display. The player controls the paddle using a joystick, and the goal is to hit the ball and break all the blocks without losing all the lives.

I wanted to recreate a childhood game and adapt it into a physical form using simple components. I added a button to pause the game, a traffic light module with three LEDs to indicate the remaining lives, and a photoresistor that changes the screen graphics based on the amount of light in the room. This project provides a foundation that I can expand in the future by adding new levels and features.

## General Description
To build this project, I used several hardware components working together to make the game function properly. At the core of the system is the Arduino Uno board, which controls all the other modules. To control the paddle, I used a KY023 joystick that sends analog signals to the Arduino based on movement along the X-axis. These signals are interpreted and the paddle moves left or right on the screen.

The display showing the game is a 0.96-inch OLED screen with an I2C interface and a 128×64 resolution. It is connected to the Arduino via the SDA and SCL pins and graphically displays all the game elements: the ball, the paddle, the bricks, and the score. I also added a 6x6x5 button connected to a digital pin, which serves to pause the game when pressed. This allows the player to pause and resume the game at any time.

To visually show the number of remaining lives, I used a traffic light module with three LEDs, each connected to a separate digital pin. At the beginning, all three LEDs are lit, and as lives are lost, they turn off one by one. Another important component is the photoresistor, which is connected to an analog pin. It reads ambient light and allows the Arduino to adapt the game’s colors accordingly.
