# License Plate Recognition

This project focuses on detecting and recognizing vehicle license plates from images. The pipeline first detects the location of the license plate on a vehicle and then recognizes the alphanumeric characters on the license plate.

## Table of Contents
- Overview
- Dataset Description
- Pre-requisites
- Installation
- Usage
- Training the Models
- Saving and Loading the Models
- Prediction Pipeline
- Conclusion
- Acknowledgements

## Overview

This repository contains code and resources for training and evaluating a license plate recognition system. The system performs two main tasks:
1. **License Plate Detection**: Identifying and locating license plates in images.
2. **License Plate Character Recognition**: Deciphering the alphanumeric text on the license plates.

## Dataset Description

The dataset comprises three sets:
1. **Training Set 1**: Contains 900 images of vehicles with annotated bounding boxes around the license plates.
2. **Training Set 2**: Contains 900 images of license plates with annotated alphanumeric text.
3. **Test Set**: Contains 201 images of vehicles without annotations.

The annotations are provided in CSV files:
- **Licplatesdetection_train.csv**: Contains bounding box coordinates (ymin, xmin, ymax, xmax) for the license plates.
- **Licplatesrecognition_train.csv**: Contains the characters present on each license plate.

## Pre-requisites

- Python 3.6 or higher
- TensorFlow 2.x
- OpenCV
- NumPy
- Pandas

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/thivakaran-mnm/license-plate-recognition.git
   cd license-plate-recognition
2. Install the required packages:
   ```sh
   pip install -r requirements.txt

## Usage

**Training the Models**

- Prepare the dataset by placing the images and CSV files in appropriate directories.
- Run the training script

## Saving and Loading the Models

**After training, the models are saved using the following code:**

detection_model.save('detection_model.h5')

recognition_model.save('recognition_model.h5')

**To load the saved models:**


from tensorflow.keras.models import load_model

detection_model = load_model('detection_model.h5')

recognition_model = load_model('recognition_model.h5')

## Prediction Pipeline

To predict the license plate text from a given image:

- Step 1: Detect license plate
- Step 2: Crop the license plate
- Step 3: Recognize characters

Run the detect and recongnize script

## Conclusion

In this project, we successfully built a pipeline for detecting and recognizing license plates from vehicle images. The two-stage process involves detecting the license plate using a bounding box regression model and then recognizing the alphanumeric characters using a CNN classifier. This approach can be further improved by using more advanced models or integrating end-to-end approaches like YOLO or SSD for real-time applications.

## Acknowledgements

- TensorFlow
- OpenCV
- NumPy
- Pandas
