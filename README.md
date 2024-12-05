# Parking Space Detection and Occupancy Monitoring System

## Overview
This project implements an automated system for parking space detection and monitoring using YOLO object detection models. The system processes video footage of parking lots to classify spaces as **vacant** or **occupied**, providing real-time feedback. 

The project uses the YOLOv5 and YOLOv8 models, showcasing their application in detecting parking spaces efficiently and accurately.

---

## Features
- Real-time parking occupancy monitoring.
- Integration with YOLOv5 and YOLOv8 for object detection.
- Vacant and occupied parking spaces visually marked on video frames.
- Automated video processing for efficient parking management.

---

## Getting Started

### Prerequisites
- Python 3.8+
- Required Python libraries:
  - `numpy`
  - `opencv-python`
  - `torch`
  - `ultralytics`
  - `pickle`

### Installation
# 1. Clone the repository:
git clone [https://github.com/your-username/parking-space-monitoring.git](https://github.com/serodula/DL_Project.git)

Usage
# 1. Training the YOLO Model
Prepare the dataset and train the model:
Train YOLOv5
python yolov5/train.py --img 640 --batch 16 --epochs 20 --data data.yaml --weights yolov5s.pt
Train YOLOv8
from ultralytics import YOLO
model = YOLO('yolov8n.pt')
model.train(data="data.yaml", epochs=10, batch=16, imgsz=640)

# 2. Inference and Parking Monitoring
Run the parking space detection and monitoring system:
from src.parking_monitor import process_video

Inputs
vid_path = "videos/input_parking_lot.mp4"
weights_path = "models/yolov8-best.pt"
output_path = "videos/output_monitoring.mp4"
pos_pickle_path = "data/CarParkPos.pkl"

Execute
process_video(vid_path, output_path, weights_path, pos_pickle_path)

# 3. Results
Processed video files with overlaid parking space statuses.
Counts of vacant and occupied spaces displayed in real-time.

# Results
YOLOv5 Demo 
YOLOv8 Demo

# Metrics
Accuracy: YOLOv8 outperformed YOLOv5 in detection precision.
Speed: YOLOv8 achieved real-time inference speeds.

# Contributing
Contributions are welcome! Please follow these steps:
Fork the repository.
Create a new branch (git checkout -b feature-branch).
Commit changes (git commit -m 'Add new feature').
Push to the branch (git push origin feature-branch).
Open a pull request.

# Acknowledgments
Ultralytics for YOLOv5 and YOLOv8.
Roboflow for dataset preparation tools.
Community contributors for open-source advancements in computer vision.
