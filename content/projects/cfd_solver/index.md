---
title: "Incompressible Flow Solver"
date: 2026-05-04

links:
  - name: Repo
    url: "https://github.com/kgupta9191/Fluid-Dynamics-Solver"
    icon: brands/github

  - name: PDF
    url: "report.pdf"

tags:
  - Flow solver
  - Single-phase CFD
  - Fluid Dynamics
---

## Background

The lid-driven cavity problem is a classical benchmark in computational fluid dynamics used to evaluate and validate numerical solvers for incompressible, single-phase flows. In this problem, the fluid is enclosed inside a square cavity, where the top wall moves tangentially with a prescribed velocity while the remaining walls are stationary and satisfy the no-slip boundary condition. The motion of the upper lid drives circulation inside the cavity, producing characteristic vortex structures whose strength and location depend strongly on the Reynolds number. Because of its simple geometry but rich flow behavior, the lid-driven cavity problem is widely used to test numerical schemes, boundary-condition implementation, pressure–velocity coupling, and grid resolution effects.

<!--more-->

## Objectives

The objective of this project is to develop and test a customized CFD solver for the lid-driven cavity problem and investigate how geometric modification and Reynolds number influence the internal flow structure. The solver is used to compute the incompressible flow field inside a square cavity driven by the motion of the top wall. A cut-off region is introduced near the lower-left corner to examine how local blockage alters vortex formation and flow symmetry.

## Computational Environment

The model is trained on a CPU-enabled system with the following configuration:
- Cluster: Unity
- Framework: python


## Results

The customized single-phase CFD solver successfully reproduces the key flow features of the lid-driven cavity problem. The velocity profiles show good agreement with the benchmark data of Ghia et al., confirming the reliability of the solver for incompressible single-phase flow simulations.

<img src="/images/cfd_solver.png" style="width:100%; max-width:900px;">

