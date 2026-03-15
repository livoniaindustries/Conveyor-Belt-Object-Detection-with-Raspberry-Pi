# Conveyor Belt Object Detection with Raspberry Pi

This project demonstrates how to detect objects (nuts) on a conveyor belt using a camera and control a conveyor belt via a relay connected to a Raspberry Pi.

---

## Features

- Real-time object detection on a conveyor belt
- Differentiates between small and large nuts
- Automatically stops the belt when a large nut is detected
- Manual control for turning the belt on and off
- Visual feedback via camera display

---

## Hardware Requirements

- Raspberry Pi (any model with GPIO)
- Relay module for controlling the conveyor belt
- Webcam or Pi Camera
- Conveyor belt setup

---

## Software Requirements

- Python 3.x
- OpenCV
- NumPy
- RPi.GPIO
- A custom Python library to control the conveyor belt relay (`conveyor_lib`)

---

## Installation

1. Install Python 3.x and pip on your Raspberry Pi  
2. Install required Python packages: OpenCV, NumPy, and RPi.GPIO  
3. Connect your relay to a GPIO pin and attach the conveyor belt to the relay  
4. Connect your camera to the Raspberry Pi and ensure it is working  

---

## How It Works

1. The camera captures live video frames of the conveyor belt  
2. The belt region is cropped from each frame for processing  
3. Frames are converted to grayscale, and a binary threshold is applied to isolate objects  
4. Contours of the objects are detected, and their areas are calculated  
5. Objects are classified as small or large based on their contour area  
6. The belt stops automatically if a large nut is detected  
7. Manual controls allow starting or stopping the belt during operation  
8. Real-time visual feedback shows the objects, their size, and classification  

---

## Usage Instructions

1. Place the conveyor belt under the camera  
2. Run the object detection program on the Raspberry Pi  
3. Watch the belt and objects appear on the display windows  
4. Press the **ESC** key to exit the program  
5. Use manual controls to start or stop the belt if needed  

---

## Notes

- Crop coordinates and threshold values may need adjustment depending on the camera position and lighting  
- Ensure GPIO pins are correctly configured to avoid damaging the Raspberry Pi or relay
