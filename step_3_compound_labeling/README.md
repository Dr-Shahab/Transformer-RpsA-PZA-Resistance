# Step 3: Compound Labeling

## Purpose
This step converts continuous minimum inhibitory concentration (MIC) values into binary classification labels (sensitive vs resistant) for supervised machine learning.

## Input
- curated_mtb_dataset.csv: Preprocessed dataset obtained from Step 1.

## Code
- mic_distribution_analysis.ipynb: Analyzes the distribution of MIC values and visualizes data spread.
- compound_labeling.ipynb: Assigns binary labels based on the selected MIC threshold.

## Output
- labeled_dataset.csv: Dataset with binary labels for machine learning.
- mic_distribution_plot.pdf: Distribution of MIC values.
- mic_log_distribution_plot.pdf: Log-transformed MIC distribution.

## Method
- MIC values were analyzed to assess distribution characteristics.
- The MIC distribution exhibited skewness and presence of extreme values.
- Therefore, the median MIC value was selected as the classification threshold to ensure robustness against outliers.
- Compounds with MIC < threshold were labeled as sensitive (1).
- Compounds with MIC ≥ threshold were labeled as resistant (0).

## How to run
Execute notebooks:

```bash
jupyter notebook code/mic_distribution_analysis.ipynb
jupyter notebook code/compound_labeling.ipynb