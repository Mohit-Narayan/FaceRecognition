# Face Recognition Attendance System

## Overview
This project is a Face Recognition Attendance System built with Python, OpenCV, Flask, and scikit-learn. It allows you to register users, take attendance using face recognition, and log attendance records in CSV files.

## Features
- Register new users with webcam images
- Train a face recognition model
- Take attendance using face recognition
- Attendance records saved as CSV files
- Simple web interface

## Setup Instructions

### 1. Clone or Download the Repository
Download or clone the repository to your local machine.

### 2. Create and Activate a Python Virtual Environment
Open a terminal in the project directory and run:
```powershell
python -m venv .venv
.venv\Scripts\activate
```

### 3. Install Required Packages
Install all dependencies using the requirements file:
```powershell
pip install -r requirements.txt
```

### 4. Project Structure
```
FaceRecognitionApp/
├── app.py
├── requirements.txt
├── haarcascade_frontalface_default.xml
├── home.html
├── Attendance/
├── static/
│   └── faces/
├── templates/
│   └── home.html
└── ...
```

### 5. Run the Application
Start the Flask app:
```powershell
python app.py
```
Open your browser and go to [http://127.0.0.1:5000/](http://127.0.0.1:5000/)

### 6. Usage
- **Add New User:** Enter a name and roll number, then capture images using the webcam.
- **Train Model:** The model is trained automatically after adding a user.
- **Take Attendance:** Click the button to start face recognition and log attendance.
- **Attendance Records:** Check the `Attendance` folder for CSV logs.

### 7. Notes
- Make sure your webcam is connected and accessible.
- The Haar cascade file (`haarcascade_frontalface_default.xml`) must be present in the project directory.
- All templates (HTML files) should be in the `templates` folder.
- For best results, add multiple images per user during registration.

### 8. Troubleshooting
- If the webcam is not detected, check permissions and device connection.
- If you see errors about missing files, ensure all required files are in the correct locations.
- For Windows, use PowerShell or Command Prompt for setup commands.

## License
This project is for educational purposes.
# face-recognition-based-attendance-system  

Line 1-9: We are importing the required libraries.
Line 11-12: Defining the Flask App.
Line 15-19: Functions that return today’s date strings to use in the program ahead.
Line 22-24: Initializing VideoCapture object to access WebCam.
Line 27-34: Checking if the required folders are in place or not, If not create them.
Line 37-39: A function that calculates the number of total registered users.
Line 42-46: A function that extracts the face from an image.
Line 49-52: A function that Identifies face using ML model.
Line 55-69: A function that trains the model on all the faces available in the faces folder.
Line 72-79: A function that extracts info from today’s attendance file in the attendance folder.
Line 82-91: A function that adds the Attendance of a specific user in our today’s Attendance file.

Routing Functions:

Line 96-100: Our main page routing function.
Line 103-126: This function will run when we click on Take Attendance Button.
Line 129-160: This function will run when we add a new user.
Line 163-165: Our main function which runs the Flask App.
