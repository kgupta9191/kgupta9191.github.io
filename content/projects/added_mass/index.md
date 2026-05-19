---
title: "Added-Mass Surrogate Model"
date: 2026-05-06

links:
  - name: Repo
    url: "https://github.com/kgupta9191/Added-mass-force"
    icon: brands/github

  - name: JAX
    url: "jax_report.pdf"

  - name: PyTorch
    url: "pytorch_report.pdf"

tags:
  - JAX
  - Non-linear Regression
  - Supervised Learning
  - Surrogate Model
---

## Abstract

The prediction of added mass force during fluid–structure interaction problems, such as water entry, is computationally expensive using traditional numerical methods. This work presents a machine learning approach using neural networks to model and predict added mass forces based on input flow and geometric parameters. A deep neural network (multi-layer perceptron) is trained on simulated or experimental data to learn the nonlinear relationship between input features and resulting hydrodynamic forces. The model achieves high accuracy and demonstrates the potential of data-driven approaches for fast and efficient prediction in complex fluid dynamics problems.

## Background

In problems such as water entry, slamming, and fluid-structure interaction (FSI), the concept of added mass plays a crucial role. Added mass represents the additional inertia a body experiences due to the surrounding fluid.

However:

Traditional CFD simulations (e.g., Navier–Stokes solvers) are:
- Computationally expensive
- Time-consuming for parametric studies Experimental measurements:
- Are difficult for transient and high-speed events
- Require sophisticated setups

Therefore, there is a strong need for:
- Fast surrogate models
- Real-time prediction capability
- Reduced computational cost

## Computational Environment

The model is trained on a CPU-enabled system with the following configuration:
- Framework: PyTorch (with torch.compile optimization) and JAX


## Results

The trained surrogate model was evaluated on test sets to assess its predictive accuracy for added mass force in water-entry FSI problems. The true versus predicted plot shows all test points lying tightly along the perfect-fit diagonal (y = x), with no systematic bias or outliers, confirming that the model has successfully learned the nonlinear relationship between input flow parameters and hydrodynamic forces. The model achieves an R² score of 0.9975 and a maximum deviation of under 2% across all test samples — demonstrating that a data-driven surrogate can match CFD-level accuracy at a fraction of the computational cost, making it viable for real-time prediction and large-scale parametric studies.

<img src="/images/added_mass.png" style="width:100%; max-width:900px;">
