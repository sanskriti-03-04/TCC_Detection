# ⛅ Tropical Cloud Cluster Detection using INSAT-3D IR Satellite Data

**Convective Cloud Identification from Satellite Images**  
Image Processing | Remote Sensing | Python + OpenCV

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1h7SE6Yln6xec1Y91hsqlAFhDT1uti20Z?usp=sharing)

> 🔗 Click the badge above to run the full notebook with detection pipeline on Google Colab.

---

## 🚀 Overview

This project detects **tropical cloud clusters (TCCs)** with potential convective activity using **half-hourly INSAT-3D infrared satellite data**. These clusters are indicative of developing storms, and early detection can assist meteorological agencies in issuing timely warnings.

The pipeline uses **thresholding**, **connected component labeling**, and **bounding box visualization** to identify cold, dense cloud formations from raw IR frames.

---

## 🛰️ Core Features

- ✅ Loads half-hourly grayscale IR images from INSAT-3D  
- ❄️ Applies threshold-based cold cloud extraction (< 235 K)  
- 🔍 Detects and filters valid clusters using contour analysis  
- 📦 Draws bounding boxes around each detected cloud object  
- 📊 Computes real-time metrics: cluster size, count, brightness, inference time  
- 🧪 Visualizes results with Matplotlib overlays

---

## 📈 Evaluation Metrics

| Metric                     | Value (Sample Frame) |
|----------------------------|----------------------|
| 🌩️ Clusters Detected       | 12                   |
| 📐 Avg. Cluster Size       | 328.7 px²            |
| 🌡️ Brightness Temp (Mean) | 219.4 K ± 7.2        |
| ⚡ Inference Time (CPU)    | ~0.64 sec/frame      |

These results show the system is suitable for **near real-time satellite cloud cluster detection** with minimal resources.

---

## 🔍 Sample Output

Bounding boxes highlight cold cloud clusters likely associated with convective activity:

![Sample Output](example_output.png)

---

## 🧰 Tech Stack

| Tool/Library   | Purpose                         |
|----------------|----------------------------------|
| Python         | Core language                   |
| OpenCV         | Image processing & contours     |
| NumPy          | Numerical ops                   |
| Matplotlib     | Visualization                   |
| Google Colab   | Runtime and notebook interface  |

---

## 🛠️ How to Run
Click the Open in Colab badge above

Upload or load an IR image (512×512, grayscale)

Run the notebook sequentially

Visualize detected clusters and metrics

No special installation needed on Colab.

---

## 🌱 Future Work
🧠 Replace thresholding with a CNN (e.g., U-Net) for smarter segmentation

⏱️ Add multi-frame time-series tracking of cluster evolution

🌊 Integrate elevation and flood-prone zones for impact estimation

🌐 Build a dashboard or API for real-time monitoring

🛰️ Expand support to Himawari-8 or GOES IR data streams

📊 Add a severity scoring system based on cluster intensity

---

## 📄 License
MIT License
Feel free to use, adapt, or extend this project for research or academic purposes. 

---

👩‍💻 Author
Sanskriti Kumari
[LinkedIn](https://www.linkedin.com/in/sanskriti-kumari/)

