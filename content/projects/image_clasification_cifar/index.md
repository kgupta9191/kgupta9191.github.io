---
title: "Image Classification with CNN on CIFAR-10"
date: 2026-05-05

links:
  - name: Repo
    url: "https://github.com/kgupta9191/Image-Classification-with-CNN-on-CIFAR-10"
    icon: brands/github

  - name: PDF
    url: "report.pdf"

tags:
  - Computer vision
  - CNN
  - Transfer learning
---

## Background

Image classification is one of the fundamental problems in computer vision, where the goal is to assign a label to an input image from a predefined set of categories.Traditional machine learning approaches relied heavily on handcrafted feature extraction, which often failed to generalize across diverse datasets.

With the advancement of deep learning, Convolutional Neural Networks (CNNs) have become the standard approach for image-related tasks. However, training deep CNNs from scratch requires large datasets and significant computational resources.

To overcome this limitation, transfer learning is widely used. In transfer learning, a model pre-trained on a large dataset (such as ImageNet) is adapted to a new task. This project uses a pre-trained ResNet18 model and fine-tunes it on the CIFAR-10 dataset to achieve high classification accuracy with reduced training effort.

<!--more-->

## Objectives

The main objectives of this project are:

- To implement an image classification pipeline using CNNs.
- To apply transfer learning using a pre-trained ResNet18 model.
- To improve model performance using data augmentation techniques.
- To evaluate the model using training, validation, and test datasets.
- To demonstrate real-world prediction on external images.

## Computational Environment

The model is trained on a GPU-enabled system with the following configuration:
- CUDA Version: 12.6
- cuDNN Version: 8.9.7
- GPU: NVIDIA A16
- Framework: PyTorch (with torch.compile optimization)


## Results

The fine-tuned ResNet18 model achieves approximately 92.8% test accuracy on the CIFAR-10 dataset, demonstrating strong classification performance across all ten categories. By leveraging pre-trained ImageNet weights, the model benefits from faster convergence and improved generalization compared to training from scratch, highlighting the effectiveness of transfer learning for efficient and accurate image classification.

