Design Goals
============

The measurement limits are:
0-60V with 1mV resolution
0-30A with 1mA resolution


Power Input
===========
We accept two different power sources: Power from the device under test and an external power supply.

Device under Test: We're using the LM2591HV simple switcher to support any voltage from 7V up to 60V.
The current draw heavily depends on optional circuitry, like the WiFi module (100mA/5V) or the display.

External Power Supply: Because we can specify the input rating

Input switching
===============



We can easily specify the rating for the external power supply, where we accept anything from 


Shunt Resistor Considerations
=============================

The full-scale output of the shunt resistor must be between 50mV and 100mV for optimal performance. For 30A and 0.1V voltage drop, this gives us:

R=U/I
R=0.1/30
R=0.003 (nearest value)

Dale WSL3637 was chosen due to the low cost and eagle library availability.


Cable Connector Considerations
==============================

The Connector needs to widthstand 30A, and the Phoenix Contact MKDS 5/ 2-6,35 can support up to 32A.

LCD
===
For the initial design, we're using a stock 





modbus rs485?
rtc?