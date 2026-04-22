An end-to-end multimodal AI system that detects user emotion via webcam and recommends music based on psychological valence-arousal mapping.

This project integrates Computer Vision + Deep Learning + Recommendation Systems into a single real-time pipeline.

🔥 Key Features
🎥 Real-time webcam-based emotion detection
🧠 Deep learning model (EfficientNet-B0) for facial emotion recognition
🎯 Emotion → Valence-Arousal (VA) mapping
🎵 Intelligent music recommendation using similarity search
🔁 Dynamic playlist with Next Song functionality
⚡ Near real-time inference pipeline
🧠 System Architecture
🛠️ Tech Stack
Component	Technology
Model	EfficientNet-B0 (PyTorch + timm)
Computer Vision	OpenCV
Backend Logic	Python
Data Handling	SQLite
UI Interaction	IPython + JavaScript (Colab widgets)
Audio Playback	IPython Audio
🧩 How It Works
1️⃣ Emotion Detection
Captures image from webcam
Preprocesses to 224x224
Passes through trained EfficientNet model
Outputs one of 7 emotions:
happy, sad, angry, neutral, fear, surprise, disgust
2️⃣ Emotion → Psychological Mapping
Each emotion is mapped to:

Valence (positivity)
Arousal (energy level)
Example:

Emotion	Valence	Arousal
Happy	0.85	0.75
Sad	0.25	0.30
Angry	0.20	0.85
3️⃣ Music Recommendation Logic
Songs are stored with:
Valence
Arousal
System computes distance between user mood and song mood
Uses Euclidean distance to rank songs
Returns top-K closest matches
4️⃣ Playback System
Randomly selects from top-K songs
Plays audio
Provides Next Song button for dynamic experience
⚙️ Installation
pip install torch torchvision timm opencv-python ipywidgets
