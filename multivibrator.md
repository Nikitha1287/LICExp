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



### SIMULATION IN VLAB:

#### PROCEDURE:
**STEP 1:** Connect the components as mentioned: (1-3), (2-4).

**STEP 2:** Click on 'Check' button to check the connections. If connected connections are wrong, Make the right connection as per given instruction.

**STEP 3:** If connections are right, Click on the'Start' button to perform the experiment.

**STEP 4:** Toggle On/Off button to control the power to the system.

**STEP 5:** Move the 'Voltage' range slider to fetch values into table.

**STEP 6:** Click on 'Plot' button to plot the graph.

![72d2928ebc264ad58f23188799b6d644 1](https://github.com/user-attachments/assets/8d407035-5ecc-497c-a0b0-6642aaf7d349)


![2d63e6e104a942299a8bdcff0cd52d5c 1](https://github.com/user-attachments/assets/8336d963-7996-48d8-8360-d5019443dd61)



![69b73a9e749b4603a37013b8a84543fd 1](https://github.com/user-attachments/assets/bdb542f7-cfc8-45f0-bb1a-7b89c26a241c)


