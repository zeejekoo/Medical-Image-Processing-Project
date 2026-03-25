# Task 2 - B-mode Ultrasound Imaging

## Overview
Reconstruct a B-mode ultrasound image from raw RF data using beamforming and signal processing techniques.

---

## 1. Delay-and-Sum (DAS) Beamforming

Reconstruct the ultrasound signal by aligning echoes from multiple transducer elements:

$$
s(x,z) = \sum_{i=1}^{N} r_i\left(t - \tau_i(x,z)\right)
$$

- $r_i(t)$: received RF signal from the $i$-th element  
- $\tau_i(x,z)$: time delay for focusing at position $(x,z)$  
- $N$: number of transducer elements  

This step improves spatial resolution by constructive interference.

---

## 2. Hilbert Transform (Envelope Detection)

Convert the RF signal into an analytic signal:

$$
s_a(t) = s(t) + j \cdot \mathcal{H}\{s(t)\}
$$

Extract the envelope:

$$
A(t) = |s_a(t)|
$$

- $\mathcal{H}\{s(t)\}$: Hilbert transform  
- $A(t)$: amplitude (envelope) of the signal  

---

## 3. Log Compression

Compress the dynamic range for visualization:

$$
I(x,z) = 20 \log_{10}\left(\frac{A(x,z)}{A_{\max}}\right)
$$

- Enhances contrast  
- Maps large intensity variations into displayable range  

---

## 4. Scan Conversion

Convert beamformed data into Cartesian coordinates:

$$
(r,\theta) \rightarrow (x,y)
$$

- Interpolate data from polar grid to Cartesian grid  
- Generate a 2D image suitable for display  

---

## 5. Dynamic Range Adjustment

Limit intensity values for better visualization:

$$
I_{\text{final}} = \max(I(x,z),\ DR_{\text{min}})
$$

- $DR_{\text{min}}$: minimum dynamic range threshold  
- Improves visibility of soft tissues  

---

## Results

> 📷 Result images and reconstructed B-mode outputs are in the notebook: [`Task2.ipynb`](./Task2.ipynb)
