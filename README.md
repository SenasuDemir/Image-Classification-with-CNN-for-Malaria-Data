# Malaria Cell Detection Using Convolutional Neural Networks (CNN)

This project utilizes **Convolutional Neural Networks (CNN)** to detect parasitized and infected cells in microscopic medical images. The primary goal is to assist healthcare professionals in diagnosing diseases like malaria, where early detection of parasitized cells in blood samples can significantly improve treatment outcomes. The automated detection system allows healthcare providers, especially in resource-limited settings, to quickly and accurately diagnose the condition, even without access to expert pathologists.

## Project Overview

This project involves training two different models using CNNs to detect malaria in microscopic images of blood cells. The models classify the cells into two categories: **Infected** (parasitized cells) and **Uninfected** (healthy cells).

### Key Features:

- **Dataset:**
  - The model is trained on a curated dataset of microscopic images, labeled as either **Infected** or **Uninfected**. This dataset contains a total of **27,558 images**, which is split between healthy and infected cell samples.
  - You can obtain the dataset from the following sources:
    - [NIH Malaria Dataset](https://ceb.nlm.nih.gov/repositories/malaria-datasets/)
    - [Kaggle Malaria Dataset](https://www.kaggle.com/datasets/iarunava/cell-images-for-detecting-malaria)
  
- **Model Architectures:**
  1. **VGG16 with Transfer Learning:** The first model leverages the VGG16 architecture, which is pre-trained on a large dataset (ImageNet). The VGG16 model is fine-tuned on the malaria dataset to classify infected and uninfected cells. By leveraging the feature extraction capabilities of VGG16, this model achieves an accuracy of **97.30%**.
  2. **Custom CNN Architecture:** The second model employs a custom-built CNN designed specifically for this task. The custom CNN is more lightweight and faster to train compared to VGG16, while still achieving comparable accuracy. This model reaches an accuracy of **97.46%**.

- **Preprocessing:**
  - **Resizing:** All images are resized to a uniform size  to make them compatible with the model input dimensions.
  - **Normalization:** Pixel values are normalized to a range of [0, 1] to ensure consistent and faster convergence during model training.
  - **Color Conversion:** All images are converted to RGB format to comply with model requirements, ensuring that color features are utilized during training.

- **Training and Evaluation:**
  - Both models are trained using a split of **80% training** and **20% validation** data to ensure the models generalize well.
  - I used accuracy to evaluate model performance, with a particular emphasis on accuracy due to the importance of correctly identifying both infected and uninfected cells.
