👁️ Smart Face Recognition System using Machine Learning

This is a GUI-based Smart Face Recognition System built using Python, Tkinter, OpenCV, and Machine Learning techniques. It can recognize faces in images, video files, and real-time webcam feeds, and also supports capturing new training data via webcam.

🔍 Features
📷 Recognize faces in uploaded images

🎞️ Recognize faces from video files

📹 Real-time face recognition using webcam

🧠 Train and predict using PCA + Logistic Regression model

🖼️ Capture 500 images for a new user and store them in dataset

🔐 Integrated simple login system

🖥️ Interactive GUI made with Tkinter

💾 Save trained model and PCA object for future use

🛠️ Technologies Used
Python

Tkinter (GUI)

OpenCV (Computer Vision)

PIL (Image Handling)

Scikit-learn (Machine Learning)

Joblib (Model Serialization)

Haar Cascade (Face Detection)

📁 Project Structure
bash
Copy
Edit
Smart-Face-Recognition-System/
│
├── images/                              # Captured images for training (per user)
├── haarcascade_frontalface_default.xml # Haar Cascade model for face detection
├── face_model.pkl                       # Trained face recognition model
├── face_pca.pkl                         # Saved PCA object
├── app.py                               # Main application code
├── screenshots/                         # UI screenshots
│   ├── login_page.png
│   ├── main_menu.png
│   ├── image_recognition.png
├── README.md                            # Project documentation
🚀 Getting Started
1. Clone the Repository
bash
Copy
Edit
https://github.com/2000pawan/Smart-Face-Recognition-System.git
cd Smart-Face-Recognition-System
2. Install Dependencies
Ensure you have Python 3 installed. Then, install the required libraries:

bash
Copy
Edit
pip install opencv-python Pillow numpy scikit-learn joblib
3. Run the Application
bash
Copy
Edit
python app.py
4. Login Credentials
Username: admin

Password: admin

🧠 How the Model Works
The system uses:

PCA (Principal Component Analysis) for dimensionality reduction

Logistic Regression for face classification

Steps:

Captured images are converted to grayscale and resized.

PCA reduces high-dimensional face vectors.

Logistic Regression predicts the identity.

face_model.pkl and face_pca.pkl contain the trained classifier and PCA transformer.

To train your own model, use the Gender_Prediction.ipynb format for guidance.

🖼️ Screenshots
🔐 Login Page

🏠 Main Menu

🖼 Image Recognition Example

📦 Sample Output
For every detected face, the application displays:

A bounding box

Predicted person name

The system supports detection in:

Static images

Pre-recorded video

Real-time webcam stream

📌 Notes
Make sure haarcascade_frontalface_default.xml is in the root folder.

Pre-trained models (face_model.pkl, face_pca.pkl) must exist to use recognition features.

Capture training images using the "Capture Screen" before training a new model.

👨‍💻 Developed By
PAWAN YADAV
AI Engineer | 2025
📧 Contact: yaduvanshi2000pawan@gmail.com

📜 License
This project is licensed under the MIT License – feel free to use and modify for personal or academic purposes.

