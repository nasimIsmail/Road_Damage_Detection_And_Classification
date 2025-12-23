# Road_Damage_Detection_And_Classification

## 1. Problem Definition
Road surface damage such as cracks and potholes can negatively affect road safety and increase maintenance costs.
This project aims to automatically detect and classify road damages from images using deep learning and computer vision techniques.

The system focuses on identifying different types of road damage to support intelligent transportation systems and automated road inspection.



## 2. Dataset and Preprocessing
The project uses the *RDD2022 (Road Damage Dataset 2022)*, which contains labeled images of road damage collected from different regions.

Preprocessing steps include:
- Image resizing
- Dataset splitting into training, validation, and test sets
- Label preparation for YOLO format
- Data organization using CSV files

Dataset configuration is defined in configs/data.yaml.

---

## 3. Model Architecture and Approach
The project is based on the *YOLO (You Only Look Once)* object detection framework.

Why YOLO:
- Real-time detection capability
- High accuracy for object localization
- Suitable for road damage detection tasks

The model is trained using custom road damage classes defined in the dataset.

---

## 4. How to Run the Project
### Requirements
- Python 3.8+
- Google Colab (recommended)
- GPU support

Install required libraries:
```bash
pip install ultralytics opencv-python pillow matplotlib numpy kaggle
