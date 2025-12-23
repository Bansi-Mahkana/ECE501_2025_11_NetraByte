# Label-Free Cell Detection Using Traditional Image Processing

This project presents a **classical image processing–based pipeline** for **cell detection, segmentation, and counting** in label-free phase-contrast microscopy images using the **LIVECell dataset**, without employing deep learning techniques.

---

## Overview

Automated cell detection is a critical step in biomedical image analysis.  
This project focuses on designing an **interpretable and computationally efficient** solution using **traditional image processing techniques** to segment and count cells.

The pipeline is evaluated on the **BV-2 cell line subset** of the LIVECell dataset.

---

## Methodology

Two segmentation approaches are implemented to handle different cell distributions:

### 1. Scattered / Distinct Cells
- Gaussian blurring for noise reduction
- Thresholding and dilation
- Connected component analysis
- Edge enhancement using Laplacian filtering
- Morphological cleaning for refined segmentation

### 2. Overlapping Cells
- Contrast enhancement using CLAHE (Contrast Limited Adaptive Histogram Equalisation)
- Gaussian blurring
- Adaptive thresholding
- Laplacian edge detection
- Morphological operations for boundary refinement

Each approach generates a **binary segmentation mask**, which is compared against **ground-truth annotations**.

---

## Dataset

- **LIVECell Dataset**
- Label-free phase-contrast microscopy images
- Pixel-level annotations provided in **COCO format**
- **BV-2 cell line subset** used for evaluation

---

## Tools & Libraries

- Python
- OpenCV
- NumPy
- Matplotlib
- pycocotools

---

## Results

- Achieves **high accuracy for scattered cells** (up to ~98%)
- Demonstrates **consistent performance** on overlapping cell regions
- Detects some cells missing in ground-truth annotations, indicating **strong boundary sensitivity**

---

## Conclusion

This project demonstrates that traditional image processing techniques, when carefully designed and tuned, can effectively segment and count cells in challenging microscopy images.  
It offers a **lightweight and interpretable alternative** to deep-learning-based methods.

---

## Team Members

- Aashi Shah
- Bansi Mahkana
- Diya Patel
- Nirjara Jain

**School of Engineering and Applied Science (SEAS)**  
**Ahmedabad University**
