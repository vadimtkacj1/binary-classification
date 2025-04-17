# Artifact Detection in Generated Images

## Project Overview
This project implements a binary classification system to detect artifacts in AI-generated images. The system identifies various artifacts including distorted text, unnatural hands and fingers, face mask remnants, tattoos, misaligned eyes, and other visual anomalies that might appear in generated images.

## Problem Statement
AI-generated images occasionally contain undesirable artifacts that reduce their quality and usability. This project aims to automatically detect such artifacts to improve quality control in image generation pipelines.

## Solution Approach

### Data Understanding
The dataset consists of 2,000 AI-generated images split into:
- 1,800 training images
- 200 test images

Each image is labeled with either:
- Class 0: Images containing artifacts
- Class 1: Clean images without artifacts


### Implementation Details

Each model contributes to the final prediction with different weights based on their individual performance on the validation set.

#### Training Strategy
- Optimizer: Adam with learning rate scheduling
- Loss function: Binary Cross-Entropy
- Early stopping based on validation performance
- Learning rate reduction on plateau
- Gradient accumulation for stable training

#### Evaluation Metrics
- Primary metric: Micro F1 Score
- Secondary metrics: Precision, Recall, Accuracy


## Setup and Installation

### Prerequisites
- Python 3.8+
- CUDA-compatible GPU (recommended) or Mac with ARM chips
