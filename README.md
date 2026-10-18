After the manuscript **“Sparse-sensing battery pack temperature distribution prediction via meta-learning for unseen conditions”** is accepted, the complete dataset and source code will be organized and released publicly in this repository. All files in this repository will be written in English.

# Sparse-Sensing Battery Pack Temperature Distribution Prediction via Meta-Learning for Unseen Conditions

## Overview

This repository accompanies a research project on reconstructing and predicting the spatial temperature distribution of a battery pack from a very small number of temperature sensors. The central objective is to maintain accurate full-field temperature awareness when the battery operates under conditions that were not observed during model training.

The project combines sparse sensing, low-dimensional temperature-field representation, cross-condition knowledge transfer, and temporal prediction. Instead of treating every operating condition as an isolated task, the proposed framework learns transferable structure from multiple source conditions and adapts that knowledge to an unseen target condition with limited support information.

## Research Motivation

Reliable battery thermal management requires more than measurements at a few isolated locations. Localized hot spots and nonuniform temperature evolution may remain unobserved when sensor coverage is sparse. Increasing the number of physical sensors can improve observability, but it also increases cost, wiring complexity, packaging difficulty, and potential failure points.

This work therefore investigates a deployment-oriented alternative: infer the full battery-pack temperature field from a small, fixed set of sensors while retaining generalization across diverse and previously unseen operating conditions.

## Methodological Interpretation

The current research framework can be understood through five connected ideas:

1. **Condition-specific low-dimensional representations**  
   Temperature fields collected under different operating conditions are compressed into compact modal subspaces using proper orthogonal decomposition or an equivalent Karhunen–Loève representation.

2. **Geometry-aware cross-condition alignment**  
   The modal subspaces are treated as points on a Grassmann manifold. Logarithmic and exponential mappings provide a principled way to describe and transfer changes in temperature-field structure between operating conditions.

3. **Meta-learning for unseen conditions**  
   Knowledge learned from multiple source conditions is organized as a transferable prior. For a previously unseen target condition, the model uses limited support information to adapt the representation and prediction components without requiring full retraining from scratch.

4. **Deployable sparse-sensor reconstruction**  
   A fixed sparse-sensor layout is optimized across conditions rather than separately for each target condition. Sparse observations are then used to recover low-dimensional coefficients and reconstruct the complete temperature distribution.

5. **Spatiotemporal prediction**  
   Temporal information from battery operating signals and previously reconstructed states is used to predict the evolution of modal coefficients, which are mapped back to the full spatial temperature field.

## Intended Contributions

The project is designed to study whether a unified framework can provide:

- accurate temperature-distribution reconstruction from sparse measurements;
- robust transfer to operating conditions excluded from training;
- a fixed sensor configuration suitable for practical deployment;
- interpretable low-dimensional representations of thermal-field evolution;
- reproducible comparisons with conventional machine-learning and deep-learning baselines.

## Evaluation Scope

The experimental protocol considers multiple battery operating conditions and evaluates transfer to held-out target conditions. The main evaluation criteria include temperature prediction error, relative error, goodness of fit, stability across repeated runs, and consistency across source–target condition pairs.

Detailed datasets, preprocessing procedures, model configurations, training scripts, evaluation code, and finalized numerical results are intentionally not included at the current manuscript stage.

## Repository Status

This repository currently contains only this project overview. No dataset, source code, trained model, experimental output, or supplementary artifact has been uploaded.

After manuscript acceptance, the planned release will include:

- dataset organization and preprocessing documentation;
- model implementation and configuration files;
- training, adaptation, and evaluation pipelines;
- sparse-sensor layout procedures;
- baseline implementations and comparison protocols;
- scripts for reproducing tables and figures;
- instructions for reproducing the reported experiments.

## Citation

Citation information will be added after the manuscript is accepted and the final bibliographic record becomes available.
