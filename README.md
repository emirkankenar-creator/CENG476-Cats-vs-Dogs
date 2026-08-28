# CENG476 – Cats vs Dogs Classification

## Project Overview

This project was developed for the CENG476 – Introduction to Deep Learning course at Turkish Aeronautical Association University.

The objective is to develop a binary image classification model that classifies images as either **Cat** or **Dog**.

The project uses transfer learning with a pretrained **ResNet18** model. The main focus is on improving the training pipeline rather than introducing a new model architecture.

## Dataset

The dataset contains cat and dog images for binary image classification.

The data was divided into:

- 70% Training
- 15% Validation
- 15% Testing

Images were resized to 224 × 224 pixels.

## Training Methodology

Several training-stage methodologies were investigated and used:

- Data augmentation
- Batch normalization
- Dropout
- AdamW optimizer
- Weight decay
- Learning-rate scheduling
- Early stopping

Data augmentation was used to increase the diversity of training images.

Dropout and weight decay were used as regularization methods.

Early stopping was used to stop training when the validation performance stopped improving.

A dropout experiment was also performed using dropout rates of 0.30, 0.50 and 0.70.

## Model

The main backbone is a pretrained ResNet18 network.

The final classification layers were adapted for the binary Cats vs Dogs classification task.

The project compares a **Baseline Model** with an **Improved Model**.

## Results

### Baseline Model

| Metric | Score |
|---|---:|
| Accuracy | 98.56% |
| Precision | 97.7953% |
| Recall | 99.3600% |
| F1-Score | 98.5714% |

### Improved Model

| Metric | Score |
|---|---:|
| Accuracy | 98.80% |
| Precision | 98.5154% |
| Recall | 99.0933% |
| F1-Score | 98.8035% |

The improved model increased the test accuracy from **98.56% to 98.80%**.

### Dropout Experiment

| Dropout | Validation Accuracy |
|---:|---:|
| 0.30 | 99.0400% |
| 0.50 | 98.8000% |
| 0.70 | 98.9333% |

Among the tested dropout values, **0.30 achieved the highest validation accuracy**.

## Confusion Matrix

The improved model produced the following results on the test set:

- 1853 Cats correctly classified as Cats
- 22 Cats classified as Dogs
- 25 Dogs classified as Cats
- 1850 Dogs correctly classified as Dogs

## Project Files

- `CENG476_Cats_vs_Dogs_Project_Colab_FIXED (1).ipynb` – Complete Google Colab notebook
- `README.md` – Project documentation

## Technologies

- Python
- PyTorch
- Torchvision
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Google Colab
- CUDA / NVIDIA T4 GPU

## Conclusion

The experiments show that training-stage methodologies can improve model performance without introducing a completely new CNN architecture.

The improved training pipeline achieved approximately **98.75% test accuracy** and **98.75% F1-score**.

## Author

**Emirkan Kenar**

CENG476 – Introduction to Deep Learning  
Turkish Aeronautical Association University
