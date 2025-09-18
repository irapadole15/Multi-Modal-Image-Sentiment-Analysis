# Multi-Modal-Image-Sentiment-Analysis

This repository contains the code and resources for a **final-year project** that performs sentiment analysis on images using a **multi-modal approach**. The system integrates **facial emotion recognition, gender classification, and OCR-based text sentiment analysis** to deliver a comprehensive sentiment score.

---

## Project Overview

Social media users increasingly express their opinions through images, memes, and visual posts. Analyzing only textual content misses a large portion of sentiment data.

This project leverages **computer vision** and **natural language processing (NLP)** to extract information from both **faces** and **embedded text** in images. It then applies **machine learning models** to classify emotions, genders, and sentiment polarity.

**Core capabilities:**

* Detect multiple faces in an image or live video stream.
* Classify emotions (happy, sad, angry, surprised, neutral, etc.) using a CNN trained on FER-2013 dataset.
* Classify gender using a CNN trained on the IMDB dataset.
* Extract text from images using Tesseract OCR and perform sentiment analysis using VADER.
* Display results through a simple **UI application** or run real-time inference via scripts.

---

## Key Features

* **Real-Time Face Detection & Emotion Classification**
* **Gender Classification with High Accuracy** (IMDB dataset – \~96%)
* **OCR-based Text Extraction** for memes and image-based text
* **Sentiment Analysis of Extracted Text** using VADER NLP model
* **Combined Sentiment Interpretation** (faces + text)
* **User-Friendly UI** for image input and analysis
* **Standalone Executable** for Windows users (UI.exe)

---

## Installation & Setup

### Prerequisites

* Python 3.6.0 (64-bit recommended for TensorFlow compatibility)
* pip (Python package manager)

### Steps to Setup

1. **Clone the Repository**

```bash
git clone https://github.com/AnkurKarmakar/Multi-Modal-Image-Sentiment-Analysis
cd Multi-Modal-Image-Sentiment-Analysis
```

2. **Install Required Dependencies**

```bash
pip install -r requirements.txt
```

3. **Install Tesseract OCR**
   Download from [Tesseract OCR Project](https://sourceforge.net/projects/tesseract-ocr-alt/files/tesseract-ocr-setup-3.02.02.exe/download) and add it to your system PATH.

4. **(Optional) Install Pre-Built Site-Packages**
   Download from [Google Drive](https://drive.google.com/file/d/1yBVfiMuq6DI8gIF4z__E_gCmwSwEL4uu/view?usp=sharing) and extract into:

```
C:\Users\<UserName>\AppData\Local\Programs\Python\Python36\Lib\
```

5. **Run the Application**
   Navigate to the `src` folder and launch `UI.exe` to use the graphical interface.

---

## Usage

### Perform Sentiment Analysis on Text in Image

```bash
python3 OCRSentiment.py
```

### Real-Time Emotion Detection Demo

```bash
python3 video_emotion_color_demo.py
```

### Analyze a Single Image

```bash
python3 image_emotion_gender_demo.py <image_path>
```

Example:

```bash
python3 image_emotion_gender_demo.py ../images/test_image.jpg
```

---

## Training the Models

### Train Emotion Classification Model

1. Download **fer2013.tar.gz** dataset from [Kaggle](https://www.kaggle.com/c/challenges-in-representation-learning-facial-expression-recognition-challenge/data)
2. Extract it to the `datasets` folder
3. Run:

```bash
python3 train_emotion_classifier.py
```

### Train Gender Classification Model

1. Download **imdb\_crop.tar** from [IMDB Wiki Dataset](https://data.vision.ee.ethz.ch/cvl/rrothe/imdb-wiki/)
2. Extract it to the `datasets` folder
3. Run:

```bash
python3 train_gender_classifier.py
```

---

## System Architecture

* **Face Detection & Emotion Classification:** Mini-Xception CNN architecture with \~600k parameters
* **Gender Classification:** Simple CNN architecture achieving \~96% accuracy
* **OCR & NLP:** Pytesseract for text extraction + VADER for sentiment scoring
* **UI Layer:** Desktop application for easy image selection and visualization

---

## Results

* **FER-2013 Emotion Classification Accuracy:** \~66%
* **IMDB Gender Classification Accuracy:** \~96%
* **End-to-End Image Sentiment Analysis:** Successfully integrates multiple modalities for improved accuracy over text-only methods

---

## Future Scope

* Extend model to use **transformer-based architectures (Vision Transformers, BERT)**
* Incorporate **scene context analysis** for better interpretation of surroundings
* Deploy as a **web-based interactive tool** for accessibility
* Enable **multilingual sentiment analysis** for extracted text

---

## Contact

For questions, collaborations, or contributions:
**Ira Padole**
📧 [irapadole2004@gmail.com](mailto:irapadole2004@gmail.com)
🔗 [LinkedIn](https://www.linkedin.com/in/ira-padole-3487062b4) • [Portfolio](https://irapadole.com)

---
