# Comparative Performance Evaluation of Class AB and Folded Cascode OTAs

This project presents a comparative analysis of two widely used Operational Transconductance Amplifier (OTA) topologies — Class AB and Folded Cascode — using 180nm CMOS technology. The circuits were simulated using LTspice XVII.
---

## 🧠 Objective

To compare the performance of Class AB and Folded Cascode OTAs in terms of:

- DC Gain
- Unity-Gain Bandwidth
- Slew Rate
- Power Consumption
- Phase Margin
- Linearity and Noise
- CMRR and PSRR

---

## 🧪 Simulations Performed
- DC Analysis
- AC Analysis
- Transient Analysis

## 🖥️ Tools Used
- LTspice XVII
- 180nm CMOS Process Library (TSMC 0.18μm)

## 📈 Key Metrics Compared
- DC Gain
- Slew Rate
- Unity Gain Bandwidth
- Power Consumption
- Noise Performance

---
## CIRCUIT:
### FOLDED CASCODE
![image](https://github.com/user-attachments/assets/e9b502ac-bbb7-47f7-abb4-76bd8c9290b3)
### CLASS AB
![image](https://github.com/user-attachments/assets/61f0fe97-1076-49bb-b79c-19b2dcb4a5ad)

---

## 📊 Summary of Results

| Parameter              | Class AB OTA         | Folded Cascode OTA       |
|------------------------|----------------------|---------------------------|
| DC Gain                | ~62 dB               | >60 dB                    |
| Unity-Gain Bandwidth   | ~8 MHz               | ~8.7 MHz                  |
| 3dB Bandwidth          | ~1.2 MHz             | ~5.5 kHz                  |
| Slew Rate              | 60 V/µs (rise)       | 8.4–40 V/µs (bias dep.)   |
| Output Swing           | Near rail-to-rail    | Wide (not rail-to-rail)   |
| Power Consumption      | ~1.22 mW             | Lower, high efficiency    |
| Input-Referred Noise   | ~38 nV/√Hz           | ~25 nV/√Hz                |
| CMRR                   | ~90 dB               | High                      |
| PSRR (VDD/VSS)         | 80 dB / 75 dB        | High                      |

---

## 🧠 Key Observations

- The **Class AB OTA** provides **faster transient response** and **high dynamic range**, making it suitable for **low-power, high-speed applications**.
- The **Folded Cascode OTA** delivers **excellent gain, input range, and noise performance**, ideal for **precision analog processing**.

---

## 🎯 Applications

### Class AB OTA:
- Switched-capacitor circuits
- Neural signal acquisition
- Audio amplifiers
- Low-voltage sensor interfaces

### Folded Cascode OTA:
- High-precision analog filters
- Low-noise front ends
- Instrumentation amplifiers
- Data acquisition systems

---

## ✍️ Authors

- **Nikitha H S** – [2023ec_nikithahs_a@nie.ac.in](mailto:2023ec_nikithahs_a@nie.ac.in)  
- **Arya B N** – [2023ec_aryabn_a@nie.ac.in](mailto:2023ec_aryabn_a@nie.ac.in)  
- **Disha N Bhushana** – [2023ec_dishanbhushana_a@nie.ac.in](mailto:2023ec_dishanbhushana_a@nie.ac.in)  
- **Nishkala** – [2023ec_nishkala_a@nie.ac.in](mailto:2023ec_nishkala_a@nie.ac.in)

---

## 📚 References

- B. Razavi, *Design of Analog CMOS Integrated Circuits*, McGraw-Hill, 2001.
- Mahapatra et al., *Design and Performance Analysis of Class-AB OTA in 180nm CMOS Technology*.
- [LTspice XVII - Analog Devices](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html)
- [Folded Cascode OTA Lecture - Texas A&M University](https://people.engr.tamu.edu/spalermo/ecen474/lecture14_ee474_folded_cascode_ota.pdf)

---
## 📃 Reference
See the full [PDF report](report/FINALLICSIMULATIONREPORT.pdf) for detailed circuit analysis and performance comparison.

