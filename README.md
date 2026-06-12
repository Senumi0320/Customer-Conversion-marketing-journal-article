# Predicting Customer Conversion in Digital Marketing: A Multi-Channel Perspective

This repository contains the full analytical pipeline, code, and supporting materials for the journal article *"Predicting Customer Conversion in Digital Marketing: A Multi-Channel Perspective."* The study investigates the factors that predict customer conversion across multiple digital marketing channels, using logistic regression as an interpretable primary model alongside tree-based benchmark classifiers.

## Overview

The analysis examines how customer demographics, campaign characteristics, and engagement metrics influence the probability of conversion. The central finding is that customer engagement and campaign design predict conversion far more strongly than demographic characteristics.

## Repository Contents

| File | Description |
|------|-------------|
| `Customer_Conversion_Analysis.ipynb` | The complete Jupyter notebook implementing the full analysis pipeline: data preprocessing, exploratory data analysis, model fitting, evaluation, and statistical tests. |
| `README.md` | This file. |

## Data Sources

The study uses two publicly available datasets from Kaggle. These are **not** included in the repository and should be downloaded directly from the sources below:

1. **Predict Conversion in Digital Marketing Dataset** (primary, customer-level, 8,000 records)
   El Kharoua, R. (2024). Kaggle.
   https://www.kaggle.com/datasets/rabieelkharoua/predict-conversion-in-digital-marketing-dataset

2. **Marketing Campaign Performance Dataset** (supporting, campaign-level, social platforms)
   Bhatt, M. (2023). Kaggle.
   https://www.kaggle.com/datasets/manishabhatt22/marketing-campaign-performance-dataset

After downloading, place the CSV files in the same directory as the notebook.

## Methods

The analytical pipeline includes:

- **Preprocessing** — one-hot encoding of categorical variables, z-score standardisation of numeric features, and an 80:20 stratified train/test split.
- **Class imbalance handling** — class weighting applied during model fitting to address the imbalanced outcome (approximately 87.6% converted vs 12.4% not converted).
- **Primary model** — binary logistic regression, reported with interpretable odds ratios.
- **Benchmark models** — random forest and gradient boosting, for an accuracy-versus-interpretability comparison.
- **Statistical checks** — variance inflation factors (VIF) for multicollinearity, five-fold stratified cross-validation for robustness, and chi-square tests of independence for categorical campaign variables.
- **Cross-platform analysis** — descriptive benchmarking of conversion rate, ROI, and acquisition cost across social platforms using the supporting dataset.

## Requirements

The analysis was conducted in Python 3. The following libraries are required:

```
pandas
numpy
scikit-learn
statsmodels
scipy
matplotlib
seaborn
```

Install them with:

```bash
pip install pandas numpy scikit-learn statsmodels scipy matplotlib seaborn
```

## Reproducing the Results

1. Clone this repository:
   ```bash
   git clone https://github.com/Senumi0320/Customer-Conversion-marketing-journal-article.git
   ```
2. Download the two Kaggle datasets (links above) and place the CSV files in the repository directory.
3. Open and run `Customer_Conversion_Analysis.ipynb` from top to bottom in Jupyter or Google Colab.

Running the notebook reproduces all figures, tables, and statistical results reported in the article.

## Citation

If you reference this work, please cite the associated journal article.

## License

This repository is provided for academic and educational purposes.
