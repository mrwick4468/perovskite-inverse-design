# Deep Generative Modeling for AI-Guided Inverse Design of Perovskite Photovoltaic Devices

Code and generated candidates accompanying the Frontiers manuscript of the same title (under review).

## Contents

- `inverse-design-of-photovoltaic-double-perovskites.ipynb` — single reproducible notebook covering the full pipeline: feature engineering, leakage-controlled 5-fold cross-validation, statistical testing (Wilcoxon / paired-t with effect sizes), SHAP explainability, cVAE + classifier-free-guidance training, and all robustness and sensitivity experiments. Executed end-to-end on Kaggle; outputs are preserved. Random seeds are fixed in the notebook.
- `generated_candidates_for_resimulation.csv` — top-100 generated device candidates decoded to simulator-ready physical units (SI), suitable for drift-diffusion re-simulation (e.g. SIMsalabim).

## Data

Kaggle DRP perovskite solar-cell dataset:
https://www.kaggle.com/datasets/mirzayasirabdullah07/drp-for-perovskite-solar-cells-dataset

## Key results (leakage-free protocol)

XGBoost surrogate R² = 0.8661 ± 0.0020 (5-fold). Inverse-design hit-rates at w* = 1.5: 73.7% (90th percentile), 12.6% (99th), 3.4% (Ultra), corresponding to lifts of 8.9×, 25.2×, and ≥34× over random sampling.

## Reproducing

Attach the Kaggle dataset above and run the notebook top to bottom (Kaggle GPU environment or local Jupyter with standard scientific Python + PyTorch + XGBoost + SHAP).

## License

MIT — see `LICENSE`.
