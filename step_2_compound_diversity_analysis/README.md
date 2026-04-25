# Step 2: Compound Diversity Analysis

## Purpose
This step evaluates the structural and physicochemical diversity of the curated *Mycobacterium tuberculosis* dataset to ensure broad chemical space coverage for robust model development.

## Input
- curated_mtb_dataset.csv: Preprocessed dataset obtained from Step 1.

## Code
- structural_diversity_analysis.ipynb: Generates MACCS fingerprints (166 bits) and computes pairwise Tanimoto similarity.
- physicochemical_analysis.ipynb: Calculates molecular descriptors including molecular weight (MW), LogP, hydrogen bond donors (HBD), and hydrogen bond acceptors (HBA).

## Output
- tanimoto_similarity.csv: Pairwise structural similarity values.
- diversity_distribution.png: Distribution of Tanimoto similarity scores.
- physicochemical_properties.csv: Calculated molecular descriptors.
- property_distribution.png: Distribution of physicochemical properties.

## How to run
Execute the notebooks:

```bash
jupyter notebook code/structural_diversity_analysis.ipynb
jupyter notebook code/physicochemical_analysis.ipynb