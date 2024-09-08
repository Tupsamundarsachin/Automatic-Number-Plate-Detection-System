# Automatic-Number-Plate-Detection-System





This project is a real-time system that detects vehicles and their corresponding number plates using YOLOv8 and OCR technology. The system is designed to track vehicles, accurately recognize their number plates, and store the results for further analysis. The project is implemented in Python and leverages advanced deep learning techniques for object detection, tracking, and optical character recognition (OCR).

## data

The video I used in this tutorial can be downloaded [here](https://www.pexels.com/video/traffic-flow-in-the-highway-2103099/).

## models

A Yolov8 pretrained model was used to detect vehicles.

A licensed plate detector was used to detect license plates. The model was trained with Yolov8 using [the dataset.](https://universe.roboflow.com/roboflow-universe-projects/license-plate-recognition-rxg4e/dataset/4) 



## dependencies

The sort module needs to be downloaded from [this repository.](https://github.com/abewley/sort)


## Features

Real-Time Vehicle Detection: Detects multiple types of vehicles in a video stream using YOLOv8.

Number Plate Recognition: Accurately identifies and reads number plates using EasyOCR.

Vehicle Tracking: Tracks detected vehicles across frames to maintain consistency in recognition.

Data Export: Exports detection results, including vehicle bounding boxes and number plates, to a CSV file.

Visualization: Generates annotated video output with bounding boxes and number plates overlaid.


## System Workflow

Model Loading: Load YOLOv8 models for vehicle detection and number plate recognition.

Video Processing: Read and process each frame of the input video.

Vehicle Detection: Detect vehicles and track them across frames.

Number Plate Detection: Detect number plates within the identified vehicles.

OCR and Formatting: Apply OCR to recognize the text on the number plates and format the results.

Result Storage: Save detection results, including bounding boxes and recognized text, to a CSV file.

Data Interpolation: Interpolate missing data to ensure smooth tracking results.

Visualization: Annotate and generate video output with all detected and tracked vehicles and number plates.

## Files and Directories

vehicle_plate_detection.py:
Main script for detecting vehicles and number plates, tracking them, and saving the results to a CSV file.

utils.py:
Contains utility functions for OCR processing, license plate formatting, and result storage.

visualise.py:
Script for visualizing the detection results by annotating the input video with bounding boxes and number plates.

add_missing_data.py:
Script for interpolating missing bounding box data, ensuring continuous tracking of vehicles across frames.

## Installation
Clone the Repository:

      git clone https://github.com/Tupsamundarsachin/Automatic-Number-Plate-Detection-System.git
      cd Automatic-Number-Plate-Detection-System


## Results
The detection results are stored in a CSV file, where each row corresponds to a frame in the video and contains:

Vehicle bounding box coordinates

Number plate bounding box coordinates

Recognized number plate text


The visualization script produces an annotated video that visually represents the detection and tracking results.

## Future Improvments
Enhance the number plate recognition accuracy by training a more specialized OCR model.

Extend the system to detect a wider range of vehicle types.

Optimize the system for real-time deployment on edge devices.
