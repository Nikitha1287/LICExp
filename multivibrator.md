# MONOSTABLE AND ASTABLE MULTIVIBRATOR
## MONOSTABLE MULTIVIBRSTOR

### AIM:
To generate a 0.5 ms output pulse using a monostable multivibrator circuit triggered by external input pulses.

### THEORY:
A monostable multivibrator using the 555 timer IC generates a single output pulse of a defined duration in response to a trigger input. A monostable multivibrator, also known as a one-shot timer, uses the 555 timer IC to produce a single output pulse when triggered. The duration of the output pulse is determined by an external resistor (R) and capacitor (C) connected to the timer. 

The monostable mode is also called “one-shot” pulse generator. The sequence of events starts when a negative going trigger pulse is applied to the trigger comparator. When this trigger comparator senses the short negative going trigger pulse to be just below the reference voltage (1/3 VCC), the device triggers and the output goes HIGH.
The discharge transistor is turned OFF and the capacitor C that is externally connected to its collector will start charging to the max value through the resistor R. The HIGH output pulse ends when the charge on the capacitor reaches 2/3 VCC. The internal connection of the IC 555 in monostable mode along with the RC timing circuit is shown below.
