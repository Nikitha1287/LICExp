# **Circuit1**
## **Aim:**
To perform DC, transient, and AC analyses on a CS amplifier circuit and use LT Spice to extract the different parameters involved.
## **COMPONENTS**:  
Mosfet-nmos4,pmos4,voltage sources-0.9V,1.8V, connection wires, Resistor-1k,   
## **CIRCUIT DIAGRAM**:  
 ![image](https://github.com/user-attachments/assets/bafef02b-dd43-4778-a7b7-a40f0978b64c)

## **PROCEDURE**:  
1. Create a folder named projects. Save the LTSPICE file in this folder. Save the tsmc018 library file also in the same folder.
2. Add the components according to the circuit diagram. Two voltage sources, one nMOS, a load resitor(1k).
3. Name the nMOS as CMOSN as per the library file.
4. DC ANALYSIS:
   1. Calculate the value of Id from the given power rating value. As we already the voltage value is provided.
   2. Now we define the aspects ration of the MOSFET to obtain the calculated Id value. Fix the value of length and vary the value of width(W) until we obtain the required drain current value.
   3. Check whether the mosfet is in saturation region, after defining the aspect ratio. In saturation region, 
7. 
