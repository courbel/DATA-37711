# Homework 1

Written answers to Problems 1-3 are in `homework_1.ipynb` (Markdown + LaTeX, plus one short numpy check after Problem 1(b)). The "Coding problems" section at the end is a placeholder for the remaining problems.

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
