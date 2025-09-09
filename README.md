# Prediction-of-Freezing-of-Gait
Developed a neural network-based detection system for identifying Freezing of Gait (FOG) episodes in Parkinson's Disease patients using wearable sensor data. The system provides real-time classification of FOG versus normal gait patterns, enabling healthcare providers to deliver timely therapeutic interventions.

# Prediction-of-Freezing-of-Gait (FOG)

Neural, real-time detection of **Freezing of Gait** in Parkinson’s using wearable **IMU** streams. Trained on windowed time-series; deployable as a lightweight API.

> **Research use only — not a medical device.**

## Overview
- **Model:** 1D CNN → (Bi)LSTM → sigmoid (optional attention)
- **Pipeline:** ingest → preprocess → window → train → eval → realtime
- **Imbalance:** class weights / focal loss + threshold tuning
- **Eval:** subject-wise (LOSO/k-fold) + event-level scoring

## Data (expected)
CSV per subject with IMU channels:
parkinsons_fog_dataset.csv
