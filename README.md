Face Recognition with Google Teachable Machine

This project demonstrates a simple implementation of face recognition using a pre-trained model from Google Teachable Machine. It is designed for beginners and runs on Python.

Overview:-

Google Teachable Machine provides an easy way to train and export machine learning models. In this project, we use it to recognize faces and implement the model in a Python-based application.

Features:-

Face recognition using a pre-trained model.

Integration with Google Teachable Machine.

Real-time face detection.

Requirements:-

INSTALLATION:

python 3.9

Pycharm Community Edition

Libraries: tensorflow, opencv-python, numpy

Webcam or external camera

Steps To Be Follwed:-

Search for google teachable machine

![image](https://github.com/user-attachments/assets/8c47c19a-e825-4ba4-b584-00c127c49682)


2.Select the link

![image](https://github.com/user-attachments/assets/08a20a80-11f0-4377-8345-89b6d68617f0)


3.Select get Started

![image](https://github.com/user-attachments/assets/f087b7d8-9e90-4b0d-bac4-5129fe77d402)


4.Select Image Project

![image](https://github.com/user-attachments/assets/b6450998-b249-4342-9550-cad5ec8d42fd)

5.Add class names

![image](https://github.com/user-attachments/assets/8cd09aa0-fb02-4fd2-b7e1-6010e85ebbbd)


6.Select tensorflow--opencvKeras .. download my model

![image](https://github.com/user-attachments/assets/300abe7f-5657-4857-889d-ced1bbd2122d)


Running the Project

Select Download ZIP to download the project files.

Extract the ZIP file to your desired location.

make sure the keras model and labels are also in the same directory

![image](https://github.com/user-attachments/assets/37ae82f2-d5b7-4945-adca-3951e73b4c4e)


Open the face_Recognition file ( code.py) to launch the application.

![image](https://github.com/user-attachments/assets/27d03b67-5a6a-44ce-be34-68bbae97c257)

REQUIREMENTS:
PYTHON 3.9(interpreter)

The required dependencies and libraries:(THIS HAS TO BE DONE IN THE TERMINAL OF PYCHARM)

1.Install TensorFlow 2.10.0:

pip install tensorflow==2.10.0

2.Install Numpy (compatible version):

pip install numpy==1.21.6

set CUDA_VISIBLE_DEVICES=-1

3.Install OpenCV with GUI suport

pip install opencv-python==4.5.5.64

FILE STRUCTURE:
Purpose of key files:

keras_model.h5: Pre-trained Keras model file.

labels.txt: Text file with class names for the model.

face_recognition.py: Main Python script for running the program.

HOW IT WORKS:
Workflow:

The script loads the model and labels.

Opens the default camera and captures video frames.

Each frame is resized and normalized before being passed to the model for prediction.

The predicted class and confidence score are displayed on the video feed.

Customization
How users can adapt the code:

Replace keras_model.h5 with a custom model trained for their use case.

Update labels.txt with corresponding class names.

Change the video source (e.g., use a video file instead of a camera).

Troubleshooting
Common issues and their solutions:

Camera Not Accessible: Ensure no other application is using the camera.

Model/Labels Not Found: Verify the paths to keras_model.h5 and labels.txt.

OpenCV Errors: Check if the camera is functioning properly.

install necessary libraries in the terminal

pip install mysql-connector-python

pip install tensorflow==2.10.0

pip install opencv-python==4.5.5.64

pip install numpy==1.21.6

run the code

Customize as Needed:

Edit files to fit your requirements.
Add custom branding or functionality.
Contribution
Feel free to contribute to this project by submitting a pull request or opening an issue.

