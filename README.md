Attendance Record System Using Face Recognition

This project implements an Attendance Record System that uses face recognition. The system employs a machine learning model trained using Google Teachable Machine and records attendance in a MySQL database.

Project Description

This project captures images using a webcam, detects faces using a trained model, and records attendance in a database. It ensures that each person is recognized with a certain confidence level and prevents duplicate entries using a cooldown mechanism.

The main steps include:

Face Detection: Images are captured using OpenCV.

Recognition: A pre-trained model identifies individuals.

Attendance Recording: Attendance is marked in a MySQL database.

 Features
- Face recognition using a model trained on Google Teachable Machine.
- Real-time face detection and classification using OpenCV.
- MySQL database integration for storing and updating attendance records.
- Cooldown mechanism to avoid duplicate recognition.
- Configurable confidence threshold.

 Technologies Used
- Python: Programming language for implementing the system.
- OpenCV: For capturing and processing webcam images.
- TensorFlow/Keras: For loading and using the trained face recognition model.
- MySQL: For storing attendance records.
- Google Teachable Machine: For training the face recognition model.

Training the model:
Training a model using Google's Teachable Machine is a straightforward process that allows you to create machine learning models without extensive coding knowledge. Here's how you can get started:

Step 1: Access Teachable Machine

Open your browser and visit Teachable Machine.

