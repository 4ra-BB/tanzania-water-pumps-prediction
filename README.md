# Predicting Water Pump Functionality in Tanzania

Predictive classification of water pump operational status using machine learning, applied to infrastructure maintenance in sub-Saharan Africa.

## The problem

Tanzania has tens of thousands of water pumps distributed across the country. Many fall into disrepair without timely maintenance, leaving communities without access to clean water. Predicting which pumps are likely to fail can help governments and NGOs allocate maintenance resources more effectively.

## Dataset

Data from the [DrivenData competition "Pump it Up: Data Mining the Water Table"](https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/), containing information on ~59,400 water pumps. Each pump is classified as:

- **functional** — the pump is operational
- **functional needs repair** — the pump works but needs maintenance
- **non functional** — the pump is not working

## Approach

| Step | Method |
|---|---|
| Imputation | Correlation-based: each variable imputed using the most related variable as grouping key |
| Feature selection | Random Forest importance scores, aggregated by original variable |
| Model | Random Forest (100 estimators) |
| Key finding | Minimal variable recoding outperformed heavy feature engineering |

## Repository structure

```
├── README.md
├── data/
│   ├── TrainingValues.csv
│   ├── TrainingLabels.csv
│   └── TestValues.csv
├── notebooks/
│   └── water_pump_status_prediction.ipynb
└── .gitignore
```

## How to run

```bash
git clone https://github.com/laurabenkel/tanzania-water-pumps-prediction.git
cd tanzania-water-pumps-prediction
pip install pandas numpy scikit-learn matplotlib seaborn scipy
jupyter notebook notebooks/water_pump_status_prediction.ipynb
```

## Tools

Python · pandas · scikit-learn · matplotlib · seaborn · scipy

## Author

**Laura Benkel Brander** — Sociologist & Data Scientist  
[LinkedIn](https://www.linkedin.com/in/laurabenkel)
