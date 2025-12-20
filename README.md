# ![Blob Sunglasses](https://emojis.slackmojis.com/emojis/images/1531849430/4246/blob-sunglasses.gif?1531849430) Image Forgery Detection Project

Welcome to this repository! This project focuses on detecting **copy-move** and **splicing** forgeries in images using a hybrid deep learning approach.  
We combine the **Stationary Wavelet Transform (SWT)** with a custom **CNN model** to enhance feature extraction and improve detection accuracy.

---

## Datasets Used
- **Copy-Move Forgery:** GRIP, COVERAGE, MICC-F220, MICC-F2000, CASIA-CMFD  
- **Splicing Forgery:** CASIA V1, CASIA V2

---

## Method Overview
1. Apply **SWT** to decompose images into four frequency sub-bands (LL, LH, HL, HH).  
2. Combine sub-bands into a 4-channel image as input for the CNN.  
3. Train the model using multiple datasets with data augmentation.  
4. Evaluate performance using accuracy, precision, recall, F1-score, and confusion matrices.

---

## Key Features
- High detection accuracy across seven datasets.  
- Robust against noise, JPEG compression, rotation, and scaling.  
- Supports both copy-move and splicing forgery detection.  
- Uses a lightweight CNN with enhanced feature extraction from SWT.

---

## Tools & Technologies
![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white) 
![TensorFlow](https://img.shields.io/badge/-TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white) 
![Keras](https://img.shields.io/badge/-Keras-D00000?style=flat-square&logo=keras&logoColor=white) 
![OpenCV](https://img.shields.io/badge/-OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white) 
![NumPy](https://img.shields.io/badge/-NumPy-013243?style=flat-square&logo=numpy&logoColor=white)

---

## Results
- Accuracy: **97–100%** across the datasets.  
- High precision, recall, and F1-score.  
- Robust performance under post-processing attacks like noise and compression.

---

## Connect with Me
[![GitHub](https://img.shields.io/badge/GitHub-%2312100E.svg?&style=for-the-badge&logo=Github&logoColor=white)](#)  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white)](#)

---

*This README summarizes the image forgery detection project using a hybrid SWT + CNN approach.*
