# Step 4: Transformer Model Development and Evaluation

## Purpose
This step develops, trains, and evaluates a Transformer-based deep learning model for predicting compound activity against *Mycobacterium tuberculosis*.

## Input
- labeled_dataset.csv: Dataset with binary labels obtained from Step 3.

## Code
- tokenizer_and_vocab.ipynb: Builds SMILES tokenizer and vocabulary.
- train_transformer_model.ipynb: Trains the Transformer model.
- chemical_space_analysis.ipynb: Visualizes chemical space using t-SNE.
- metrics_evaluation.ipynb: Computes evaluation metrics (AUC, accuracy, MCC, F1, precision, sensitivity, specificity).
- roc_curve_plot.ipynb: Generates ROC curve.
- training_curves_plot.ipynb: Plots loss and MCC curves.

## Output
- model_weights.pt: Trained Transformer model.
- predictions.csv: Model predictions on test set.
- performance_metrics.csv: Evaluation results.
- roc_curve.png: ROC curve visualization.
- loss_curve.png: Training loss curve.
- mcc_curve.png: MCC progression.
- chemical_space_tsne.png: Chemical space visualization.

## Method
- SMILES strings were tokenized and encoded into numerical sequences.
- A Transformer encoder architecture was used for feature extraction.
- Model training used stratified data splits and repeated experiments with different random seeds.
- Performance was evaluated using multiple classification metrics, with MCC as the primary metric.

## How to run
Execute notebooks in sequence:

```bash
jupyter notebook code/tokenizer_and_vocab.ipynb
jupyter notebook code/train_transformer_model.ipynb
jupyter notebook code/metrics_evaluation.ipynb
jupyter notebook code/roc_curve_plot.ipynb
jupyter notebook code/training_curves_plot.ipynb