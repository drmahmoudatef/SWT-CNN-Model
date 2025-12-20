Image Forgery Detection using SWT and CNN
Overview

This repository presents a hybrid deep learning framework for image forgery detection, targeting both copy-move and splicing attacks.
The proposed method integrates Stationary Wavelet Transform (SWT) with a Convolutional Neural Network (CNN) to enhance discriminative feature representation and improve robustness against post-processing operations.

Key Contributions

Integration of SWT sub-bands (LL, LH, HL, HH) as multi-channel CNN input.

Lightweight yet effective CNN architecture.

Evaluation on multiple public benchmark datasets.

Robust performance under noise, compression, rotation, and scaling.

Datasets

All datasets are publicly available on Kaggle and are reorganized into Train / Validation / Test splits on Google Drive.

Copy-Move Forgery Datasets

MICC-F2000
https://www.kaggle.com/datasets/manas29/micc-f2000

MICC-F200
https://www.kaggle.com/datasets/nishaahin/miccf200

CASIA-CMFD
https://www.kaggle.com/datasets/mashraffarouk/casia-cmfd

Splicing Forgery Datasets

CASIA V1
https://www.kaggle.com/datasets/sophatvathana/casia-dataset

CASIA V2
https://www.kaggle.com/datasets/divg07/casia-20-image-tampering-detection-dataset

Methodology

Data Loading
Datasets are stored on Google Drive and accessed via Google Colab.

Preprocessing

Resize to 224×224

Normalization

Data augmentation (rotation, shift, zoom, flip)

SWT Decomposition
Each image is decomposed using Haar SWT into four sub-bands (LL, LH, HL, HH).

Feature Fusion
The four sub-bands are stacked as a 4-channel input tensor.

CNN Architecture

3 convolutional blocks

Batch Normalization

Global Average Pooling

Fully connected layers

Training Strategy

Adam optimizer (LR = 0.001)

Binary Cross-Entropy loss

Class-weight balancing

Model checkpointing

Evaluation
Performance is measured on unseen test sets.

Evaluation Metrics

The proposed model is evaluated using:

Accuracy

Precision

Recall

F1-score

TPR, TNR

FPR, FNR

Matthews Correlation Coefficient (MCC)

Confusion Matrix

Comparative and robustness evaluations are conducted against baseline CNN-based approaches.

Results

Achieved high detection accuracy across all datasets.

Stable performance under post-processing attacks.

Reduced false positives and false negatives compared to baseline models.

Limitations

Training requires GPU acceleration for large datasets.

Performance may degrade for unseen forgery types.

Dataset imbalance can influence minority class detection.
