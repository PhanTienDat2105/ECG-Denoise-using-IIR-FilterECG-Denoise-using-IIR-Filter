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
## References
Gadawe, N. T., Hamad, R. W., & Qaddoori, S. L. (2024). Realization of IIR digital filter structures for ECG denoising. *Journal Européen des Systèmes Automatisés, 57*(2), 599. https://doi.org/10.18280/jesa.570218

Jayant, H. K., Rana, K. P. S., Kumar, V., Nair, S. S., & Mishra, P. (2015). Efficient IIR notch filter design using minimax optimization for 50 Hz noise suppression in ECG. In *Proceedings of the 2015 International Conference on Signal Processing, Computing and Control (ISPCC)* (pp. 290–295). IEEE. https://doi.org/10.1109/ISPCC.2015.7375044

Manjula, N., Singh, N. P., & Babu, P. A. (2023). An efficient design of IIR filter for ECG signal classification using MATLAB. *Engineering Proceedings, 34*(1), 24. https://doi.org/10.3390/engproc2023034024

Niyama, A., Ramane, S., & Chhadwa, N. (2022). *Implementation of IIR and FIR filters in Simulink MATLAB and its application in ECG*. SSRN. https://doi.org/10.2139/ssrn.4190314


