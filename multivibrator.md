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

### DIAGRAM:

![image](https://github.com/user-attachments/assets/f50458a4-42f6-4912-89df-6e6e338e6217)

### PROCEDURE:
1. Open LTspice and create a new schematic.

2. Place components: 555 timer IC (NE555), Resistor (R), Capacitor (C), Voltage source (V1 for Vcc, V2 for trigger), Ground (GND)

3. Connect the 555 timer in monostable mode: Pin 1 → GND, Pin 8 → Vcc (e.g., 5V), Pin 4 (Reset) → Vcc, Pin 5 (Control Voltage) → 0.01 µF to GND, Pin 2 (Trigger) → Pulse input (V2), Pin 6 → Pin 7, Pin 7 → Resistor (R) → Vcc, Pin 6 → Capacitor (C) → GND, Pin 3 → Output node, Set the trigger source (V2): Use PULSE() with a brief low-time (e.g., PULSE(5 0 1m 10n 10n 0.1m 10m))

4. Set simulation command: .tran 0 10ms to observe waveform

5. Run the simulation and probe the output (Pin 3) to observe the HIGH pulse.

### CALCULATION:
t=1.1RC
fix R such that:

R=V<sub>CC</sub>/3I<sub>min</sub>

V<sub>CC</sub>=5V, I<sub>min</sub>=10uA;
R=5/(3 * 10 * 10 <SUP>-6</SUP>) = 166kohm

C=(0.5* 10<sup>-3</sup>/1.1 * 166 * 10<sup>3</sup> = 0.0027uF.



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



## ASTABLE MULTIVIBRATOR
### AIM:
To generate a pulse of width 1 ms using 555 timer IC, and analyze waveform shaping using a differentiator, clipper, and monostable multivibrator.

### THEORY:
An astable multivibrator using the 555 timer IC continuously oscillates between high and low states, generating a square wave output without requiring an external trigger.
Astable Multivibrator
An astable multivibrator circuit based on the 555 timer IC generates a continuous square wave without requiring an external trigger. The timing cycle is set by two resistors, 
𝑅𝑎 and Rb, and one capacitor 𝐶 .The high time (T_ON) and low time (T_OFF) are given by:

T ON =0.693(Ra + Rb)C,  T OFF = 0.693(Rb)C

Differentiator Circuit
A differentiator highlights rapid changes in a signal. It converts a square waveform into short positive and negative spikes, centered around transitions. The basic RC differentiator has a capacitor in series with the input signal and a resistor to ground. Output spikes occur at the rising and falling edges of the input.

Clipper Circuit
A negative clipper blocks or “clips” the negative half of a signal using a diode and reference voltage. This leaves only positive-going spikes, which are suitable triggers for the monostable multivibrator.

Monostable Multivibrator
This 555 timer configuration produces a single, fixed-duration output pulse when triggered. It has one stable state (LOW), and a temporary HIGH state when a negative trigger is applied.
The pulse width is:

T=1.1RC

The circuit is built to alternate between two stable states, resulting in a steady oscillation. 
By changing the values of the resistors and capacitors in the circuit, the frequency and duty cycle of the output waveform can be altered.
In digital circuits, the astable multivibrator is frequently employed as a clock source. The timing of data transfers between various components can be synchronized using the frequency of the output waveform.

### CIRCUIT:
![image](https://github.com/user-attachments/assets/415d4461-51f4-434b-87a7-ce6892d9a613)

### PROCEDURE:
1. Create the Astable Multivibrator:
i. Place a 555 timer IC (use NE555 model or equivalent).
ii. Connect two resistors Ra, Rb, and capacitor 𝐶 to configure the 555 in astable mode.
iii. Use a voltage source (e.g., 5V) as Vcc.
2.Simulate the Output:
i. Run a transient analysis (e.g., tran 0 10ms) to observe the periodic square waveform at the output (pin 3).

3. Build the Differentiator Circuit:
i. Connect a capacitor and resistor in series from the astable output to ground.
ii. Observe the output across the resistor to visualize edge spikes.

4. Add the Negative Clipper:
i. Insert a diode in parallel with the resistor in reverse bias to clip negative voltage spikes.
ii. View the clipped output waveform.

5. Create the Monostable Multivibrator:
i. Add another 555 timer in monostable configuration.
ii. Trigger its input (pin 2) using the clipped edge pulse.
iii. Select R and C values to generate a 0.5 ms pulse (T = 1.1RC).

6. Run Transient Analysis:
i. Use .tran simulation (e.g., tran 0 10ms) and place probes at key nodes.
ii. Verify waveforms at each stage: astable output, differentiator, clipper, and monostable output.

7. Analyze Results:
i. Measure ON/OFF times and pulse widths using cursors.
ii. Confirm the monostable output pulse is approximately 0.5 ms.

### RESULT:
![image](https://github.com/user-attachments/assets/6de23f4e-fdfa-4e3f-b149-730da17d439c)



### SIMULATION IN VLAB:
![image](https://github.com/user-attachments/assets/b580019d-44e1-4647-95fd-0440eaf1e3dd)

ACROSS CAPACITOR:
![image](https://github.com/user-attachments/assets/7db47906-ed41-453e-be8f-70e20cd3299e)


THE GENERATED OUTPUT WAVEFORM:
![image](https://github.com/user-attachments/assets/2054c12f-4a44-4f8f-b241-4a7bfc6c35a4)






