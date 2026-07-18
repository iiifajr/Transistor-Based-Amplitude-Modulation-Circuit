# 📡 Transistor-Based Amplitude Modulation (AM) Circuit (NI Multisim Simulation)

An advanced hardware-level communication system design simulating an Amplitude Modulation (AM) circuit within NI Multisim. The project leverages the unique non-linear operating properties of a BC107BP Bipolar Junction Transistor (BJT) to execute precise signal mixing, modulating a high-frequency carrier signal with a low-frequency baseband message signal, followed by a tuned passive LC resonance branch to extract a clean, modulated output envelope.

---

## 🔗 Project Resources & Drive Link

The complete architectural simulation schematic, parametric test benches, and official documentation are fully accessible via the link below:

https://drive.google.com/drive/folders/15KS2QsOVQZEwjaAfXba6VMesSm_g3Jv4

---

## 📊 Core Objectives & System Architecture

This project systematically demonstrates fundamental analog communication principles by substituting idealized mathematical multiplier blocks with real-world, transistor-level physical circuitry.

### 🎯 Key Project Milestones:
* **Non-Linear Signal Mixing:** Utilizing the active non-linear dynamic regions of a BJT to generate standard cross-product sum and difference frequencies essential for modulation.
* **Hardware-Level Filtering:** Implementing an isolated passive filter network tuned precisely to resonate at the nominal carrier frequency.
* **Transient Waveform Verification:** Conducting exhaustive time-domain simulation diagnostics using virtual oscilloscopes to verify absolute envelope tracking parameters.

---

## 🛠️ System Components & Technical Specifications

The system architecture features a robust hardware component footprint engineered for stable active biasing and frequency selectivity:

| Component | Specification / Value | Operational Function |
| :--- | :--- | :--- |
| **BC107BP Transistor** | NPN Bipolar Junction Transistor | Serves as the central active non-linear mixing and modulating element. |
| **Carrier Signal Source ($V_1$)** | $11 \text{ kHz}$ / $15 \text{ Vpk}$ | High-frequency RF signal injected directly into the active Base terminal. |
| **Message Signal Source ($V_2$)**| $1 \text{ kHz}$ / $2 \text{ Vpk}$ | Low-frequency baseband intelligence injected into the Emitter node. |
| **Tuned Inductor ($L_1$)** | $1 \text{ mH}$ | Inductive branch forming half of the high-Q parallel collector tank filter. |
| **Tuned Capacitor ($C_1$)** | $10 \text{ nF}$ | Capacitive branch working in parallel resonance with the tank inductor. |
| **Biasing Resistors** | $R_1=22\text{ kΩ}, R_2=1\text{ kΩ}, R_3=10\text{ kΩ}, R_4=6.8\text{ kΩ}$ | Fixed resistor network stabilizing transistor quiescent operating points. |

---

## 🔌 Circuit Interfacing & Theory of Operation

The circuit relies on an intentional Emitter/Collector Modulator topology to alter active device voltage gain synchronously with the baseband input:

1. **The Modulation Mechanism:** The strong carrier signal ($11 \text{ kHz}$) dynamically switches the transistor's conduction state. Concurrently, the lower-frequency message signal ($1 \text{ kHz}$) applied at the emitter systematically varies the instantaneous collector current, shaping the carrier's amplification profile into a recognizable AM envelope.
2. **The Bandpass Filtering Stage:** The parallel LC Tank filter ($L_1$ and $C_1$) is deployed directly on the collector branch to attenuate unwanted high-order harmonic distortions, effectively smoothing the output wave into a continuous analog envelope.

---

## 🚀 Virtual Verification & Screenshots

### 1. NI Multisim Advanced Simulation Workspace
Full-scale schematic layout capturing the discrete transistor biasing topology, dual-source injection lines, and localized terminal parameter values.

<img width="1649" height="889" alt="IMG_5448" src="https://github.com/user-attachments/assets/7709a570-5de7-4684-a67a-ae70b2ba4613" />


### 2. Oscilloscope Waveform Analysis (XSC1)
Time-domain transient analysis verifying successful envelope tracking where the $11 \text{ kHz}$ carrier successfully carries the amplitude variations of the $1 \text{ kHz}$ source.

<img width="1652" height="891" alt="IMG_5449" src="https://github.com/user-attachments/assets/98e9832c-86f3-43bc-85fa-493ea6f91cf3" />


---

## 🌐 Industrial & Communication Applications

The discrete architecture modeled in this simulation forms the foundational hardware baseline for several practical transmission systems:
* **Commercial AM Radio Broadcasting:** Directly scalable to low-power Medium Wave (MW) and Shortwave commercial transmitter blocks.
* **Aviation Radio Communications:** Deployed in legacy aircraft VHF communication systems due to its high immunity to localized multi-path phase fading.
* **Analog Signal Processing Labs:** Serves as a foundational educational benchmark circuit demonstrating practical non-linear RF mixing operations.

---

## 📈 Engineering Outlook & Future Enhancements

To upgrade this simulated educational architecture into a high-stability, field-deployable transmitter module, the following refinements are planned:
1. **Adding an RF Power Amplifier Stage:** Appending a Class-C power amplifier stage following the LC filter to boost transmission range and maximize power efficiency.
2. **Active Temperature Compensation:** Integrating localized thermistor networks or active current mirrors to stabilize the BJT's operating point against thermal runaway.
3. **Upgrading to an Automatic Gain Control (AGC) Loop:** Designing a secondary feedback demodulation loop to regulate baseline modulation depth dynamically, mitigating clipping distortions.

---

## 👥 Project Team & Affiliation

* **Eng. Fajr Aldajani**
  * 🔗 [GitHub Profile](https://github.com/iiifajr)

* **Eng. Zain Hani**
  * 🔗 [GitHub Profile](https://github.com/user)

---
* **Course:** Electronics
* **Affiliation:** Taif University
* **Project Status:** Completed Successfully! 🚀
