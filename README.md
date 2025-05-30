### Smart Face Recognition System
This is a GUI-based Smart Face Recognition System built using Python, Tkinter, OpenCV, and scikit-learn. The system can:

Detect and recognize faces from images, videos, and webcam feed

Capture images for training dataset

Train a face recognition model using PCA and Logistic Regression

## 💡 Features

📷 Image-based face detection and recognition

🎥 Video file-based face recognition

🎦 Real-time face recognition using webcam

🧠 Face model training using PCA + Logistic Regression

📁 Save training images per person name

🎮 Simple and interactive Tkinter GUI

🛠️ Requirements
Install the required dependencies using pip:

       pip install opencv-python numpy pillow scikit-learn 
       
📁 Folder Structure

          project/
│
├── images/                     # Folder where captured faces will be stored
├── haarcascade_frontalface_default.xml   # Haar cascade for face detection
├── face_model.pkl              # Trained face recognition model (optional)
├── face_pca.pkl                # Trained PCA object (optional)
├── smart_face_recognition.py   # Main Python file
└── README.md                   # This file


🚀 How to Run
Capture Training Images
Run the program and select "Start Camera" under Capture Screen, then enter your name and capture images. 500 images will be saved for training.

Train the Model (optional)
You can train a model using the captured images (not included in code, but assumed to be trained externally using PCA + Logistic Regression). Save the model as face_model.pkl and PCA as face_pca.pkl.

Recognize Faces

Use Image Mode to browse and recognize faces in an image.

Use Video Mode to recognize faces in a video file.

Use Webcam Mode for real-time face recognition.

🧠 Model Training (Basic Idea)
Convert face images to grayscale and resize (e.g., 40x40 or 100x100).

Flatten the images into 1D arrays.

Apply PCA for dimensionality reduction.

Train a LogisticRegression model using the reduced data.

Save both the trained model and PCA object using joblib or pickle.

python
Copy
Edit
from sklearn.decomposition import PCA
from sklearn.linear_model import LogisticRegression
import joblib

# Assuming X_train contains flattened grayscale face images
pca = PCA(n_components=100)
X_reduced = pca.fit_transform(X_train)

model = LogisticRegression(max_iter=1000)
model.fit(X_reduced, y_train)

joblib.dump(model, 'face_model.pkl')
joblib.dump(pca, 'face_pca.pkl')
📸 Sample GUI Screens
Main Menu: Choose Image, Video, Webcam, or Capture

Image Detection: Browse an image and detect faces

Video Detection: Play and detect faces in a video

Webcam Detection: Real-time face recognition

Capture Screen: Capture 500 face images for a new user

📌 Notes
Make sure haarcascade_frontalface_default.xml is in the working directory.

You must pre-train and save the model and PCA before using recognition features.

You can improve accuracy using CNNs or modern deep learning approaches in future versions.

👨‍💻 Developed By
PAWAN YADAV

(AI Engineer) | 2025

📧 Contact: yaduvanshi2000pawan@gmail.com

📜 License
This project is provided for educational purposes only.

