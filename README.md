# 🚦 Multilingual Traffic Sign Board Detection Using Deep Learning

This project focuses on detecting **multilingual traffic signboards** using a **YOLOv5** deep learning-based object detection approach. It is designed to support autonomous vehicle systems and smart traffic management by recognizing traffic signs in **real-time**.

---

## 📌 Project Overview

Traffic sign detection is a vital component in autonomous driving and intelligent transportation systems. This project leverages the power of **YOLOv5 (You Only Look Once)** for detecting and classifying multiple types of traffic signboards, such as:

- Left Turn
- Right Turn
- Speed Limits (60, 70)
- Stop Signs

The signs are presented in multiple Indian languages, including **Kannada** and **Hindi**, making this solution suitable for multilingual environments.

---

## 🧠 Technologies Used

- Python
- [YOLOv5](https://github.com/ultralytics/yolov5) (included as a submodule)
- OpenCV
- PyTorch
- Roboflow (for dataset annotation)
- Google Colab (for model training & prototyping)

---

## 📂 Dataset

The dataset is a custom collection of traffic signboard images in Indian languages.

### Categories:

- Turn Left (Kannada & Hindi)
- Turn Right (Kannada & Hindi)
- Stop (Kannada & Hindi)
- Speed Limit 60
- Speed Limit 70

### Structure:
siya/
├── images/
│ ├── train/
│ └── val/
├── labels/
│ ├── train/
│ └── val/
└── data.yaml

yaml

Annotations are formatted for YOLOv5 compatibility.

---

## 🚀 Getting Started

### ✅ Option 1: Clone with Submodules and Dataset

```bash
git clone --recurse-submodules https://github.com/yourusername/traffic-sign-detection.git
cd traffic-sign-detection
⚠️ Make sure to include --recurse-submodules to fetch the YOLOv5 submodule.

✅ Option 2: Open in GitHub Codespaces (Recommended)
YOLOv5 submodule is already initialized.

Dataset (siya/) is preloaded.

Dependencies are easily installed.

🛠️ Setup Instructions
1. Install Python Dependencies
bash
pip install -r requirements.txt
cd yolov5
pip install -r requirements.txt
cd ..
🔧 Option 1: Train the Model
bash

python yolov5/train.py --img 640 --batch 16 --epochs 50 --data siya/data.yaml --weights yolov5s.pt
💡 Tip: Increase --epochs to 100+ for better performance on larger datasets.

⚡ Option 2: Run Inference
Use an already trained model for testing:

bash

python yolov5/detect.py --weights yolov5/runs/train/exp/weights/best.pt --img 640 --source test_image/

