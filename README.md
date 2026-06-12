# 🌿 Deep Learning Plant Disease Detector

## Project Overview
This project is a Convolutional Neural Network (CNN) deployed via a Streamlit web application. It is designed to identify 38 different classes of plant diseases and healthy leaves from user-uploaded images. 

**Model Architecture:** Custom CNN trained on the Augmented Plant Village Dataset.
**Accuracy:** ~98% Validation Accuracy
**Deployment:** Streamlit & TensorFlow/Keras

## 🧠 Training & Development
The CNN was trained using Google Colab to leverage cloud GPU resources. 
* **Training Notebook:** [Click Here to View the Colab Notebook](INSERT_YOUR_VIEWER_LINK_HERE)
* **Log Reconstruction:** Final epoch metrics were reconstructed directly from terminal logs to generate the evaluation graphs after a runtime disconnection.
* **Production Scrubbing:** The raw development model was patched and re-serialized locally as `scrubbed_model.keras` to bypass Keras versioning conflicts (`quantization_config` errors) during Streamlit deployment.

## 🛠️ Installation & Setup (Local Environment)
### 📥 Download the Pre-Trained Model
Due to GitHub's file size limits for deep learning architectures, the trained model is hosted securely via Google Drive.
1. Download the model here: [INSERT_YOUR_DRIVE_LINK_HERE]
2. Place the downloaded `scrubbed_model.keras` file directly into the main project folder alongside `app.py`.
To run this application locally without dependency conflicts, use **Anaconda/Miniconda**.

### 1. Create a Virtual Environment
Type the following commands into your Anaconda Prompt:
`conda create -n plant_env python=3.10`
`conda activate plant_env`

### 2. Install Required Dependencies
With the environment activated, install the necessary libraries:
`pip install tensorflow streamlit pillow numpy`

### 3. Run the Application
Navigate to the project directory and execute the Streamlit server:
`streamlit run app.py`
