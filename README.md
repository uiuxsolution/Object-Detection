# Real-time Object Detection with Audio Alerts

This project implements a real-time object detection system using YOLOv8 with audio feedback capabilities. It can detect various objects through your webcam and provides both visual and audio notifications, with special alerts for person detection.

## Features

- Real-time object detection using YOLOv8
- Webcam integration for live video feed
- Audio alerts when a person is detected
- Text-to-speech announcements for all detected objects
- Visual bounding boxes and labels for detected objects
- Performance optimization with frame skipping

## Prerequisites

Ensure you have Python installed on your system. This project requires Python 3.7 or higher.

## Installation

1. Clone or download this repository

2. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```

3. Download the YOLOv8 model file (yolov8n.pt) if not already present

## Files Description

- `object_detection.py`: Main script containing the object detection and alert system
- `requirements.txt`: List of Python dependencies
- `danger_warning.mp3`: Audio file for person detection alerts
- `yolov8n.pt`: YOLOv8 model weights

## Usage

1. Run the script:
   ```
   python object_detection.py
   ```

2. The program will:
   - Access your webcam
   - Display the video feed with detection boxes
   - Announce detected objects via text-to-speech
   - Play an alarm sound when a person is detected

3. Press 'q' to quit the program

## Configuration

The following parameters can be adjusted in the code:

- Frame skip rate (currently set to 2)
- Detection confidence threshold (currently 0.5)
- Alarm cooldown period (currently 3 seconds)
- Camera resolution (currently 640x480)
- FPS setting (currently 30)

## Dependencies

- opencv-python: For video capture and image processing
- ultralytics: For YOLO object detection
- numpy: For numerical operations
- playsound: For audio alerts
- pyttsx3: For text-to-speech functionality

## Notes

- Ensure your webcam is properly connected and accessible
- The system requires audio output capability for alerts and announcements
- Performance may vary based on your hardware specifications