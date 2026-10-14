# Homework 1

Everything is in `homework_1.ipynb`:

- Problems 1-3: written answers (Markdown + LaTeX), plus a short numpy check after Problem 1(b).
- Problem 4: fits several sklearn regression models to the ALE dataset and tests their residuals for normality (scipy `normaltest`, Shapiro-Wilk, Q-Q plots).
- Problem 5: logistic and probit regression (Breast Cancer Wisconsin) and linear regression with squared-error and Student-t losses (ALE), each implemented in JAX and trained with `optax.sgd`, compared to sklearn baselines.

The ALE dataset ([UCI ML Repository, id 844](https://archive.ics.uci.edu/dataset/844)) is included as `data/ale.csv`, so no download is needed.

## How to run

Requires Python 3.9+.

```bash
cd homework_1
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter nbconvert --to notebook --execute homework_1.ipynb
```

The last command runs every cell from a fresh kernel and writes the executed notebook to `homework_1.nbconvert.ipynb`. To execute it in place instead, add `--inplace`. To work interactively, run `jupyter notebook homework_1.ipynb`.

A PDF copy of the notebook is in `homework_1.pdf`.
