---
title: "Credit card fraud"
date: 2026-05-04

links:
  - name: Repo
    url: "https://github.com/kgupta9191/Credit-card-Fraud"
    icon: brands/github

  - name: PDF
    url: "report.pdf"

tags:
  - Class imbalance
  - Deep Neural Network
  - Classification
---

## Background

Credit card fraud detection is a critical problem in financial systems due to increasing online transactions and evolving fraud techniques. A key challenge is the highly imbalanced nature of the data, where fraudulent transactions represent a very small fraction of total transactions (≈0.17%) . Traditional methods struggle with such imbalance, making machine learning approaches more suitable for detecting complex fraud patterns.

<!--more-->

## Objectives

The objective of this project is to develop a neural network based model for accurate fraud detection on an imbalanced dataset. The model aims to:

- Effectively identify fraudulent transactions
- Handle class imbalance using weighted loss functions

## Computational Environment

The model is trained on a GPU-enabled system with the following configuration:
- CUDA Version: 12.6
- cuDNN Version: 8.9.7
- GPU: NVIDIA A16
- Framework: PyTorch (with torch.compile optimization)


## Results

The confusion matrix highlights the strong classification performance of the trained model. It correctly classifies 28,413 non-fraudulent transactions and 49 fraudulent transactions, with only 11 false positives and 9 false negatives.

<img src="/images/credit_card_fraud.png" style="width:100%; max-width:900px;">

