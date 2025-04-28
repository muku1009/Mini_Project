# 📁 Dataset Description

This folder contains the dataset utilized for lung cancer detection analysis using CT images. 

---

## 📌 **Dataset Source**

The dataset used in this study is publicly available from:

- **Dataset Name:** Lung Image Database Consortium and Image Database Resource Initiative (LIDC-IDRI)
- **Hosting Platform:** [The Cancer Imaging Archive (TCIA)](https://wiki.cancerimagingarchive.net/display/Public/LIDC-IDRI)

---

## 📌 **Dataset Overview**

The LIDC-IDRI dataset consists of diagnostic and lung cancer screening thoracic Computed Tomography (CT) scans with marked annotations identifying lung nodules.

- **Total Scans Available:** 1018 CT scans  
- **Annotations:** Radiologist-generated annotations for nodule locations and characteristics  
- **Format:** Images stored in DICOM (Digital Imaging and Communications in Medicine) format  
- **Image Modality:** Thoracic CT (Computed Tomography)

---

## 📌 **Dataset Features**

Each CT scan in the dataset provides:

- Multiple annotated nodules per image (where present).
- Information regarding nodule size, location, shape, and malignancy rating.
- Ground-truth labels derived from radiologists’ consensus (benign vs malignant).
- High-quality diagnostic images suitable for machine learning and deep learning applications.

---

## 📌 **Purpose of Dataset**

This dataset is widely used for:

- Lung nodule detection, segmentation, and classification.
- Development of computer-aided detection (CAD) systems for lung cancer.
- Evaluation of artificial intelligence and deep learning algorithms for medical imaging tasks.

---

## 📌 **Dataset Structure**

For convenience, the dataset used in this project has been preprocessed:

```
Dataset/
│
├── lidc_images.npy                 # Numpy array containing preprocessed CT images
├── lidc_labels.npy                 # Corresponding binary labels (0: benign, 1: malignant)
├── lidc_gan_augmented_images.npy   # GAN-generated augmented images
└── lidc_gan_augmented_labels.npy   # Corresponding labels for GAN-augmented images
```

- All images are resized to `(224 × 224 pixels)`.
- Data normalized to the range `[0, 1]`.
- Labels clearly denote nodule malignancy status.

---

## 📌 **Dataset Accessibility**

- **License:** Open access under Creative Commons Attribution 3.0 Unported License  
- **Citation:** If utilizing this dataset, cite as follows:

```text
Armato, S. G., et al. (2011). The Lung Image Database Consortium (LIDC) and Image Database Resource Initiative (IDRI): A completed reference database of lung nodules on CT scans. Medical Physics, 38(2), 915-931. doi:10.1118/1.3528204
```

---

## 📌 **How to Use**

- Download or clone this repository.
- Load `.npy` files directly into Python scripts or Jupyter notebooks using NumPy:
```python
import numpy as np

images = np.load('lidc_images.npy')
labels = np.load('lidc_labels.npy')
```

---

## 📌 **Dataset Link**

[🌐 Click here to access the original LIDC-IDRI dataset on TCIA](https://wiki.cancerimagingarchive.net/display/Public/LIDC-IDRI)


---
