# Step 5: Machine Learning Model Comparison

## Purpose
This step evaluates and compares the performance of the Transformer model with classical machine learning models to validate predictive robustness.

## Input
- labeled_dataset.csv: Dataset with binary labels obtained from Step 3.

## Code
- fingerprint_generation.ipynb: Generates ECFP4 molecular fingerprints.
- rf_xgboost_models_ecfp4_training.ipynb: Trains Random Forest and XGBoost models using ECFP4 fingerprints.
- model_comparison_plots.ipynb: Visualizes and compares model performance metrics.

## Output
- rf_results.csv: Random Forest performance metrics.
- xgboost_results.csv: XGBoost performance metrics.
- comparison_metrics.csv: Combined performance comparison of all models.
- roc_comparison.png: ROC curve comparison across models.
- mcc_comparison.png: MCC comparison across models.
- accuracy_comparison.png: Accuracy comparison across models.

## Method
- ECFP4 fingerprints (radius = 2, nBits = 2048) were generated as molecular descriptors.
- Random Forest and XGBoost models were trained using identical training and test splits.
- Model performance was evaluated using AUC, accuracy, MCC, F1-score, sensitivity, and specificity.
- Results were compared against the Transformer model to assess relative performance.

## How to run
Execute notebooks in sequence:

```bash
jupyter notebook code/fingerprint_generation.ipynb
jupyter notebook code/rf_xgboost_models_ecfp4_training.ipynb
jupyter notebook code/model_comparison_plots.ipynb