# ♻ cnn-waste-sorter
A Convolutional Neural Network (CNN) for classifying waste into **Dry**, **Wet**, and **E-Waste** using custom preprocessing and EDA-driven architecture improvements.  
Built with **TensorFlow/Keras**.

---

## Overview

This project implements a **deep learning approach** to sustainable waste management.  
By combining **exploratory data analysis (EDA)**, **custom preprocessing (HSV brightness correction)**, and a **CNN with regularization**, the model learns to accurately distinguish between three waste categories.

The workflow includes:

1. **EDA** for dataset inspection and balancing.  
2. **Custom Preprocessing** with brightness correction in the HSV color space.  
3. **CNN Architecture** with Conv2D, Batch Normalization, Dropout, and dense layers.  
4. **Training Optimization** with EarlyStopping, ReduceLROnPlateau, and class weights.  
5. **Evaluation** using accuracy, precision, recall, F1-score, and confusion matrix.

---

## Features

* **EDA-driven preprocessing** (brightness equalization, augmentation, class balance)  
* **Custom CNN** with multiple convolutional blocks and dropout layers  
* **Training optimizations**: EarlyStopping + ReduceLROnPlateau  
* **Evaluation**: Accuracy, Precision, Recall, F1-score, Confusion Matrix  
* **Exportable trained model** (`.h5`) for deployment  

---

## Repository Structure

```text
cnn-waste-sorter/
│── data/                 # Dataset (or link/instructions)
│── notebooks/            # Jupyter/Colab notebooks
│   ├── preprocessing.py  # Data preprocessing & augmentation
│   ├── model 1           # Training & Evaluation model 1 script
│   ├── model 2           # Training & Evaluation model 2 script
│── models/               # Saved models (.h5)
│── README.md             # Project documentation

```
---

## Installation
Clone the repo and install requirements:
```bash
git clone https://github.com/<your-username>/cnn-waste-sorter.git
cd cnn-waste-sorter
pip install -r requirements.txt
```

## Usage
# 1. Preprocess Dataset
python src/preprocessing.py

# 2. Train Model
python src/train.py

# 3️. Evaluate Model
python src/evaluate.py

# Results
Achieved ~71–75% validation accuracy on a balanced dataset of ~600 images.

Confusion matrix & classification report show:
Strong performance on E-Waste
Dry/Wet waste improved with class weighting & augmentation

```text
Example metrics (previous run):
              precision    recall  f1-score   support
   Dry waste       0.77      0.50      0.61
     E-Waste       0.73      0.93      0.81
   Wet waste       0.77      0.82      0.80
```

## Future Improvements
  - Try EfficientNet / MobileNetV2 for transfer learning
  - Expand dataset with more diverse waste images

## License
MIT License © 2025 Brinda Muralikannan

## Acknowledgements
TensorFlow/Keras team for the framework
Inspiration from SDGs on sustainable waste management

