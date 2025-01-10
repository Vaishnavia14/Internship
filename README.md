Face Recognition with Google Teachable Machine

This project demonstrates a simple implementation of face recognition using a pre-trained model from Google Teachable Machine. It is designed for beginners and runs on Python.

Overview

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

1. Search for google teachable machine
   
   
![image](https://github.com/user-attachments/assets/a5a0c240-f755-4109-8964-0711799d8777)



2.Select the link


![image](https://github.com/user-attachments/assets/5d649f98-7b87-448d-8765-8889db083182)



3.Select get Started


![Screenshot 2025-01-10 114909](https://github.com/user-attachments/assets/e135da17-82ab-4d34-84ec-3de58d6a0456)



4.Select Image Project


![image](https://github.com/user-attachments/assets/2f10bcf6-7373-4e6c-818c-fc975e0ae14f)



5.Add class names


![image](https://github.com/user-attachments/assets/ebfdaedc-1e33-4109-989f-570a735553ba)



6. Select tensorflow--opencvKeras .. download my model

    
![Screenshot 2025-01-10 115855](https://github.com/user-attachments/assets/0f3ca776-fe25-4e4d-aef8-2b0818b66867)



Running the Project


Select Download ZIP to download the project files.


Extract the ZIP file to your desired location.


make sure the keras model and labels are also in the same directory


![image](https://github.com/user-attachments/assets/f8ca2bc4-a421-44c6-91f6-a6a30327cc50)


Open the face_Recognition file ( code.py) to launch the application.


![image](https://github.com/user-attachments/assets/51e26fb1-3656-4206-80e1-4d10b963b319)


4. REQUIREMENTS:

   
PYTHON 3.9(interpreter)

The required dependencies and libraries:(THIS HAS TO BE DONE IN THE TERMINAL OF PYCHARM)

1.Install TensorFlow 2.10.0:

pip install tensorflow==2.10.0

2.Install Numpy (compatible version):

pip install numpy==1.21.6

set CUDA_VISIBLE_DEVICES=-1

3.Install OpenCV with  GUI suport

pip install opencv-python==4.5.5.64


6. FILE STRUCTURE:
   
Purpose of key files:

keras_model.h5: Pre-trained Keras model file.

labels.txt: Text file with class names for the model.

face_recognition.py: Main Python script for running the program.


9. HOW IT WORKS:

    
Workflow:

The script loads the model and labels.

Opens the default camera and captures video frames.

Each frame is resized and normalized before being passed to the model for prediction.

The predicted class and confidence score are displayed on the video feed.


11. Customization
    
How users can adapt the code:

Replace keras_model.h5 with a custom model trained for their use case.

Update labels.txt with corresponding class names.

Change the video source (e.g., use a video file instead of a camera).


13. Troubleshooting
    
Common issues and their solutions:

Camera Not Accessible: Ensure no other application is using the camera.

Model/Labels Not Found: Verify the paths to keras_model.h5 and labels.txt.

OpenCV Errors: Check if the camera is functioning properly.













