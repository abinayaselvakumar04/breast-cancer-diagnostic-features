# Breast Cancer Diagnostic Features

A structured tabular dataset of breast tumor measurements, derived from digitized images of fine needle aspirate (FNA) samples of breast masses. Each record describes the mean values of eight cell nuclei characteristics computed from a sample image, alongside a diagnosis label.

## Overview

| Property | Value |
|---|---|
| Total samples | 569 |
| Features | 8 numeric mean-value features |
| Target variable | `diagnosis` (M = Malignant, B = Benign) |
| Class distribution | 357 Benign, 212 Malignant |
| Missing values | None |
| File format | CSV |

## Dataset Description

Each row represents one tumor sample. The features are computed from digitized images and describe the geometry and texture of cell nuclei present in the sample. Only the mean-value variants of each measurement are included in this file (as opposed to standard error or "worst" variants found in the full Wisconsin Diagnostic Breast Cancer dataset).

## Columns

| Column | Type | Description |
|---|---|---|
| `id` | integer | Unique identifier for each sample |
| `diagnosis` | categorical | Diagnosis result: `M` (Malignant) or `B` (Benign) |
| `radius_mean` | float | Mean distance from center to points on the perimeter |
| `texture_mean` | float | Standard deviation of gray-scale values |
| `perimeter_mean` | float | Mean perimeter of the nucleus |
| `area_mean` | float | Mean area of the nucleus |
| `smoothness_mean` | float | Mean of local variation in radius lengths |
| `compactness_mean` | float | Mean of (perimeter² / area − 1.0) |
| `concavity_mean` | float | Mean severity of concave portions of the contour |
| `concave points_mean` | float | Mean number of concave portions of the contour |

## Summary Statistics

| Feature | Min | Max | Mean |
|---|---|---|---|
| radius_mean | 6.981 | 28.110 | 14.127 |
| texture_mean | 9.710 | 39.280 | 19.290 |
| perimeter_mean | 43.790 | 188.500 | 91.969 |
| area_mean | 143.500 | 2501.000 | 654.889 |
| smoothness_mean | 0.053 | 0.163 | 0.096 |
| compactness_mean | 0.019 | 0.345 | 0.104 |
| concavity_mean | 0.000 | 0.427 | 0.089 |
| concave points_mean | 0.000 | 0.201 | 0.049 |

## Intended Use

This dataset is suitable for:

- Binary classification tasks (benign vs. malignant prediction)
- Exploratory data analysis and statistical summarization
- Feature scaling, normalization, and preprocessing exercises
- Educational use in machine learning and data science coursework
- Benchmarking classification algorithms (logistic regression, decision trees, SVM, ensemble methods, etc.)

## Data Source and Provenance

This dataset is derived from the Wisconsin Diagnostic Breast Cancer (WDBC) dataset, originally created by Dr. William H. Wolberg, W. Nick Street, and Olvi L. Mangasarian at the University of Wisconsin. The original dataset is publicly available through the UCI Machine Learning Repository. This repository contains a reduced version limited to the mean-value features described above.

## Usage Notes

- The `id` column is an identifier and should be excluded from model training.
- The `diagnosis` column should be encoded numerically (e.g., M = 1, B = 0) prior to use in most machine learning libraries.
- Feature scales vary considerably (e.g., `area_mean` versus `smoothness_mean`); normalization or standardization is recommended before training distance-based or gradient-based models.

## License

This dataset is intended for research and educational purposes. Refer to the original UCI Machine Learning Repository entry for licensing terms applicable to the source data.

## Disclaimer

This dataset is provided for educational and research purposes only. It is not intended for clinical or diagnostic use.
