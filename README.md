# 🌿 AI-Based Plant Disease Detection System

## 📌 Project Overview

The **AI-Based Plant Disease Detection System** uses Deep Learning to identify plant diseases from leaf images.

The system classifies leaf images into **38 different classes**, including healthy and diseased plants. It uses a Custom Convolutional Neural Network (CNN) and MobileNetV2 Transfer Learning to identify the best-performing model.

## 🎯 Objectives

- Detect plant diseases using leaf images.
- Classify images into 38 plant disease and healthy categories.
- Build and compare Custom CNN and MobileNetV2 models.
- Evaluate model performance using classification metrics.
- Save the trained model for future deployment.

## 📂 Dataset

**Dataset:** [New Plant Diseases Dataset (Augmented) – Kaggle](https://www.kaggle.com/datasets/vipoooool/new-plant-diseases-dataset)

- 38 classes
- 70,295 training images
- 17,572 original validation images
- 14 different crops
- RGB leaf images

The original validation dataset is divided into two equal parts for validation and testing.

| Dataset | Images |
|---|---:|
| Training | 70,295 |
| Validation | 8,786 |
| Testing | 8,786 |

## 🛠️ Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- KaggleHub

## ⚙️ Project Workflow

1. Dataset Collection
2. Exploratory Data Analysis (EDA)
3. Image Preprocessing
4. Image Resizing (224 × 224)
5. Data Normalization
6. Custom CNN Model Building
7. MobileNetV2 Transfer Learning
8. Model Training
9. Model Evaluation
10. Model Comparison
11. Image Prediction
12. Model Saving

## 🧠 Models Implemented

### 1. Custom CNN

A Convolutional Neural Network built from scratch.

**Architecture:**
- Input Layer
- Conv2D (32 filters) + MaxPooling
- Conv2D (64 filters) + MaxPooling
- Conv2D (128 filters) + MaxPooling
- Flatten Layer
- Dense Layer (128 neurons)
- Output Layer (38 classes, Softmax)

### 2. MobileNetV2 – Transfer Learning

MobileNetV2 is a pre-trained model using ImageNet weights.

**Architecture:**
- MobileNetV2 Base Model
- Frozen Pre-trained Layers
- Global Average Pooling
- Dropout (0.3)
- Dense Output Layer (38 classes, Softmax)

Both models were trained for 5 epochs.

## 📊 Model Performance

| Model | Training Accuracy | Validation Accuracy | Validation Macro Recall |
|---|---:|---:|---:|
| Custom CNN | 93.06% | 89.53% | 89.48% |
| MobileNetV2 | 94.89% | 95.72% | 95.64% |

### Final Model: MobileNetV2

**Test Performance**

| Metric | Score |
|---|---:|
| Test Accuracy | 95.62% |
| Test Macro Recall | 95.63% |

MobileNetV2 was selected as the final model based on its validation performance.

## 📈 Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1-Score
- Classification Report
- Confusion Matrix

## 🔍 Prediction

The trained MobileNetV2 model predicts the plant disease class from an input leaf image.

The prediction output includes:
- Predicted plant and disease class
- Prediction confidence score

## 💾 Model Saving

The final trained model and class names are saved as:

- `plant_disease_model.keras`
- `class_names.json`

These files can be loaded for future predictions without retraining.

## 🚀 How to Run

This project was developed in Google Colab.

1. Open the notebook in Google Colab.
2. Select a GPU runtime (T4 GPU recommended).
3. Install the required KaggleHub package:

```bash
pip install kagglehub
```

4. Run the notebook cells in order.
5. Allow KaggleHub to download the dataset.
6. Train and evaluate both models.
7. Generate predictions and save the final model.

## 🔮 Future Enhancements

- Develop a Streamlit web application for image uploads and real-time predictions.
- Fine-tune the top MobileNetV2 layers.
- Test with real-world field images.
- Add disease treatment and prevention recommendations.

## 👨‍💻 Author

**Jeeva Sankar**

Aspiring Data Scientist | Python | SQL | Machine Learning | Deep Learning

---

⭐ If you find this project interesting, feel free to explore the repository!
