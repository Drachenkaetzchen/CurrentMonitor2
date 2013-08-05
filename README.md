Design Goals:

2.7V-30V or 2.7V-60V
30A


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
