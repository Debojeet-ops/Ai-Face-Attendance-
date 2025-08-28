# Face Attendance System

An **AI-powered Face Recognition Attendance System** built using **Python, OpenCV, and pyttsx3**.
This project automates the process of **employee/student attendance marking** by detecting and recognizing faces in real-time through a webcam.

---

## Key Features

* **Employee Registration** 

  * Capture multiple face images using the webcam.
  * Stores face samples in the `dataset/` folder.
  * Saves employee details in `Employee/info.txt`.

* **Model Training** 

  * Uses **OpenCV’s LBPH (Local Binary Pattern Histogram)** face recognizer.
  * Trains a recognition model (`trainer.yml`) using the registered face samples.

* **Attendance Marking** 

  * Recognizes registered employees in real-time.
  * Marks their attendance in `attendance.csv` with timestamp.
  * Prevents duplicate attendance on the same day.

* **Voice Feedback** 

  * Speaks important system events using `pyttsx3`.
  * Example: *“Attendance marked for John Doe”*.

* **Menu Driven System** 

  * Easy-to-use **CLI menu** with options:

    1. Register New Employee
    2. Train Model
    3. Start Attendance
    4. Exit

---

## 📂 Project Structure

```
Face-Attendance-System/
│
├── dataset/                # Stores captured face samples (User.ID.X.jpg)
├── Employee/
│   └── info.txt            # Stores employee IDs and names
├── attendance.csv          # Stores attendance records
├── trainer.yml             # Trained model file (created after training)
├── face_attendance.py      # Main Python script
└── README.md               # Project documentation
```

---

##  Requirements

You’ll need the following installed on your system:

* Python **3.7+**
* OpenCV (with contrib module)
* NumPy
* pyttsx3

Install all dependencies:

```bash
pip install opencv-contrib-python numpy pyttsx3
```

---

## Usage Guide

### 1,Run the System

```bash
python face_attendance.py
```

### 2️,Main Menu Options

```
========================================
     FACE ATTENDANCE SYSTEM
========================================
1. Register New Employee
2. Train Model
3. Start Attendance
4. Exit
```

### 3️,Step by Step Workflow

1. **Register New Employee**

   * Enter a unique **numeric Employee ID** and **Name**.
   * Look into the webcam → system captures **20 face samples**.
   * Press `Q` to stop manually.
   * Data is saved in `dataset/` and `Employee/info.txt`.

2. **Train Model**

   * Trains the LBPH face recognizer using stored face images.
   * Creates `trainer.yml` (the trained model).

3. **Start Attendance**

   * Opens webcam and starts detecting faces.
   * Recognized employees are marked in `attendance.csv`.
   * Duplicate attendance for the same day is **prevented**.
   * Press `Q` to stop attendance session.

4. **Exit**

   * Closes the program safely.

---

## Attendance Format

All attendance is logged in `attendance.csv` in the format:

```
EmployeeID,Name,Timestamp
101,John Doe,2025-08-28 10:32:15
102,Jane Smith,2025-08-28 10:33:01
```
---
## 1.Installation & Setup
Clone the Repository
git clone https://github.com/Debojeet-ops/Face-Attendance-System.git
cd Face-Attendance-System

## 2️.Install Dependencies

Make sure you have Python 3.7+ installed.
Then install required libraries:

pip install opencv-contrib-python numpy pyttsx3

## 3️.Run the Program
python face_attendance.py

---

## Future Improvements

* Add **GUI (Tkinter or PyQt)** for user-friendly interface.
* Store attendance in a **database (SQLite/MySQL)** instead of CSV.
* Email/SMS notifications for attendance.
* Deploy as a **web application** using Flask/Django.

---

## Author

<h4>Debojeet Adhikari
| Passionate Python & AI Developer | Building AI-driven projects with OpenCV and Machine Learning </h4>
---

