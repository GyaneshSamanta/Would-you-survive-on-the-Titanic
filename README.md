# 🚢 Would You Survive the Titanic?

[![Kaggle](https://img.shields.io/badge/Kaggle-Competition-blue.svg)](https://www.kaggle.com/c/titanic)
[![Python](https://img.shields.io/badge/Python-3.7+-yellow.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

This repository contains a comprehensive analysis and predictive model for the classic **Titanic: Machine Learning from Disaster** competition on Kaggle.

---

## 📖 Background

The sinking of the RMS Titanic is one of the most infamous shipwrecks in history. On April 15, 1912, during her maiden voyage, the "unsinkable" Titanic sank after colliding with an iceberg. Unfortunately, there weren't enough lifeboats for everyone onboard, resulting in the death of 1502 out of 2224 passengers and crew.

While survival involved an element of luck, it appears some groups of people (such as women, children, and the upper-class) were more likely to survive than others.

**The Goal:** Build a predictive model that answers the question: "What sorts of people were more likely to survive?" using passenger data (name, age, gender, socio-economic class, etc.).

---

## 📂 Repository Structure

The project is organized as follows to ensure clarity and maintainability:

```text
.
├── data/                   # Raw and processed datasets
│   ├── train.csv           # Training data (features + survival labels)
│   ├── test.csv            # Test data (features only)
│   └── gender_submission.csv # Sample submission format
├── notebooks/              # Jupyter notebooks for analysis
│   └── Titanic_Survival_Prediction.ipynb # Main EDA and Modelling
├── submissions/            # Generated prediction files
│   └── my_submission.csv   # Model predictions for Kaggle
└── README.md               # Project overview and documentation
```

---

## 🛠️ Getting Started

### Prerequisites

To run the analysis locally, you'll need Python and the following libraries:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/GyaneshSamanta/Would-you-survive-on-the-Titanic.git
   cd Would-you-survive-on-the-Titanic
   ```
2. Navigate to the `notebooks` directory and launch Jupyter:
   ```bash
   cd notebooks
   jupyter notebook Titanic_Survival_Prediction.ipynb
   ```

---

## 📊 Dataset Overview

The dataset provides various features for each passenger:

- **PassengerId**: Unique ID for each passenger.
- **Survived**: Survival (0 = No, 1 = Yes) — _Target variable_
- **Pclass**: Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd)
- **Sex**: Passenger gender
- **Age**: Age in years
- **SibSp**: # of siblings / spouses aboard the Titanic
- **Parch**: # of parents / children aboard the Titanic
- **Ticket**: Ticket number
- **Fare**: Passenger fare
- **Cabin**: Cabin number
- **Embarked**: Port of Embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)

---

## 🏆 Model Performance

The current model uses a **Random Forest Classifier** (or check notebook for details) to predict survival based on engineered features.

_Key Highlights:_

- Detailed Exploratory Data Analysis (EDA).
- Missing value imputation (Age, Embarked).
- Feature Engineering (Family size, Title extraction).
- Hyperparameter tuning using GridSearchCV.

---

## ✉️ Contact

Developed with ❤️ by [Gyanesh Samanta](https://github.com/GyaneshSamanta).
Feel free to reach out for questions or collaborations!
