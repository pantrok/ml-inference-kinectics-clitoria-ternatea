# Machine-Learning-Assisted UV-Vis Inference and Kinetic Modeling of *Clitoria ternatea*

This repository contains the complete computational framework, empirical datasets, and Machine Learning workflows developed for the instantaneous inference and physics-informed kinetic modeling of *Clitoria ternatea* horticultural extracts.

## Project Description

The recovery of thermolabile bioactive compounds (anthocyanins and phenolics) presents analytical challenges due to simultaneous thermal degradation and matrix effects. This project proposes a **Physics-Informed Machine Learning (PIML)** approach to:
1. Infer instantaneous concentrations by decoupling target chemical responses from thermal degradation noise (overcoming the limitations of the conventional Beer-Lambert law).
2. Estimate macroscopic extraction rate constants ($k_{ext}$) by coupling a phenomenological extraction-degradation model with Monte Carlo simulations and optimized Random Forest regressors.

## Repository Structure

The computational workflow is strictly modularized to ensure the exact reproducibility of the figures and tables presented in the scientific manuscript:

- `dataset.csv`: Empirical dataset derived from the factorial extraction design.
- `script_1_eda_pairplot.py`: Exploratory Data Analysis (EDA) and bivariate correlations.
- `script_2_instantaneous_inference.py`: Multivariable inference with strict Leave-One-Batch-Out validation (Generates Table 1 and Figure 3).
- `script_3_feature_importance.py`: Gini impurity reduction extraction to interpret the algorithm's decision-making process (Generates Figure 4).
- `script_4_ablation_study_global.py`: Iterative algorithmic ablation study demonstrating the necessity of the multivariate space (Generates Figure 5).
- `script_5_augmented_kinetic_prediction.py`: Phenomenological variance filtering, Monte Carlo data augmentation, and predictive mapping for extraction kinetics (Generates Tables 2 and 3, and Figure 6).
- `main_workflow.ipynb`: Master Jupyter Notebook orchestrating the sequential execution of all analytical scripts.

## Installation and Usage Instructions

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/yourusername/clitoria-ternatea-ml-kinetics.git](https://github.com/yourusername/clitoria-ternatea-ml-kinetics.git)
   cd clitoria-ternatea-ml-kinetics