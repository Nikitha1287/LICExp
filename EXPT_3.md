# **EXPERIMENT 3: DESIGN OF NMOS DIFFERENTIAL AMPLIFIER**
# **AIM:**
Design and analyze the differential amplifier for the following specification, VDD=2.2V, P<=2.2mW, Vin(CM)=1.2V,Vo(CM)=1.25V, Vp=0.4V. Perform DC analysis, Transient analysis, Frequency response and extract parameters.

# **DIFFERENTIAL AMPLIFIER:**
![Screenshot 2025-03-08 065620](https://github.com/user-attachments/assets/3723883c-ccbd-4b8b-a3ca-f1d688b8a0de)

## **INTRODUCTION:**
A differential amplifier is a amplifier configuration that consists of two identical MOSFETs, with the same transistor biasing point. This amplifier amplifies the difference between the two input voltage signals and rejects the common mode voltages. Let Vin1 and Vin2 be the two input gate voltages for each MOSFET, then the output voltage Vout is given by:

**Vout=Av(Vin1-Vin2)**, where Av is the differential gain of the amplifier. 
The differential amplifier doesn't require coupling capacitors. As the noise is rejected by the common rejection mode(By suppressing the common input voltages). The output is amplification(gain multiplied to the difference between the two inputs) of the difference of input signals.

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
1. Differential Amplifier with Load Resistor
2. Differential Amplifier with Current Source



## **CIRCUIT ANALYSIS:**












# **CIRCUIT 1: Differential Amplifier with Load Resistor**
## **COMPONENTS REQUIRED:**
## **CIRCUIT DIAGRAM:**

![Screenshot 2025-03-10 012058](https://github.com/user-attachments/assets/96e64d79-2c4a-4bde-98bd-d65c4ce80f70)



![Screenshot 2025-03-10 012123](https://github.com/user-attachments/assets/cd36c812-a731-43cb-93f7-3e6f65bef39f)
DC op point







![Screenshot 2025-03-10 012208](https://github.com/user-attachments/assets/7d26f935-b125-4fbc-b3b1-ba99b88cb1f9)

DC analysis






![Screenshot 2025-03-10 012255](https://github.com/user-attachments/assets/132acedc-866d-4d93-a919-1571a8692993)

Transient Analysis





![Screenshot 2025-03-10 012322](https://github.com/user-attachments/assets/7f94e7f8-08fc-4ddf-9dc3-a4747023a77c)
Transient Analysis



![Screenshot 2025-03-10 012450](https://github.com/user-attachments/assets/1c280a14-62d5-41e0-9139-3f5fd30dbcf0)

Sine wave


![Screenshot 2025-03-10 012501](https://github.com/user-attachments/assets/fad98043-3f5b-4530-8573-a7108e761273)

Sine wave


![Screenshot 2025-03-10 012619](https://github.com/user-attachments/assets/c5de68c0-524a-4f3f-a247-db22e56471c2)


![Screenshot 2025-03-10 012934](https://github.com/user-attachments/assets/b6fb0d51-ca16-4d4f-92da-2ebefb366e74)



![Screenshot 2025-03-10 013011](https://github.com/user-attachments/assets/ae0c4cca-d2f7-48f7-8e3c-b403f2997210)








