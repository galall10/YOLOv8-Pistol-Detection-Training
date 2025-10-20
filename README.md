# 🔫 YOLOv8 Pistol Detection Training

This project demonstrates how to **train a YOLOv8 model** for **pistol detection** using a **custom dataset** hosted on **Roboflow**.  
The notebook includes the full training pipeline — from dataset preparation to model evaluation and export.

---

## 📘 Overview

This notebook covers the following workflow:

1. 📦 Installing dependencies (`ultralytics`, `roboflow`, `torch`, `opencv-python`)
2. 📁 Downloading a custom **Pistol Detection Dataset** from Roboflow
3. ⚙️ Configuring YOLOv8 training parameters
4. 🧠 Training the **YOLOv8s** model with advanced augmentations
5. 💾 Exporting and saving the **best-trained weights**

---

## 🧩 Dataset

- **Source:** [Roboflow - Pistols Dataset](https://roboflow.com)  
- **Classes:** 1 (`Pistol`)  
- **Training Images:** 4,184  
- **Validation Images:** 595  

The dataset is automatically fetched through the **Roboflow API** and prepared in YOLO format.

---

## ⚙️ Training Configuration

| Parameter | Value |
|------------|--------|
| **Model** | YOLOv8s (pretrained on COCO) |
| **Epochs** | 50 |
| **Image Size** | 640×640 |
| **Optimizer** | AdamW |
| **Learning Rate** | 0.001 |
| **Augmentations** | Mosaic (0.5), Horizontal Flip (0.5), Random Erasing (0.1) |

---

## 📊 Results

| Metric | Score |
|---------|--------|
| **mAP50** | 0.918 |
| **mAP50-95** | 0.738 |
| **Precision** | 0.922 |
| **Recall** | 0.867 |

The trained YOLOv8s model demonstrates strong performance in detecting pistols with high precision and recall.

---

## 🚀 Usage

1. **Run the notebook** in [Google Colab](https://colab.research.google.com/) (recommended with a **T4 GPU**).  
2. The **dataset** will be automatically downloaded via the Roboflow API.  
3. Training progress, metrics, and validation results will be displayed and logged.  
4. The **best model weights (`best.pt`)** will be saved and available for download.

---

## 📁 Files

| File | Description |
|------|--------------|
| `pretrained_yolo_beyond.ipynb` | Main training notebook |
| `data.yaml` | Dataset configuration file |
| `best.pt` | Trained model weights (output) |

---

## 🧠 Requirements

| Package | Minimum Version |
|----------|-----------------|
| `ultralytics` | ≥ 8.3.203 |
| `torch` | ≥ 1.8.0 |
| `roboflow` | latest |
| `opencv-python` | latest |

Install all dependencies using:
```bash
pip install ultralytics torch roboflow opencv-python
