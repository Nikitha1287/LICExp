 # **AIM:**
Design and analyze the differential amplifier for the following specification, VDD=2.2V, P<=2.2mW, Vin(CM)=1.2V,Vo(CM)=1.25V, Vp=0.4V. Perform DC analysis, Transient analysis, Frequency response and extract parameters.

# **DIFFERENTIAL AMPLIFIER:**
![Screenshot 2025-03-08 065620](https://github.com/user-attachments/assets/3723883c-ccbd-4b8b-a3ca-f1d688b8a0de)

## **INTRODUCTION:**
A differential amplifier is a amplifier configuration that consists of two identical MOSFETs, with the same transistor biasing point. This amplifier amplifies the difference between the two input voltage signals and rejects the common mode voltages. Let Vin1 and Vin2 be the two input gate voltages for each MOSFET, then the output voltage Vout is given by 
Vout=Av(Vin1-Vin2), where Av is the differential gain of the amplifier. 
The differential amplifier doesn't require coupling capacitors. As the noise is rejected by the common rejection mode(By suppressing the common input voltages). The output is amplification(gain multiplied to the difference between the two inputs) of the difference of input signals.

## **ADVANTAGES:**
