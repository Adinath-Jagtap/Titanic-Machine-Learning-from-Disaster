<div align="center">
<h1>Titanic Survival Prediction</h1>
</div>
<div align="center">

[![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=Kaggle&logoColor=white)](https://www.kaggle.com/code/adinathjagtap777/titanic-machine-learning-from-disaster)
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)](https://www.tensorflow.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](LICENSE)

**Machine Learning solution for Kaggle's Titanic competition using Ensemble Gradient Boosted Trees**

[Features](#-features) • [Installation](#-installation) • [Usage](#-usage) • [Methodology](#-methodology) • [Results](#-results)

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Project Structure](#-project-structure)
- [Installation](#-installation)
- [Usage](#-usage)
- [Methodology](#-methodology)
- [Results](#-results)
- [Contact](#-contact)

---

## 🎯 Overview

This repository contains a machine learning solution for the iconic [Titanic - Machine Learning from Disaster](https://www.kaggle.com/c/titanic) competition on Kaggle. The challenge involves predicting passenger survival based on features such as age, sex, ticket class, fare, and family relationships.

### Competition Objective

Build a predictive model that answers the question: *"What sorts of people were more likely to survive the Titanic disaster?"*

### Achievement

- **Public Leaderboard Score**: 0.80143
- **Approach**: Ensemble of 100 Gradient Boosted Tree models
- **Framework**: TensorFlow Decision Forests

---

## ✨ Features

- **Ensemble Learning Architecture** – 100 gradient boosted tree models with probability averaging
- **Advanced Feature Engineering** – Name title extraction, ticket parsing, and categorical encoding
- **Production-Ready Code** – Clean, minimal dependencies with reproducible results
- **Efficient Training** – Complete model training in approximately 3 minutes
- **Seed-Controlled Experiments** – Deterministic results for research reproducibility

---

## 📁 Project Structure

```
Titanic-Machine-Learning-from-Disaster/
│
├── 100% Score CSV File/
│   └── Submission.csv                    # Reference submission file
│
├── Titanic - Machine Learning from Disaster/
│   ├── requirement.txt                   # Python dependencies
│   ├── submission.csv                    # Generated predictions (0.80143)
│   ├── titanic-machine-learning-from-disaster.ipynb
│   └── README.md                         # Project documentation
│
└── README.md                             # This file
```

> **Note**: The `100% Score CSV File` directory contains a reference submission for benchmarking purposes.

---

## 🚀 Installation

### Prerequisites

- Python 3.8 or higher
- pip package manager
- Jupyter Notebook (optional, for running `.ipynb` files)

### Setup

1. **Clone the repository**

```bash
git clone https://github.com/Adinath-Jagtap/Titanic-Machine-Learning-from-Disaster.git
cd Titanic-Machine-Learning-from-Disaster
```

2. **Navigate to project directory**

```bash
cd "Titanic - Machine Learning from Disaster"
```

3. **Install dependencies**

```bash
pip install -r requirement.txt
```

### Required Libraries

```
tensorflow>=2.12.0
tensorflow-decision-forests>=1.2.0
pandas>=1.5.0
numpy>=1.23.0
```

---

## 💻 Usage

### Running the Notebook

**Option 1: Local Jupyter**

```bash
jupyter notebook titanic-machine-learning-from-disaster.ipynb
```

**Option 2: Kaggle Kernels**

Upload the notebook directly to [Kaggle](https://www.kaggle.com/code/adinathjagtap777/titanic-machine-learning-from-disaster) and run with GPU acceleration enabled.

### Training the Model

The notebook follows this workflow:

1. Load training and test datasets
2. Preprocess features (name tokenization, ticket parsing)
3. Train ensemble of 100 Gradient Boosted Tree models
4. Generate predictions through probability averaging
5. Export `submission.csv` for Kaggle submission

---

## 🧠 Methodology

### Data Preprocessing

The preprocessing pipeline handles missing values and engineers new features:

| Feature | Processing | Purpose |
|---------|-----------|---------|
| **Name** | Tokenization & title extraction | Extract social status indicators (Mr., Mrs., etc.) |
| **Ticket** | Split into prefix + number | Identify ticket groups and classes |
| **Cabin** | Keep as-is | Tree models handle missing values naturally |
| **Age** | No imputation | Decision trees manage gaps automatically |
| **Fare** | Numeric | Direct usage |

### Feature Set

```
Input Features:
├── Pclass          → Passenger class (1st, 2nd, 3rd)
├── Name            → Tokenized for title extraction
├── Sex             → Male/Female
├── Age             → Passenger age
├── SibSp           → Number of siblings/spouses aboard
├── Parch           → Number of parents/children aboard
├── Fare            → Ticket price
├── Cabin           → Cabin identifier (if available)
├── Embarked        → Port of embarkation (C, Q, S)
├── Ticket_number   → Engineered from ticket
└── Ticket_item     → Engineered ticket prefix
```

### Model Architecture

**Algorithm**: Gradient Boosted Trees with Honest Learning

```python
Model Configuration:
├── Number of Models: 100
├── Random Seeds: 0-99 (for diversity)
├── Honest Trees: True (separate structure/leaf data)
├── Ensemble Method: Probability averaging
└── Training Strategy: Sequential with different seeds
```

**Key Algorithm Properties**:
- **Honest Trees** reduce overfitting by splitting data for structure learning and leaf value estimation
- **Ensemble Diversity** achieved through varied random seeds
- **Probability Averaging** produces more stable predictions than voting

---

## 📊 Results

### Performance Metrics

| Metric | Value |
|--------|-------|
| **Public Leaderboard Score** | 0.80143 |
| **Number of Models** | 100 |
| **Training Duration** | ~3 minutes |
| **Feature Count** | 11 |

### Key Insights

1. **Ensemble Strength**: Averaging 100 models significantly reduces variance and improves generalization
2. **Feature Engineering Impact**: Ticket parsing and name tokenization capture hidden survival patterns
3. **Honest Trees Benefit**: Data splitting for structure/values prevents overfitting better than standard boosting
4. **Simplicity Wins**: Clean preprocessing without excessive hyperparameter tuning achieves strong results

---

## 🔬 Technical Details

### Why Gradient Boosted Trees?

- **Handles mixed data types** naturally (numeric, categorical, text)
- **Robust to missing values** without imputation
- **Captures non-linear relationships** automatically
- **Fast training** compared to deep learning approaches
- **Interpretable** through feature importance analysis

### Why Ensemble of 100 Models?

- **Reduces overfitting** through model diversity
- **Stabilizes predictions** via averaging
- **Captures different aspects** of data through varied random seeds
- **Low computational cost** due to efficient tree training

---

## 📧 Contact

**Adinath Jagtap**

- **Kaggle**: [@adinathjagtap777](https://www.kaggle.com/adinathjagtap777)
- **GitHub**: [@Adinath-Jagtap](https://github.com/Adinath-Jagtap)

Feel free to reach out for collaboration or questions!

---

## 📚 References

- [Kaggle Titanic Competition](https://www.kaggle.com/c/titanic) – Official competition page
- [TensorFlow Decision Forests](https://www.tensorflow.org/decision_forests) – Framework documentation
- [Gradient Boosting](https://en.wikipedia.org/wiki/Gradient_boosting) – Algorithm overview
- [Honest Trees Paper](https://arxiv.org/abs/1504.01132) – Research on honest splitting

---

## ⭐ Acknowledgments

Special thanks to the Kaggle community for inspiration and the TensorFlow team for Decision Forests library.

---

<div align="center">

**If this project helped you, please consider giving it a ⭐**

Made with dedication for the Kaggle community

</div>
