# Reading the notebook code

You can learn the ML ideas before memorizing every Python command. Here are the operations used most often in the course.

## Tools and names

| Code | What it means | Why we use it |
|---|---|---|
| `import pandas as pd` | Load pandas and call it `pd`. | Read CSV files and work with tables. |
| `import numpy as np` | Load NumPy and call it `np`. | Work with numerical arrays and calculations. |
| `import matplotlib.pyplot as plt` | Load Matplotlib's plotting tools and call them `plt`. | Draw charts. |
| `from sklearn.preprocessing import StandardScaler` | Import one tool from scikit-learn. | Put numerical features on comparable scales. Each method is explained in its chapter. |
| `TARGET = "is_scored"` | Give the answer column a name we can reuse. | Avoid repeating the column name throughout the code. |
| `ID_COLUMNS = [...]` | Store the identifier column names in a list. | Exclude these identifiers from the course's model inputs; Chapter 02 explains the decision. |
| `RANDOM_STATE = 42` | Set a fixed seed for random operations. | Repeat the same splits and experiments. The choice of 42 has no special ML meaning. |

## Reading and inspecting data

```python
DATA_DIR = "/kaggle/input/competitions/penalty-kick-outcome-prediction-challenge"

train = pd.read_csv(f"{DATA_DIR}/train.csv")
test = pd.read_csv(f"{DATA_DIR}/test.csv")
```

`DATA_DIR` is a folder name. The `f` before the quoted string inserts its value where `{DATA_DIR}` appears. `pd.read_csv` reads the resulting file path into a table.

| Code | Meaning |
|---|---|
| `train["is_scored"]` | Select one column. |
| `train[["minute_taken", "is_scored"]]` | Select several columns. |
| `train.head(3)` | Show the first three rows. |
| `train.shape` | Get the number of rows and columns. |
| `train.isna().sum()` | Count missing values in each column. |
| `train.drop(columns=ID_COLUMNS)` | Create a table without these columns. |
| `frame.copy()` | Make a separate table so new features do not overwrite the original. |
| `assert condition` | Stop if an expected condition is false, such as labels appearing in the test data. |

## Following calculations

| Code | Meaning |
|---|---|
| `player_percentage / 100` | Convert a percentage to a fraction. |
| `score_diff > 0` | Check which rows have a positive score difference. |
| `(score_diff > 0).astype(float)` | Turn `True`/`False` into `1.0`/`0.0`. |
| `values ** 2` | Square each value. |
| `values.clip(0, 1)` | Keep values within the range 0 to 1. |
| `for column in columns:` | Repeat the following indented steps for each column. |
| `def make_features(frame):` | Define a reusable sequence of steps, called a function. |
| `return result` | Give the function's result back to the code that called it. |

Example: a skill-gap feature expresses a relationship already present in two columns.

```python
skill_gap = (
    train["player_last5_scored_percent"]
    - train["goalkeeper_last5_saved_percent"]
)
```

A negative gap means the keeper's recent saving percentage is higher than the kicker's recent scoring percentage. This is a feature hypothesis; validation decides whether it helps prediction.

## Understanding the ML plumbing

| Tool or operation | What it does |
|---|---|
| `ColumnTransformer` | Apply different preparation to numerical and categorical columns. |
| `Pipeline` | Put preparation and a model in one ordered sequence. During validation, each fold learns preparation from its training rows only. |
| `.fit(X, y)` | Learn from the inputs `X` and known answers `y`. |
| `.transform(X)` | Apply an already learned preparation step to a table. |
| `.predict_proba(X)` | Produce class probabilities; `[:, 1]` selects the probability of class 1, scored. |
| `probability >= 0.50` | Turn probabilities into scored/missed decisions using a cutoff. |

`pd.set_option(...)` changes how tables are displayed, and `plt.style.use(...)` changes chart appearance. These optional settings do not train or change a model.

The final save cells use `Path` to name output files and `.to_csv(...)` to write tables. Those operations save results after the experiment; they are not ML methods.
