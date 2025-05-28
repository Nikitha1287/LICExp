# MONOSTABLE AND ASTABLE MULTIVIBRATOR
## MONOSTABLE MULTIVIBRSTOR

### AIM:
To generate a 0.5 ms output pulse using a monostable multivibrator circuit triggered by external input pulses.

### THEORY:
A monostable multivibrator using the 555 timer IC generates a single output pulse of a defined duration in response to a trigger input. A monostable multivibrator, also known as a one-shot timer, uses the 555 timer IC to produce a single output pulse when triggered. The duration of the output pulse is determined by an external resistor (R) and capacitor (C) connected to the timer. 

The monostable mode is also called “one-shot” pulse generator. The sequence of events starts when a negative going trigger pulse is applied to the trigger comparator. When this trigger comparator senses the short negative going trigger pulse to be just below the reference voltage (1/3 VCC), the device triggers and the output goes HIGH.
The discharge transistor is turned OFF and the capacitor C that is externally connected to its collector will start charging to the max value through the resistor R. The HIGH output pulse ends when the charge on the capacitor reaches 2/3 VCC. The internal connection of the IC 555 in monostable mode along with the RC timing circuit is shown below.

### WORKING PRINCIPLE:

Normally, the circuit's output is LOW (off).

When you give it a trigger pulse (a short LOW signal), the output goes HIGH (on).

As soon as the trigger is received, a capacitor starts charging through a resistor.

The output stays HIGH while the capacitor charges.

Once the capacitor voltage reaches a certain level (2/3 of the power supply voltage), the timer automatically turns the output LOW again.

The time the output stays HIGH depends on the values of the resistor (R) and capacitor (C).

After the output returns to LOW, it waits for the next trigger to repeat the process.


We know that the voltage across the capacitor C rises exponentially. Hence the equation for the capacitor voltage VC can be written as

VC = VCC (1 – e-t/RC)

When the capacitor voltage is 2/3 VCC, then

2/3 VCC = VCC (1 – e-t/RC)

2/3 = 1 – e-t/RC

e-t/RC = 1/3

– t/RC = ln (1/3)

– t/RC = -1.098

t = 1.098 RC

∴ t ≈ 1.1 RC

The pulse width of the output rectangular pulse is W = 1.1 RC.


The output waveforms are shown below

![image](https://github.com/user-attachments/assets/76bad3dd-7510-4c5c-9e4c-29c427ea525d)
