# Image Forgery Detection Project

**Hybrid SWT + CNN Model for Copy-Move and Splicing Forgery Detection**

[![GitHub Stars](https://img.shields.io/github/stars/drmahmoudatef/SWT-CNN-Model?style=for-the-badge)](https://github.com/drmahmoudatef/SWT-CNN-Model/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/drmahmoudatef/SWT-CNN-Model?style=for-the-badge)](https://github.com/drmahmoudatef/SWT-CNN-Model/network)
[![GitHub Actions](https://github.com/drmahmoudatef/SWT-CNN-Model/workflows/README%20build/badge.svg)](https://github.com/drmahmoudatef/SWT-CNN-Model/actions)

---

## 1. Description

This repository implements a hybrid image forgery detection method combining **Stationary Wavelet Transform (SWT)** for enhanced feature extraction with a **Convolutional Neural Network (CNN)** classifier.  
The model aims to detect both **copy-move** and **splicing** forgeries across multiple benchmark datasets.

---

## 2. Datasets Used

| Forgery Type | Dataset | Source / Link |
|--------------|---------|---------------|
| Copy-Move    | GRIP | https://github.com/greatzh/Image-Forgery-Datasets-List#GRIP |
| Copy-Move    | COVERAGE | https://github.com/greatzh/Image-Forgery-Datasets-List#COVERAGE |
| Copy-Move    | MICC-F200 | https://www.kaggle.com/datasets/nishaahin/miccf200 |
| Copy-Move    | MICC-F2000 | https://www.kaggle.com/datasets/manas29/micc-f2000 |
| Copy-Move    | CASIA-CMFD | https://www.kaggle.com/datasets/mashraffarouk/casia-cmfd |
| Splicing     | CASIA-V1 | https://www.kaggle.com/datasets/sophatvathana/casia-dataset |
| Splicing     | CASIA-V2 | https://www.kaggle.com/datasets/divg07/casia-20-image-tampering-detection-dataset |

> ⚠️ Before training, make sure you download the datasets and place them in the correct subfolders under `/data`. Most Kaggle datasets require a free Kaggle account login.

---

---

## 4. Usage Instructions

### Clone Repository
```bash
git clone https://github.com/drmahmoudatef/SWT-CNN-Model.git
cd SWT-CNN-Model

pip install -r requirements.txt
/data/MICC-F200
/data/MICC-F2000
/data/CASIA-CMFD
/data/CASIA-V1
/data/CASIA-V2

python src/train_model.py

python src/evaluate_model.py
pip install -r requirements.txt
/results


## 3. Code Structure

The repository is organized as follows:

