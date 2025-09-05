# Kerr-Coupled-QRC-supplementary
---
This repository contains some supplemetary work in the coupled Kerr QRC project which are not discussed in the paper such as algorithmic hyperparameter optimization, delay effect analysis, and data anlysis of MG series results.

*This is the README for a repository with the name **Kerr-Coupled-QRC-supplementary**, which will be public soon.
---
This repository is structured as follows:
- [finalDA](https://github.com/alikauc/Kerr-Coupled-QRC-supplementary/tree/main/finalDA) contains codes for data generation (QRC) and analysis of the MG series task, which includes data analysis techniques such as model fitting, outlier analysis, binned analysis, and correlation coefficient.
- [Delay effect](https://github.com/alikauc/Kerr-Coupled-QRC-supplementary/tree/main/delay_effect) contains the data (and the codes for generating those data) for assessing the effects of delay in the task (for how long in the future the model should predict the data) on the performance of the model and entanglement advantage. Note that the task in this section is the frequency task used in the main paper.
- [Algorithmic Hyperparameter Optimization]() This folder contains codes for running an algorithmic search through the parameter space of our Kerr QRC system, which includes the following algorithms:
  * **Deep surrogate with active learning**: A neural network-based surrogate model that learns to approximate the expensive objective function while actively selecting the most informative parameter configurations to evaluate next. The model uses uncertainty estimates to balance exploration and exploitation in the parameter space.

  * **BOHB search**: Bayesian Optimization and Hyperband (BOHB) combines the strengths of Bayesian optimization with Hyperband's principled early-stopping mechanism. It uses a tree-structured Parzen estimator (TPE) as a probabilistic model and dynamically allocates computational resources to promising configurations while terminating poor performers early.
  * **Surrogate model optimization**: Classical Bayesian optimization using Gaussian Processes as surrogate models. The method builds a probabilistic model of the objective function and uses acquisition functions (Expected Improvement, Upper Confidence Bound, or Probability of Improvement) to guide the search toward promising regions of the parameter space.
  * **Differential evolution**: A population-based evolutionary algorithm that optimizes by iteratively improving a population of candidate solutions. It uses mutation, crossover, and selection operations to evolve the population toward better solutions, making it particularly effective for non-convex, multimodal optimization landscapes without requiring gradient information. 

