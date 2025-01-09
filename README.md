Face Recognition

Real-Time Image Classification

This project uses a pre-trained Keras model to perform real-time image classification from a webcam feed.


Features

Loads a trained .h5 model and class labels from labels.txt.
Captures video from the webcam.
Resizes and normalizes video frames for model predictions.
Displays predicted class and confidence score in real-time.
Shows live video feed with an option to quit.

Setup

Install required libraries:
pip install tensorflow opencv-python numpy
Ensure the following files are available:
keras_model.h5: Pre-trained model.
labels.txt: Class labels, one per line.

How to Run

Place the files in the appropriate directory.
Run the script:
python script_name.py
Press q to exit.

Key Functions

Frame Processing: Resizes to 224x224 and normalizes to [0, 1].
Model Prediction: Identifies the class with the highest confidence.
Real-Time Display: Outputs class and confidence on the terminal and shows live video.
Requirements
Python 3.7+
Webcam

Note

Ensure the webcam is accessible and the paths to keras_model.h5 and labels.txt are correct.





