# Artificial Intelligence-Driven Life Cycle Assessment of Injectable Aesthetic Products: A Multi-Regional and Temporal Sustainability Analysis

This repository contains the complete source code, datasets, trained models, analysis outputs, and publication-quality figures associated with the study:

**Firat, Y. and Sarikaya, H.A. (2024). Artificial Intelligence-Driven Life Cycle Assessment of Injectable Aesthetic Products: A Multi-Regional and Temporal Sustainability Analysis. Black Sea Journal of Engineering and Science.**

## Overview

This study develops an AI-enhanced Life Cycle Assessment (AI-LCA) framework to evaluate the carbon footprint of injectable aesthetic products across four geographic regions (European Union, United States, Asia-Pacific, and Turkey) over a five-year period (2020-2024). A Random Forest regression model was trained on a systematically expanded dataset to predict environmental impacts with high accuracy.

**Key findings:**

- The model achieved R² = 0.954, RMSE = 0.132, and MAE = 0.075 on the test set.

- Product type (~57%) and cold chain requirement (~39%) are the dominant factors determining carbon footprint.

- Cold chain logistics increase the carbon footprint by approximately 7.8 times.

- The Asia-Pacific region exhibits the highest carbon footprint (54.83 kg CO2e), approximately 189% higher than the EU.

- An 8.5% reduction in carbon footprint was observed across all regions from 2020 to 2024.

## Repository Structure

```
AI_LCA_Complete_Codes/
  final_codes_package/
  |
  |-- codes/
  |     ai_lca_models.py              AI-LCA model architecture and definitions
  |     expanded_model_training.py     Main model training script (Random Forest)
  |     generate_graphics.py           Generation of Figures 3-7
  |     model_usage.py                 Model inference and usage examples
  |     simple_ai_test.py              Quick model validation test
  |
  |-- data/
  |     expanded_aesthetic_products_dataset.csv   Base dataset (300 records)
  |     improved_dataset.csv                      Quality-enhanced dataset (498 records)
  |     regional_expanded_dataset.csv             Regionally expanded dataset (1,992 records)
  |     temporal_expanded_dataset.csv             Temporally expanded dataset (9,960 records)
  |
  |-- graphics/
  |     figure1_600dpi.jpg             Dataset evolution and analysis framework
  |     figure2_flowchart.jpg          AI-Enhanced LCA model architecture
  |     figure3_enhanced.jpg           AI model performance and feature importance
  |     figure4_enhanced.jpg           Correlation heatmap of dataset features
  |     figure5_enhanced.jpg           Carbon footprint comparison of products
  |     figure6_enhanced.jpg           Environmental impact analysis by category
  |     figure7_enhanced.jpg           Impact of cold chain on carbon footprint
  |     figure8_enhanced.jpg           Multi-regional and temporal analysis
  |
  |-- graphics_codes/
  |     figure3_enhanced.py            Code for Figure 3
  |     figure4_enhanced.py            Code for Figure 4
  |     figure5_enhanced.py            Code for Figure 5
  |     figure6_enhanced.py            Code for Figure 6
  |     figure7_enhanced.py            Code for Figure 7
  |     pasted_file_JNsSEk_figure1_600dpi.py       Code for Figure 1
  |     pasted_file_jSlG6O_figure2_flowchart.py    Code for Figure 2
  |     pasted_file_SQrZmP_figure8_enhanced.py     Code for Figure 8
  |
  |-- models/
  |     expanded_ai_lca_model.pkl      Trained AI-LCA model (Random Forest)
  |     expanded_final_model.pkl       Final expanded model with full dataset
  |
  |-- analysis/
  |     analysis_results.json          Model performance metrics and key findings
  |
  |-- README.md
```

## Datasets

The study employs a four-stage dataset development process:

| Stage | Records | Description |
| --- | --- | --- |
| Base dataset | 300 | Six injectable products, 50 records each |
| Quality-enhanced | 498 | Monte Carlo simulation and parameter variation |
| Regional expansion | 1,992 | Four regions with region-specific environmental factors |
| Temporal expansion | 9,960 | Five-year period (2020-2024) with temporal factors |

**Products analyzed:** Botox 100U, Dysport 300U, Xeomin 100U, Restylane 1 mL, HA Filler 1 mL, Sculptra 5 mL.

**Regions covered:** European Union, United States, Turkey, Asia-Pacific.

## Requirements

The following Python packages are required:

```
pandas
numpy
matplotlib
seaborn
scikit-learn
joblib
```

Install all dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn joblib
```

## Usage

**Train the model:**

```bash
cd AI_LCA_Complete_Codes/final_codes_package/codes/
python expanded_model_training.py
```

**Generate figures:**

```bash
cd AI_LCA_Complete_Codes/final_codes_package/graphics_codes/
python figure3_enhanced.py
python figure4_enhanced.py
python figure5_enhanced.py
python figure6_enhanced.py
python figure7_enhanced.py
python pasted_file_SQrZmP_figure8_enhanced.py
```

**Run model inference:**

```bash
cd AI_LCA_Complete_Codes/final_codes_package/codes/
python model_usage.py
```

## Model Performance

| Metric | Value |
| --- | --- |
| R² (test set) | 0.954 |
| RMSE | 0.132 kg CO2e |
| MAE | 0.075 kg CO2e |
| Algorithm | Random Forest Regressor |
| Number of trees | 200 |
| Maximum depth | 15 |
| Cross-validation R² (mean) | 0.954 (std: 0.018) |

## Environmental Impact Results

| Product | Carbon Footprint (kg CO2e) | Cold Chain |
| --- | --- | --- |
| Botox 100U | 1.600 | Yes |
| Dysport 300U | 1.494 | Yes |
| Xeomin 100U | 0.349 | No |
| Restylane 1 mL | 0.176 | No |
| HA Filler 1 mL | 0.151 | No |
| Sculptra 5 mL | 0.111 | No |

## Contact

Yelda Firat - [yelda.firat@mudanya.edu.tr](mailto:yelda.firat@mudanya.edu.tr)

Mudanya University, Faculty of Engineering, Architecture and Design, Department of Computer Engineering, Bursa, Turkey
