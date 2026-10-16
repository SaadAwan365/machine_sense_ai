# Machine Sense AI — Motor Sound Anomaly Detection

## 📌 Project Overview

**Machine Sense AI** is an AI-powered predictive maintenance prototype designed to detect unusual motor sounds using audio signal processing and machine learning.

The project analyzes motor audio recordings, extracts meaningful audio features, and uses an **Isolation Forest anomaly detection model** to identify recordings that differ from a learned baseline.

The current prototype uses dummy motor audio collected by recording YouTube motor sounds. It demonstrates the audio-processing and anomaly-detection pipeline and will later be extended to work with real motor data and ESP32-based sensors.

## 🎯 Objectives

- Collect and organize motor audio recordings.
- Extract useful audio features from WAV files.
- Analyze sound characteristics using audio visualization.
- Train an Isolation Forest model on baseline audio samples.
- Detect and flag unusual audio recordings.
- Build a foundation for a real-time predictive maintenance system.

## ⚙️ Technologies Used

- **Python** — Core programming language
- **NumPy** — Numerical computing
- **Pandas** — Dataset management and CSV processing
- **Librosa** — Audio feature extraction
- **SoundDevice** — Audio recording
- **SoundFile** — WAV file handling
- **Matplotlib** — Data visualization
- **Scikit-learn** — Isolation Forest anomaly detection
- **Joblib** — Saving and loading the trained model
- **Jupyter Notebook** — Development and experimentation

## 🔍 Current Features

- Records 20 audio samples, each 5 seconds long.
- Saves audio recordings in WAV format at a 16 kHz sample rate.
- Stores recording timestamps and metadata in CSV format.
- Extracts 37 numerical audio features for model training.
- Visualizes audio characteristics and feature distributions.
- Trains an Isolation Forest model for anomaly detection.
- Saves the trained model for future inference.
- Tests the trained model on a new audio recording.

## 🧠 Audio Features

The current pipeline extracts features including:

- Root Mean Square (RMS) energy
- Zero-Crossing Rate (ZCR)
- Spectral Centroid
- Spectral Bandwidth
- Spectral Rolloff
- Spectral Flatness
- Mel-Frequency Cepstral Coefficients (MFCCs)

These features describe different characteristics of the audio signal and help the model identify unusual patterns.

## 📂 Project Structure

```text
Machine_Sense_AI/
├── data/
│   ├── raw/
│   │   └── machine_01/
│   │       └── healthy/
│   │           ├── audio_metadata.csv
│   │           └── *.wav
│   ├── audio_features.csv
│   ├── audio_training_results.csv
│   └── test/
│       └── new_motor.wav
├── models/
│   └── audio_isolation_forest.joblib
├── notebooks/
│   └── audio_anomaly_detection.ipynb
└── README.md
```

*Note: Large audio files and trained model artifacts may be excluded from the GitHub repository. The structure above represents the local development project.*

## 🚀 Current Results

- Audio samples collected: 20
- Duration per sample: 5 seconds
- Audio sample rate: 16,000 Hz
- Numerical feature columns used for training: 37
- Model: Isolation Forest
- Training samples flagged as anomalies: 2

These are initial prototype results, not validated fault-detection accuracy.

## 🔮 Future Improvements

- Collect real motor audio under healthy and abnormal operating conditions.
- Compare Isolation Forest with Autoencoder-based anomaly detection.
- Integrate ESP32 with current, vibration, and temperature sensors.
- Synchronize audio and sensor measurements using timestamps.
- Develop a Streamlit dashboard for monitoring motor conditions.
- Add real-time alerts for unusual machine behavior.
- Evaluate the system using independent test recordings and appropriate metrics.

## ⚠️ Current Limitations

The current dataset consists of dummy audio recorded from YouTube playback. Therefore, the model demonstrates the anomaly-detection workflow but is not yet validated for detecting real mechanical faults.

The system should not be used for industrial maintenance decisions until it has been tested and validated using representative real-world motor data.

## 👨‍💻 Project Status

**In Development — Audio Anomaly Detection Prototype**

Machine Sense AI is being developed incrementally, starting with audio collection and machine learning, followed by real sensor integration and dashboard development.
