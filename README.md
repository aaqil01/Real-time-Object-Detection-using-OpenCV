# Real-time-Object-Detection-using-OpenCV

Python script utilizing OpenCV to perform real-time object detection with a pre-trained model from the COCO dataset, displaying live video feed with bounding boxes and labels.

## Overview
This Python script utilizes OpenCV to perform real-time object detection using a pre-trained deep learning model from the COCO dataset. The script captures video from the default webcam, detects objects in each frame, and overlays bounding boxes and labels for detected objects.

## Dependencies
OpenCV: 4.5.3 or later
Python: 3.x
Pre-trained Model:
Model Files: ssd_mobilenet_v3_large_coco_2020_01_14.pbtxt (configuration) and frozen_inference_graph.pb (weights)
Class Names: coco.names file containing class names corresponding to the COCO dataset.

## Setup
# 1.Installation

Install OpenCV for Python:
```
pip install opencv-python-headless
```
Ensure Python 3.x is installed.
# 2.Download Model Files

Download the pre-trained model files (ssd_mobilenet_v3_large_coco_2020_01_14.pbtxt and frozen_inference_graph.pb) from the TensorFlow Model Zoo.
# 3.Download Class Names

Download the coco.names file which contains the class names used in the COCO dataset. Ensure it is in the same directory as the script.

## Usage
# 1.Running the Script

Execute the script in your Python environment:
```
python object_detection.py
```
This will launch the webcam and display real-time object detection results.
# 2.Customization

Adjust the thres variable to change the detection threshold (default is 0.55).
Modify the video capture settings (cap.set(3,1280), cap.set(4,720), cap.set(10,70)) as needed for your webcam.

## Workflow
The script initializes the webcam using OpenCV's VideoCapture.
Loads the pre-trained model and class names from files (coco.names, ssd_mobilenet_v3_large_coco_2020_01_14.pbtxt, frozen_inference_graph.pb).
Continuously captures frames, performs object detection using the loaded model.
Draws bounding boxes and labels around detected objects on each frame.
Displays the processed frames in real-time using OpenCV's imshow and waitKey functions.

## Notes
Ensure proper lighting and camera positioning for optimal object detection performance.
Depending on your system's performance, adjust parameters such as input size and input scale (net.setInputSize, net.setInputScale) for better detection accuracy and speed.

This README file provides a comprehensive guide on setting up, running, and customizing the object detection script using OpenCV. Adjust the dependencies and instructions based on your specific environment and requirements.
