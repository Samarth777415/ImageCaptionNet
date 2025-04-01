# Image Caption Generator

[![Python](https://img.shields.io/badge/-Python-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/-TensorFlow-FF6F00?logo=tensorflow&logoColor=white)](https://www.tensorflow.org/)
![Pandas](https://img.shields.io/badge/-Pandas-150458?logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/-NumPy-013243?logo=numpy&logoColor=white)
![Jupyter](https://img.shields.io/badge/-Jupyter-F37626?logo=jupyter&logoColor=white)
[![Streamlit](https://img.shields.io/badge/-Streamlit-FF4B4B)](https://www.streamlit.io/)

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Installation](#installation)
- [Deployment](#deployment)
- [Directory Structure](#directory-structure)
- [Future Enhancements](#future-enhancements)

## Overview

This project implements an image caption generator using deep learning techniques. The model is trained on the Flickr8K dataset and combines CNNs (for feature extraction) with LSTMs (for text generation). A Streamlit app has been developed to allow users to upload images and receive AI-generated captions in real time.

### Features:
- Image feature extraction using a pretrained CNN (VGG16/MobileNetV2 for efficiency)
- Text generation using an LSTM-based captioning model
- Streamlit web app for interactive caption generation
- Attention mechanism for improved caption relevance

## Dataset

The [Flickr8K dataset] is used for training and evaluation. It consists of 8,091 images, each with five captions describing the content. The dataset structure:

```
/flickr8k
│── Images/  (image files)
│── captions.txt  (text annotations)
```

## Installation

Ensure Python 3.10+ is installed. Clone the repository and install dependencies:

```bash
git clone https://github.com/yourusername/image-caption-generator.git
cd image-caption-generator
pip install -r requirements.txt
```

## Deployment

To deploy the Streamlit app:

1. Create an account on Streamlit Sharing.
2. Fork this repository.
3. Log in to Streamlit Sharing, create a new app, and connect your GitHub repository.
4. Configure `server` settings:
   ```
   [server]
   headless = true
   port = $PORT
   enableCORS = false
   ```
5. Click "Deploy app" to launch.

## Directory Structure

```
|── app.py                 # Streamlit app script
|── image-captioner.ipynb  # Model implementation notebook
|── mymodel.h5             # Trained model file
|── requirements.txt       # Required dependencies
|── tokenizer.pkl          # Saved tokenizer
|── README.md              # Project documentation
|── /resource/demo.gif     # Demo preview
```

## Future Enhancements

- **Improve Model Performance**: Experiment with different architectures and hyperparameters.
- **Expand Dataset**: Train on larger datasets like Flickr30K or MS COCO.
- **Beam Search Decoding**: Implement beam search for better caption selection.
- **Multilingual Support**: Extend caption generation to multiple languages.
- **UI Enhancements**: Improve the user interface and add more interactive features.

Contributions and feedback are welcome! 🚀

