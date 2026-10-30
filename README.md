# Education, Well-Being, and Employment in Young Adulthood

This project examines whether education and psychological well-being improve the prediction of employment among young adults beyond demographics, family economic resources, and prior employment history.

The analysis links predictors measured in the 2021 Panel Study of Income Dynamics Transition into Adulthood Supplement to employment status measured in 2023. Work experience and earnings reported in the 2021 survey refer to calendar year 2020.

## Research question

How much do education and well-being measured before 2023 improve prediction of employment in 2023, beyond demographics, family economic resources, and prior employment?

## Methods

- Nested logistic regression models
- Stratified train-test evaluation
- Five-fold cross-validation
- Paired bootstrap comparisons
- Repeated train-test splits
- XGBoost benchmark model
- Permutation importance and SHAP interpretation
- Calibration, threshold, complete-case, and subgroup checks

## Main findings

- Adding education improved held-out ROC AUC from 0.717 to 0.741 and reduced the Brier score from 0.179 to 0.170.
- Adding PHQ-9 and GAD-7 scores produced only a small incremental change in ROC AUC, from 0.741 to 0.742.
- Bootstrap intervals for the incremental well-being contribution included zero, and the improvement was not stable across repeated splits.
- The logistic regression model performed at least as well as the tuned XGBoost model while providing better calibration and interpretability.
- Prior employment status, weeks worked, education, and family economic resources were the most useful predictors.

These findings concern predictive performance and should not be interpreted as causal effects of education or mental health on employment.

## Repository contents

- `PSID_Education_Wellbeing_Employment.ipynb` — complete analysis notebook with outputs
- `PSID_Education_Wellbeing_Employment_Report.pdf` — final research report
- `requirements.txt` — Python package requirements

## Data availability

The individual-level PSID data are not included in this public repository. Researchers can obtain PSID data and documentation through the [PSID Data Center](https://psidonline.isr.umich.edu/).

To reproduce the analysis, download the required PSID variables, place the customized extract in the notebook working directory, and update the input file path in the data-import section if necessary.

## Author

Ying Li
