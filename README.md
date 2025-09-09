# Face Recognition Attendance System

An advanced face recognition-based attendance system built with OpenCV, face_recognition, and SVM classifier.  
The system detects and recognizes faces in real-time, tracks multiple people using Deep SORT, and marks attendance automatically into a CSV file.

## Features
- Automatic face detection and recognition
- Real-time face tracking using Deep SORT
- SVM classifier with hyperparameter tuning
- Data augmentation and preprocessing for robust training
- Stores attendance with Name, Date, and Time in CSV
- Supports multiple people in the dataset
- Saves and loads trained models (.pkl file)

## Project Structure
```
FaceRecognitionAttendance/
│── dataset/                 # Folder containing training images
│   ├── John/                # Each person has a separate folder
│   │   ├── img1.jpg
│   │   ├── img2.jpg
│   └── Mary/
│       ├── img1.jpg
│       ├── img2.jpg
│
│── index.ipynb              # Script to train the face recognition model and Main attendance system script
│── trained_face_model.pkl   # Saved trained model
│── attendance_YYYY-MM-DD.csv # Generated attendance file
│── README.md                # Project documentation
```

## Installation
1. Clone this repository:
   ```
   git clone https://github.com/Khushipatel27/face-recognition-attendance.git
   cd face-recognition-attendance
   ```

2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

## Dataset Setup
1. Create a dataset/ folder in the project directory.
2. Inside dataset/, create one subfolder per person (e.g., dataset/John/, dataset/Mary/).
3. Add at least 3–5 clear face images per person.
   Supported formats: .jpg, .jpeg, .png, .bmp
Example:
```
dataset/
├── John/
│   ├── 1.jpg
│   ├── 2.jpg
├── Mary/
│   ├── 1.jpg
│   ├── 2.jpg
```

## Training and Testing the Model
Open and run the Jupyter Notebook:
   jupyter notebook index.ipynb

This notebook includes:
- Dataset validation
- Image preprocessing and augmentation
- Training an SVM classifier with hyperparameter tuning
- Testing the model on validation data
- Saving the trained model as trained_face_model.pkl

## Running the Attendance System
Once the model is trained, open the Jupyter Notebook:
   jupyter notebook index.ipynb

- Run the second cell in the notebook to start the attendance system.
- The system will open your webcam.
- Detected and recognized faces will appear with bounding boxes.
- Attendance will be logged in attendance_YYYY-MM-DD_HH-MM-SS.csv
- Press q to quit the application.

## Output Example
Attendance file (attendance_2025-09-09_10-30-00.csv):

Name    Date        Time
John    2025-09-09  10:31:05
Mary    2025-09-09  10:32:47

## Demo Screenshot
Below is an example screenshot of the system in action:

<img width="1600" height="1262" alt="Screenshot 2025-09-09 122747" src="https://github.com/user-attachments/assets/24220bbc-267b-4c7a-97bd-b197bc1b62e2" />
<img width="1587" height="1196" alt="Screenshot 2025-09-09 123149" src="https://github.com/user-attachments/assets/51731fc8-5242-40e5-b313-f7d8c29b1507" />
<img width="1603" height="1191" alt="Screenshot 2025-09-09 123218" src="https://github.com/user-attachments/assets/f490905d-1f7a-4b30-9d9b-55ae7e22a508" />
<img width="1171" height="595" alt="Screenshot 2025-09-09 142815" src="https://github.com/user-attachments/assets/7bd6812d-db9c-40fa-889d-f9b655e559a3" />

## Future Improvements
- Add a GUI for better usability
- Integrate with a database (MySQL / MongoDB)
- Deploy on cloud for remote attendance marking
- Mobile app integration for teachers/students




