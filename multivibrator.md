# MONOSTABLE AND ASTABLE MULTIVIBRATOR
## MONOSTABLE MULTIVIBRATOR

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

### CALCULATION:
t=1.1RC
fix R such that:

R=V<sub>CC</sub>/3I<sub>min</sub>

V<sub>CC</sub>=5V, I<sub>min</sub>=10uA;
R=5/(3 * 10 * 10 <SUP>-6</SUP>) = 166kohm

C=(0.5* 10<sup>-3</sup>/1.1 * 166 * 10<sup>3</sup> = 0.0027uF.

### DIAGRAM:

![image](https://github.com/user-attachments/assets/f50458a4-42f6-4912-89df-6e6e338e6217)

### RESULT:
**THE TRIG PULSE:**
![image](https://github.com/user-attachments/assets/f3af1dc7-64ca-4c47-96ef-2a402684d3a4)

**THE OUTPUT GENERATED WAVEFORM:**
![image](https://github.com/user-attachments/assets/3c94199c-09ec-4c2f-9449-9bcb3e75cbee)


### SIMULATION IN VLAB:

#### PROCEDURE:
Connect the components as mentioned below: L1-L12, L14-L12, L16-L12, L4-L9, L8-L9, L9-L10, L3-L17, L11-L13, L7-L11, L6-L13, L5-L15.(For eg. click on 1 and then drag to 12 and so on.)
Click on 'Check Connection' button to check the connections.
If connected wrong, click on the wrong connection. Else click on 'Delete all connection' button to erase all the connections.
Intially set R a=10 kΩ, C=1 µf, Vcc=5 V, Tin = 20 msec.
Click on "Calculate" button.
Now note the output voltage.
Click on "Plot" button to plot, Trigger Input Voltage, Output Voltage, Capacitance Voltage
Click on "Clear" button to clear the data.
Repeat the experiment for another set of resistance value and capacitance value.
Set the Resistance (R a) value (1 kΩ - 10 kΩ).
Set the Capacitance (C) value .
Set supply voltage (Vcc).


![image](https://github.com/user-attachments/assets/dab08e60-6633-4803-a3e4-7bd7ec4b226d)




### INFERENCE:
1. The circuit stays LOW until triggered. The output of the monostable multivibrator is LOW by default and doesn’t change until a trigger is given.

2. Generates a single pulse when triggered. When a negative trigger pulse is applied, the output goes HIGH for a short time and then returns to LOW automatically.

3. The duration of the pulse depends on R and C. The width of the HIGH output pulse is controlled by the resistor and capacitor values using the formula:

T = 1.1 × 𝑅 × 𝐶

4. This makes it easy to adjust the timing by choosing suitable components.

5. In this experiment, 0.5 ms pulse was achieved. By using a 0.1 µF capacitor and a resistor of around 4.54 kΩ, we got a pulse width close to 0.5 milliseconds, as expected from the formula.

6. The output goes HIGH instantly when triggered. As soon as the trigger voltage drops below 1/3 of Vcc, the timer responds immediately and the output goes HIGH. Returns to LOW automatically after time delay. After the set time, the capacitor charges up to 2/3 of Vcc, which makes the output go LOW again without needing another input.

7. Useful for time delay and pulse generation. This setup is a simple way to create accurate time delays or single output pulses, useful in digital circuits and control systems.

8. Circuit works reliably and repeatedly. The timer responded consistently to multiple triggers, producing the same output pulse each time, showing it’s stable and reliable.



## MONOSTABLE MULTIVIBRATOR
### AIM:
To design and simulate a monostable multivibrator using a 555 Timer IC that generates a pulse of width 1 ms using input trigger signals.


### THEORY:
An astable multivibrator using the 555 timer IC continuously oscillates between high and low states, generating a square wave output without requiring an external trigger.

















