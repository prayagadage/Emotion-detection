<div align="center">

# 😊 Emotion Detection System

**Real-time face and emotion recognition from your webcam using deep learning.**

[![Python](https://img.shields.io/badge/Python-3.7%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-Keras-orange?logo=tensorflow)](https://www.tensorflow.org/)
[![OpenCV](https://img.shields.io/badge/OpenCV-Face%20Detection-green?logo=opencv)](https://opencv.org/)
[![Model](https://img.shields.io/badge/Model-mini__XCEPTION-blueviolet)](https://github.com/oarriaga/face_classification)

</div>

---

## 📌 Overview

**Emotion Detection System** is a real-time computer vision application that detects faces from a live webcam feed and classifies the emotion on each face — instantly and accurately.

It combines **OpenCV's Haar Cascade** for fast face detection and a pre-trained **mini XCEPTION** deep learning model for emotion classification, outputting both the emotion label and confidence score on screen.

---

## 🎭 Detected Emotions

| Emotion | Emoji |
|---|---|
| Angry | 😠 |
| Disgust | 🤢 |
| Scared | 😨 |
| Happy | 😊 |
| Sad | 😢 |
| Surprised | 😲 |
| Neutral | 😐 |

---

## 🛠️ How It Works

```
Webcam Feed
     ↓
Frame Capture (OpenCV)
     ↓
Grayscale Conversion
     ↓
Face Detection (Haar Cascade)
     ↓
ROI Extraction → Resize (64×64) → Normalize
     ↓
Emotion Prediction (mini XCEPTION model)
     ↓
Overlay Bounding Box + Emotion Label on Frame
     ↓
Live Display
```

1. **Face Detection** — Haar Cascade (`haarcascade_frontalface_default.xml`) scans each frame and detects face regions
2. **Preprocessing** — Detected face regions are converted to grayscale, resized to `64×64`, and normalized
3. **Emotion Classification** — The `mini_XCEPTION` model predicts probabilities across 7 emotion classes
4. **Visualization** — Bounding boxes and emotion labels with confidence scores are drawn live on the feed

---

## ⚙️ Installation & Setup

### Prerequisites
- Python **3.7+**
- A working webcam

### 1. Clone the Repository
```bash
git clone https://github.com/prayagadage/Emotion-detection.git
cd Emotion-detection
```

### 2. Set Up Virtual Environment
```bash
python3 -m venv venv
source venv/bin/activate     # macOS/Linux
venv\Scripts\activate        # Windows
```

### 3. Install Dependencies
```bash
pip install tensorflow keras numpy opencv-python imutils
```

---

## 🚀 Run the App

```bash
python face_detection.py
```

- The webcam feed opens automatically
- Detected faces are highlighted with bounding boxes
- Emotion label and confidence score appear above each face
- Press **`q`** to quit

---

## 📂 Project Structure

```
Emotion-detection/
├── face_detection.py                   # Main application — detection + prediction loop
├── _mini_XCEPTION.102-0.66.hdf5        # Pre-trained emotion classification model
├── haarcascade_frontalface_default.xml # OpenCV Haar Cascade for face detection
└── README.md
```

---

## 📦 Tech Stack

| Tool | Purpose |
|---|---|
| [OpenCV](https://opencv.org/) | Face detection & video capture |
| [TensorFlow / Keras](https://www.tensorflow.org/) | Deep learning model inference |
| [mini XCEPTION](https://github.com/oarriaga/face_classification) | Emotion classification model |
| [NumPy](https://numpy.org/) | Array operations & preprocessing |
| [Imutils](https://github.com/jrosebr1/imutils) | Frame resizing utilities |

---

## 🔮 Roadmap

- [x] Real-time single face emotion detection
- [x] 7-class emotion classification with confidence score
- [ ] Multi-face detection support
- [ ] GPU acceleration for faster inference
- [ ] Save annotated video output
- [ ] Streamlit / Gradio web interface
- [ ] Additional emotions (confusion, excitement)

---

## 📬 Author

**Prayag Adage**
GitHub: [@prayagadage](https://github.com/prayagadage)
Location: Pimpri-Chinchwad, Maharashtra, India

⭐ Star this repo if you found it useful!
