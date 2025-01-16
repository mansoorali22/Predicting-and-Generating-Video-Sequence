# Video Prediction Model: Predicting Future Frames with Deep Learning

This repository contains the implementation of a video prediction model that generates future frames based on short input sequences from the UCF101 dataset. The project aims to predict multiple consecutive frames to create a coherent video clip, effectively simulating the continuation of an action based on a short input sequence. Applications of this project include video synthesis, animation, and scene prediction.

## Problem Statement
The primary objective is to develop a model capable of "imagining" ongoing actions in the same scene by learning motion patterns. The project includes training three different models, generating video sequences, building a user interface for visualization, and documenting the approach and findings in a detailed report.

Dataset: [UCF101 - Action Recognition Dataset](https://www.kaggle.com/datasets/matthewjansen/ucf101-action-recognition/data)

---

## Project Objectives
1. Train a deep learning model to predict multiple consecutive frames in a video sequence from the UCF101 dataset.
2. Generate a video by combining the predicted frames into a continuous sequence.
3. Develop a user interface to visualize input frames, predicted frames, and the complete video clip, including runtime inference.
4. Experiment with three different models to compare their effectiveness in generating realistic video sequences.
5. Document the approach, challenges, and results in a detailed report.

---

## Requirements

### 1. Data Preparation
- **Dataset**: Use a subset of the UCF101 dataset, focusing on actions with consistent motion (e.g., "Walking," "Jumping," "Biking").
- **Preprocessing**:
  - Resize video frames to 64x64 pixels.
  - Convert frames to grayscale or RGB to manage computational requirements.
- **Classes**: Select at least 5 classes from the dataset.

### 2. Model Development
- **Model Selection**: Implement and compare three different deep learning models:
  1. **Convolutional LSTM (ConvLSTM)**: Captures spatial-temporal patterns.
  2. **PredRNN**: Provides advanced temporal modeling.
  3. **Transformer-based Model**: Emphasizes long-term dependencies for frame generation.
- **Training**:
  - Input: A short sequence of frames (e.g., 10 frames).
  - Output: Predict the next several frames (e.g., 5-10 frames) to simulate continuous motion.

### 3. Video Generation
- Combine predicted frames into a video file using libraries like OpenCV or moviepy.
- Ensure smooth transitions from the input frames through the predicted frames.

### 4. User Interface
- Create a user interface using **Streamlit**, **Gradio**, or **Flask** to:
  - Upload or select a sample input video clip from the dataset.
  - Run each model and display the generated frames and final video clip.
  - Display runtime inference for each model, showing predictions and generated frames.

### 5. Evaluation and Reporting
- **Metrics**:
  - Mean Squared Error (MSE).
  - Structural Similarity Index (SSIM).
- **Comparative Analysis**:
  - Assess prediction quality, computational efficiency, and visual coherence for each model.
- **Documentation**:
  - Summarize results, challenges, and insights in a comprehensive report.

---