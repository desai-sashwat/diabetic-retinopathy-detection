# Detection of Diabetic Retinopathy Using Deep Learning Techniques

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![IEEE](https://img.shields.io/badge/Publication-IEEE-blue)](https://doi.org/10.1109/AIC61668.2024.10731034)

## 📋 Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Repository Structure](#repository-structure)
- [Models Implemented](#models-implemented)
- [Results](#results)
- [Publication](#publication)
- [Setup and Installation](#setup-and-installation)
- [Usage](#usage)
- [Future Scope](#future-scope)
- [Acknowledgments](#acknowledgments)

## Project Overview
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

## Repository Structure
.
├── data
├── models
├── notebooks
│   ├── cnn
│   ├── densenet
│   └── resnet
├── results
│   ├── figures
│   └── metrics
├── src
├── LICENSE
└── README.md

## Models Implemented
This project implements and compares several deep learning models:

### 1. Convolutional Neural Network (CNN)
Three custom CNN architectures were implemented and tested:
- **CNN V3**: A basic implementation of a convolutional neural network for DR detection
- **CNN V7**: An improved CNN architecture with additional layers and optimizations
- **CNN V9-Raw**: CNN model tested on the raw (non-augmented) dataset

### 2. Dense Convolutional Network (DenseNet)
Four DenseNet experiments were conducted using pre-trained models:
- **DenseNet 121**: Tested on both augmented and raw datasets
- **DenseNet 169**: Tested on both augmented and raw datasets, with further optimization in the "-2" version

### 3. Residual Network (ResNet)
- **ResNet 50**: Implemented and tested on both augmented and raw datasets

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

## Publication
This work has been published in the IEEE 3rd World Conference on Applied Intelligence and Computing (AIC):

S. Desai and S. Dodani, "Detection of Diabetic Retinopathy Using Deep Learning Techniques," 2024 IEEE 3rd World Conference on Applied Intelligence and Computing (AIC), Gwalior, India, 2024, pp. 898-904, doi: 10.1109/AIC61668.2024.10731034

## Setup and Installation
### Prerequisites
```bash
# Clone this repository
git clone https://github.com/desai-sashwat/diabetic-retinopathy-detection.git
cd diabetic-retinopathy-detection

# Install dependencies
pip install -r requirements.txt
```

## Dataset Preparation
Due to privacy considerations, the raw dataset is not included in this repository. However, you can:
1. Use your own fundus images
2. Access publicly available DR datasets such as APTOS 2019 or EyePACS

## Usage
The project notebooks are organized into three main categories:

### CNN Models
- `notebooks/cnn/cnnv3.ipynb`: Basic CNN implementation for DR detection
- `notebooks/cnn/cnnv7.ipynb`: Improved CNN with additional layers and optimizations
- `notebooks/cnn/cnnv9-raw.ipynb`: CNN model tested on the raw dataset

### DenseNet Models
- `notebooks/densenet/densenet121-dr.ipynb`: DenseNet 121 tested on the augmented dataset
- `notebooks/densenet/densenet121-dr-raw.ipynb`: DenseNet 121 tested on the raw dataset
- `notebooks/densenet/densenet169-dr-2.ipynb`: Enhanced DenseNet 169 implementation
- `notebooks/densenet/densenet169-dr-raw.ipynb`: DenseNet 169 tested on the raw dataset

### ResNet Models
- `notebooks/resnet-50/resnet50-dr.ipynb`: ResNet 50 tested on the augmented dataset
- `notebooks/resnet-50/resnet50-dr-raw.ipynb`: ResNet 50 tested on the raw dataset

## Future Scope
Future enhancements for this project include:
- Implementing multi-class classification for DR severity grading
- Exploring attention mechanisms and transformer-based models
- Developing a web interface for real-time DR detection
- Integration with ophthalmology information systems

## Acknowledgments
- Malpani Eye Hospital And Laser Centre for providing the dataset
- IEEE for publishing our research
- The research community for developing and sharing deep learning frameworks and models
