# Data access

This repository does not redistribute the competition dataset or organizer labels.

To run the notebooks:

1. Open the [Penalty Kick Outcome Prediction Challenge](https://www.kaggle.com/competitions/penalty-kick-outcome-prediction-challenge).
2. Join the competition and accept its rules.
3. Run the notebooks on Kaggle with the competition data attached, or download the data for use in Google Colab.

Chapters 01–14 require `train.csv` and `test.csv`. Chapter 15 also requires `sample_submission.csv` to preserve the submission format and ID order.

Every notebook reads `train.csv` and `test.csv` from the folder set in `DATA_DIR`:

```python
DATA_DIR = "/kaggle/input/competitions/penalty-kick-outcome-prediction-challenge"
```

For Colab, extract the ZIP, upload the CSV files to `/content`, and change `DATA_DIR` to `"/content"`. Notebook 15 also requires `sample_submission.csv` for the submission format.
