# **Circuit1**

## **AIM:**
To perform DC, transient, and AC analyses on a CS amplifier circuit and use LT Spice to extract the different parameters involved.

## **COMPONENTS:**
Mosfet-nmos4,pmos4,voltage sources-0.9V,1.8V, connection wires, Resistor-1k,  

## **THEORY:**
A common source amplifier is a type of field-effect transistor (FET) amplifier that is used to boost transconductance or voltage. For single-stage FET amplifiers, it is one of the three basic topologies. How it works The input signal is sent to the gate terminal.The output signal is supplied via the drain terminal.A common source terminal is shared by the input and output.The input resistance of common source amplifiers is higher than that of equivalent CE amplifiers.has a lower gain than the equivalent CE amplifier. Capable of acting as a voltage or transconductance amplifierSource amplifiers are commonly used in amplifier circuits that require signals with very low input voltages. It is possible to use both voltage and transconductance amplifiers.
The drain current:
Id = 1/2 kn Vov2 ; Vov=Vgs-Vth and kn=un Cox W/L

## **CIRCUIT DIAGRAM:**  
 ![image](https://github.com/user-attachments/assets/bafef02b-dd43-4778-a7b7-a40f0978b64c)

## **PROCEDURE:** 
1. Create a folder named projects. Save the LTSPICE file in this folder. Save the tsmc018 library file also in the same folder.
2. Add the components according to the circuit diagram. Two voltage sources, one nMOS, a load resitor(1k).
3. Name the nMOS as CMOSN as per the library file.
4. DC ANALYSIS:
   1. Calculate the value of Id from the given power rating value. As we already the voltage value is provided.
   2. Now we define the aspects ration of the MOSFET to obtain the calculated Id value. Fix the value of length and vary the value of width(W) until we obtain the required drain current value.
   4. Check whether the mosfet is in saturation region, after defining the aspect ratio. In saturation region, Vds is greater than Vov(Overdrive voltage).
   5. Note down the values of DC Analysis.
      ![Screenshot 2025-02-18 050356](https://github.com/user-attachments/assets/0f41656f-ff70-446d-9560-422308af03e2)

7. Transient Analysis:
   1. Set the input gate voltage to sine wave with amplitude of 50mV and DC offset value to 0.9V.
   2. Then click on transient analysis.
   3. Observe the input and output waveforms.
      ![Screenshot 2025-02-18 050559](https://github.com/user-attachments/assets/50201c56-58f6-4595-8313-28a7e3a96bec)

8. AC Analysis:
   1. Go to spice directive and give the library file path for the simulator to access the data through the path .
   2. Go to simulate option in the tab , edit simulation command .
   3. Click on AC analysis and mention the time of sweep as decade , no of points as 20 and frequency as .1Hz to 1THzand click on ok.
   4. Now Run to analyze the gain and frequency response of the circuit.(.ac dec 20 .1 1T)
![Screenshot 2025-02-18 050811](https://github.com/user-attachments/assets/6bee813f-049a-4114-ae5d-8bca499988c7)

## **DC ANALYSIS:**
### For RD = 1KΩ
Set the VDD to 1.8 V and the input voltage to 0.9 V linked to the gate terminal.Choose 1K Ω.

Applying the formula, P = VI

55µ A is the ID (Drain Current).

Make sure the transistor is functioning in the saturation region, that is, VDS >= Vov, and set the W/L ratio such that it corresponds with the obtained ID value.
Vov = VGS - VTH

For the above ID value , the obtained W/L ratio is 203/180.
![Screenshot 2025-02-17 230031](https://github.com/user-attachments/assets/43c24a70-c77e-4b91-806a-be65daa84906)
To perform DC analysis select DC operating point and run the simulation.

The obtained DC operating point is (1.74 V , 55µ A).

