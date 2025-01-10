# AEC-PROJECT
---

# **Quadrature Down Converter**

This repository contains the implementation and analysis of a **Quadrature Down Converter (QDC)** for wireless communication systems, as part of the Analog Electronic Circuits course project.

## **Project Description**
The Quadrature Down Converter is a key component in modern wireless receivers such as **Bluetooth**, **Wi-Fi**, and **WLAN**. It helps in **interference mitigation** and improves communication quality by generating in-phase (I) and quadrature-phase (Q) components. These components have a phase difference of 90° and are used in **direct conversion receivers**.

### **Features**
- Implements a **Quadrature Oscillator** for generating sine and cosine signals with a phase difference of 90°.
- Uses **MOSFET-based Mixer** for down-conversion of RF signals.
- Incorporates a **Low-Pass Filter (LPF)** to isolate intermediate frequency (IF) components.
- Provides simulation and hardware implementation details.

---


## **Key Components**

### **1. Quadrature Oscillator**
- Generates two sinusoidal signals (I and Q components) at **100 kHz** with:
  - **Amplitude**: 1 V (peak-to-peak)
  - **Phase Difference**: 90°
- Simulation Results:
  - Transient waveforms
  - FFT spectrum showing signal purity

### **2. MOSFET-Based Mixer**
- Mixes input signal (\(v_{\text{in}}\)) with oscillator signals (\(v_{\text{oscI}}\) and \(v_{\text{oscQ}}\)).
- Produces down-converted IF signals.

### **3. Low-Pass Filter**
- RC filter designed with a cutoff frequency of **2 kHz**.
- Blocks high-frequency components from the mixer output.

### **4. Complete QDC Circuit**
- Integrates the oscillator, mixer, and LPF.
- Outputs I and Q signals with **90° phase difference**.

---

## **Simulations**
- **Tools**: LTSpice
- **Simulation Results**:
  - Transient analysis for oscillator, mixer, and LPF stages.
  - Frequency response and FFT plots.

---

## **Hardware Implementation**
- **Op-Amp**: LM741 for oscillator and active filter stages.
- **MOSFET**: Used as a switch in the mixer.
- **Passive Components**: Resistors, capacitors, and biasing networks.

---

## **Results Summary**
| Parameter                     | Simulated     | Measured      |
|-------------------------------|---------------|---------------|
| Oscillator Frequency          | 100 kHz       | 98.7 kHz      |
| I-phase Amplitude             | 1 V           | 800 mV        |
| Q-phase Amplitude             | 1 V           | 800 mV        |
| Input Frequency               | 100 kHz       | 100 kHz       |
| IF Frequency                  | 2 kHz         | 2 kHz         |

---

## **Acknowledgments**
- **Instructor**: Prof. Abhishek Srivastava, IIIT Hyderabad
- **References**:
  - Behzad Razavi, *Design of Analog CMOS Integrated Circuits*.
  - Sedra & Smith, *Microelectronic Circuits*.
  - IEEE Papers on Quadrature Down Conversion.

---
