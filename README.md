# 🌕 Lunar Crater Detection using Chandrayaan-2 Imagery

This repository presents an end-to-end pipeline for detecting lunar craters using high-resolution imagery captured by ISRO’s **Chandrayaan-2** mission. Leveraging state-of-the-art deep learning techniques, this system has been evaluated on two distinct datasets: **OHRC** and **TMC-2**.

---

## 📌 Project Highlights

- 📡 **Imagery Sources:** Chandrayaan-2’s *Orbiter High Resolution Camera (OHRC)* and *Terrain Mapping Camera-2 (TMC-2)*.
- 🧠 **Detection Framework:** YOLOv11 enhanced with **ResNet101** backbone from the *Timm* library.
- 🏷️ **Annotations:** Supervised dataset curated using **Roboflow** with precise crater bounding boxes.
- 📈 **Performance:** Demonstrated high detection accuracy and strong generalization across both datasets.

---

## 🛰️ Datasets Used

| Camera | Resolution     | Tile Sizes Used |
|--------|----------------|------------------|
| OHRC   | ~0.25 m/pixel  | 304×640 px       |
| TMC-2  | ~5 m/pixel     | 79×640 px        |

- Images preprocessed to maintain aspect ratio.
- Manual bounding box annotations via Roboflow.

---

## 🧠 Model Architecture

- **Framework:** [Ultralytics YOLOv11](https://github.com/ultralytics/ultralytics)
- **Backbone:** ResNet101 (via [Timm](https://rwightman.github.io/pytorch-image-models/))
- **Custom Modifications:**
  - Integrated Timm backbone into YOLOv11.
  - Optimized for crater-like morphology and varying lunar terrain.

---

## 📊 Results

### OHRC (Epochs 0–300)

- **Precision:** 74.6%  
- **Recall:** 66.8%  
- **mAP@0.50:** 66.7%  
- **mAP@0.50:0.95:** 32.4%  

### TMC-2 (Epochs 0–150)

- **Precision:** 80.9%  
- **Recall:** 51.9%  
- **mAP@0.50:** 58.7%  
- **mAP@0.50:0.95:** 33.7%  

> These results indicate strong detection and localization performance, especially under stricter IoU thresholds.

---

## 🔗 Google Colab Notebooks

- 📘 [**OHRC Code**](<insert-colab-link-here>)
- 📙 [**TMC-2 Code**](<insert-colab-link-here>)

---

## 🚀 How to Use

```bash
git clone https://github.com/your-username/lunar-crater-detector.git
cd lunar-crater-detector
```

1. Open the appropriate Google Colab notebook (OHRC or TMC-2).
2. Run the cells to:
   - Load and visualize datasets
   - Initialize and train the YOLOv11 model
   - Evaluate and visualize results
3. Customize model or backbone settings through the Timm interface.

---

## 🧩 Future Work

- Integrate TMC-2 **elevation data** for better detection in low-contrast regions.
- Improve annotation precision using **ArcGIS Pro** for geospatial alignment.
- Experiment with **segmentation-based models** for crater rims and interiors.
- Extend the pipeline to **Martian and Mercurian** datasets.

---

## 🌌 Applications

- Automated planetary surface mapping
- Lunar surface age estimation
- Hazard planning for future lunar missions
- Geological feature extraction from high-res orbital imagery

---

## 📜 License

This project is licensed under the **MIT License**.
