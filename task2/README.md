Task 2: B-mode Ultrasound Imaging

📌 Overview

This task focuses on reconstructing a B-mode ultrasound image from raw RF data.
The pipeline follows the standard ultrasound imaging process used in medical imaging systems.

⸻

⚙️ Processing Pipeline

The reconstruction consists of the following steps:
	1.	Delay-and-Sum (DAS) Beamforming
	•	Aligns signals from multiple transducer elements
	•	Improves signal focus and spatial resolution
	2.	Hilbert Transform
	•	Converts RF signal to analytic signal
	•	Extracts the envelope of the signal
	3.	Log Compression
	•	Compresses dynamic range for visualization
	•	Enhances contrast in the image
	4.	Scan Conversion
	•	Converts polar coordinates to Cartesian grid
	•	Produces displayable B-mode image

⸻

📂 Data Description
	•	Input: Raw RF ultrasound data
	•	Output: Reconstructed B-mode image (grayscale)

⸻

🛠️ Implementation Details
	•	Language: Python
	•	Libraries: NumPy, SciPy, Matplotlib

⸻

📊 Results

The final output is a 2D grayscale B-mode image representing tissue structures.

[👉 Open Notebook](./Task2.ipynb)
