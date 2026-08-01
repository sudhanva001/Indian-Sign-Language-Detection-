# Indian Sign Language Recognition using CNN

A real-time sign-to-speech system that recognizes Indian Sign Language (ISL) gestures from a live camera feed and converts them into spoken audio — built to help bridge communication between sign language users and non-signers.

---

## Overview

Communication barriers between the deaf/hard-of-hearing community and non-signers remain a significant real-world challenge. This project tackles that gap by building a **real-time CNN-based ISL recognition pipeline** that:

- Captures hand gestures live via webcam
- Classifies them into corresponding ISL signs using a trained Convolutional Neural Network
- Converts recognized signs into **spoken output** instantly using text-to-speech

The result is an end-to-end sign-to-speech translator achieving **~90% recognition accuracy**.

---

## Key Features

- **Real-Time Recognition** — Live webcam feed processed frame-by-frame using OpenCV for instant gesture detection.
- **CNN-Based Classification** — A custom-trained TensorFlow/Keras CNN model classifies hand gestures into ISL alphabet/sign categories.
- **~90% Accuracy** — Achieved through careful preprocessing (background removal, hand segmentation, normalization) and iterative model/hyperparameter tuning.
- **Text-to-Speech Output** — Recognized signs are converted to natural spoken audio using `pyttsx3`, enabling immediate voice communication.

---

## How It Works

1. **Capture** — OpenCV accesses the webcam feed and extracts the region of interest (hand area) frame by frame.
2. **Preprocess** — Frames are cleaned (grayscale/thresholding/background subtraction, resizing) to isolate the hand gesture and reduce noise.
3. **Predict** — The preprocessed frame is passed through the trained CNN model, which outputs the predicted sign class.
4. **Speak** — The predicted sign/letter is converted to speech in real time via `pyttsx3`, giving immediate audible output.

---

## Tech Stack

- **Language:** Python
- **Deep Learning:** TensorFlow / Keras
- **Computer Vision:** OpenCV
- **Text-to-Speech:** pyttsx3
- **Model Architecture:** Convolutional Neural Network (CNN)

---

## Getting Started

### Prerequisites

- Python 3.x
- Webcam (for real-time inference)

### Installation

```bash
git clone https://github.com/<your-username>/isl-recognition-cnn.git
cd isl-recognition-cnn
pip install -r requirements.txt
```

### Requirements

```
tensorflow
opencv-python
pyttsx3
numpy
```

> Update `requirements.txt` with your exact package versions.

### Usage

```bash
python main.py
```

Point your webcam at an ISL hand sign — the recognized letter/word will be displayed on screen and spoken aloud.

> Update this section with your actual entry-point filename and any setup steps (e.g., model file path, camera index).

---

## Dataset

- Trained on an Indian Sign Language image dataset covering [alphabets / numbers / words — specify which].
- Preprocessing pipeline included: [background subtraction / skin segmentation / grayscale conversion / resizing — list what you actually used].

> Add a link to the dataset source if it's publicly available (e.g., Kaggle, Mendeley Data), and note any train/test split details.

---

## Model Performance

- **Accuracy:** ~90% on the test set
- **Improvements from:**
  - Data preprocessing (noise reduction, hand segmentation)
  - Model architecture tuning (layers, filters, dropout)
  - Hyperparameter tuning (learning rate, batch size, epochs)

> Add your confusion matrix, accuracy/loss curves, or class-wise accuracy here if available — strengthens the README significantly.

---

## Project Structure

```
isl-recognition-cnn/
├── model/                 # trained CNN model files
├── dataset/                # training/testing image data
├── src/
│   ├── preprocess.py       # image preprocessing pipeline
│   ├── train.py              # CNN training script
│   ├── recognize.py           # real-time webcam recognition + prediction
│   └── speak.py                 # text-to-speech integration
├── requirements.txt
└── README.md
```

> Adjust to match your actual folder layout.

---

## Future Improvements

- [ ] Expand from static alphabet signs to dynamic word/phrase recognition
- [ ] Improve robustness to lighting conditions and backgrounds
- [ ] Add support for two-handed and continuous signing
- [ ] Deploy as a mobile app for wider accessibility

---

## Contributing

Contributions are welcome. Please open an issue to discuss proposed changes before submitting a pull request.

---

## License

[MIT / Apache 2.0 / Other — choose and add a LICENSE file]

---

## Acknowledgments

Built as part of [course/project name], aimed at improving accessibility and communication for the Indian deaf and hard-of-hearing community through real-time AI-powered sign language translation.
