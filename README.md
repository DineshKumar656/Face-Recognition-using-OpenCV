# Face-Recognition-using-OpenCV
Face Recognition System
This repository contains a simple, yet effective, face recognition system built using Python and OpenCV. The project is split into two main components: a data collection script and a real-time face recognition application.

Features
Data Collection: Gathers a dataset of faces from a webcam.

Model Training: Trains a face recognition model using the collected data.

Real-Time Recognition: Identifies known faces and labels unknown faces in a live video feed.

Simple and Intuitive: Easy to set up and run, making it ideal for beginners learning computer vision.

Prerequisites
Before you begin, ensure you have the following installed:

Python 3.x

OpenCV

Numpy

You can install the necessary Python libraries using pip:

Bash

pip install opencv-python numpy
You will also need the Haar Cascade XML file for face detection. Download haarcascade_frontalface_default.xml and place it in the same directory as the scripts. This file is commonly available in the OpenCV library's data folder or can be found online.

How to Use
Step 1: Collect Face Data
First, you need to create a dataset of the faces you want the system to recognize.

Open the data_collector.py script.

Change the sub_data variable to the name of the person whose face you are collecting data for (e.g., 'steve').

Run the script from your terminal. It will open your webcam and start capturing 100 images of your face.

Bash

python data_collector.py
A new folder with the name you specified (e.g., datasets/steve) will be created, containing the captured images.

Repeat this process for every person you want the system to recognize.

Step 2: Train the Model
Once you have collected a dataset for all the individuals, you can train the recognition model.

Run the main script from your terminal.

Bash

python main.py
The script will load all the images from the datasets folder, train the model, and then open the webcam.

Step 3: Real-Time Recognition
After the model is trained, the webcam feed will display. The system will now:

Draw a green rectangle around known faces and display their name with a confidence score.

Draw a yellow rectangle around unknown faces and label them as "Unknown".

To exit the application at any time, press the Esc key.

File Structure
.
├── datasets/
│   ├── steve/
│   │   ├── 1.png
│   │   ├── 2.png
│   │   └── ...
│   └── jane/
│       └── ...
├── haarcascade_frontalface_default.xml
├── main.py
└── data_collector.py

demo:
<img width="1919" height="1079" alt="Screenshot 2025-09-24 195631" src="https://github.com/user-attachments/assets/43defce8-f88b-4ace-89e4-f6a618f01ebf" />
