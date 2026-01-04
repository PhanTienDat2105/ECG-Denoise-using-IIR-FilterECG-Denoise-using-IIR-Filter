ECG Signal Processing using IIR Filters

## 📌 Project Overview
This project is centered on the design and implementation of Infinite Impulse
Response (IIR) digital filters for processing raw electrocardiogram (ECG)
signals. The primary goal is to improve signal quality by mitigating typical
noise sources that degrade ECG recordings.

Specifically, the proposed filtering framework addresses baseline drift,
high-frequency disturbances, and power-line interference. By effectively
suppressing these noise components, the system aims to recover a cleaner
ECG signal that is suitable for accurate analysis and further biomedical
applications.


---

## ⚙️ Features & Filter Specifications
A combination of elliptic IIR filters and a notch filter is employed to
achieve efficient noise suppression while maintaining a low filter order,
making the design suitable for hardware-oriented implementation.

### 1. High-Pass Filter (HPF)
- **Filter Type:** Elliptic IIR  
- **Function:** Suppresses low-frequency components responsible for baseline
  drift caused by respiration and slow body movements.
- **Design Rationale:** The elliptic structure enables a sharp cutoff,
  ensuring baseline correction without degrading important ECG features.

### 2. Low-Pass Filter (LPF)
- **Filter Type:** Elliptic IIR  
- **Function:** Reduces unwanted high-frequency noise such as muscle activity
  (EMG) and sensor-related disturbances.
- **Design Rationale:** Provides effective attenuation of high-frequency noise
  with a compact filter order.

### 3. Notch Filter
- **Filter Type:** IIR Notch  
- **Notch Frequency:** 50 Hz  
- **Function:** Eliminates power-line interference commonly present in ECG
  acquisition systems.

---

## 🛠 Technologies & Tools
- **Programming Languages:** MATLAB, Verilog HDL
- **Design & Verification:** MATLAB-based filter design and simulation
- **HDL Generation:** HDL Coder for translating DSP algorithms into hardware logic

---

## 📊 Results
- Baseline drift in the raw ECG signal is significantly reduced.
- High-frequency noise components are effectively smoothed.
- Power-line interference at 50 Hz is strongly attenuated.
- The processed ECG waveform clearly reveals characteristic P, QRS,
  and T components.
- Consistent behavior observed between MATLAB simulation and HDL implementation.