![image](https://github.com/user-attachments/assets/e1a41aeb-1280-4834-8814-af19b3fb2dbb)


Step 2: Choose a Project Type

![image](https://github.com/user-attachments/assets/3ddfe908-e47c-4102-8b1d-f7b3231f7281)


Select Image Project since you’re working with face recognition.

Step 3: Add Classes

![image](https://github.com/user-attachments/assets/f7cf461c-1068-4523-84b3-ab0558e4ef58)


Add more classes by clicking "Add a Class" if needed.

![image](https://github.com/user-attachments/assets/2c75aed5-67df-4b0c-bfc2-8be73392b6eb)

Step 4: Collect Images for Each Class
Use your webcam or upload images for each class:

Using Webcam:

Click "Webcam" under the desired class.

Collect images of yourself or another person by holding the button.

Take images from multiple angles (front, left, right) and in different lighting conditions.

Step 5: Train the Model

 click "Train Model".

Step 6: Test the Model

Ensure the model correctly identifies faces for each class.

Step 7: Export the Model

Click "Export Model".

![image](https://github.com/user-attachments/assets/7549905b-44a5-4f2f-8680-58de0e3a13a3)

Choose the TensorFlow tab (for integration with Python).

Step 8: Integrate the Model into Your Code

Place keras_model.h5 and labels.txt in your project directory.

Modify the code to load the model and use it for face recognition.

![image](https://github.com/user-attachments/assets/cfb465b5-2685-494f-9867-dcc0f8a1d578)

Installation

Prerequisites
1. Python 3.7 or higher
2. MySQL database
3. Required Python libraries:
   - `opencv-python`
   - `numpy`
   - `tensorflow`
   - `mysql-connector-python`

 Setup Steps

Install dependencies:

   bash
   pip install -r requirements.txt
   
![image](https://github.com/user-attachments/assets/8f59c831-dc30-46ae-b4ab-f444c4ca5d32)

 Create and configure the MySQL database:
   - Create a database named `attendance_system`.
   - Use the following SQL to create a table:

     sql
     CREATE TABLE attendance (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    count INT DEFAULT 0
);
     );

![image](https://github.com/user-attachments/assets/f73e9a2e-feff-44b7-8abc-e176f8d1bde7)

 Place the following files in the project directory:
   - `keras_model.h5` (Trained model file)
   - `labels.txt` (Labels corresponding to the trained model)

Usage
1.Run the script:
```bash
python attendance_system.py
```
2.The system will:

•Open a webcam window to detect and recognize faces.

![image](https://github.com/user-attachments/assets/e2977944-7b20-4b04-bfe2-246fbfe74ec0)

•Record attendance in the database.

3.Press the ESC key to exit the program.

Database Structure

Database Name: attendance_system

Table Name: attendance

Columns:

id: Auto-incrementing unique ID for each record.

name: Name of the person recognized.

count: Number of times the person has been recognized.

Code Explaination

![image](https://github.com/user-attachments/assets/c994f49b-1910-4dd6-a0be-506b09d1ed43)

cv2:

OpenCV for capturing and processing images from the webcam.

numpy:

For array manipulation and numerical operations.

mysql.connector:

To connect and interact with a MySQL database.

tensorflow.keras.models.load_model:

For loading the trained face recognition model.

time:

For managing cooldown times between recognitions.

2. Load the Trained Model
   
![image](https://github.com/user-attachments/assets/c3b54db8-c852-4a1d-82b9-0d1d3b1ff623)
![image](https://github.com/user-attachments/assets/27918d54-5edf-4b2c-8df9-36ea0944bcda)

model:

Loads the pre-trained model created using Google Teachable Machine.

class_names:

Reads the labels associated with the model's classes from labels.txt.

3. Connect to MySQL Database
4. 
![image](https://github.com/user-attachments/assets/05438f4b-f5c8-4a0b-809e-2416ba349eb3)

conn:

Establishes a connection to the MySQL database.

c: Creates a cursor to execute SQL queries.

4. Function to Record Attendance
5. 
![image](https://github.com/user-attachments/assets/8c638503-ced3-467b-b2c4-8762f6a3f97e)

record_attendance(name):

Updates the attendance database.

If the name exists:

Increments the attendance count by 1.

If the name does not exist:

Inserts a new record with an initial count of 1.

conn.commit():

Ensures the changes are saved to the database.

Error Handling:

Catches and logs any database errors.

5. Initialize Webcam
   
![image](https://github.com/user-attachments/assets/d513698b-b009-4272-bf02-c1ed268f34ff)

camera:

Opens the default webcam (0). Change to 1 for an external webcam.

confidence_threshold:

Minimum confidence level to consider a recognition valid.

cooldown_time:

Prevents repeated attendance for the same person within a short period (3 seconds).

last_recognition_time:

Tracks the last time a person was recognized.

6. Main Loop for Face Recognition
   
![image](https://github.com/user-attachments/assets/9773f133-a276-4926-bc73-04e7129e08da)

camera.read():

Captures an image frame from the webcam.

cv2.resize():

Resizes the frame to 224x224 pixels, the required input size for the model.

cv2.imshow():

Displays the resized frame in a window titled "Webcam Image."

image_array:

Converts the image into a NumPy array and normalizes pixel values between -1 and 1 to match the model's input format.

7. Model Prediction
   
![image](https://github.com/user-attachments/assets/ee4ecf5c-0d61-4216-ae78-74e656071ef5)

model.predict(image_array):

Passes the preprocessed image to the model for prediction.

np.argmax(prediction):

Finds the class index with the highest confidence score.

class_name:

Retrieves the corresponding label from labels.txt.

confidence_score:

The confidence of the model for the predicted class.

8. Record Attendance if Confidence is High
   
![image](https://github.com/user-attachments/assets/015708a0-f0ef-4cc7-96bd-77ea2121211b)

Checks if the confidence score meets the threshold.

Ensures the cooldown time has elapsed since the last recognition of the same person.

Calls record_attendance(class_name) to update the database.

9. Exit on ESC Key

![image](https://github.com/user-attachments/assets/a9d98566-152f-4ebb-ae65-d2e3ffb93be3)

cv2.waitKey(1): Waits for a key press.

27: ASCII code for the ESC key. Breaks the loop and stops the program.

10. Cleanup
    
![image](https://github.com/user-attachments/assets/5455868c-6255-4d9e-ae6b-637e17c8ae94)

camera.release():

Releases the webcam.

cv2.destroyAllWindows():

Closes all OpenCV windows.

conn.close():

Closes the database connection.

![image](https://github.com/user-attachments/assets/a019fba8-d442-4279-ab66-db385c154d07)


![image](https://github.com/user-attachments/assets/cd9fea58-ad20-4d5e-bd9a-bd1810ffcc6c)

![image](https://github.com/user-attachments/assets/85b6154d-dbf6-43aa-91c6-4df632015e78)







