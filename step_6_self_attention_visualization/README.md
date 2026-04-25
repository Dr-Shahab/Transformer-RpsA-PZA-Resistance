# Step 6: Self-Attention Visualization

## Purpose
This step visualizes the self-attention mechanism of the trained Transformer model to interpret how different parts of the SMILES sequences contribute to predictions.

## Input
- sample_compounds.csv: Selected compounds for attention analysis.
- trained_transformer_model.pt: Trained Transformer model obtained from Step 4.
- tokenizer_config.json: Tokenizer configuration for SMILES encoding.

## Code
- attention_visualization.ipynb: Extracts and visualizes attention weights from the Transformer model.

## Output
- attention_heatmap_1.png: Attention map for sample compound 1.
- attention_heatmap_2.png: Attention map for sample compound 2.
- attention_scores.csv: Numerical attention weight values.

## Method
- SMILES strings were tokenized using the trained tokenizer.
- Attention weights were extracted from Transformer encoder layers.
- Heatmaps were generated to highlight important tokens contributing to predictions.

## How to run
Execute notebook:

```bash
jupyter notebook code/attention_visualization.ipynb