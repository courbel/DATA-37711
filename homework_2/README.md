# Homework 2

Everything is in `homework_2.ipynb`:

- Problem 1: an MLP (PyTorch) that outputs a conditional mean and standard deviation for NYC taxi trip durations, trained with the Gaussian negative log-likelihood and compared to constant and linear baselines. It then predicts P(trip < 45 min) and evaluates it with the Brier score, log-loss and accuracy.
- Problem 2: target encoding (`category_encoders`) + gradient boosting, an embedding network, and a combined model for the heavy-tailed `Quantity` in the retail data (log1p target, MSE loss).
- Problem 3: Random Kitchen Sinks with ridge regression (sweep over the kernel scale σ) vs a one-hidden-layer MLP (sweep over hidden width), with fitted-surface plots.

All datasets provided with the assignment are in `data/`. Test-set predictions for Problem 3 are in `rks_test_predictions.csv` and `mlp_test_predictions.csv` (one prediction per row, same order as `data/test.csv`).

## How to run

Requires Python 3.10+ (tested with Python 3.12).

```bash
cd homework_2
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter nbconvert --to notebook --execute homework_2.ipynb
```

The last command runs every cell from a fresh kernel (about a minute on a laptop CPU) and writes the executed notebook to `homework_2.nbconvert.ipynb`. To execute it in place instead, add `--inplace`. Running the notebook also rewrites the two prediction CSVs. To work interactively, run `jupyter notebook homework_2.ipynb`.

A PDF copy of the notebook is in `homework_2.pdf`.
