# 🌸 Transfer Learning for Flower Classification

Deep Learning Project – Image Classification with Pretrained CNN Models

## 📌 Overview

This project focuses on classifying five flower categories using **Transfer Learning** with several state-of-the-art convolutional neural networks such as **InceptionV3**, **ResNet50**, **VGG16**, **MobileNetV2**, and **Xception**.
The dataset includes 5,000 labeled flower images and is automatically downloaded from Kaggle using **kagglehub**.

The workflow includes:

* Dataset download and preprocessing
* Exploratory data analysis
* Image visualization
* Train/Validation/Test split
* Data augmentation
* Transfer Learning model training
* Evaluation and saving the final model

---

## 📂 Dataset

**Kaggle dataset:** *5 Flower Types Classification Dataset*
It contains 5 equally balanced classes:

* Lily
* Lotus
* Orchid
* Sunflower
* Tulip

The images are downloaded automatically through the command:

```python
dataset_path = kagglehub.dataset_download("kausthubkannan/5-flower-types-classification-dataset")
```

---

## 🧪 Project Structure

```
│── Projet_DL_Transfer_Learning.ipynb                   # Main script
│── README.md                 # Project documentation
```

---

## 🚀 Main Steps

### 1. Imports

Libraries used: TensorFlow, Keras, Sklearn, Pandas, NumPy, Matplotlib, Seaborn.

### 2. Dataset Download & Loading

The images are loaded using `sklearn.datasets.load_files` to retrieve filenames and labels.

### 3. Visualization

Random samples from the dataset are displayed to verify quality and class distribution.

### 4. Data Splitting

Dataset split into:

* **60%** training
* **20%** validation
* **20%** test

### 5. Data Augmentation

Applied transformations include rotation, shifting, zooming, flipping, and brightness variation.

### 6. Model Architecture

Example: **InceptionV3** (pretrained on ImageNet)

* Frozen convolutional base
* Added classification head with Dense + Dropout layers
* Softmax output for 5 classes

### 7. Training

* Optimizer: **Adam**
* Learning rates: `0.001` and `0.0005`
* Callbacks: EarlyStopping, ReduceLROnPlateau

### 8. Evaluation

Accuracy and loss are evaluated on the test set.
Model is saved using:

```python
model.save("inceptionv3_001.h5")
```

---

## 📈 Results

The InceptionV3 model reaches strong performance with:

* Test accuracy ≈ **90%** (depending on training environment)

---

## 🛠 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/amina-moueddene/Transfer_learning_project.git
cd Transfer_learning_project
```
<img width="896" height="860" alt="tasks" src="https://github.com/user-attachments/assets/3770c2ff-5c97-40b0-af7b-b3ae3dc21b78" />

## 📧 Contact

For questions or improvements, feel free to open an issue or reach out.
