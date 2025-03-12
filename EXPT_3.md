# **EXPERIMENT 3: DESIGN OF NMOS DIFFERENTIAL AMPLIFIER**
# **AIM:**
Design and analyze the differential amplifier for the following specification, VDD=2.2V, P<=2.2mW, Vin(CM)=1.2V,Vo(CM)=1.25V, Vp=0.4V. Perform DC analysis, Transient analysis, Frequency response and extract parameters.

# **DIFFERENTIAL AMPLIFIER:**

![Screenshot 2025-03-11 045431](https://github.com/user-attachments/assets/e6118dc4-f333-4d2d-bb37-d8c57f63700e)


## **INTRODUCTION:**
A differential amplifier is a amplifier configuration that consists of two identical MOSFETs, with the same transistor biasing point. This amplifier amplifies the difference between the two input voltage signals and rejects the common mode voltages. Let Vin1 and Vin2 be the two input gate voltages for each MOSFET, then the output voltage Vout is given by:

**Vout=Av(Vin1-Vin2)**, where Av is the differential gain of the amplifier. 
The differential amplifier doesn't require coupling capacitors. As the noise is rejected by the common rejection mode(By suppressing the common input voltages). The output is amplification(gain multiplied to the difference between the two inputs) of the difference of input signals.
![Screenshot 2025-03-11 045443](https://github.com/user-attachments/assets/74df841c-58ac-4938-aead-d92874fb9518)

## **ADVANTAGES:**
1. **Noise Reduction:** Suppress noise by cancelling common mode signals.
2. **High Impedance:** High impedance at both input and output terminals.
3. **Improved Voltage Swing:** Larger dynamic range than common source amplifiers.
4. **Small phase shift:** Small phase shift between input and output.

## **APPLICATIONS:**
1. **Noise suppression**
2. **Communication**

## **COMPARISON BETWEEN DIFFERENTIAL AMPLIFIERS AND COMMON SOURCE AMPLIFIER:**
1. Differential Amplifiers have two input terminals and Common Source Amplifiers have single input terminal.
2. In Differential Amplifier the output is proportional to the difference between the two input signals.
   In Common Source Amplifier the output is taken from the drain and is proportional to the input signal, but referenced to ground. 
3. Differential Amplifier is designed to reject the common mode signals and apply gain to the difference between inputs.
   Common Source.
## **TYPES OF DIFFERENTIAL AMPLIFIER:**
1. CIRCUIT 1: Differential Amplifier with Load Resistor
2. CIRCUIT 2: Differential Amplifier with Current Source
   
![Screenshot 2025-03-11 045459](https://github.com/user-attachments/assets/25fd18ef-d23b-4b54-878d-4bea5865b636)

3. CIRCUIT 3: Differential Amplifier with Active load


## **CIRCUIT ANALYSIS:**

![Screenshot 2025-03-11 045510](https://github.com/user-attachments/assets/585dd92a-0659-4013-a3e2-67ca5ed5a739)
1. Perform DC Analysis and set the Q-point.
2. Then perform Ac analysis and analyze the differential gain of the circuit. 
3. Then find out the frequency response graph and deduce the -3dB gain and bandwidth of the ciruit.

# **CIRCUIT 1: Differential Amplifier with Load Resistor**
## **COMPONENTS REQUIRED:**
1. Resistors: 1.89921kohm(2),0.4kohm(1),
2. NMOS - 2,
3. Supply volatge:2.2V(1), 1.2V(2)
4. ac ground,
5. Connecting wires.

## **CIRCUIT DIAGRAM:**

![Screenshot 2025-03-10 012058](https://github.com/user-attachments/assets/96e64d79-2c4a-4bde-98bd-d65c4ce80f70)

## PROCEDURE:
1. Usind LTSPICE, construct a circuit as per the given circuit diagram.
2. Give input supply voltage 1.2 for each nmos,and set V<sub>DD</sub> to 2.2V supply. Set the R<sub>D</sub> values to 1.89921kohm, and R<sub>SS</sub> value to 400ohm.
3. Download the library tsmc018.lib file. Create a folder. Save the library file and LTspice file to the same folder. Import the library file to LTspice using spice directive(.op).
4. Name the nmos as CMOSN according to the library file.
5. Find the I<sub>SS</sub>, and hence I<sub>D</sub> value for each MOSFET.
6. DC analysis: Go to Run option, and select DC op and click on run. Observe the V<sub>OUT</sub>, I<sub>SS</sub>, V<sub>P</sub>. Vary the aspect ration and R<sub>D</sub> value in order to meet the design requirements.

![Screenshot 2025-03-10 012123](https://github.com/user-attachments/assets/cd36c812-a731-43cb-93f7-3e6f65bef39f)

7. Transient analysis: Go to edit simulation option. Change from dc op to transient analysis. Set the dc offset as 1.2V, Amplitude 50mV, frequency 1KHz. Keep stop time for 5ms and run to get the expected waveform. Take the difference of V<sub>out1</sub> and V<sub>out2</sub> waveforms,and calculate the diffrential gain. Also note down for what value of input amplitude the distortion starts to occur by varying the input amplitude. Then set the amplitude value to 100mV and repeat the same. Since we get the better gain for this input amplitude, we continue with this amplitude.

![Screenshot 2025-03-10 012255](https://github.com/user-attachments/assets/132acedc-866d-4d93-a919-1571a8692993)

![Screenshot 2025-03-10 012450](https://github.com/user-attachments/assets/1c280a14-62d5-41e0-9139-3f5fd30dbcf0)

![Screenshot 2025-03-10 012501](https://github.com/user-attachments/assets/fad98043-3f5b-4530-8573-a7108e761273)

![Screenshot 2025-03-11 032741](https://github.com/user-attachments/assets/05ca1747-443a-4cc0-85b1-abb803a68ce5)

![Screenshot 2025-03-11 032754](https://github.com/user-attachments/assets/cc0353c3-b13a-4c13-8559-6c52801f5ca8)


8. AC analysis : Go to edit simulation option. Change from transient analysis to ac analysis. Set type of sweep as decade, number of points per decade as 20, start and stop frequency as 0.1Hz and 1THz respectively to get the expected ac waveform(Frequency response graph). Note down the -3dB gain of the circuit and the bandwidth.

![Screenshot 2025-03-11 033306](https://github.com/user-attachments/assets/57692b49-6802-4b1b-9ced-537a5a17e161)

## **CALCULATION:**
### **Formulae:**
1. P=V<sub>DD</sub>*I<sub>SS</sub>
2. I<sub>D</sub>=I<sub>SS</sub>/2
3. V<sub>DS</sub>=V<sub>O(CM)</sub>-V<sub>P</sub>
4. V<sub>O(CM)</sub>=V<sub>DD</sub>-(I<sub>D</sub>* R<sub>D</sub>)
5. V<sub>P</sub>= I<sub>SS</sub>* R<sub>SS</sub>
6. V<sub>IN(CM)</sub>=V<sub>GS</sub>+V<sub>P</sub>
7. V<sub>OV</sub>= V<sub>GS</sub>-V<sub>TH</sub>
8. V<sub>IN(max)</sub>=V<sub>O(CM)</sub>+V<sub>TH</sub>
9. V<sub>IN(min)</sub>=sqrt(2)*V<sub>OV</sub>
10. g<sub>m</sub>=(2*I<sub>D</sub>)/V<sub>OV</sub>
11. A<sub>V</sub>=-g<sub>m</sub>*R<sub>D</sub>
12. A<sub>V</sub>(in dB)=20*log<sub>10</sub>*(A<sub>V</sub>)

### **Substitution:**
1. P=1mW, V<sub>DD</sub>=2.2V, V<sub>IN(CM)</sub>=1.2V, V<sub>O(CM)</sub>=1.25V, V<sub>P</sub>=0.4V 
2. I<sub>SS</sub>=P/V<sub>DD</sub>=2.2mW/2.2=1mA
3. I<sub>D(CM)</sub>=1mA/2=0.5mA
4. V<sub>DS</sub>=1.25V-0.4V=0.85V
5. R<sub>D</sub>=(V<sub>DD</sub>-V<sub>O(CM)</sub>)/I<sub>D</sub>=(2.2-1.25)V/1mA=1.9kohm
6. R<sub>SS</sub>=V<sub>P</sub>/I<sub>SS</sub>=o.4V/1mA=400ohm
7. V<sub>GS</sub>=V<sub>IN(CM)</sub>-V<sub>P</sub>=1.2V-0.4V=0.8V
8. V<sub>OV</sub>=V<sub>GS</sub>-V<sub>TH</sub>=0.8v-0.3662V=0.4338V
9. V<sub>IN(max)</sub>=1.25V+0.3662V=1.6162V
10. V<sub>IN(min)</sub>=sqrt(2)*0.4338V=0.613V
11. g<sub>m</sub>=0.002A/V
12. A<sub>V</sub>=3.798A/V<sup>2</sup>
13. A<sub>V</sub>=11.59dB

## **RESULT:**
**1. DC Analysis:**

![Screenshot 2025-03-10 012208](https://github.com/user-attachments/assets/dd3bef34-333b-4384-8e62-38bad1a73249)

DC operating point:
V<sub>O<sub>1</sub></sub>=V<sub>O<sub>2</sub></sub>=1.25V
V<sub>DD</sub>=2.2V
V<sub>IN(CM)</sub>=1.2V
V<sub>P</sub>=0.40165
I<sub>D<sub>1</sub></sub>=V<sub>D<sub>2</sub></sub>=0.500mA

**2. Transient Analysis:**
1. For V<sub>IN</sub> amplitude = 50mV, V<sub>IN(pp)</sub>=100mV
![Screenshot 2025-03-10 012619](https://github.com/user-attachments/assets/2002204f-6fc4-4e6e-a042-4576917ec1ed)
V<sub>O</sub>=1.4681V-1.0239V=0.442V
A<sub>V</sub>=0.442/0.1=4.42

2. For V<sub>IN</sub> amplitude = 100mV, V<sub>IN(pp)</sub>=200mV
  
   ![Screenshot 2025-03-11 032910](https://github.com/user-attachments/assets/fdc977c7-1aa0-460c-b29b-5006c9af7fed)
V<sub>O</sub>=1.8899V-0.8108V=1.0791V
A<sub>V</sub>=1.0791V/0.2=5.3955


![Screenshot 2025-03-11 033127](https://github.com/user-attachments/assets/66c94e9f-acdd-458a-a4d0-14df8d2eff62)

Differential Gain = (0.8592V-(-0.8585V))/.2V=8.5885

**2. AC Analysis:**

![Screenshot 2025-03-11 034405](https://github.com/user-attachments/assets/7a9d73e3-613c-4e6a-b448-d23aefd7150a)

![Screenshot 2025-03-11 034439](https://github.com/user-attachments/assets/753741b9-9e10-459c-bbef-a28ceab51879)

-3dB bandwidth=1.4890MHz


# **CIRCUIT 2: Differential Amplifier with Current Source**
## **COMPONENTS REQUIRED:**
1. Resistors: 1.9kohm(2),
2. NMOS - 2,
3. Supply volatge:2.2V(1), 1.2V(2)
4. ac ground,
5. Connecting wires,
6. Current source: 1mA(1).

## **CIRCUIT DIAGRAM:**

![Screenshot 2025-03-11 035228](https://github.com/user-attachments/assets/359d5114-a25b-499e-8ed6-d40bef0afcc6)

## **RESULT:**
**1. DC Analysis:**
TRIAL 1:

![Screenshot 2025-03-11 035244](https://github.com/user-attachments/assets/6e19fb31-1803-4510-b3b3-eb7677482a56)

V<sub>O</sub> changes to 1.2504V in the first trial, so we increase the R<sub>D</sub> value slightly in order to decrease V<sub>O</sub> value to 1.25V exactly.

TRIAL 2:
We get R<sub>D</sub>=1.9kohm

![Screenshot 2025-03-11 035533](https://github.com/user-attachments/assets/3296c675-0eb7-4afd-9515-d05cbdc2ee3e)

![Screenshot 2025-03-11 035555](https://github.com/user-attachments/assets/680c1217-d1d9-4c47-a694-66c964952dc3)


**2. Transient Analysis:**
 1. For V<sub>IN</sub> amplitude = 100mV, V<sub>IN(pp)</sub>=200mV

![Screenshot 2025-03-11 035745](https://github.com/user-attachments/assets/bb43f7e0-db2d-41fc-9e12-dcab5588fd8a)

V<sub>O</sub>=1.6802V-0.8227V=0.8575V
A<sub>V</sub>=4.2875

![Screenshot 2025-03-11 035924](https://github.com/user-attachments/assets/d31b3c15-0061-4558-8c1d-bd14e330db77)


Differential Gain = (0.8571V-(-0.8567V))/.2V=8.569

**2. AC Analysis:**

![Screenshot 2025-03-11 040105](https://github.com/user-attachments/assets/f8b3f967-5335-445a-81ae-208ce462e6dd)


![Screenshot 2025-03-11 040323](https://github.com/user-attachments/assets/cafb081c-2d10-4338-95fd-b3648d8b6e6c)

-3dB bandwidth = 695.192kHz


# **CIRCUIT 2: Differential Amplifier with Active Load**
## **COMPONENTS REQUIRED:**
1. Resistors: 1.9kohm(2),
2. NMOS - 3(identical),
3. Supply volatge:2.2V(1), 1.2V(2), 0.993506V(1),
4. ac ground,
5. Connecting wires.

## **CIRCUIT DIAGRAM:**

![Screenshot 2025-03-11 041819](https://github.com/user-attachments/assets/ea9e5501-ef36-4f78-bbb9-23ec302336e2)


![image](https://github.com/user-attachments/assets/cd7adf7f-2688-4987-852b-0b100cd89a89)

![image](https://github.com/user-attachments/assets/cd2d510d-15a5-4d61-87da-e0d43d95a50e)


![image](https://github.com/user-attachments/assets/8c89efa3-ee8a-4d4a-8f38-9ee7dfeb7468)


![image](https://github.com/user-attachments/assets/32bd8245-7a28-4757-9050-fa196871c516)


![image](https://github.com/user-attachments/assets/b9778456-53ec-4696-be25-4c4389e88a0f)


![image](https://github.com/user-attachments/assets/5d4731ce-aedf-401e-a788-45a6da4bcccf)

![image](https://github.com/user-attachments/assets/0b308a69-8e7d-4b00-93ab-591c0dd4fde3)


![image](https://github.com/user-attachments/assets/37cb23c3-e669-4fca-8e2c-aa59faa6ffa2)




![image](https://github.com/user-attachments/assets/10a8f42d-0611-4dc0-9be2-87142a8817d5)




![image](https://github.com/user-attachments/assets/38394eb0-04ad-42e0-89c0-a355a0d7b03c)


![image](https://github.com/user-attachments/assets/1eef11ab-452b-40e5-a0c3-599768abad4d)


![image](https://github.com/user-attachments/assets/f52e8ae2-7ccc-4660-a80a-79ad15fc6236)

![image](https://github.com/user-attachments/assets/80c988b3-d5ad-427b-90a9-a8e556e6e5a9)


![image](https://github.com/user-attachments/assets/b8273cd3-9234-4b51-a280-82ebcbe7e10c)

![image](https://github.com/user-attachments/assets/38fa750a-3162-4ce8-be85-3dd0cd113b9c)


![image](https://github.com/user-attachments/assets/fcf49d12-d6c5-4975-adc5-2fa868a9aae8)




![image](https://github.com/user-attachments/assets/e5df9868-7ad4-408b-847a-86f86eac278f)


