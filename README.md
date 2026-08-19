# ML from Scratch

Jupyter notebooks that explain core machine-learning ideas through executable examples.

## Notebooks

### `Magic_Gamma/Linear_reg.ipynb`

A linear-regression walkthrough using the Seoul Bike Sharing Demand dataset. It covers:

- Simple and multiple linear regression
- Ordinary least squares and squared error
- Linearity, independence, homoscedasticity, normality, and multicollinearity
- MAE and RMSE
- A comparison between linear regression and neural-network models

The regression experiments use a shared, reproducible train/validation/test split. With the current split, the temperature-only model scores about $R^2 = 0.17$ and the multiple-feature model scores about $R^2 = 0.46$ on the test set.

### `Magic_Gamma/Classification.ipynb`

A classification walkthrough using the MAGIC Gamma Telescope dataset. It compares:

- K-nearest neighbors
- Gaussian Naive Bayes
- Support vector machines
- Logistic-regression section notes
- Neural networks and hyperparameter tuning

The preprocessing pipeline fits `StandardScaler` on the training features only, then transforms validation and test features with that same scaler. Oversampling is applied only to the training split.

## Setup

The notebooks were tested with Python 3.12. Create a virtual environment with [uv](https://docs.astral.sh/uv/) and install the dependencies from `requirements.txt`:

```bash
uv venv --python 3.12
uv pip install -r requirements.txt
```

Activate the environment with:

```bash
source .venv/bin/activate
```

On Windows:

```powershell
.venv\Scripts\Activate.ps1
```

## Run

Open the repository in VS Code with the Jupyter extension, select the virtual environment as the notebook kernel, and run cells from top to bottom.

Alternatively, start JupyterLab from the repository root:

```bash
jupyter lab
```

Both notebooks download their public datasets through `kagglehub` when the dataset-loading cell runs. The first run may take longer while the data is cached locally.

Dataset pages:

- [Seoul Bike Sharing Demand Prediction](https://www.kaggle.com/datasets/saurabhshahane/seoul-bike-sharing-demand-prediction)
- [MAGIC Gamma Telescope](https://www.kaggle.com/datasets/abhinand05/magic-gamma-telescope-dataset)

## Runtime Notes

The classification hyperparameter sweep trains 54 model configurations for 100 epochs each and can take a while. It also produces one loss plot per configuration.

Two existing teaching notes remain in the classification notebook:

- The variable named `lg_model` currently instantiates `GaussianNB`, so that section is not yet a true logistic-regression experiment.
- The `plot_history(history)` section depends on the relevant `history` variable having been created earlier in the current kernel session.

These are documented in the notebook and are separate from the preprocessing and review fixes described above.
