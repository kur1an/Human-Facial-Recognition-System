# Human Facial Recognition System

This repository contains code for a Human Facial Recognition System built using TensorFlow and Keras. The system is designed to recognize and classify human faces from a given dataset.

## Table of Contents
- [Introduction](#introduction)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## Introduction
This project aims to develop a facial recognition system using deep learning techniques. It uses TensorFlow and Keras libraries to train a model that can classify human faces into different categories. The model is trained and validated using a dataset of images stored on Google Drive.

## Requirements
- Python 3.x
- TensorFlow
- Keras
- Google Colab
- Google Drive account

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/Human-Facial-Recognition-System.git
   cd Human-Facial-Recognition-System
   ```
2. Install the required Python packages:
   ```bash
   pip install tensorflow
   ```

## Usage
1. Open the project in Google Colab by clicking the badge below:

   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kur1an/Human-Facial-Recognition-System/blob/main/Human_Facial_Recognition_System.ipynb)

2. Mount your Google Drive:
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```

3. Import TensorFlow and Keras libraries:
   ```python
   import tensorflow as tf
   from tensorflow import keras
   from tensorflow.keras import layers
   ```

4. Load the dataset from your Google Drive:
   ```python
   image_size = (256, 256)
   batch_size = 3

   train_ds = tf.keras.preprocessing.image_dataset_from_directory(
       "/content/drive/MyDrive/hackthon",
       validation_split=0.2,
       subset="training",
       seed=1337,
       image_size=image_size,
       batch_size=batch_size,
   )

   val_ds = tf.keras.preprocessing.image_dataset_from_directory(
       "/content/drive/MyDrive/hackthon",
       validation_split=0.2,
       subset="validation",
       seed=1337,
       image_size=image_size,
       batch_size=batch_size,
   )
   ```

5. Train your model using the loaded dataset.

## Project Structure
- `Human_Facial_Recognition_System.ipynb`: Main notebook containing the code for training and validating the model.
- `README.md`: This file.

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.