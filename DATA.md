# Data access

This repository does not redistribute competition data or hidden test answers.

To run the notebooks:

1. Open the [Penalty Kick Outcome Prediction Challenge](https://www.kaggle.com/competitions/penalty-kick-outcome-prediction-challenge).
2. Join the competition and accept its rules.
3. Run on Kaggle with the competition data attached, or download the CSV files for Colab or a local virtual environment.

The notebooks read only `train.csv` and `test.csv`. Put them in the ignored `data/` folder for local use. On Kaggle or Colab, change the single `DATA_DIR` setting; see [the running guide](README.md#running-the-notebooks).

The expected competition version has 20,000 labeled training rows and 6,000 unlabeled test rows. The target is `is_scored`; the identifier is `id`.
