<a name="readme-top"></a>

<h3 align="center">CoxPASNet</h3>

<p align="center">
  Explainable pathway-aware sparse neural network for survival analysis
  <br />
  <strong>Deep learning for interpretable prognosis modeling using SHAP + Automated hyperparameter tuning</strong>
</p>


## Project Overview

Survival analysis plays a crucial role in biomedical research and clinical decision-making. In oncology, it helps estimate patient survival probabilities and predict disease progression. Traditional statistical models like the Cox Proportional Hazards (CoxPH) model, although widely used, assume linear relationships and struggle to integrate high-throughput genomic and clinical data — limiting their real-world applicability.

Recent advances in machine learning (ML) and deep learning (DL) have transformed survival analysis by enabling models to capture complex non-linear interactions and incorporate high-dimensional datasets. Despite this progress, challenges remain in hyperparameter tuning, overfitting control, and model interpretability.

This project centers on **Cox-PASNet**, a sparse, biologically informed deep neural network for survival prediction. It was selected for its strong predictive performance and biological interpretability. The main objectives of this work include:

- Integrating **Optuna** for automated hyperparameter optimization, improving model performance over manual empirical tuning.
- Applying **SHAP (SHapley Additive Explanations)** to enhance interpretability and identify key genomic and clinical predictors of survival.
- Extending Cox-PASNet to support **dual-covariate analysis**, incorporating both survival status and disease condition to improve patient risk stratification.

The model was applied to a real-world dataset of patients with Acute Myeloid Leukemia (AML), combining clinical and genomic data. Results demonstrate that:

- Optuna-optimized Cox-PASNet outperforms empirically tuned versions.
- SHAP reveals biologically relevant features and pathways influencing survival.
- Dual-covariate modeling improves prediction over single-covariate (survival status only) approaches.

These enhancements contribute to the advancement of personalized medicine by improving prognostic accuracy and clinical interpretability in cancer survival analysis.

---

## Built With

- Python 3.10
- PyTorch 2.6.0
- Optuna 4.2.0
- SHAP 0.42.0
- Pandas 2.2.3
- Numpy 1.23.5
- JupyterLab


## Manual Setup 

Set up the Python environment manually using `conda` and `pip`:

```bash
conda create -n my-env python=3.10
conda activate my-env

pip install jupyterlab
pip install openpyxl
pip install pandas==2.2.3
pip install numba==0.56.4
pip install numpy==1.23.5
pip install shap==0.42.0
pip install optuna==4.2.0
pip install matplotlib
pip install torch==2.6.0 torchvision==0.21.0 torchaudio==2.6.0
