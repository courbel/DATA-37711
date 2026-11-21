# Homework 3

Everything is in `homework_3.ipynb`:

- Problem 1: Poisson boosting with regression trees: why Poisson and the exp link, the loss, its gradient, and how each tree is chosen in gradient boosting.
- Problem 2: a Hoeffding + union bound for selecting among k hyperparameter settings on a test set, why reusing the test set is optimistic, and a 70/10/20 train/validation/test grid search on the white wine data with `KNeighborsRegressor` and `RandomForestRegressor` (600 parameter sets each, more than the 490 validation points).
- Problem 3: `GradientBoostingClassifier` with 1, 10, 100, 300 and 1000 trees on `dset0` and `dset1` (5-fold cross-validated accuracy and log-loss), and why the two datasets behave differently.

All datasets provided with the assignment are in `data/`.

## How to run

Requires Python 3.9+.

```bash
cd homework_3
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter nbconvert --to notebook --execute homework_3.ipynb
```

The last command runs every cell from a fresh kernel (about two minutes on a laptop CPU, mostly the two grid searches) and writes the executed notebook to `homework_3.nbconvert.ipynb`. To execute it in place instead, add `--inplace`. To work interactively, run `jupyter notebook homework_3.ipynb`.

A PDF copy of the notebook is in `homework_3.pdf`.
