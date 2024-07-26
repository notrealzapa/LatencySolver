# LatencySolver: Reducing Latency in NLP Models

This project aims to drastically reduce the latency of Natural Language Processing (NLP) models from approximately 4 seconds to 0.02 seconds using a combination of techniques such as model pruning, dynamic quantization, and custom lightweight architectures.

## Table of Contents
- [Introduction](#introduction)
- [Techniques Used](#techniques-used)
  - [Custom Lightweight Model](#custom-lightweight-model)
  - [Model Pruning](#model-pruning)
  - [Dynamic Quantization](#dynamic-quantization)
  - [Knowledge Distillation](#knowledge-distillation)
- [Results](#results)
- [Usage](#usage)
  - [Installation](#installation)
  - [Running the Notebook](#running-the-notebook)
- [Future Work](#future-work)
- [Contributors](#contributors)

## Introduction
LatencySolver is a project designed to optimize the performance of NLP models by significantly reducing inference latency. We achieved this by creating a custom lightweight model, applying model pruning, and using dynamic quantization. Additionally, we explored knowledge distillation to further enhance the model's efficiency.

## Techniques Used

### Custom Lightweight Model
We designed a custom lightweight model with a smaller embedding layer and convolutional layers to process input data efficiently. This model architecture reduces the computational complexity while maintaining reasonable accuracy.

### Model Pruning
Pruning involves removing less significant weights from the model. We applied unstructured pruning to the linear and convolutional layers of our custom model to reduce the number of parameters and enhance inference speed.

### Dynamic Quantization
Dynamic quantization reduces the precision of weights and biases, resulting in a faster and smaller model. This technique was applied to the pruned model to further optimize it.

### Knowledge Distillation
We used knowledge distillation to transfer knowledge from a larger, pre-trained teacher model to our custom lightweight student model. This technique helps the student model achieve better performance by learning from the teacher model's outputs.

## Results
- **Baseline Inference Time**: ~4 seconds
- **Optimized Inference Time**: ~0.02 seconds
- **Model Performance**:
  - **Training Loss**: 0.647900
  - **Validation Loss**: 0.614900
  - **Accuracy**: 0.683824
  - **F1 Score**: 0.812227

## Usage

### Installation
To use this project, clone the repository and install the required packages:
```bash
git clone https://github.com/notrealzapa/LatencySolver.git
cd LatencySolver
pip install -r requirements.txt
