# Task 1 - Color Image Processing

## Overview
Load and process a color image (`pepperImage.png`) using RGB manipulation, color filtering, and intensity distribution techniques.

---

## 1. Load & Plot RGB Components

Load the image using the RGB system where the color image is represented as:

$$f(x,y) = [R(x,y),\ G(x,y),\ B(x,y)]$$

- Plot the original color image
- Plot each component $R(x,y)$, $G(x,y)$, $B(x,y)$ individually using a **grayscale map**

---

## 2. Red Component Thresholding

Apply a threshold of 180 to isolate the red channel:

$$R^*(x,y) = \begin{cases} R(x,y) & \text{if } R(x,y) > 180 \\ 0 & \text{if } R(x,y) \leq 180 \end{cases}$$

$$G^*(x,y) = 0, \quad B^*(x,y) = 0$$

Plot the modified image $f^*(x,y) = [R^*(x,y),\ G^*(x,y),\ B^*(x,y)]$

---

## 3. Extract Reddish Peppers Only

Extend the thresholding approach from Step 2 by combining RGB conditions to filter out non-red objects (garlic, yellow peppers, etc.), leaving only **reddish peppers and chili peppers** visible.

---

## 4. Histogram Equalization

1. Convert to grayscale intensity $I(x,y)$ and plot its histogram
2. Apply **histogram equalization** using PDF and CDF to produce a uniformly distributed $I^*(x,y)$:

$$\text{CDF}(k) = \sum_{j=0}^{k} \text{PDF}(j), \quad I^*(x,y) = \text{CDF}(I(x,y)) \times 255$$

3. Plot $I^*(x,y)$ with grayscale map and its histogram

---

## 5. Gaussian Distribution Mapping

Transform $I^*(x,y)$ so that intensity values follow a **Gaussian distribution**:

$$I^{**}(x,y) \sim \mathcal{N}(\mu,\ \sigma^2)$$

- $\mu$ and $\sigma$ are chosen experimentally
- Plot $I^{**}(x,y)$ using a grayscale map and its histogram

---

## Results

> 📷 Result images and plots are in the notebook: [`Task1.ipynb`](./Task1.ipynb)
