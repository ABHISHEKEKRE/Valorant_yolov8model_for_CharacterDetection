# Valorant Agent Detection Model (Instance Segmentation)

## Introduction

This project focuses on building a custom computer vision model for detecting **Valorant agents** using instance segmentation. The model is trained on a manually annotated dataset using Roboflow and implemented with YOLOv8, achieving high accuracy in identifying individual agents in game screenshots.

## Project Highlights

- **Dataset**: Curated and annotated a dataset of 600 images using Roboflow.
- **Annotations**: Labeled 8 different Valorant agents: `cypher`, `fade`, `jett`, `phoenix`, `raze`, `reyna`, `sage`, and `sova`.
- **Data Handling**: Applied over-sampling and under-sampling techniques to balance classes effectively.
- **Model**: Developed using YOLOv8 for real-time instance segmentation with strong performance.

## Features

- **Custom Dataset Annotation**: Efficient use of Roboflow for image labeling.
- **Data Augmentation**: Managed class imbalance using resampling strategies.
- **High-Accuracy Detection**: YOLOv8-based model for detecting and identifying multiple agents in a single frame.
- **Model Export**: Final trained model exported as `.pt` for deployment or inference use.

## Technology Stack

- **Language**: Python
- **Model**: YOLOv8 (Ultralytics)
- **Tools Used**: Roboflow, OpenCV, PyTorch

## Getting Started

### Prerequisites

- Python 3.8 or above
- `ultralytics` package (`pip install ultralytics`)
- Roboflow account (optional for dataset management)

### Installation

1. Clone the repository
```bash
git clone https://github.com/ABHISHEKEKRE/Valorant-Agent-Detection.git
cd Valorant-Agent-Detection
```
2. Install Dependencies
```bash
pip install -r requirements.txt
```

3.Run Inference or Training with YOLOv8
```bash
yolo task=detect mode=train model=yolov8n.pt data=data.yaml epochs=50 imgsz=640
```

### Project Structure
```
Valorant-Agent-Detection/
├── data.yaml              # Dataset configuration for YOLOv8
├── vvaloinsta.pt          # Trained YOLOv8 model file
├── README.md              # Project documentation
├── README.dataset.txt     # Notes on the dataset used
├── README.roboflow.txt    # Roboflow-specific documentation
├── requirements.txt       # Python dependencies

```

### Use Case Flow
- Image Collection → Capture Valorant gameplay screenshots
-Annotation → Use Roboflow to label agents
-Preprocessing → Apply sampling techniques for class balance
-Model Training → Train YOLOv8 with data.yaml
-Inference → Use trained .pt model to detect agents in new images

### Use Case Flow
✅ Dataset of 600 images annotated on Roboflow

✅ Balanced data with augmentation and sampling

✅ YOLOv8 model trained and evaluated

✅ Final .pt model file ready for use
