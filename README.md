# SkyFan DC ESPhome Setup

The basic yaml config for the SkyfanDC made by Ventair flashing it onto your ESP8266 module and put it in the fan controller.
If you would like the physical module it is for ESPhome and Home Assistant only www.egglec.com.au
This module will not work with Tuya Smart App

Video about the fan : https://youtu.be/DethhMjQXy0

EasyEDA files : https://oshwlab.com/james_6977/sky-fan-dc

## SkyFan DC Module Version 2
If you have version 2 the pinout is different to accommodate the JST SH port that is for I2C, that port is connected to pins 4 and 5 which are the default I2C pins for the ESP8285.  If you have that style board please use the micro_skyfan2.yaml file as a base file to use if you wish to make modifications.

### Fan

- When a remote control command is received by the fan motor the fan entity is updated.
- The speed and direction of the fan motor can also be controlled by the fan entity.

| Fan Entity Speed | Skyfan DC      |
| ---------------- | -------------- |
| 0.0              | OFF            |
| 0.17             | NORMAL speed 1 |
| 0.33             | ECO            |
| 0.5              | NORMAL speed 2 |
| 0.67             | NORMAL speed 3 |
| 0.83             | NORMAL speed 4 |
| 1.0              | NORMAL speed 5 |

### Timer

Run on Timer with 12 setting options (1hr to 12hrs)

- The Timer duration can be set by the Timer select entity. This entity is disabled by default.

### Modes

ECO, SLEEP and NORMAL

- The Mode can be selected by the Mode select entity. This entity is disabled by default.

#### ECO

Fan will operate at peak energy efficiency level, usually somewhere between speeds 1 and 2.

#### SLEEP

Fan will reduce by 1 speed every 30mins until speed 1. (select preferred starting speed level first)

#### NORMAL

Cancels Mode and returns to normal function.
