# Vehicle detection,tracking and counting

## Overview
The Vehicle Detection and Speed Calculation project is a computer vision application that leverages the YOLOv8 object detection model to identify and track vehicles in a video stream. The system calculates the speed of vehicles as they cross two predefined lines on the road, providing real-time speed data and visual annotations. This project is useful for traffic monitoring, vehicle analysis, and automated traffic management systems.

## Key Features
1. **Object Detection:** Utilizes the YOLOv8 model to detect various types of vehicles (e.g., cars, trucks, motorcycles) in video frames.
2. **Vehicle Tracking:** Implements a custom tracking algorithm to maintain the identity of vehicles across multiple frames.
3. **Speed Calculation:** Measures the time it takes for vehicles to travel between two lines in the video to compute their speed in kilometers per hour.
4. **Real-time Visualization:** Annotates video frames with bounding boxes, vehicle IDs, and calculated speeds.
5. **Frame and Video Output:** Saves frames with detected vehicles and speed annotations as images and compiles them into an output video file.

## Components
1. **YOLOv8 Model:** The YOLOv8 (You Only Look Once version 8) object detection model, used to identify vehicles in video frames.
2. **Tracker Class:** A custom tracking class responsible for updating and maintaining the state of detected vehicles across frames.
3. **Video Processing:** Captures video frames, processes them to detect and track vehicles, calculates their speed, and saves the results.
4. **Annotations:** Draws bounding boxes around detected vehicles, adds speed information, and marks two reference lines (red and blue) on the video frames.

## Workflow
**Initialization:**
Load the YOLOv8 model weights.
Set up video capture and output directories.

**Processing:**
Read each frame from the video.
Use YOLOv8 to detect vehicles in the frame.
Update the tracker with the detected vehicle bounding boxes.
Calculate vehicle speeds based on their crossing time between two reference lines.

**Visualization:**
Annotate frames with bounding boxes, vehicle IDs, and calculated speeds.
Draw reference lines on the frames to indicate the points of speed calculation.
Save annotated frames and compile them into an output video.

## Applications
1. **Traffic Monitoring:** Provides real-time speed data for traffic analysis and management.
2. **Vehicle Analysis:** Useful for studying vehicle behavior, traffic flow, and congestion.
3. **Automated Systems:** Can be integrated into automated traffic control systems for better management and enforcement.
