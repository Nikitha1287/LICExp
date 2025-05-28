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

---
## CIRCUIT:
### FOLDED CASCODE
![image](https://github.com/user-attachments/assets/e9b502ac-bbb7-47f7-abb4-76bd8c9290b3)
### CLASS AB
![image](https://github.com/user-attachments/assets/61f0fe97-1076-49bb-b79c-19b2dcb4a5ad)

---
## 🧪 Circuit Description

### 🔹 Class AB OTA

- **Differential Input Stage** using matched NMOS transistors and PMOS current mirrors.
- **Push-Pull Output Stage** for high slew rate and dynamic swing.
- **Common-Mode Feedback (CMFB)** ensures output symmetry.
- Applications: Battery-powered systems, neural circuits, switched-capacitor blocks.

### 🔹 Folded Cascode OTA

- Uses **folded topology** to enhance output swing and common-mode input range.
- Cascode current mirrors provide high output impedance and gain.
- Low noise, high linearity design ideal for precision analog signal paths.

---
## 📈 Key Metrics Compared
- DC Gain
- Slew Rate
- Unity Gain Bandwidth
- Power Consumption
- Noise Performance

---
## 📐 Calculations

The following equations and measurement methods were used during simulation in LTspice to extract the key performance parameters of the OTAs.

**Formula**:  
Av (dB) = 20 × log10(Vout / Vin)



**Class AB**:  
Vin = 10 mV, Vout = 1.26 V  
Av = 20 × log10(1.26 / 0.01) ≈ 62 dB



**Folded Cascode**:  
Vin = 10 mV, Vout = 1.2 V  
Av = 20 × log10(1.2 / 0.01) ≈ 61.5 dB



---

### 🔸 2. Unity-Gain Bandwidth (UGBW)

- **Class AB OTA**: ~8 MHz (from AC plot)
- **Folded Cascode OTA**: ~8.7 MHz

---

### 🔸 3. 3 dB Bandwidth

- **Class AB OTA**: ~1.2 MHz (gain falls to 59 dB from peak 62 dB)
- **Folded Cascode OTA**: ~5.5 kHz (gain drops by 3 dB at low frequency)

---

### 🔸 4. Slew Rate (SR)

**Formula**:  
SR = ΔVout / Δt


**Class AB OTA** (rising):  
ΔVout = 1.2 V, Δt = 20 ns  
SR ≈ 60 V/µs


**Folded Cascode OTA**:  
ΔVout = 0.84 V, Δt = 100 ns  
SR ≈ 8.4 V/µs (can go up to 40 V/µs with high bias current)



---

### 🔸 5. Power Consumption

**Formula**:  
P = VDD × I



**Class AB OTA**:  
VDD = 1.8 V, I = 0.68 mA  
P ≈ 1.22 mW



**Folded Cascode OTA**:  
Estimated I ≈ 0.45 mA  
P ≈ 0.81 mW



---

### 🔸 6. Input-Referred Noise

**Class AB OTA**: ~38 nV/√Hz  
**Folded Cascode OTA**: ~25 nV/√Hz (measured at 1 MHz via `.noise`)

---

### 🔸 7. PSRR / CMRR

**CMRR (Class AB)**:
- Differential gain: 62 dB  
- Common-mode gain: ~ -28 dB  
CMRR = 20 × log10(10^(62/20)/10^(-28/20)) ≈ 90 dB


**PSRR**:
- Estimated from power supply AC injection analysis.
- ~80 dB (VDD), ~75 dB (VSS) for Class AB OTA.

## 📊 Summary of Results
### CLASS AB:
![image](https://github.com/user-attachments/assets/f05b0de9-e706-4539-a385-68dd0ef80d4c)
### FOLDED CASCODE
![image](https://github.com/user-attachments/assets/f31a58f1-6cde-46b7-95ba-e8a643a9c93d)


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
## 🧠 Inference

From the LTspice simulations and performance evaluation of Class AB and Folded Cascode OTAs in 180nm CMOS technology, the following insights were obtained:

1. 🔧 **Trade-off Between Speed and Precision**  
   - Class AB OTA offers significantly higher **slew rate** (~60 V/µs rising) and faster **settling time**, making it suitable for fast-switching analog applications.
   - Folded Cascode OTA provides **higher linearity** and better **low-noise performance**, suitable for high-fidelity signal amplification.

2. ⚡ **Dynamic Range and Output Swing**  
   - Class AB OTA achieves **rail-to-rail output swing**, enhancing its suitability in low-voltage environments and maximizing signal swing within supply limits.
   - Folded Cascode OTA, though not rail-to-rail, maintains **good dynamic swing** with higher **output impedance**, ideal for precision analog stages.

3. 📉 **Bandwidth and Gain Characteristics**  
   - Both architectures achieve comparable **unity-gain bandwidths** (~8–8.7 MHz), but Class AB has a wider 3 dB bandwidth (~1.2 MHz) compared to Folded Cascode’s (~5.5 kHz), emphasizing its higher bandwidth efficiency.
   - Folded Cascode OTA maintains high gain across a narrower frequency range, offering better signal integrity at low frequencies.

4. 🔋 **Power and Biasing Efficiency**  
   - Class AB OTA consumes slightly more power (~1.22 mW), primarily due to its push-pull output stage. This power is efficiently used for achieving high-speed operation.
   - Folded Cascode OTA demonstrates **higher power efficiency** in low-frequency analog domains, especially where linearity and noise immunity are critical.

5. 🔇 **Noise and Precision**  
   - Folded Cascode OTA achieves lower **input-referred noise (~25 nV/√Hz)** compared to Class AB (~38 nV/√Hz), making it ideal for instrumentation and analog front-end circuits.
   - This noise advantage is further supported by its high **CMRR** and **PSRR**, contributing to robust signal processing under noisy or fluctuating power conditions.

6. 🔌 **CMFB and Stability**  
   - Class AB OTA utilizes **Common-Mode Feedback (CMFB)** to stabilize its output swing and maintain symmetry, especially important under process-voltage-temperature (PVT) variations.

7. 🔄 **Design Complexity vs. Flexibility**  
   - Class AB OTA involves more complex biasing and feedback networks but delivers greater **flexibility** for low-voltage and dynamic applications.
   - Folded Cascode OTA, though structurally simpler, excels in **high-gain, low-distortion scenarios** with fewer biasing constraints.

8. 🎯 **Application-Specific Superiority**  
   - Class AB OTA is favored in **battery-powered**, **real-time**, and **communication** systems requiring speed and range.
   - Folded Cascode OTA is preferred in **precision analog**, **ADC front-ends**, and **signal acquisition chains** demanding noise resilience.

These inferences provide a clear, comparative understanding of the performance domains of both OTA topologies, allowing analog designers to make architecture choices aligned with application constraints and goals.
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

