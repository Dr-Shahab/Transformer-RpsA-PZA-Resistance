# Step 7: Virtual Screening

## Purpose
This step applies the trained Transformer model to screen external compound libraries and identify potential inhibitors against Mycobacterium tuberculosis.

## Input
- fda_compounds.csv: FDA-approved drug library.
- tcm_compounds.csv: Traditional Chinese Medicine (TCM) compound library.
- trained_transformer_model.pt: Trained Transformer model from Step 4.
- tokenizer_config.json: Tokenizer configuration for SMILES encoding.

## Code
- virtual_screening_fda.ipynb: Performs screening on FDA compounds.
- virtual_screening_tcm.ipynb: Performs screening on TCM compounds.

## Output
- fda_screening_results.csv: Predicted activity scores for FDA compounds.
- tcm_screening_results.csv: Predicted activity scores for TCM compounds.
- top_hits_fda.csv: Top-ranked FDA compounds based on prediction scores.
- top_hits_tcm.csv: Top-ranked TCM compounds based on prediction scores.

## Method
- External compound libraries were processed and converted into SMILES representations.
- The trained Transformer model was used to predict activity scores for each compound.
- Compounds were ranked based on predicted probabilities.
- Top candidates were selected for further structure-based validation.

## How to run
Execute notebooks:

```bash
jupyter notebook code/virtual_screening_fda.ipynb
jupyter notebook code/virtual_screening_tcm.ipynb