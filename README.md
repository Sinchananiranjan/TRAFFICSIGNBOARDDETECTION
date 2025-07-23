MULTI LINGUAL TRAFFIC SIGN BOARD DETECTION.

🚦 Traffic Sign Board Detection Using Deep Learning
This project focuses on detecting traffic signboards using a deep learning-based object detection approach. It is designed to aid autonomous vehicle systems and smart traffic management by recognizing traffic signs in real-time.

📌 Project Overview
Traffic sign detection is a critical component in the development of autonomous driving systems. This project utilizes a YOLO-based (You Only Look Once) object detection model to detect and classify various traffic signboards, including left-turn, right-turn, speed limit, and stop signs.

🧠 Technologies Used
Python
YOLOv5 ([added as a Git submodule](https://github.com/ultralytics/yolov5))
OpenCV
PyTorch
Roboflow  (for annotation)
Google Colab

📂 Dataset
Custom dataset containing traffic signboard images.
Includes Indian road signboards such as:

Turn Left in Kannada
Turn Left in Hindi
Turn Right in Kannada 
Turn Right in Hindi
Stop in Kannada
Stop in Hindi
Speed limit 60
Speed limit 70
Images are annotated in YOLO format.

📁 Dataset Location
The training and validation data are stored inside the siya/ folder.
It contains:
Images (images/train, images/val)
Labels in YOLO format (labels/train, labels/val)
data.yaml configuration file

✅ Option 1: Clone with Submodule and Dataset
bash
Copy
Edit
git clone --recurse-submodules [https://github.com/yourusername/traffic-sign-detection.git](https://github.com/Sinchananiranjan/TRAFFICSIGNBOARDDETECTION.git)
cd traffic-sign-detection
⚠️ Make sure to use --recurse-submodules to include the YOLOv5 model.

✅ Option 2: Use GitHub Codespace (Recommended)
Open the project in GitHub Codespaces, where:
YOLOv5 submodule is already cloned.
Dataset (siya/) is uploaded.
All dependencies can be quickly installed.

🛠️ Setup Instructions
Install Python dependencies:

pip install -r requirements.txt
cd yolov5
pip install -r requirements.txt
cd ..

🔧 Option 1: Train the Model
If you want to train or fine-tune the model on the dataset in siya/, run:
python yolov5/train.py --img 640 --batch 16 --epochs 50 --data siya/data.yaml --weights yolov5s.pt
💡 You can increase the --epochs value (e.g., 100 or more) to improve accuracy depending on your system and dataset size.

⚡ Option 2: Run Inference Directly
If you don't want to train and just want to detect using existing trained weights, use:
python yolov5/detect.py --weights yolov5/runs/train/exp/weights/best.pt --img 640 --source test_image/
📂 test_image/ should contain the images or videos you want to test.

👥 Contributors
Sinchana Niranjan


