# **Circuit1**

## **AIM:**
To perform DC, transient, and AC analyses on a CS amplifier circuit and use LT Spice to extract the different parameters involved.

## **COMPONENTS:**
Mosfet-nmos4,voltage sources-0.9V,1.8V, connection wires, Resistor-1k. 

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
   5. Note down the values of DC Analysis.To perform DC analysis select DC operating point and run the simulation.
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

## **CALCULATION:**
1. ID calculation:
Applying the formula, P = VI
P=100uW,V=1.8V
ID=55.5uA
2. Gain calculation:
   Av = Vout/Vin.
From the graph of transient analysis in result,
Vout = 1.744 V
Vin = 900m V
Gain(Av) = Vout/Vin
Av = 1.744/900m
Av=1.937777777777778
## **RESULT:**
## **I. DC ANALYSIS:**
### For RD = 1KΩ
1. 55µ A is the ID (Drain Current).
2. For the above ID value , the obtained W/L ratio is 203nm/180nm.L=180nm,W=203nm
![Screenshot 2025-02-17 230031](https://github.com/user-attachments/assets/43c24a70-c77e-4b91-806a-be65daa84906)
3. The obtained DC operating point is (1.74 V , 55µ A).

## **II. TRANSIENT ANANLYSIS:**
![Screenshot 2025-02-17 232059](https://github.com/user-attachments/assets/897a3c13-1977-4248-b453-2b15598504f5)
1. There is 180 degree phase shift between input and output.
2. Gain=1.937777777777778

## **AC ANALYSIS:**
![Screenshot 2025-02-17 232518](https://github.com/user-attachments/assets/99f81b8a-4b0d-4bef-a22a-f593dd88fbfa)
Gain=4dB
## **INFERENCE:**
1. The Drain Current of the mosfet is dependent on the aspect ratio of the mosfet. It is directly proportional to the width of the mosfet and inversely proportional to the length of the mosfet.
2. Mosfet works as an amplifier only in the saturation region.
3. Gain is maximum in the mid band frequency.
4. For a single ID value, we have multiple design values.
5. While performing transient analysis, we set DC offset to 0.9V.
6. Mosfet behaves as a constant current source in the saturation region, and it produces an amplified signal across the load.

# **Circuit2**
## **AIM:**
To perform DC, transient, and AC analyses on a CS amplifier circuit and use LT Spice to extract the different parameters involved.

## **COMPONENTS:**
Mosfet-nmos4,pmos4,voltage sources-0.9V,1.8V, connection wires.

## **THEORY:**
A common source amplifier is a type of field-effect transistor (FET) amplifier that is used to boost transconductance or voltage. For single-stage FET amplifiers, it is one of the three basic topologies. How it works The input signal is sent to the gate terminal.The output signal is supplied via the drain terminal.A common source terminal is shared by the input and output.The input resistance of common source amplifiers is higher than that of equivalent CE amplifiers.has a lower gain than the equivalent CE amplifier. Capable of acting as a voltage or transconductance amplifierSource amplifiers are commonly used in amplifier circuits that require signals with very low input voltages. It is possible to use both voltage and transconductance amplifiers.
The drain current:
Id = 1/2 kn Vov2 ; Vov=Vgs-Vth and kn=un Cox W/L
**DC analysis** is used to determine the transistor's DC operating point and to make sure the mosfet is operating at saturation. By doing this, signal distortion is avoided.
This helps us to find out the exact operating point even if the other parameters vary with the surrounding environment. We fix the Load resistance value.
**Transient Analysis:** This is done to examine how the circuit reacts to signals that change over time.
This is useful for figuring out the DC shift and sign distorton between the input and the output. This is essential for identifying problems like phase distortion.For high-speed applications like communication systems, this is crucial.
**AC Analysis:** This is merely a circuit's minor signal analysis.This is done in order to ascertain the amplifier circuit's gain. It also helps in the analysis of the amplifier circuit's frequency response as well. The formula for the gain is Av = -gm Rd.

## **CIRCUIT DIAGRAM:** 
![Screenshot 2025-02-18 060437](https://github.com/user-attachments/assets/255a0d93-028c-41a5-acbf-a7e319bd1757)

## **PROCEDURE:**
1. Make a new folder called "project file."The LT spice file should be saved in this folder.
2. Initially, set the mosfet's width to 3um, its length to 180nm, and its name to CMOSN.
3. For the pmos, set the width to 3um and the length to 180nm, and call it CMOSP, as specified in the tsmc018 library.
4. DC Analysis:
    Assemble the circuit according to the schematic, making sure that all the connections are correct to ensure that the circuit is legitimate for additional analysis.
   2. Apply Vgs = 0.9 V and Vdd = 1.8 V as the DC voltages.
   3.  Navigate to the tab's "simulate" option, update the simulation command, choose "DC analysis," and then click "OK."(.op) To obtain the DC operating point, Vout, and ID, select Run from the tab menu.
     
      ![Screenshot 2025-02-18 060934](https://github.com/user-attachments/assets/6422e04d-1c23-4457-ba28-68af7778a8bf)

5. Transient Analysis:
   1. Select the advanced menu in the voltage setting option and apply a sine wave input of Vgs=0.9V with an amplitude of 50mV and frequency of 1kHz.
   2. Select "Edit Simulation Command" under "Simulate" on the tab. Then, select "Transient Analysis" and enter "3m" as the stop time.
   3. Click "OK."(.tran 3m) Run now to see how the circuit reacts to a signal that changes over time.
  ![Screenshot 2025-02-18 061743](https://github.com/user-attachments/assets/8fe879b8-3efc-4eba-9722-aa48fff48b8c)
![Screenshot 2025-02-18 061826](https://github.com/user-attachments/assets/1904c7c6-94ad-4714-99e7-adf0d45dae0b)

6. AC Analysis:
   1. Open the Spice directive and enter the location to the library file so that the simulator can access the data.
   2. Navigate to the "simulate" option in the tab, choose "edit simulation command," pick "AC analysis," enter "decade," "number of points," and "frequency" (.1Hz to 1THz), and then click "ok."
   3. Run now to examine the circuit's gain and frequency response.(.ac dec 20.1 1T).
   
![Screenshot 2025-02-18 062556](https://github.com/user-attachments/assets/75def661-6fe9-4a5b-86f7-f436d3757611)

## **CALCULATION:**
1. ID calculation:
Applying the formula, P = VI
P=100uW,V=1.8V
ID=55.5uA

## **RESULT:**
## **I. DC ANALYSIS:**
![Screenshot 2025-02-18 062314](https://github.com/user-attachments/assets/d0cb78f7-0690-48ff-b7cd-8c198e1a1b82)

![Screenshot 2025-02-18 060934](https://github.com/user-attachments/assets/e6c63e5d-9cf1-432d-b6e2-a7126267312b)


## **II. TRANSIENT ANANLYSIS:**
![Screenshot 2025-02-18 062035](https://github.com/user-attachments/assets/21a89254-24b3-4db7-89df-01da119227e2)
1. There is 180 degree phase shift between input and output, as visible in the above graph.

## **AC ANALYSIS:**
![Screenshot 2025-02-18 062651](https://github.com/user-attachments/assets/cf87ec4b-6d43-4b98-85c9-9b79e45da0a4)

1. The drain current is directly impacted by the MOSFET's width.
2. By altering the MOSFET's size -M1 -The drain current does not change significantly when the width of PMOS is changed (i.e., ID is not affected greatly). -M2-The drain current drastically changes when the NMOS width is changed.
3. An increase in width results in a larger gain.
4. PMOS functions as a resistor that is linear. Phase shift between the input and output waveforms of 5.180 degrees.
5. The gain of the CMOS amplifier is 5.5 dB.The output signal is nearly six times greater than the input signal, for example.
