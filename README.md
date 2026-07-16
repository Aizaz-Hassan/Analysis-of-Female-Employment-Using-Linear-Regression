# Female Employment Rate Prediction (Bangladesh) — Multiple Linear Regression

A machine learning project analyzing socioeconomic factors affecting female employment in Bangladesh (1995–2019), using multiple linear regression to predict female employment rate from fertility rate, wage/salaried employment percentage, and male-to-female population ratio.

## Dataset

Source: World Bank databank. Covers a population survey in Bangladesh spanning 1995–2019, with 12 socioeconomic indicators related to female employment (fertility rate, employment sector breakdowns, wage structure, etc.).

Raw data: [`data/dataset.csv`](data/dataset.csv)

## Workflow

1. **Data cleaning** — handle missing/placeholder values in `FertilityRate`, convert to numeric, impute with mean
2. **Outlier filtering** — IQR-based filtering on `Wage&Salaried`
3. **Exploratory analysis** — distribution plots, correlation checks
4. **Modeling** — Multiple Linear Regression predicting `PerFemEmploy` from:
   - `FertilityRate`
   - `Wage&Salaried`
   - `Ratio_MaletoFemale`
5. **Evaluation** — MAE, MSE, R² on train/test splits, cross-validation, coefficient visualization, residual analysis

## Results

The model evaluates linear relationships between the selected features and female employment rate, with performance reported via MAE, MSE, and R² on both training and test sets, plus 5-fold cross-validation.
