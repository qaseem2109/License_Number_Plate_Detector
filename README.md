# 🚘 Automatic Number Plate Recognition (ANPR) using YOLOv8 + OCR

A complete **end-to-end ANPR system** that detects vehicle license plates using **YOLOv8** and extracts readable text using **OCR**.  
Built with a focus on **accuracy, scalability, and real-world deployment readiness**.

---

## 🔍 Project Overview

This project implements a **two-stage computer vision pipeline**:

1. **License Plate Detection**  
   - Trained a custom **YOLOv8 object detection model**  
   - Detects license plates in images and videos with high precision

2. **Optical Character Recognition (OCR)**  
   - Crops detected plates
   - Extracts alphanumeric characters from plates using OCR

The system works on:
- Static images
- Video files
- Real-world noisy scenes

---

## 📌 Key Features

- ⚡ Fast and lightweight YOLOv8 inference  
- 🎯 High detection accuracy on real-world images  
- 🧠 Modular detection → OCR pipeline  
- 📷 Supports both images and videos  
- ☁️ Fully compatible with Google Colab (GPU)  
- 🧪 Clean dataset handling and reproducible training  

---

## 🚗 Dataset
```

import kagglehub

# Download latest version
path = kagglehub.dataset_download("andrewmvd/car-plate-detection")

print("Path to dataset files:", path)

```

## 🧠 Model Architecture

```text
Input Image / Video
        ↓
YOLOv8 License Plate Detector
        ↓
Bounding Box Cropping
        ↓
OCR Engine
        ↓
Extracted Plate Text
```
## 📁 Project Structure

```
license-plate-anpr/
│
├── src/
│   ├── detect.py        # YOLOv8 inference
│   ├── ocr.py           # OCR logic
│   └── pipeline.py     # Detection → OCR pipeline
│
├── notebooks/
│   └── training.ipynb  # Model training (Colab)
│
├── models/
│   └── README.md       # Download trained weights
│
├── samples/
│   ├── images/
│   └── results/
│
├── data.yaml
├── requirements.txt
├── README.md
└── .gitignore
```

## 🚀 Installation

pip install -r requirements.txt

## 🔮 Future Enhancements

🌍 Multi-country license plate formats
🎥 Real-time CCTV stream support
🧠 Improved OCR with EasyOCR / CRNN
📦 Dockerized deployment
🌐 Web dashboard (FastAPI / Streamlit)

## 👤 Author

### Muhammad Qaseem
