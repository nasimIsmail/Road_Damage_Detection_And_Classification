# Road_Damage_Detection_And_Classification

## 1. Problem Definition
Road surface damages such as cracks, potholes, and surface deformations negatively affect road safety and increase maintenance costs. Manual inspection is time-consuming, subjective, and inefficient at scale.
This project aims to automatically detect and classify road damages from images using deep learning and computer vision techniques. The proposed system supports intelligent transportation systems and automated road inspection by providing accurate localization and classification of road damage types.

---

## 2. Dataset and Preprocessing

### Dataset
The project uses the *RDD2022 (Road Damage Dataset 2022)*, which contains labeled road damage images collected from multiple regions under varying environmental conditions.

### Data Split
The dataset is organized into:
- Training set
- Validation set
- Test set

### Preprocessing Steps
The following preprocessing steps were applied:
- Image resizing
- Dataset splitting into train/validation/test sets
- Label preparation in YOLO format
- Data organization using CSV files

Dataset configuration is defined in:

---

## 3. Model Architecture and Approach

This project follows a *two-stage hybrid pipeline* combining object detection and classification.

### 3.1 YOLO-based Detection Module
YOLO (You Only Look Once) is used for detecting and localizing road damage regions in images.

*Why YOLO:*
- Real-time object detection capability
- High accuracy for object localization
- Suitable for large-scale road inspection tasks

The YOLO model outputs bounding boxes corresponding to detected road damage regions.

---

### 3.2 MobileNet-based Classification Module
After detection, the cropped regions of interest (ROIs) are passed to a *MobileNet-based convolutional neural network* for damage type classification.

*Why MobileNet:*
- Lightweight and computationally efficient architecture
- Low number of parameters
- Suitable for real-time and resource-constrained environments
- Strong performance on image classification tasks

The MobileNet model is fine-tuned on the road damage dataset to classify different damage categories accurately.
This hybrid detection–classification approach enables both precise localization and semantic categorization of road damages.

---

## 4. How to Run the Project

### Requirements
- Python 3.8+
- GPU support (recommended)
- Google Colab (recommended)

Install required libraries:
```bash
pip install -r requirements.txt
