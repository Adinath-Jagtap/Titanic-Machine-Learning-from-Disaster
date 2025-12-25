# 🚢 Titanic Survival Prediction

[![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=Kaggle&logoColor=white)](https://www.kaggle.com/code/adinathjagtap777/titanic-machine-learning-from-disaster)
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)](https://www.tensorflow.org/)

> **Top Score**: 0.80143 | Ensemble Decision Forest Model

---

## 📊 Competition Overview

This repository contains my solution for the [Titanic - Machine Learning from Disaster](https://www.kaggle.com/c/titanic) competition on Kaggle. The goal is to predict passenger survival based on various features like age, sex, ticket class, and more.

### 🏆 Achievement
- **Public Score**: 0.80143
- **Approach**: Ensemble Gradient Boosted Trees

---

## 🎯 Key Features

- **Clean, Production-Ready Code**: Minimal dependencies, maximum efficiency
- **Ensemble Learning**: 100 gradient boosted tree models for robust predictions
- **Feature Engineering**: Smart preprocessing of names, tickets, and categorical variables
- **Reproducible Results**: Seed-controlled training for consistency

---

## 🛠️ Technical Stack

```
├── TensorFlow Decision Forests (tfdf)
├── Pandas & NumPy
├── Gradient Boosted Trees
└── Ensemble Averaging
```

---

## 📁 Repository Structure

```
titanic-survival-prediction/
│
├── titanic_model.ipynb          # Main training notebook
├── submission.csv               # Kaggle submission file (0.80143 score)
├── README.md                    # This file
└── requirements.txt             # Python dependencies
```

---

## 🚀 Quick Start

### Installation

```bash
# Clone the repository
git clone 

# Install dependencies
pip install -r requirements.txt
```

### Usage

```bash
# Run the notebook
jupyter notebook titanic_model.ipynb
```

Or use the provided cells directly in Kaggle notebooks.

---

## 🧠 Methodology

### 1. **Data Preprocessing**
- Name tokenization for title extraction
- Ticket splitting into prefix and number
- Handling missing values naturally through tree models

### 2. **Feature Engineering**
```python
Features Used:
├── Pclass (Passenger Class)
├── Name (Tokenized)
├── Sex
├── Age
├── SibSp (Siblings/Spouses)
├── Parch (Parents/Children)
├── Fare
├── Cabin
├── Embarked
├── Ticket_number (Engineered)
└── Ticket_item (Engineered)
```

### 3. **Model Architecture**
- **Algorithm**: Gradient Boosted Trees
- **Ensemble Size**: 100 models
- **Technique**: Honest trees (separate data for structure and leaf values)
- **Averaging**: Probability averaging across all models

### 4. **Training Strategy**
```python
for i in range(100):
    model = GradientBoostedTreesModel(
        random_seed=i,
        honest=True
    )
    predictions += model.predict()
final_prediction = predictions / 100
```

---

## 📈 Results

| Metric | Score |
|--------|-------|
| **Public Leaderboard** | 0.80143 |
| **Best Score** | 0.80143 |
| **Models Used** | 100 |
| **Training Time** | ~3 minutes |

---

## 💡 Key Insights

1. **Ensemble Power**: Averaging 100 models significantly improves stability
2. **Feature Engineering**: Ticket and name features provide valuable signals
3. **Honest Trees**: Reduces overfitting through data splitting
4. **Simplicity**: Clean code without complex hyperparameter tuning

---

## 🔧 Requirements

```txt
tensorflow>=2.12.0
tensorflow-decision-forests>=1.2.0
pandas>=1.5.0
numpy>=1.23.0
```

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](../../issues).

---

## 📧 Contact

**Adinath Jagtap**

- Kaggle: [@adinathjagtap777](https://www.kaggle.com/adinathjagtap777)
- GitHub: [@Adinath-Jagtap]([https://github.com/Adinath-Jagtap])

---

## ⭐ Show Your Support

Give a ⭐️ if this project helped you!

---

## 📚 References

- [Kaggle Titanic Competition](https://www.kaggle.com/c/titanic)
- [TensorFlow Decision Forests](https://www.tensorflow.org/decision_forests)
- [Gradient Boosted Trees](https://en.wikipedia.org/wiki/Gradient_boosting)

---

<div align="center">
  <sub>Built with ❤️ for the Kaggle community</sub>
</div>
