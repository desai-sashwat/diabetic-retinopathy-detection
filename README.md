# Detection of Diabetic Retinopathy Using Deep Learning Techniques

## Overview
This project implements deep learning techniques to detect diabetic retinopathy (DR) from fundus images. Diabetic retinopathy is a severe eye condition affecting retinal blood vessels, which can lead to vision impairment or blindness if not detected and treated early. This work aims to assist ophthalmologists in diagnosing DR more efficiently and accurately.

## 📋 Table of Contents
- [Project Background](#project-background)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Results](#results)
- [Conclusion](#conclusion)
- [Publication](#publication)
- [Setup and Installation](#setup-and-installation)
- [Usage](#usage)
- [Future Scope](#future-scope)
- [Acknowledgments](#acknowledgments)

## Project Background
Diabetic Retinopathy (DR) is a prevalent microvascular complication occurring due to diabetes mellitus. It affects the blood vessels inside the retina, potentially causing vision loss or complete blindness if left untreated. Currently, doctors examine and classify the severity of DR based on manual interpretations of fundus images, which is time-consuming and labor-intensive. This project aims to automate this process using deep learning techniques.

## Dataset
The dataset used in this project consists of fundus images collected from Malpani Eye Hospital And Laser Centre in Santacruz, Mumbai, India. The dataset includes:

- **Raw Dataset**: 102 high-quality images
  - 52 fundus images of patients with varying grades of DR
  - 50 fundus images of patients with healthy retinas

- **Augmented Dataset**: 703 images created using augmentation techniques
  - 350 fundus images of patients with DR
  - 353 fundus images of patients with healthy retinas

The augmentation techniques used include:
- Horizontal Flipping
- Vertical Flipping
- Rotation
- Changing Brightness
- Shearing

## Methodology
This project implements and compares several deep learning models:

### 1. Convolutional Neural Network (CNN)
Two custom CNN architectures were designed and implemented:
- **Custom CNN 1**: A sequential model with multiple convolutional and pooling layers
- **Custom CNN 2**: A modified architecture with different filter configurations

### 2. Dense Convolutional Network (DenseNet)
Two pre-trained DenseNet variants were used:
- **DenseNet 121**: 31 MB model with dense connections between layers
- **DenseNet 169**: 55 MB model with more layers than DenseNet 121

### 3. Residual Network (ResNet)
- **ResNet 50**: Implemented with residual blocks to improve gradient flow

## Results
Performance comparison of the models:

| Model | Raw Dataset |  | Augmented Dataset |  |
| --- | --- | --- | --- | --- |
| | Training Accuracy (%) | Testing Accuracy (%) | Training Accuracy (%) | Testing Accuracy (%) |
| Custom CNN 1 | 95.9 | 87.5 | 100 | 82.08 |
| Custom CNN 2 | 100 | 87.5 | 100 | 81.13 |
| DenseNet 121 | 92.75 | 81.25 | 97.78 | 94.34 |
| DenseNet 169 | 97.14 | 93.75 | 98.97 | 97.17 |
| ResNet 50 | 67.7 | 50 | 73.95 | 72.64 |

DenseNet 169 demonstrated the best performance with a testing accuracy of 97.17% on the augmented dataset.

## Conclusion
This research successfully applied deep learning techniques to detect Diabetic Retinopathy from fundus images. The results show that DenseNet 169 outperforms other models in terms of accuracy. The augmented dataset generally produced better results than the raw dataset, highlighting the importance of data augmentation in medical imaging applications.

## Publication
This work has been published in the IEEE 3rd World Conference on Applied Intelligence and Computing (AIC):

S. Desai and S. Dodani, "Detection of Diabetic Retinopathy Using Deep Learning Techniques," 2024 IEEE 3rd World Conference on Applied Intelligence and Computing (AIC), Gwalior, India, 2024, pp. 898-904, doi: 10.1109/AIC61668.2024.10731034

## Setup and Installation
### Prerequisites
```python
# Required libraries will be listed in requirements.txt
