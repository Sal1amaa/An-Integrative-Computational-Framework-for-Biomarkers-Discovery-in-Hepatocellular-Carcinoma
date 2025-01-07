Machine Learning-Driven Identification of Biomarkers in Hepatocellular Carcinoma

Project Description

This project implements a machine learning pipeline to identify key biomarkers from RNA-Seq data for hepatocellular carcinoma (HCC). Using SHAP (SHapley Additive exPlanations) values derived from a CatBoost classifier, the project highlights the most influential genes contributing to HCC classification. The pipeline optimizes feature selection, reduces redundancy, and links selected genes to biological pathways through functional enrichment analysis.

Customizable Features

Hyperparameter Tuning: Optimize CatBoost parameters, including learning rate, depth, and iterations, to achieve the best performance.

Feature Selection: Use SHAP values to rank genes by importance, with options for redundancy removal via correlation analysis.

Functional Enrichment: Leverage GProfiler to analyze biological significance and identify enriched pathways linked to selected genes.

Cross-Validation: Ensure robust evaluation of model performance.

Prerequisites

This project requires the following dependencies:

Python 3.8+

Pandas: Data manipulation and analysis.

NumPy: Numerical computations.

CatBoost: Machine learning model.

SHAP: Explainable AI for feature importance.

Matplotlib: Visualization of results.

GProfiler: Functional enrichment analysis.

Usage

Prepare Your Data

Ensure the RNA-Seq data is formatted as a CSV file with:

Rows representing samples.

Columns representing genes.

A binary classification label as the last column.

A sample identifier as the first column.

Run the Pipeline

Train and Evaluate:

from pipeline import run_pipeline
results = run_pipeline(
data="your_data.csv",
population_size=50,
num_generations=25,
max_selected_features=120,
crossover_prob=0.1,
mutation_prob=0.1,
fitness_function="SHAP"
)

Visualize Results:
Generate plots for fitness vs. generations or enriched pathways using Matplotlib.

Run Experiments:
Test multiple hyperparameter combinations by preparing a parameter list and calling:

run_experiments(parameters_list)

Compare Approaches

Evaluate the selected features against standard methods such as Recursive Feature Elimination or Mutual Information.

Author

Islam
