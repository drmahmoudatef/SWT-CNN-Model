
Welcome to this repository!  
This project focuses on detecting **copy-move** and **splicing** image forgeries using a **hybrid deep learning framework**.  
The proposed approach integrates the **Stationary Wavelet Transform (SWT)** with a custom **Convolutional Neural Network (CNN)** to enhance feature representation and improve detection accuracy and robustness.

---

## Datasets Used

All datasets are publicly available and downloaded from **Kaggle**, then reorganized into **Train / Validation / Test** splits on Google Drive and accessed through Google Colab.

### Copy-Move Forgery Datasets
- **MICC-F2000**  
  https://www.kaggle.com/datasets/manas29/micc-f2000
- **MICC-F200**  
  https://www.kaggle.com/datasets/nishaahin/miccf200
- **CASIA-CMFD**  
  https://www.kaggle.com/datasets/mashraffarouk/casia-cmfd
- **GRIP**  
  Listed via: https://github.com/greatzh/Image-Forgery-Datasets-List
- **COVERAGE**  
  Listed via: https://github.com/greatzh/Image-Forgery-Datasets-List

### Splicing Forgery Datasets
- **CASIA V1**  
  https://www.kaggle.com/datasets/sophatvathana/casia-dataset
- **CASIA V2**  
  https://www.kaggle.com/datasets/divg07/casia-20-image-tampering-detection-dataset

---

## Method Overview

1. Images are loaded from Google Drive after mounting it in Google Colab.
2. Each image is resized and normalized.
3. **Stationary Wavelet Transform (SWT)** using the Haar wavelet is applied to decompose the image into four frequency sub-bands:
   - LL, LH, HL, HH
4. The four sub-bands are stacked to form a **4-channel input tensor**.
5. A custom **CNN architecture** is trained using these SWT-based inputs.
6. Data augmentation is applied during training to improve generalization.
7. The trained model is evaluated on unseen test data.

---

## Model Architecture
- Input shape: **224 × 224 × 4**
- Three convolutional blocks with:
  - Convolution layers
  - Batch Normalization
  - Max Pooling
- Global Average Pooling
- Fully connected layer with Dropout
- Sigmoid output for binary classification

---

## Training Details
- Optimizer: **Adam**
- Learning rate: **0.001**
- Loss function: **Binary Cross-Entropy**
- Epochs: **15**
- Batch size: **32**
- Class imbalance handled using **class weights**
- Best model saved using **ModelCheckpoint**

---

## Evaluation Metrics

The proposed method is evaluated using multiple metrics to ensure reliability:

- Accuracy
- Precision
- Recall
- F1-score
- **True Positive Rate (TPR)**
- **True Negative Rate (TNR)**
- **False Positive Rate (FPR)**
- **False Negative Rate (FNR)**
- **Matthews Correlation Coefficient (MCC)**
- Confusion Matrix

Comparative analysis and robustness evaluation are performed against baseline CNN-based approaches.

---

## Results
- Accuracy ranging from **97% to 100%** across datasets.
- High precision, recall, and F1-score.
- Strong robustness against:
  - Noise
  - JPEG compression
  - Rotation
  - Scaling

---

## Limitations
- Training requires GPU acceleration for large-scale datasets.
- Performance may degrade for unseen or novel forgery techniques.
- Dataset imbalance can affect minority class prediction.

---

## Tools & Technologies
- Python
- TensorFlow / Keras
- PyWavelets
- OpenCV
- NumPy
- Scikit-learn
- Matplotlib / Seaborn
- Google Colab

---

## Usage

```bash
git clone https://github.com/drmahmoudatef/SWT-CNN-Model.git
