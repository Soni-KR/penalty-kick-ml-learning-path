# Penalty Kick Outcome Prediction — A Beginner-Friendly ML Learning Path

An end-to-end machine-learning course built around the [Penalty Kick Outcome Prediction Challenge](https://www.kaggle.com/competitions/penalty-kick-outcome-prediction-challenge).

Instead of showing only one high-scoring model, this repository explains the decisions that lead to a solution: exploring the data, building honest baselines, preprocessing safely, comparing alternatives, validating fairly, and interpreting the final model.

## What makes this beginner-friendly?

Each chapter follows the same pattern:

1. Explain the problem and any new terminology.
2. Show a concrete example from the penalty-kick dataset.
3. Compare a small number of meaningful methods fairly.
4. Briefly introduce additional alternatives with their advantages and disadvantages.
5. Finish with the technical evidence and the theoretical reason for the decision.

All notebooks include their saved Kaggle outputs. You can read the complete analysis directly on GitHub before running anything yourself.

## Learning path

| # | Notebook | Main question |
|---:|---|---|
| 00 | [Learning roadmap](notebooks/00_Learning_Roadmap.ipynb) | How is the course organized? |
| 01 | [Exploratory data analysis](notebooks/01_Exploratory_Data_Analysis.ipynb) | What is in the data, and which issues require later decisions? |
| 02 | [Baselines and validation](notebooks/02_Baselines_and_Validation.ipynb) | What must a useful model beat, and how are scores calculated honestly? |
| 03 | [Missing values and scaling](notebooks/03_Missing_Values_and_Scaling.ipynb) | How should incomplete and differently scaled features be handled? |
| 04 | [Categorical encoding](notebooks/04_Categorical_Encoding.ipynb) | How can text categories become model inputs without leakage? |
| 05 | [Feature engineering](notebooks/05_Feature_Engineering.ipynb) | Which domain relationships can be expressed more clearly? |
| 06 | [Feature selection](notebooks/06_Feature_Selection.ipynb) | Which features contain useful signal, and which may be distractions? |
| 07 | [Dimensionality reduction](notebooks/07_Dimensionality_Reduction.ipynb) | Can many encoded inputs be compressed without losing useful information? |
| 08 | [Outlier handling](notebooks/08_Outlier_Handling.ipynb) | Are unusual observations errors, noise, or informative hard cases? |
| 09 | [Class imbalance](notebooks/09_Class_Imbalance.ipynb) | Can resampling or class weights improve minority-class prediction? |
| 10 | [Model comparison](notebooks/10_Model_Comparison.ipynb) | Which model family best fits this tabular problem? |
| 11 | [Hyperparameter optimization](notebooks/11_Hyperparameter_Optimization.ipynb) | How can model settings be tuned without overfitting validation? |
| 12 | [Ensembling](notebooks/12_Ensembling.ipynb) | Can complementary models improve one another? |
| 13 | [Calibration and thresholds](notebooks/13_Calibration_and_Thresholds.ipynb) | Are probabilities reliable, and should the cutoff remain 0.5? |
| 14 | [Interpretation and error analysis](notebooks/14_Interpretation_and_Error_Analysis.ipynb) | Why does the model make its predictions and mistakes? |
| 15 | [Final frozen solution](notebooks/15_Final_Frozen_Solution.ipynb) | How do the selected decisions fit into one reproducible pipeline? |

## Running the notebooks

The notebooks are self-contained and designed for Kaggle or Google Colab; local execution is not required.

### Kaggle

1. Join the competition and accept its rules.
2. Open or import a notebook from this repository.
3. Add the competition data as an input.
4. Run all cells.

The loaders look for:

```text
/kaggle/input/competitions/penalty-kick-outcome-prediction-challenge
```

### Colab

Upload `train.csv` and `test.csv`, or the downloaded competition ZIP, to `/content` or `/content/data`, then run all cells.

## Data and reproducibility

Competition data is not redistributed in this repository. Download it from Kaggle after accepting the competition rules.

The notebooks use stratified validation, fixed random seeds, leakage-safe preprocessing, and dataset fingerprints. Hidden test labels are not used for training or model selection. Any organizer-only, post-competition evaluation is clearly separated from the training workflow.

## Final solution status

Notebook 15 is a frozen, reproducible teaching solution. Its predictions were saved before the separate organizer evaluation. The next improvement stage should compare imbalance-handling and recall-oriented alternatives under validation before freezing another submission.
