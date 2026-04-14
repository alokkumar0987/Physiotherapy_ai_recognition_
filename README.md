# 🏋️‍♂️ PhysioAI: Deep Learning Architectures for Physiotherapy Action Recognition

## 🚀 Overview

**PhysioAI** is an AI-powered system for recognizing and analyzing physiotherapy exercises using **pose estimation and deep learning architectures**.

This project is designed as a **research-driven experimental framework**, where multiple spatial-temporal models are implemented and benchmarked to understand their performance in **real-world rehabilitation scenarios**.

---

## 🎯 Objective

To systematically evaluate different deep learning approaches for human activity recognition based on:

* ⚡ Inference Latency (FPS)
* 🧠 Clinical Accuracy
* 💻 Computational Cost

📌 Goal: Build an efficient and scalable system for **AI-assisted physiotherapy monitoring**

---

## 🧠 Problem Formulation

The task is modeled as:
👉 **Multivariate Time-Series Classification / Sequence Modeling problem**

Input: Sequence of pose landmarks (frames × features)
Output: Predicted physiotherapy exercise class

---

## 🏗️ Model Architectures Explored

### 1. 🧬 Temporal Embedding + DTW (Baseline)

**Approach:**

* Extract 3D pose landmarks using MediaPipe
* Compute domain-specific features (angles, distances)
* Generate sequence embeddings
* Compare with reference sequence using Dynamic Time Warping (DTW)

**Pros:**

* Zero-shot learning
* Highly interpretable
* Extremely lightweight

**Cons:**

* Sensitive to intra-class variation
* Requires manual threshold tuning

---

### 2. 🚀 1D CNN (Temporal Convolutional Network)

**Approach:**

* Treat pose sequence as a 1D signal
* Apply Conv1D layers to capture temporal motion patterns

**Pros:**

* Fast training & inference
* Good at detecting short-term motion patterns

**Cons:**

* Limited ability to capture long-term dependencies

---

### 3. 🔄 CNN-LSTM (Spatio-Temporal Model)

**Approach:**

* CNN → Extract spatial features from frames
* LSTM → Model temporal dynamics across sequence

**Pros:**

* Captures both posture + motion evolution
* Strong performance on sequential data

**Cons:**

* Computationally expensive
* Risk of overfitting on small datasets

---

### 4. 🎯 LSTM + Attention Mechanism

**Approach:**

* LSTM processes sequence
* Attention layer assigns importance to critical frames

**Pros:**

* Improved accuracy on long sequences
* Better interpretability (focus on key frames)

**Cons:**

* Slower training
* Requires sufficient data

---

## 📊 Pipeline Overview

### 🔹 Step 1: Pose Extraction

* MediaPipe extracts **33 body landmarks per frame**

### 🔹 Step 2: Feature Engineering

* Convert landmarks → angles, distances, normalized coordinates
* Build structured temporal sequences

### 🔹 Step 3: Model Training

* Train multiple architectures (CNN, LSTM, Attention)
* Compare performance across metrics

### 🔹 Step 4: Prediction

* Output: 🎯 Classified physiotherapy exercise

---

## ⚙️ Key Features

* 🧍 Real-time human pose tracking
* 🏋️ Exercise classification
* 🔁 Temporal sequence modeling
* 🧠 Attention-based interpretability
* ⚡ Architecture benchmarking framework

---

## 📈 Evaluation Metrics

* Accuracy
* Precision / Recall
* FPS (Inference Speed)
* Model Size / Latency

---






## 💡 Use Cases

* 🏥 Clinical physiotherapy monitoring
* 🏠 Home-based rehabilitation systems
* 💪 Fitness & posture tracking
* 🤖 AI healthcare assistants

---

#
