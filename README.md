# SkyFan DC ESPhome Setup

The basic yaml config for the SkyfanDC made by Ventair flashing it onto your ESP8266 module and put it in the fan controller.
If you would like the physical module it is for ESPhome and Home Assistant only www.egglec.com.au
This module will not work with Tuya Smart App

Video about the fan : https://youtu.be/DethhMjQXy0

EasyEDA files : https://oshwlab.com/james_6977/sky-fan-dc

# SkyFan DC Module Version 2
If you have version 2 the pinout is different to accomodate the JST SH port that is for I2C, that port is connected to pins 4 and 5 which are the default I2C pins for the ESP8285.  If you have that style board please use the micro_skyfan2.yaml file as a base file to use if you wish to make modifications.
