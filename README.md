# 🎵 Mood-Based Music Recommendation System

An end-to-end multimodal AI system that detects user emotion via webcam and recommends music based on psychological valence-arousal mapping.

This project integrates **Computer Vision + Deep Learning + Recommendation Systems** into a single real-time pipeline.

---

## 🔥 Key Features

* 🎥 Real-time webcam-based emotion detection
* 🧠 Deep learning model (EfficientNet-B0) for facial emotion recognition
* 🎯 Emotion → Valence-Arousal (VA) mapping
* 🎵 Intelligent music recommendation using similarity search
* 🔁 Dynamic playlist with Next Song functionality
* ⚡ Near real-time inference pipeline

---

## 🧠 System Architecture

User Face → Emotion Model → Emotion → VA Mapping → Song Matching → Playback

---

## 🛠️ Tech Stack

| Component       | Technology                       |
| --------------- | -------------------------------- |
| Model           | EfficientNet-B0 (PyTorch + timm) |
| Computer Vision | OpenCV                           |
| Backend         | Python                           |
| Database        | SQLite                           |
| UI              | IPython + JavaScript (Colab)     |
| Audio           | IPython Audio                    |

---

## 🧩 How It Works

### 1️⃣ Emotion Detection

* Capture image from webcam
* Resize to 224x224
* Pass through EfficientNet model
* Output:
  `happy, sad, angry, neutral, fear, surprise, disgust`

---

### 2️⃣ Emotion → VA Mapping

| Emotion | Valence | Arousal |
| ------- | ------- | ------- |
| Happy   | 0.85    | 0.75    |
| Sad     | 0.25    | 0.30    |
| Angry   | 0.20    | 0.85    |
| Neutral | 0.50    | 0.50    |

---

### 3️⃣ Music Recommendation

* Songs stored with valence & arousal
* Compute similarity using **Euclidean distance**
* Return top-K closest songs

---

### 4️⃣ Playback System

* Randomly plays from top-K songs
* Provides **Next Song button**
* Continuous listening experience 🎶

---

## ⚙️ Installation

```bash
pip install torch torchvision timm opencv-python ipywidgets
```

---

## ▶️ Run the Project

1. Open in Google Colab
2. Mount Google Drive
3. Load model & database
4. Run script
5. Capture mood → Get music 🎵

---


