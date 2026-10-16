# Penalty Kick ML Learning Path

Predict whether a football penalty is **scored (1)** or **missed (0)**. Learn the full ML workflow through **16 practical lessons**, built around a [competition I created](https://www.kaggle.com/competitions/penalty-kick-outcome-prediction-challenge).

**Dataset:** 20,000 labeled training kicks · 6,000 unlabeled test kicks.

**Final CatBoost pipeline:** validation F1 **0.9414** · accuracy **0.9470** · ROC-AUC **0.9905**. These are validation results, not leaderboard scores. [Result details](#results).

**Start with EDA:** [Read with outputs](notebooks/01_Exploratory_Data_Analysis.ipynb) · [Open in Colab](https://colab.research.google.com/github/Soni-KR/penalty-kick-ml-learning-path/blob/main/notebooks/01_Exploratory_Data_Analysis.ipynb) · [Get the Kaggle data](https://www.kaggle.com/competitions/penalty-kick-outcome-prediction-challenge/data)

**See the full project:** [Complete pipeline](notebooks/16_Complete_ML_Pipeline.ipynb) · [Open in Colab](https://colab.research.google.com/github/Soni-KR/penalty-kick-ml-learning-path/blob/main/notebooks/16_Complete_ML_Pipeline.ipynb) · [Learning roadmap](notebooks/00_Learning_Roadmap.ipynb)

To run in Colab: upload `train.csv` and `test.csv`, set `DATA_DIR = "/content"`, then run all cells. For the final pipeline, also set `OUTPUT_DIR = "/content"`. [Full setup guide](#running-the-notebooks).

![Eight models compared using training cross-validation F1; CatBoost performs best in this comparison.](assets/model-comparison.png)

*Preview from [Lesson 10](notebooks/10_Model_Comparison.ipynb): training cross-validation before tuning, not the final validation score above.*

## Learning path

| # | Notebook | Main question | Open in browser |
|---:|---|---|---|
| 00 | [Learning roadmap](notebooks/00_Learning_Roadmap.ipynb) | How is the course organized? | Read the roadmap |
| 01 | [Exploratory data analysis](notebooks/01_Exploratory_Data_Analysis.ipynb) | What is in the data, and which issues require later decisions? | [Colab](https://colab.research.google.com/github/Soni-KR/penalty-kick-ml-learning-path/blob/main/notebooks/01_Exploratory_Data_Analysis.ipynb) |
| 02 | [Baselines and validation](notebooks/02_Baselines_and_Validation.ipynb) | What must a useful model beat, and how are scores calculated honestly? | [Colab](https://colab.research.google.com/github/Soni-KR/penalty-kick-ml-learning-path/blob/main/notebooks/02_Baselines_and_Validation.ipynb) |
| 03 | [Missing values and scaling](notebooks/03_Missing_Values_and_Scaling.ipynb) | How should incomplete and differently scaled features be handled? | [Colab](https://colab.research.google.com/github/Soni-KR/penalty-kick-ml-learning-path/blob/main/notebooks/03_Missing_Values_and_Scaling.ipynb) |
| 04 | [Categorical encoding](notebooks/04_Categorical_Encoding.ipynb) | How can text categories become model inputs without leakage? | [Colab](https://colab.research.google.com/github/Soni-KR/penalty-kick-ml-learning-path/blob/main/notebooks/04_Categorical_Encoding.ipynb) |
| 05 | [Feature engineering](notebooks/05_Feature_Engineering.ipynb) | Which domain relationships can be expressed more clearly? | [Colab](https://colab.research.google.com/github/Soni-KR/penalty-kick-ml-learning-path/blob/main/notebooks/05_Feature_Engineering.ipynb) |
| 06 | [Feature selection](notebooks/06_Feature_Selection.ipynb) | Which features contain useful signal, and which may be distractions? | [Colab](https://colab.research.google.com/github/Soni-KR/penalty-kick-ml-learning-path/blob/main/notebooks/06_Feature_Selection.ipynb) |
| 07 | [Dimensionality reduction](notebooks/07_Dimensionality_Reduction.ipynb) | Can many encoded inputs be compressed without losing useful information? | [Colab](https://colab.research.google.com/github/Soni-KR/penalty-kick-ml-learning-path/blob/main/notebooks/07_Dimensionality_Reduction.ipynb) |
| 08 | [Outlier handling](notebooks/08_Outlier_Handling.ipynb) | Are unusual observations errors, noise, or informative hard cases? | [Colab](https://colab.research.google.com/github/Soni-KR/penalty-kick-ml-learning-path/blob/main/notebooks/08_Outlier_Handling.ipynb) |
| 09 | [Class imbalance](notebooks/09_Class_Imbalance.ipynb) | Can resampling or class weights improve minority-class prediction? | [Colab](https://colab.research.google.com/github/Soni-KR/penalty-kick-ml-learning-path/blob/main/notebooks/09_Class_Imbalance.ipynb) |
| 10 | [Model comparison](notebooks/10_Model_Comparison.ipynb) | Which model family best fits this tabular problem? | [Colab](https://colab.research.google.com/github/Soni-KR/penalty-kick-ml-learning-path/blob/main/notebooks/10_Model_Comparison.ipynb) |
| 11 | [Hyperparameter optimization](notebooks/11_Hyperparameter_Optimization.ipynb) | How can model settings be tuned without overfitting validation? | [Colab](https://colab.research.google.com/github/Soni-KR/penalty-kick-ml-learning-path/blob/main/notebooks/11_Hyperparameter_Optimization.ipynb) |
| 12 | [Ensembling](notebooks/12_Ensembling.ipynb) | Can complementary models improve one another? | [Colab](https://colab.research.google.com/github/Soni-KR/penalty-kick-ml-learning-path/blob/main/notebooks/12_Ensembling.ipynb) |
| 13 | [Calibration and thresholds](notebooks/13_Calibration_and_Thresholds.ipynb) | Are probabilities reliable, and should the cutoff remain 0.5? | [Colab](https://colab.research.google.com/github/Soni-KR/penalty-kick-ml-learning-path/blob/main/notebooks/13_Calibration_and_Thresholds.ipynb) |
| 14 | [Interpretation and error analysis](notebooks/14_Interpretation_and_Error_Analysis.ipynb) | Why does the model make its predictions and mistakes? | [Colab](https://colab.research.google.com/github/Soni-KR/penalty-kick-ml-learning-path/blob/main/notebooks/14_Interpretation_and_Error_Analysis.ipynb) |
| 15 | [Original selected pipeline: short version](notebooks/15_Final_Frozen_Solution.ipynb) | How do we refit and export the original lesson recipe? | [Colab](https://colab.research.google.com/github/Soni-KR/penalty-kick-ml-learning-path/blob/main/notebooks/15_Final_Frozen_Solution.ipynb) |
| 16 | [Revised complete ML pipeline](notebooks/16_Complete_ML_Pipeline.ipynb) | How do we select a training-only cutoff, validate, refit and export the revised recipe? | [Colab](https://colab.research.google.com/github/Soni-KR/penalty-kick-ml-learning-path/blob/main/notebooks/16_Complete_ML_Pipeline.ipynb) |

Lesson comparisons stay within the training part. They are teaching experiments, not independent final performance claims.
Outlier plots flag unusual values; they do not prove errors. Balancing is tested, not assumed helpful for the mild 55/45 imbalance.

## Running the notebooks

Each notebook runs independently. No earlier notebook or extra project module is required.

### Colab — no clone needed

1. Open [EDA in Colab](https://colab.research.google.com/github/Soni-KR/penalty-kick-ml-learning-path/blob/main/notebooks/01_Exploratory_Data_Analysis.ipynb), or choose **Colab** beside any lesson above. Sign in to run it.
2. Download `train.csv` and `test.csv` from the [Kaggle competition](https://www.kaggle.com/competitions/penalty-kick-outcome-prediction-challenge/data) after accepting its rules.
3. Upload both files through Colab's **Files** panel. Set `DATA_DIR = "/content"` in Setup.
4. For Notebooks 15/16, also set `OUTPUT_DIR = "/content"`. Run the cells from top to bottom; see the library notes below if an import is missing.

If GitHub import fails, download the `.ipynb` from GitHub and use **File → Upload notebook** in Colab. Uploaded data is temporary and must be added again after a runtime reset. [Colab help](https://research.google.com/colaboratory/faq.html#using-colab).

### Kaggle

1. Join the competition and accept its rules.
2. Download the lesson's `.ipynb` from GitHub. Create a Kaggle notebook, then use **File → Import Notebook**.
3. Add the competition data as an input.
4. Set `DATA_DIR` to the path below. For Notebooks 15/16, set `OUTPUT_DIR = "/kaggle/working"`. Run all cells.

Set the single input folder:

```text
/kaggle/input/competitions/penalty-kick-outcome-prediction-challenge
```

### Local / VS Code

1. Put `train.csv` and `test.csv` in a `data/` folder at the repository root.
2. Create a virtual environment and install the requirements:

   ```powershell
   python -m venv .venv
   .venv\Scripts\python -m pip install -r requirements.txt
   ```

   Earlier saved lessons used Python 3.12.14 and the pinned versions in `requirements.txt`. Notebook 16's latest Kaggle run used Python 3.13.15; its actual library versions are recorded in the notebook metadata.

3. Open a notebook, select that environment, and run all cells. Use `notebooks/` as the working directory.
4. Notebooks 15 and 16 save predictions to the ignored `results/` folder.

### Extra libraries in hosted runtimes

Lessons 10–16 can use XGBoost/CatBoost; Lesson 11 also uses Optuna. If your Kaggle/Colab kernel does not have them, run this in a new notebook cell before the imports:

```python
%pip install xgboost==3.4.1 catboost==1.2.10 optuna==5.0.0 ipywidgets==8.1.9
```

For local use, install `requirements.txt` inside your virtual environment instead. Native CatBoost category handling is an alternative; these saved comparisons use the same prepared inputs for every model.

## Results

<!-- RESULTS_START -->
Rerun on 15 October 2026. These are the measured model-comparison results from Lesson 10, before tuning and ensembling.

| Model | Cross-validation F1 | Accuracy | ROC-AUC |
|---|---:|---:|---:|
| CatBoost | 0.944 | 0.950 | 0.991 |
| Gradient boosting | 0.942 | 0.948 | 0.990 |
| XGBoost | 0.940 | 0.947 | 0.990 |
| Random forest | 0.927 | 0.935 | 0.984 |
| Extra trees | 0.926 | 0.934 | 0.984 |
| Logistic regression | 0.899 | 0.910 | 0.967 |
| Decision tree | 0.878 | 0.891 | 0.957 |
| RBF support vector machine | 0.872 | 0.886 | 0.957 |

**Original recipe (Notebook 15):** CatBoost with fixed settings `{'learning_rate': 0.1, 'depth': 6}` (chosen in Lesson 11 by random search); single model; original probabilities; cutoff 0.50.

Original recipe on the 4,000-row validation set: **F1 0.9395**, **accuracy 0.9457**, **ROC-AUC 0.9901**. This is not a Kaggle leaderboard score.

**Revised complete pipeline (Notebook 16), complete Kaggle run on 16 October 2026:** keep and impute incomplete rows; training-selected cutoff **0.47**. Training out-of-fold F1 at the selected cutoff: **0.9476** (a selection score, not independent evaluation). On the same validation rows: **F1 0.9414**, **accuracy 0.9470**, **ROC-AUC 0.9905**. These rows have been inspected before, so this rerun is not a fresh independent benchmark.

Notebook 16 ends with an optional **50% expected-goal-rate example**. It labels the upper half of test probabilities as goals. This is an assumption, not a rate measured from the unlabeled test file or selected by training validation. Use such an adjustment only with a credible, independent reason for the expected rate. Otherwise, keep the training-selected cutoff. This example changes predictions, not the model or its probabilities, and is not ordinary class balancing.

Notebook 16 saves its two prediction files to the ignored `results/pipeline_update/` folder. Both passed 6,000-row, ID-order, and binary-label checks. Validation metrics above describe only the standard training-selected cutoff.
<!-- RESULTS_END -->

Cross-validation scores help choose the model, so the winning search score is optimistic. The separate validation set checks only the chosen pipeline; this is not a Kaggle leaderboard score.
The dataset was explored in earlier project versions. This split protects the rerun's selection procedure; it is not a claim that these rows were never seen historically.

## What makes this beginner-friendly?

Each lesson: detect the problem → apply several strategies → compare on the same splits → carry one justified choice forward. Earlier lessons retain their experiments and saved outputs. Notebook 16 has been rerun end-to-end on Kaggle, including its training-only cutoff search.

Every notebook follows ten short sections: **problem, importance, key concepts, intuitive example, methods, retained choices, setup, experiments, results and decision, takeaways and next step**. The roadmap uses a learning route instead of a method comparison; final notebooks describe their execution plan. There is one Markdown summary of earlier decisions, not repeated explanations between code cells. EDA and diagnostic lessons do not invent an F1 winner.

Each runnable notebook has **one reusable Setup code cell** containing its repeated imports, loading, earlier preparation, and fold helpers. **Run it, then skip to the lesson: beginners do not need to study all its lines.** New topic-specific methods stay visible under **Experiments**. The roadmap has no executable setup. Run Setup before Experiments, or use **Run all**. Setup is marked collapsed where supported; GitHub may show it expanded. Every notebook remains independent, and PCA/SMOTE illustrations are embedded.

The regrouped Setup cells in earlier lessons were checked separately without fitting models. Notebook 16 completed a fresh Kaggle run on **16 October 2026**: all 11 lesson code cells, three plots, and both exports. Its three-fold training predictions and 0.01–0.99 cutoff search reproduced **0.47**. Validation answers and competition-test answers do not select this cutoff.

## Pipeline

Start with EDA: missing values, duplicates, class counts, distributions, boxplots, and PCA.
Then follow the lessons in order. Every later comparison starts from the earlier chosen steps.

```mermaid
flowchart TD
    A[EDA: understand the training file] --> B[Each lesson: try several strategies]
    B --> C[Compare on the same training-only splits]
    C --> D[Choose one method and explain why]
    D -->|Next phase| B
    D --> E[Final notebook: chosen recipe only]
    E --> F[Check on separate validation rows]
    F --> G[Refit using the full training file]
    G --> H[Predict competition test and save submission]
```

| Data | Source | Purpose |
|---|---|---|
| Training: 16,000 rows | 80% of `train.csv` | Compare methods and choose settings |
| Validation: 4,000 rows | Other 20% of `train.csv` | Check the fixed final recipe |
| Competition test: 6,000 rows | `test.csv` | Predict unknown answers for Kaggle |

Cross-validation rotates hidden groups inside the training part. All learned filling, encoding,
selection, sampling, calibration, and tuning stay inside those training splits. Evaluation rows are never removed or balanced.

### What is actually applied?


| Lesson | Applied here | More alternatives explained |
|---|---|---|
| 01 · EDA | Missing/unique counts, four duplicate rules, class counts, category rates, correlations, histograms, boxplots, PCA, train/test comparisons | What each finding means and which lesson handles it |
| 02 · Baselines and validation | Common-class, always-goal, random, logistic baselines; stratified split and three-fold comparisons | Group/time splits; precision, recall, F1 and accuracy |
| 03 · Missing values and scaling | Drop rows, drop columns, mean/mode, median/mode; no/standard/robust scaling | KNN/iterative filling, missing flags, min–max and log transforms |
| 04 · Encoding | One-hot, grouped one-hot, ordinal, cross-fitted target rates | Frequency, hashing, binary encoding |
| 05 · Feature engineering | 20 candidates; original inputs, three separate groups, all groups together | Binning, polynomial expansion, past-only historical aggregates |
| 06 · Selection | Keep all, ANOVA top 10, L1, forest selection, drop suspected decoys, drop decoys + L1 | Constants, mutual information, correlation, recursive elimination, Boruta |
| 07 · Compression | Keep inputs, PCA, SVD, LDA | Kernel PCA, autoencoders, t-SNE/UMAP maps |
| 08 · Outliers | Boxplots, IQR, physical limits, PCA, scatter; keep, clip, flag, fixed-rule removal, rules + IQR removal, Isolation Forest removal | Z-score, local outlier factor |
| 09 · Imbalance | Original counts, oversampling, undersampling, weights; separate numerical SMOTE experiment | SMOTENC, ADASYN, BorderlineSMOTE, Tomek links, SMOTE–ENN |
| 10 · Models | Logistic regression, decision tree, random forest, extra trees, gradient boosting, RBF SVM, XGBoost, CatBoost | KNN, naive Bayes, neural networks, LightGBM, native CatBoost categories |
| 11 · Tuning | Defaults, manual settings, grid search, random search, eight-trial Optuna/TPE search | More trials, continuous ranges, pruning, successive halving |
| 12 · Ensembles | Single learner, average two, average three, weighted average | Hard voting, bagging, stacking |
| 13 · Probabilities | Original, sigmoid/isotonic calibration, training-selected cutoff | Brier/log loss, recall/cost-based cutoffs |
| 14 · Errors | Confusion matrix, both error types, confident mistakes, subgroups, probability buckets, permutation importance | Partial dependence, error clustering, SHAP |
| 15–16 · Final pipeline | Original fixed recipe (15); revised fixed model with training-only cutoff selection, validation and test predictions (16) | Optional assumed-rate example stays separate; no repeated model search |


Usually 3–6 strategies are tested in a handling lesson. Feature engineering has **20 explained candidates**, tested as five feature sets.
EDA and error analysis use complementary diagnostics, rather than inventing a winning algorithm.

### Original lesson decisions

| Earlier EDA decision | Choice |
|---|---|
| Exact duplicates | Keep all rows: none found |

| Phase | Chosen in the lesson |
|---|---|
| Missing · 03 | Drop incomplete training rows |
| Scaling · 03 | Robust scaling |
| Encoding · 04 | One-hot |
| Features · 05 | All candidate groups |
| Selection · 06 | Drop suspected decoys + L1 |
| Reduction · 07 | No PCA |
| Outliers · 08 | Add a flag |
| Balancing · 09 | Original class counts |
| Model · 10 | CatBoost |
| Tuning · 11 | Random search |
| Ensemble · 12 | Single model |
| Probabilities · 13 | Original probabilities |
| Decision cutoff · 13 | 0.50 |

These are two deliberately different recipes, not interchangeable copies:

| Configuration | Notebook 15: original | Notebook 16: revised |
|---|---|---|
| Incomplete training rows | Drop them during fitting | Keep them; fill numerical median / categorical mode |
| Normal decision cutoff | Fixed 0.50 from the original lessons | Select using training-only three-fold predictions; earlier run: 0.47 |
| Model and other preparation | Selected CatBoost recipe | Same model settings, features, selection, scaling, encoding and outlier flag |
| Purpose | Short refit/export of original lesson decisions | Reproduce revised cutoff selection, validate, refit/export |

A winning step is best in its particular comparison, not a guarantee of the globally best combination; small score gaps may be noise.

## Data and reproducibility

Competition data is not redistributed in this repository. Download it from Kaggle after accepting the competition rules.

The notebooks use fixed seeds and stratified splits (similar goal/miss proportions in each part). Preprocessing, selection, tuning, and resampling stay inside training folds. Hidden competition-test labels are not used.

The complete pipeline keeps 20% of labeled rows for validation; all model choices use the other 80%. Earlier project exploration means a genuinely new dataset is still needed for a stronger generalization claim.

### Validation references

[Scikit-learn: selection versus independent evaluation](https://scikit-learn.org/stable/auto_examples/model_selection/plot_nested_cross_validation_iris.html) · [Imbalanced-learn: resampling leakage](https://imbalanced-learn.org/stable/common_pitfalls.html)
