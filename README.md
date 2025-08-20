# ♻ cnn-waste-sorter
A Convolutional Neural Network (CNN) for classifying waste into **Dry**, **Wet**, and **E-Waste** using custom preprocessing and EDA-driven architecture improvements.  
Built with **TensorFlow/Keras**.

---

## Overview
This project implements a **deep learning approach** to waste classification.  
By leveraging **EDA insights, custom preprocessing, and CNNs**, the model learns to distinguish waste types from images.  

The workflow includes:
- Dataset augmentation & balancing
- Brightness correction (HSV preprocessing)
- Custom CNN with regularization
- Model evaluation with detailed metrics

---

## Features
- **EDA-driven preprocessing** (brightness equalization, augmentation, class balance)  
- **Custom CNN** with Batch Normalization & Dropout  
- **Training optimizations**: EarlyStopping + ReduceLROnPlateau  
- **Evaluation**: Accuracy, Precision, Recall, F1-score, Confusion Matrix  
- Exportable trained model (`.h5`)  

---

## Repository Structure
cnn-waste-sorter/
│── data/ # Dataset (or link/instructions)
│── notebooks/ # Jupyter/Colab notebooks
│── src/ # Source code
│ ├── preprocessing.py # Data preprocessing & augmentation
│ ├── train.py # Training script
│ ├── evaluate.py # Evaluation script
│── models/ # Saved models (.h5)
│── results/ # Plots, logs, confusion matrix
│── README.md # Project documentation
│── requirements.txt # Dependencies

---


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

Example metrics (previous run):
              precision    recall  f1-score   support
   Dry waste       0.77      0.50      0.61
     E-Waste       0.73      0.93      0.81
   Wet waste       0.77      0.82      0.80

## Future Improvements
  - Try EfficientNet / MobileNetV2 for transfer learning
  - Deploy as a Streamlit/Flask web app for real-time predictions
  - Expand dataset with more diverse waste images

## License
MIT License © 2025 Brinda Muralikannan

## Acknowledgements
TensorFlow/Keras team for the framework
Inspiration from SDGs on sustainable waste management

