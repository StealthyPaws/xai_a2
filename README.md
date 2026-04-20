#  Responsible & Explainable AI

## Python environment

- **Python:** 3.10+ recommended (tested with 3.10 in Conda).
- **Install:** `pip install -r requirements.txt`

This project is **PyTorch-only**. If `import transformers` fails because of a broken TensorFlow install, either set `USE_TF=0` as in the notebooks or run:

```
pip uninstall -y tensorflow tensorflow-macos tensorflow-metal keras
```

## GPU

- **Expected:** NVIDIA GPU with CUDA (e.g. **Google Colab T4**) for training DistilBERT in reasonable time (~25–35 minutes per full baseline run at 100k rows × 3 epochs, per course notes).
- **Apple Silicon:** Training uses **MPS** when available; CPU-only runs are much slower.
- **Colab:** Runtime → Change runtime type → **GPU**.

## Data

1. Accept the [Kaggle competition](https://www.kaggle.com/competitions/jigsaw-unintended-bias-in-toxicity-classification/) and download **`train.csv`** (or the competition zip).
2. Place **`jigsaw-unintended-bias-in-toxicity-classification.zip`** in this folder **or** ensure `train.csv` is available; the notebooks default to reading `train.csv` from the zip.

Do **not** commit large CSVs or model checkpoints (see `.gitignore`).


## Repository layout

| File | Purpose |
|------|---------|
| `part1.ipynb` | Baseline DistilBERT |
| `part2.ipynb` | Bias audit |
| `part3.ipynb` | Adversarial attacks |
| `part4.ipynb` | Mitigation |
| `part5.ipynb` | Guardrail pipeline demo |
| `pipeline.py` | `ModerationPipeline` |

**Roll number:** i220560
