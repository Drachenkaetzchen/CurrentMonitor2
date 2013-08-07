Design Goals
============

The measurement limits are:
0-60V with 1mV resolution
0-30A with 1mA resolution


Power Input
===========

We accept two different power sources: Power from the device under test and an external power supply.

To reduce the part count we're using the LM2591HV simple switcher for powering via the device under test
or via an external power supply and an LTC4412 to switch over between the 5V rails.

Having two step-down DC converters might seem to be overkill, but I wasn't able to find an easy power
switching device which supports up to 60V which is required for the measurement input, so switching
two separate 5V rails seems to be convinient for now.


Drawbacks
=========

- We will have marginally wrong readings if powering the meter via the device under test. This needs to
  be fixed, because our current draw isn't constant (especially with the WiFi module).


Shunt Resistor Considerations
=============================

The full-scale output of the shunt resistor must be between 50mV and 100mV for optimal performance. For
30A and 0.1V voltage drop, this gives us:

R=U/I
R=0.1/30
R=0.003 (nearest value)

Dale WSL3637 was chosen due to the low cost and eagle library availability.


Cable Connector Considerations
==============================

The Connector needs to widthstand 30A, and the Phoenix Contact MKDS 5/ 2-6,35 can support up to 32A.

LCD
===
For the initial design, we're using an industry standard LCD. I'm not sure how well this works and how
interchangeable different LCDs are, or if I need to stick to a specific manufacturer.





modbus rs485?
rtc?
