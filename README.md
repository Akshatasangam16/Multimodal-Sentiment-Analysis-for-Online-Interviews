Multimodal Emotion Analysis System
Streamlit App License: MIT Python

This project is an advanced, interactive web application built with Streamlit that provides multimodal emotion analysis. It analyzes human emotion from uploaded videos or live webcam streams by integrating facial emotion recognition and speech sentiment analysis to offer a holistic and detailed view of emotional state and communication congruence.

📁 Repository Contents
File	Description
final.py	The main Streamlit application script containing all logic and UI.
haarcascade_frontalface_default.xml	OpenCV's pre-trained Haar Cascade file for robust facial detection.
model_file_30epochs.zip	Archive containing the TensorFlow/Keras model (model_file_30epochs.h5) used for facial emotion classification. You must unzip this file before running the app.
README.md	This documentation file.

🚀 Key Features
Multimodal Fusion: Integrates emotion data from both visual (face) and auditory (speech/text) channels.
Comprehensive Video Analysis: Upload a video to get a detailed, frame-by-frame facial emotion distribution, Whisper transcription, DistilBERT speech emotion, and a final combined analytical report with recommendations.
Real-time Webcam Streaming: Live emotion monitoring with on-screen bounding boxes, MediaPipe facial landmarks, and an updating emotion trend chart.
Hybrid Face Detection: Supports both lightweight MediaPipe (for speed) and the heavy-duty DeepFace library (for robustness in video analysis).
Emotion Analytics Dashboard: Visualizes historical emotion data from streaming sessions using interactive Plotly charts (pie charts, timeline, and emotion transition heatmaps).

⚙️ Setup and Installation
1. Prerequisites
Python 3.8+
A decent CPU (or GPU for optimal real-time performance).
2. Prepare Model Files
The primary Keras emotion model is in a zipped format to ease cloning:

Unzip the file: Extract model_file_30epochs.zip.
Ensure the extracted file, model_file_30epochs.h5, is placed in the root directory alongside final.py and haarcascade_frontalface_default.xml.
3. Clone and Install Dependencies
Clone the repository:
git clone [https://github.com/your-username/emotion-analysis-system.git](https://github.com/your-username/emotion-analysis-system.git)
cd emotion-analysis-system
Install dependencies: The application relies on several heavyweight packages (tensorflow, mediapipe, whisper, deepface). Run the following command to install everything needed:

pip install streamlit opencv-python numpy mediapipe librosa plotly pandas Pillow whisper deepface tensorflow transformers moviepy scipy

💻 Running the Application
Execute the Streamlit application:

streamlit run final.py
Access: The application will automatically open in your web browser at http://localhost:8501.

Navigate: Use the sidebar to switch between the four operational modes: Upload Video Analysis, Webcam Emotion Detection, Live Streaming Analysis, and Emotion Analytics Dashboard.

⚠️ Important Notes
Model Caching: The application uses Streamlit's resource caching to load all large models only once, ensuring quick restarts after the initial setup.
Webcam Permissions: Ensure your browser and operating system grant access to your webcam for the real-time modes.
Audio Extraction: The video analysis mode extracts audio using MoviePy; ensure your video file has a readable audio track.
