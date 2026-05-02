<div align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/fd/RMS_Titanic_3.jpg/960px-RMS_Titanic_3.jpg" width="80%" alt="RMS Titanic" />

# Would You Survive the Titanic?

**A walk through the world's most-taught dataset — feature engineering, EDA, and a model for who lived and who didn't.**

[![Kaggle](https://img.shields.io/badge/Kaggle-Titanic-20BEFF.svg)](https://www.kaggle.com/c/titanic)
[![Python](https://img.shields.io/badge/Python-3.7+-yellow.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

</div>

---

## About

|        |                                                                                          |
| ------ | ---------------------------------------------------------------------------------------- |
| Who    | [Gyanesh Samanta](https://github.com/GyaneshSamanta), as a portfolio data-science piece. |
| What   | Predictive modeling on Kaggle's "Titanic: Machine Learning from Disaster" dataset.       |
| When   | Built September 2021; documentation refreshed 2026.                                      |
| Where  | Pure-Python notebook stack — pandas, scikit-learn, matplotlib, seaborn.                  |
| Why    | The canonical first ML problem: small dataset, rich feature engineering, real stakes.    |

## The Story

On 15 April 1912, the RMS Titanic went down with 1,502 of 2,224 souls aboard. Survival looked random in the moment — chaos, cold, lifeboats half-full — but the data tells a different story. Class mattered. Sex mattered. Age mattered. The lifeboats reflected an Edwardian social hierarchy as much as they reflected luck.

This notebook walks the dataset end-to-end: a careful EDA that surfaces the survival gap between first-class women (~97%) and third-class men (~14%), imputation strategies for the inevitably-missing `Age` and `Cabin` columns, and engineered features (`FamilySize`, salutation extracted from `Name`, fare bins) that lift accuracy beyond what raw columns can.

The final model is a **Random Forest** tuned via `GridSearchCV`. The result isn't groundbreaking on the Kaggle leaderboard — that's not the point. The point is the trail of decisions: every cell answers a small question, and the conclusions are defensible because the EDA earned them.

If you're new to ML, read the notebook top-to-bottom. If you're benchmarking your own approach, the `submissions/` folder has a Kaggle-formatted baseline you can diff against.

## Gallery

The full visual story lives in **[`notebooks/Titanic_Survival_Prediction.ipynb`](notebooks/Titanic_Survival_Prediction.ipynb)** — survival-by-class bar charts, age distributions split by outcome, correlation heatmaps, and a confusion matrix for the final model.

---

## Tech Stack

- **Python 3.7+**
- **pandas / numpy** — data wrangling
- **matplotlib / seaborn** — plotting
- **scikit-learn** — preprocessing, RandomForest, GridSearchCV, metrics
- **Jupyter** — runtime

## Repo Structure

```
Would-you-survive-on-the-Titanic/
├── data/
│   ├── train.csv               # Features + survival labels
│   ├── test.csv                # Features only (Kaggle holdout)
│   └── gender_submission.csv   # Sample submission format
├── notebooks/
│   └── Titanic_Survival_Prediction.ipynb   # EDA + modelling
└── submissions/
    └── my_submission.csv       # Generated predictions
```

## Getting Started

```bash
git clone https://github.com/GyaneshSamanta/Would-you-survive-on-the-Titanic.git
cd Would-you-survive-on-the-Titanic

pip install pandas numpy matplotlib seaborn scikit-learn jupyter

jupyter notebook notebooks/Titanic_Survival_Prediction.ipynb
```

To regenerate a Kaggle submission, run the notebook to completion — the final cells write `submissions/my_submission.csv`.

## Contributing

Fork, branch, PR. If your model beats this one on the Kaggle public leaderboard, I'd genuinely like to read the diff.

## License

MIT.

## Credits

- Data: [Kaggle — Titanic: Machine Learning from Disaster](https://www.kaggle.com/c/titanic).
- Author: [Gyanesh Samanta](https://github.com/GyaneshSamanta).
- Hero image: RMS Titanic, public domain via Wikimedia Commons.
