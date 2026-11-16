# 🌊 AlertWave
### AI-Based Environmental Sound Anomaly Detection and Emergency Alert System

## 📌 Project Overview

AlertWave is an AI-powered environmental sound detection system designed to identify potentially dangerous sounds from audio recordings and microphone input.

The system uses a Convolutional Neural Network (CNN) trained on environmental audio data to classify sounds into different categories. When a potentially dangerous sound is detected, the system generates an emergency alert.

AlertWave also provides an interactive dashboard built using Gradio, allowing users to upload audio files or record sounds directly through a microphone, view detection results, and monitor sound analysis statistics.

## 🎯 Objectives

- Detect potentially dangerous environmental sounds using Artificial Intelligence.
- Classify audio into multiple environmental sound categories.
- Identify emergency-related sounds and generate alerts.
- Provide real-time audio input through microphone recording.
- Display sound detection statistics through an analytics dashboard.
- Improve environmental safety through automated sound monitoring.

## 🚨 Features

- **AI-Based Sound Detection:** Uses a trained CNN model for environmental sound classification.
- **Multiple Sound Categories:** Recognizes 10 different types of environmental sounds.
- **Audio Upload:** Allows users to upload audio recordings.
- **Microphone Recording:** Supports direct audio recording through the browser.
- **Emergency Alert Detection:** Generates an alert when selected dangerous sound categories are detected.
- **Analytics Dashboard:** Displays total recordings, alert count, non-alert count, and alert percentage.
- **Visual Analytics:** Displays a graphical representation of detected alerts.
- **Reset Functionality:** Allows users to reset the analytics history.

## 🔊 Sound Categories

The CNN model classifies audio into the following 10 categories:

| No. | Sound Category |
|---|---|
| 1 | Alarm Siren |
| 2 | Children Playing |
| 3 | Dog Bark |
| 4 | Engine |
| 5 | Footsteps |
| 6 | Glass Breaking |
| 7 | Gun Shot |
| 8 | Metro Train |
| 9 | Rain |
| 10 | Screams |

### Emergency Alert Categories

The following sounds are configured to trigger an emergency alert:

- Dog Bark
- Alarm Siren
- Screams
- Glass Breaking

Other sound categories are classified as NOT ALERT.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| TensorFlow / Keras | CNN model development and training |
| Librosa | Audio processing and feature extraction |
| NumPy | Numerical operations |
| Pandas | Dataset and metadata handling |
| Scikit-learn | Dataset splitting and model evaluation |
| Matplotlib | Visualization and analytics |
| Gradio | Interactive web dashboard |
| Google Colab | Model training and execution |

## 🧠 Model Architecture

AlertWave uses a Convolutional Neural Network (CNN) to classify environmental audio signals.

The model consists of:

1. Input Layer
2. Gaussian Noise Augmentation
3. Random Translation Augmentation
4. Convolutional Block 1 – 32 filters
5. Convolutional Block 2 – 64 filters
6. Convolutional Block 3 – 128 filters
7. Batch Normalization and ReLU Activation
8. Max Pooling Layers
9. Global Average Pooling
10. Dense Layer – 128 neurons
11. Dropout Layer – 40%
12. Softmax Output Layer – 10 classes

The model is trained using the Adam optimizer and sparse categorical cross-entropy loss function.

## ⚙️ Audio Processing

The audio preprocessing pipeline consists of:

1. Loading audio files using Librosa.
2. Converting audio to mono.
3. Resampling audio to 22,050 Hz.
4. Standardizing audio duration to 4 seconds.
5. Generating Mel Spectrograms.
6. Converting spectrograms into decibel values.
7. Normalizing the extracted features.
8. Passing the processed features to the CNN model.

**Model input configuration:**

- Sample Rate: 22,050 Hz
- Audio Duration: 4 seconds
- Mel Bands: 128
- Maximum Frames: 128
- FFT Size: 1024
- Hop Length: 512
- Input Shape: 128 × 128 × 1

## 📂 Dataset

AlertWave uses the environmental audio dataset downloaded from Zenodo.

Dataset: DATASET_AOB

Dataset download:
https://zenodo.org/records/4319802

The notebook automatically downloads the dataset ZIP file and its metadata CSV file.

## 🚀 Installation and Execution

### Step 1: Clone the Repository

```bash
git clone https://github.com/your-username/AlertWave.git
cd AlertWave
```

### Step 2: Install Dependencies

```bash
pip install numpy pandas librosa soundfile scikit-learn tensorflow matplotlib gradio
```

### Step 3: Open the Notebook

Open `NNDL_Mini_Project.ipynb` using Google Colab or Jupyter Notebook.

### Step 4: Run the Notebook

Execute the notebook cells in the following order:

1. Dataset download and setup.
2. Audio preprocessing and CNN model training.
3. Model evaluation and performance analysis.
4. Frontend debugging (optional).
5. Launch the AlertWave detection dashboard.

### Step 5: Use the Dashboard

After the model is trained and saved:

1. Upload an audio file or record audio using the microphone.
2. Click **ANALYZE SOUND**.
3. Wait for the CNN model to classify the audio.
4. View the detection result.
5. Check the analytics dashboard.
6. Click **RESET ANALYTICS** to clear the current session statistics.

## 📊 Model Evaluation

The project evaluates model performance using:

- Test Accuracy
- Test Loss
- Classification Report
- Confusion Matrix
- Class-wise Prediction Analysis
- Dog Bark vs Glass Breaking Classification Analysis

The evaluation results are generated during notebook execution.

## 📈 Expected Output

The dashboard provides:

- Predicted sound category through the CNN model.
- Top three predicted sound categories and their confidence scores in the execution output.
- Emergency alert status.
- Total number of audio recordings.
- Total number of detected alerts.
- Number of non-alert recordings.
- Alert percentage.
- Graphical alert statistics.

## 🔮 Future Enhancements

- Integrate GPS-based emergency location tracking.
- Send emergency notifications to registered contacts.
- Implement continuous real-time environmental sound monitoring.
- Add SMS and email emergency notifications.
- Improve sound detection accuracy using larger datasets.
- Introduce mobile application support.
- Add background noise reduction.
- Implement cloud-based monitoring and alert management.

## ⚠️ Disclaimer

AlertWave is an academic project prototype developed for environmental sound classification and emergency alert research.

The current implementation generates alerts based on classified sound categories. It does not yet implement GPS-based location tracking or automatic emergency notifications.

It should not be used as the sole method of emergency detection or personal safety.

## 👩‍💻 Project Information

**Project Name:** AlertWave

**Project Domain:** Artificial Intelligence and Deep Learning

**Project Type:** Mini Project

**Core Technology:** Convolutional Neural Network (CNN)

**Interface:** Gradio Web Dashboard

**Programming Language:** Python

---

⭐ If you find this project interesting, consider giving the repository a star!
