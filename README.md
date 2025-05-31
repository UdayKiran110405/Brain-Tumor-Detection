# Brain Tumor Detection using Transfer Learning with VGG16

A deep learning system for detecting and classifying brain tumors from MRI scans using VGG16 with and without fine-tuning.
![Brain Tumor Classification](static/uploads/Screenshot%202025-04-18%20212441.png)

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Key Features](#key-features)
- [Model Architectures](#model-architectures)
- [Performance](#performance)
- [Training Progress](#training-progress)
- [Web Interface](#web-interface)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Visualizations](#visualizations)
- [License](#license)

## Overview
This project implements two approaches:
1. **Feature Extraction** (without fine-tuning)
2. **Fine-Tuning** (with partial unfreezing of VGG16)

Classifies MRI scans into:
- Glioma
- Meningioma
- Pituitary
- No tumor

## Dataset
- 3,000+ MRI scans
- 4 classes
- Multiple planes (axial, coronal, sagittal)

## Key Features
- VGG16 transfer learning
- Two training strategies
- Data augmentation
- Dropout regularization
- Performance comparison

## Model Architectures

### 1. Without Fine-Tuning
VGG16 (frozen) → Flatten → Dense(256) → Dense(4)

![Base Architecture](static/uploads/Screenshot%202025-04-18%20213308.png)

### 2. With Fine-Tuning
VGG16 (trainable) → Flatten → Dropout → Dense(128) → Dropout → Dense(4)

![Fine-Tuned Architecture](static/uploads/Screenshot%202025-04-18%20213906.png)

## Performance

### Comparative Results
| Setup               | Training Acc | Validation Acc | Test Acc |
|---------------------|--------------|----------------|----------|
| Without Fine-Tuning | 95.37%       | 92.85%         | 91.20%   |
| With Fine-Tuning    | 98.42%       | 95.94%         | 94.18%   |

![Performance Comparison](static/uploads/Screenshot%202025-04-18%20214446.png)

## Training Progress

### Without Fine-Tuning
![Training Baseline](static/uploads/Screenshot%202025-04-18%20213403.png)

### With Fine-Tuning
![Training Fine-Tuned](static/uploads/Screenshot%202025-04-18%20213924.png)

## Installation
```bash
git clone https://github.com/UdayKiran110405/Brain-Tumor-Detection.git
cd Brain-Tumor-Detection
pip install -r requirements.txt
```


## Web Interface

### Input Page
![Input Interface](static/uploads/Screenshot%202025-04-18%20214611.png)

Upload an MRI image for classification with:
- File selection dialog
- Supported format information
- Clear analyze button

### Results Page
![Results Interface](static/uploads/Screenshot%202025-04-18%20214626.png)

Displays:
- Classification from both models
- Confidence percentages
- Option to analyze another image

## Installation
```bash
git clone https://github.com/UdayKiran110405/Brain-Tumor-Detection.git
cd Brain-Tumor-Detection
pip install -r requirements.txt
```

## Usage
```bash
# Run the web application
python app.py

# Access in browser at:
http://localhost:5000
```
## Results
Fine-tuned model achieved:
- 94.18% test accuracy
- 0.1042 validation loss

![Detailed Metrics](static/uploads/Screenshot%202025-04-18%20214312.png)

## Visualizations

### MRI Planes
![Scan Planes](static/uploads/Screenshot%202025-04-18%20212441.png)

### Performance Metrics
![Metrics Table](static/uploads/Screenshot%202025-04-18%20214446.png)




