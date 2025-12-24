# Automated Diabetes Classification using PyCaret (AutoML)

## Overview
This repository presents a fully automated machine learning (AutoML) pipeline for diabetes classification using PyCaret. The project demonstrates a research-oriented workflow focused on reproducibility, benchmarking, and objective model selection. It is structured and documented to be suitable for inclusion in a PhD portfolio, highlighting methodological rigor rather than ad-hoc experimentation.

## Dataset
The dataset is obtained from PyCaret’s built-in data repository using `get_data('diabetes')`. It is a binary classification dataset commonly used in medical machine learning research. The target variable is **Class variable**, representing diabetic vs non-diabetic outcomes.

## Experimental Design
The dataset is split into training (70%) and testing (30%) subsets using a fixed random seed to ensure reproducibility. All preprocessing, feature engineering, and internal validation are handled automatically by PyCaret during the experiment setup phase.

## Methodology
The experiment is initialized using PyCaret’s `setup()` function, which performs data cleaning, feature scaling, encoding, and cross-validation configuration. Multiple classification algorithms are then trained and evaluated using `compare_models()`, enabling systematic benchmarking across traditional machine learning models. The best-performing model is selected automatically using PyCaret’s AutoML routine with accuracy as the optimization metric. Hyperparameter tuning is subsequently applied to improve generalization performance. The tuned model is finally evaluated on a held-out test set to assess real-world predictive capability.

## Model Evaluation
Predictions are generated on unseen test data, and classification accuracy is computed using scikit-learn’s `accuracy_score`. This ensures that performance metrics reflect genuine generalization rather than training or validation leakage.

## Results
The AutoML pipeline successfully identifies an optimal classifier and improves its performance through automated hyperparameter tuning. The final accuracy score represents the model’s performance on completely unseen data, providing a reliable baseline for comparison with more complex models such as deep neural networks.

## Tools and Technologies
Python, PyCaret, Scikit-learn, Pandas, NumPy, and AutoML-based model selection and optimization techniques are used throughout this project.

## Research Significance
This project demonstrates a scalable, transparent, and reproducible approach to medical classification problems. It is particularly relevant for PhD-level research in artificial intelligence, biomedical engineering, and data science, where rapid benchmarking and objective model selection are essential. The workflow can be extended to other clinical datasets or used as a baseline before deploying deep learning architectures.

## Disclaimer
This project is intended strictly for academic and research purposes. It is not designed for clinical deployment or real-world medical diagnosis without appropriate medical validation.

## Author
This repository reflects a research-driven AutoML implementation developed for academic use and PhD portfolio presentation.
