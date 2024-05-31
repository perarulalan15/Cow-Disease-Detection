# Cow Disease Detection using YOLOv8n

This repository contains the implementation of a cow disease detection system using the YOLOv8n model. The project aims to accurately detect and classify diseases in cows from images using deep learning techniques.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Dataset](#dataset)
- [Model](#model)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Early detection of diseases in cows is crucial for maintaining herd health and productivity. This project leverages the YOLOv8n model, a state-of-the-art object detection algorithm, to identify various diseases in cows from images.

## Features

- **State-of-the-art detection**: Utilizes the YOLOv8n model for high accuracy and real-time detection.
- **Scalable**: Can be extended to detect more diseases with additional data and training.
- **User-friendly**: Easy to use and integrate into existing systems.

## Dataset

The dataset used for training and testing includes images of cows with and without diseases. Each image is annotated with bounding boxes around the diseased areas.

- **Sources**: Various publicly available datasets and collected field data.
- **Annotations**: Bounding boxes around diseased areas.

## Model

- **YOLOv8n**: The YOLO (You Only Look Once) v8n model is a neural network designed for real-time object detection. It provides a good balance between speed and accuracy.

## Installation

To set up the project, follow these steps:

1. **Clone the repository**:
    ```sh
    git clone https://github.com/yourusername/cow-disease-detection.git
    cd cow-disease-detection
    ```

2. **Set up a virtual environment**:
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. **Install the required packages**:
    ```sh
    pip install ultralytics torch torchvision torchaudio
    ```

## Usage

To use the cow disease detection system, follow these steps:

1. **Prepare your dataset**: Ensure your images are in the `data/images` directory and annotations in the `data/labels` directory.

2. **Train the model**:
    ```sh
    python train.py --data data.yaml --cfg yolov8n.yaml --weights yolov8n.pth --epochs 50
    ```

3. **Detect diseases in new images**:
    ```sh
    python detect.py --source path/to/your/image_or_folder --weights yolov8n.pth --conf 0.25
    ```

## Results

The model achieves high accuracy in detecting various cow diseases. Below are some example detections:

![Example Detection 1](examples/detection1.jpg)
![Example Detection 2](examples/detection2.jpg)

## Contributing

Contributions are welcome! Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeature`).
3. Commit your changes (`git commit -m 'Add your feature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Create a new Pull Request.
