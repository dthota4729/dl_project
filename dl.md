
# Brain Tumor Detection and Segmentation using CNN and U-Net with Explainable AI

## Project Overview

This project aims to develop an end-to-end deep learning pipeline for **automated brain tumor detection and segmentation** from MRI scans. It leverages **EfficientNet** for classification, **U-Net** for segmentation, and **Grad-CAM** for explainable AI to make predictions interpretable for medical professionals.

---

## Project Structure

```
├── model_final_script.ipynb       # Final notebook with code implementation
├── /data                          # MRI images and segmentation masks
├── /models                        # Saved models (EfficientNet, U-Net)
├── /outputs                       # Plots, Grad-CAM heatmaps, segmentation results
└── README.md                      # Project documentation
```

---

## Key Features

- **Tumor Classification** using EfficientNet (normal vs. tumor)
- **Tumor Segmentation** using U-Net
- **Explainability** via Grad-CAM visualizations
- **Performance Metrics:** Accuracy, Precision, Recall, F1 Score, Dice Coefficient, IoU
- **Statistical Tests** included (e.g., Wilcoxon test) for result validation

---

## Sample Workflow

1. **Input:** Brain MRI Image
2. **Classification:** EfficientNet detects presence of tumor
3. **Segmentation:** U-Net segments the tumor region (if tumor present)
4. **Explainability:** Grad-CAM highlights important regions

---

## Results & Evaluation

- **Classification Accuracy:** ~96%
- **Segmentation Dice Score:** ~0.88
- **IoU:** ~0.79
- **Grad-CAM:** Successfully highlights tumor regions in explainable format
- **Wilcoxon Test:** Used to validate performance differences

---

## Technologies Used

- **Frameworks:** PyTorch, OpenCV, Matplotlib
- **Models:** EfficientNet, U-Net
- **Explainability:** Grad-CAM
- **Environment:** Google Colab / Jupyter Notebook with GPU

---

## Dataset

- **LGG Brain MRI Dataset** (T1-weighted MRI slices with segmentation masks)
- Includes both **grayscale and RGB** images
- Preprocessing steps: normalization, resizing, augmentation

---

## How to Run

1. Clone the repo and open `model_final_script.ipynb`
2. Set dataset path and run each cell sequentially
3. Trained models can be reused for inference
4. Results (segmentation, heatmaps) are saved in `/outputs` folder

---

## Future Work

- Improve generalizability across datasets (e.g., BraTS, multi-institution data)
- Integrate multi-modal imaging (PET + MRI)
- Develop real-time web interface using Flask/Django

---

## References

- Selvaraju et al. (2017). **Grad-CAM: Visual Explanations from Deep Networks**
- Isensee et al. (2021). **nnU-Net for Biomedical Image Segmentation**
- Litjens et al. (2017). **A Survey on Deep Learning in Medical Imaging**
