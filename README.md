## Title

**Hybrid SWT-CNN Model for Image Forgery Detection**

---

## Description

This project presents a **hybrid deep learning framework** for detecting **copy-move** and **splicing image forgeries**.
The proposed method integrates the **Stationary Wavelet Transform (SWT)** with a custom-designed **Convolutional Neural Network (CNN)** to enhance feature representation and improve detection accuracy and robustness under various post-processing operations.

---

## Dataset Information

All datasets used in this project are **publicly available** and downloaded from **Kaggle**.
After downloading, each dataset is reorganized into **Train / Validation / Test** splits on **Google Drive** and accessed through **Google Colab**.

### Copy-Move Forgery Datasets

* **MICC-F2000**
  [https://www.kaggle.com/datasets/manas29/micc-f2000](https://www.kaggle.com/datasets/manas29/micc-f2000)
* **MICC-F200**
  [https://www.kaggle.com/datasets/nishaahin/miccf200](https://www.kaggle.com/datasets/nishaahin/miccf200)
* **CASIA-CMFD**
  [https://www.kaggle.com/datasets/mashraffarouk/casia-cmfd](https://www.kaggle.com/datasets/mashraffarouk/casia-cmfd)
* **GRIP**
  [https://github.com/greatzh/Image-Forgery-Datasets-List](https://github.com/greatzh/Image-Forgery-Datasets-List)
* **COVERAGE**
  [https://github.com/greatzh/Image-Forgery-Datasets-List](https://github.com/greatzh/Image-Forgery-Datasets-List)

### Splicing Forgery Datasets

* **CASIA V1**
  [https://www.kaggle.com/datasets/sophatvathana/casia-dataset](https://www.kaggle.com/datasets/sophatvathana/casia-dataset)
* **CASIA V2**
  [https://www.kaggle.com/datasets/divg07/casia-20-image-tampering-detection-dataset](https://www.kaggle.com/datasets/divg07/casia-20-image-tampering-detection-dataset)

---

## Code Information

The implementation is written in **Python** and executed using **Google Colab**.
The code covers the full experimental pipeline as follows:

* Mounting Google Drive for dataset access.
* Image preprocessing and resizing.
* Applying **Stationary Wavelet Transform (SWT)** using the Haar wavelet.
* Generating four sub-bands (LL, LH, HL, HH) and stacking them into a **4-channel tensor**.
* Custom data generator based on `keras.utils.Sequence`.
* CNN model construction and training.
* Model evaluation using confusion matrix and advanced statistical metrics.

All steps are explicitly implemented in the provided Colab notebook.

---

## Usage Instructions

1. Clone the repository:

   ```bash
   git clone https://github.com/drmahmoudatef/SWT-CNN-Model.git
   ```
2. Upload datasets to Google Drive and organize them into:

   ```
   dataset/
     ├── train/
     ├── val/
     └── test/
   ```
3. Open the notebook in **Google Colab**.
4. Mount Google Drive when prompted.
5. Run all cells sequentially to train and evaluate the model.

---

## Requirements

The following libraries and tools are required:

* Python 3.x
* TensorFlow / Keras
* PyWavelets
* NumPy
* OpenCV
* Scikit-learn
* Matplotlib
* Seaborn
* Pillow
* Google Colab (recommended)

---

## Methodology

1. Load images from Google Drive.
2. Resize images to **224 × 224**.
3. Convert images to grayscale when necessary.
4. Apply **Stationary Wavelet Transform (SWT)** to obtain LL, LH, HL, HH sub-bands.
5. Stack the sub-bands to form a **4-channel input**.
6. Train a CNN model using SWT-based features.
7. Handle class imbalance using **class weights**.
8. Evaluate the trained model on unseen test data.

---

## Evaluation

The model is evaluated using multiple performance metrics to ensure reliability:

* Accuracy
* Precision
* Recall
* F1-score
* True Positive Rate (TPR)
* True Negative Rate (TNR)
* False Positive Rate (FPR)
* False Negative Rate (FNR)
* Matthews Correlation Coefficient (MCC)
* Confusion Matrix

---

## Citations

If you use any of the datasets or the proposed methodology, please cite the original dataset providers and relevant academic publications associated with SWT and CNN-based image forgery detection.

---

## License & Contribution Guidelines

* This project is intended for **research and academic use**.
* Dataset licenses follow the terms specified by their original providers.
* Contributions, improvements, and issue reports are welcome via GitHub pull requests.

---

*This README provides a complete and reproducible description of the Hybrid SWT-CNN Image Forgery Detection framework.*
