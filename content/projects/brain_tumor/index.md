---
title: "Brain Tumor Classification Using ResNet18"
date: 2026-05-18

links:
  - name: Repo
    url: "https://github.com/kgupta9191/Brain-Tumor-Classification"
    icon: brands/github

  - name: PDF
    url: "report.pdf"

tags:
  - Transfer Learning
  - Deep Neural Network
  - Classification
---

## Background

Brain tumors are among the most life-threatening neurological conditions, with early and accurate diagnosis being critical for effective treatment. MRI is the gold standard imaging modality for brain tumor detection, but manual interpretation by radiologists is time-consuming and subject to inter-observer variability. The four primary categories addressed in this work are:

- Glioma — the most common and aggressive primary brain tumor, originating in glial cells
- Meningioma — typically benign, arising from the meninges surrounding the brain and spinal cord
- Pituitary Tumor — affects the pituitary gland and may be hormone-secreting
- No Tumor — normal brain MRI scans serving as a negative class

Deep learning, particularly CNNs, has shown remarkable success in medical image analysis by automatically learning hierarchical features directly from pixel data. Transfer learning via ResNet18 — pretrained on ImageNet — allows the model to leverage low-level features (edges, textures) learned from natural images and adapt them to the medical domain, significantly reducing training time and data requirements.

## Objectives

- Develop a robust CNN-based classifier for multi-class brain tumor detection from MRI scans
- Apply transfer learning with ResNet18 to achieve high accuracy with limited labeled medical data
- Evaluate model performance using accuracy, loss curves, confusion matrix, and per-class classification metrics
- Provide a reproducible pipeline suitable as a baseline for clinical decision-support research


## Computational Environment

The model is trained on a GPU-enabled system with the following configuration:
- CUDA Version: 12.6
- cuDNN Version: 8.9.7
- GPU: NVIDIA A16
- Framework: PyTorch (with torch.compile optimization)


## Results

The fine-tuned ResNet18 model achieved a test accuracy of 98.25% with a test loss of 0.0485 after 20 epochs of training. Loss and accuracy curves show rapid convergence within the first 5 epochs, with both training and validation metrics remaining closely aligned throughout — indicating strong generalization with minimal overfitting.

The confusion matrix reveals near-perfect classification across all four classes. The "No Tumor" class achieved perfect separation (405/405), while Glioma (291/300), Pituitary (298/300), and Meningioma (294/306) all exceeded 96% per-class accuracy. The small number of misclassifications in Meningioma — where a few samples were confused with adjacent classes — is clinically understandable given the overlapping imaging characteristics of meningiomas with other tumor types.

Overall, these results confirm that transfer learning with ResNet18 is highly effective for multi-class brain tumor MRI classification, providing a strong and reproducible baseline for further clinical research.

