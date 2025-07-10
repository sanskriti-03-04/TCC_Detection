# 🌩️ Tropical Cloud Cluster Detection using INSAT-3D IR Data

This project implements a deep learning and image processing pipeline to detect **Tropical Cloud Clusters (TCCs)** with convective characteristics using half-hourly **INSAT-3D infrared (IR) satellite data**. Convective clouds are often early indicators of severe weather systems like cyclones, and this system aims to identify them through temperature-based segmentation and contour analysis.

---

## 🌐 Use Case

This pipeline simulates a lightweight real-time tool that could assist in:
- 🌪️ Early detection of convective cloud formations
- 📡 Satellite-based weather anomaly monitoring
- 🚨 Pre-cyclone alert systems in tropical regions

---

## 🧠 Project Theory

- **INSAT-3D** is an Indian geostationary satellite capturing IR imagery at high temporal resolution.
- **Convective clouds** have cold cloud tops, and in IR imagery, colder pixels indicate potential convective activity.
- **Thresholding** is used to segment cold cloud regions.
- **Connected component analysis** identifies and localizes cloud clusters.
- **Bounding boxes** are used to visualize the spatial extent of each cluster.

---

## 🛠️ Tech Stack

| Tool | Description |
|------|-------------|
| Python | Main programming language |
| OpenCV | Image processing & contour detection |
| NumPy | Numerical analysis |
| Matplotlib | Visualization |
| Google Colab | Development platform |

--- 

## ⚙️ How It Works

Load grayscale IR satellite image

Apply temperature threshold (< 235 K) to isolate cold cloud tops

Perform binary masking and contour detection

Filter small/noisy clusters based on area

Draw bounding boxes over valid clusters

Compute metrics: cluster count, average size, brightness temp, runtime 

---

## 🚀 Future Improvements
🧠 Add ConvNet to classify convective vs non-convective clouds

🌍 Integrate elevation or flood risk maps

⏱️ Perform temporal analysis to track cluster movement over time

☁️ Build a web dashboard or REST API for real-time use 

---

## 🧪 Getting Started (Run in Colab)
To run this project:

Open the notebook: [Colab file link](https://colab.research.google.com/drive/1h7SE6Yln6xec1Y91hsqlAFhDT1uti20Z?usp=sharing)

Upload sample IR data 

Run all cells and visualize bounding boxes

No installation required if run on Colab. 

---

## 🙋‍♀️ Author
Sanskriti Kumari

Data Science & AI | Meteorological AI Systems | OpenCV + Satellite Imagery

[Connect with me on LinkedIn](https://www.linkedin.com/in/sanskriti-kumari/)

---

#### 🚀 Future Work

This project serves as a foundational system for satellite-based tropical cloud cluster detection. The following enhancements can significantly improve accuracy, scalability, and real-world applicability:

- **🧠 Integrate Deep Learning Models**  
  Replace thresholding with CNN-based segmentation (e.g., U-Net) to improve cluster classification and reduce false positives in cloudy but non-convective regions.

- **⏱️ Temporal Cloud Tracking**  
  Extend the pipeline to process time-series satellite frames to track the evolution, movement, and merging of cloud clusters.

- **🌊 Flood Risk & Geographic Overlay**  
  Incorporate flood-prone zone layers or digital elevation models (DEM) to assess the geographical risk associated with convective cloud formations.

- **🌐 Real-Time Deployment**  
  Package the system as a REST API or lightweight dashboard to allow real-time satellite stream ingestion and monitoring.

- **📡 Cross-Satellite Support**  
  Generalize the system to support other geostationary satellites (e.g., Himawari-8, GOES) for broader regional analysis.

- **📊 Cluster Severity Scoring**  
  Design a scoring model for each cluster based on area, brightness temperature, and growth rate to help rank their severity or storm potential.

- **🛰️ Multi-Channel Fusion**  
  Fuse visible, water vapor, and IR channels for richer, more accurate cloud characterization.

These future directions aim to take the system from a rule-based prototype to a fully scalable meteorological analytics tool.


