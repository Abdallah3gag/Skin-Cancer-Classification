#  Skin Cancer Classification using EfficientNet-B0

## Overview

Skin cancer is one of the most common forms of cancer worldwide, and early detection plays a crucial role in improving treatment outcomes. This project aims to classify dermoscopic skin lesion images into seven different diagnostic categories using deep learning and transfer learning techniques.

A pre-trained EfficientNet-B0 model was fine-tuned on the HAM10000 dataset to automatically recognize various types of skin lesions from medical images.

---

## Dataset

The project uses the **HAM10000 (Human Against Machine with 10000 Training Images)** dataset, which contains over 10,000 dermoscopic images of pigmented skin lesions.

### Classes

| Label | Description                   |
| ----- | ----------------------------- |
| nv    | Melanocytic Nevi              |
| mel   | Melanoma                      |
| bkl   | Benign Keratosis-like Lesions |
| bcc   | Basal Cell Carcinoma          |
| akiec | Actinic Keratoses             |
| vasc  | Vascular Lesions              |
| df    | Dermatofibroma                |

---

## Project Structure

```bash
Skin-Cancer-Classification/
│
├── data/
│   ├── HAM10000_metadata.csv
│   ├── HAM10000_images_part_1/
│   └── HAM10000_images_part_2/
│
├── notebooks/
│   └── skin_cancer_classification.ipynb
│
├── outputs/
│   ├── confusion_matrix.png
│   ├── sample_predictions.png
│   └── training_results.png
│
├── models/
│   └── efficientnet_b0_skin_cancer.pth
│
├── README.md
└── requirements.txt
```

---

## Workflow

### 1. Exploratory Data Analysis (EDA)

* Dataset inspection
* Missing value analysis
* Class distribution visualization
* Sample image visualization

### 2. Data Preprocessing

* Missing value handling
* Label encoding
* Image path generation
* Train / Validation / Test split
* Image normalization

### 3. Data Augmentation

* Random Horizontal Flip
* Random Rotation

### 4. Model Development

* Transfer Learning with EfficientNet-B0
* Modified classification layer for 7 classes
* CrossEntropy Loss
* Adam Optimizer

### 5. Model Evaluation

* Validation Accuracy
* Test Accuracy
* Confusion Matrix
* Classification Report
* Sample Prediction Visualization

---

## Model Configuration

| Parameter     | Value            |
| ------------- | ---------------- |
| Architecture  | EfficientNet-B0  |
| Framework     | PyTorch          |
| Input Size    | 224 × 224        |
| Classes       | 7                |
| Optimizer     | Adam             |
| Loss Function | CrossEntropyLoss |
| Epochs        | 30               |

---

## Results

| Metric              | Score  |
| ------------------- | ------ |
| Validation Accuracy | 86.11% |
| Test Accuracy       | 86.23% |

The model achieved strong and consistent performance on both validation and test sets. The minimal difference between the two results demonstrates good generalization ability and indicates that the model is not significantly overfitting.

---




## Conclusion

This project demonstrates the effectiveness of transfer learning for medical image classification. Using EfficientNet-B0, the model achieved **86.11% validation accuracy** and **86.23% test accuracy** on the HAM10000 dataset. The results show strong generalization performance and highlight the potential of deep learning models for assisting in skin lesion diagnosis.
