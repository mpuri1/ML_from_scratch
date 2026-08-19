# ML from Scratch: Linear Regression & Classification Notebooks

## Summary

- Adds `Magic_Gamma/Linear_reg.ipynb`: a from-scratch walkthrough of linear regression — the objective, why squared error is minimized, the five core assumptions, and MAE/RMSE as evaluation metrics — applied to the Seoul Bike Sharing dataset via simple regression, multiple regression, and two neural network variants for comparison.
- Adds `Magic_Gamma/Classification.ipynb`: a comparison of KNN, Naive Bayes, SVM, and a tuned neural network on the MAGIC Gamma Telescope dataset, with process/observation commentary throughout.

## Test plan

- [x] Validate both notebooks as JSON and compile all Python cells.
- [x] Run representative data-loading and model-evaluation cells in `mlevenv`.
- [ ] Run both notebooks top to bottom. The classification hyperparameter sweep is intentionally expensive: 54 configurations times 100 epochs.

## Files

- `Magic_Gamma/Linear_reg.ipynb`
- `Magic_Gamma/Classification.ipynb`