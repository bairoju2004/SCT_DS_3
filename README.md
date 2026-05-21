#  Decision Tree Classifier — Bank Marketing Dataset

> **Task 03** | Data Science Internship at **SkillCraft Technology**

Predicting whether a customer will subscribe to a term deposit based on demographic and behavioral data, using a Decision Tree Classifier trained on the UCI Bank Marketing Dataset.

---

## 📌 Objective

Build a supervised machine learning model that classifies customers into two categories:
- **Yes** — will subscribe to a term deposit
- **No** — will not subscribe

This helps banks target the right customers during marketing campaigns, reducing cost and improving conversion rates.

---

## 📂 Dataset

| Property | Details |
|----------|---------|
| Source | [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Bank+Marketing) |
| File | `bank-additional-full.csv` |
| Rows | 41,188 |
| Features | 20 input features + 1 target (`y`) |
| Target | `y` — Has the client subscribed? (`yes` / `no`) |

### Key Features
- **Demographic** — age, job, marital status, education
- **Financial** — housing loan, personal loan, default status
- **Campaign** — contact type, number of contacts, last contact duration
- **Economic** — employment variation rate, euribor 3-month rate, consumer price index

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3 | Programming language |
| Pandas | Data loading & manipulation |
| NumPy | Numerical operations |
| Scikit-learn | Model building & evaluation |
| Matplotlib | Visualizations |
| Seaborn | Statistical plots |
| Google Colab | Development environment |

---

## 🔄 Project Workflow

```
1. Download Dataset (UCI Repository)
        ↓
2. Exploratory Data Analysis (EDA)
        ↓
3. Data Preprocessing
   - Handle 'unknown' values
   - Label Encoding
   - Feature/Target separation
        ↓
4. Train / Test Split (80% / 20%, stratified)
        ↓
5. Build Decision Tree Classifier
   - criterion = 'gini'
   - max_depth = 5
        ↓
6. Model Evaluation
   - Accuracy, Precision, Recall, F1-Score
   - Confusion Matrix
        ↓
7. Visualization
   - Tree structure plot
   - Feature importance chart
        ↓
8. Hyperparameter Tuning (GridSearchCV)
        ↓
9. Final Results & Conclusions
```

---

## 📊 Results

| Metric | Base Model | Tuned Model |
|--------|-----------|-------------|
| Accuracy | ~90% | ~91% |
| F1-Score (Yes class) | ~52% | ~55% |
| Overfitting | None | None |

> ⚠️ **Note:** The dataset is imbalanced (~88% No / ~12% Yes). F1-Score is the primary evaluation metric, not just accuracy.

---

## 🔍 Key Insights

- 📞 **Call duration** is the strongest predictor — longer calls correlate strongly with subscription
- 📈 **Euribor 3-month rate** reflects economic conditions and affects customer decisions
- 👤 **Age** plays a moderate role — older customers tend to subscribe more
- 📵 Customers contacted **fewer times** during a campaign are more likely to subscribe
- 💡 Behavioral signals outweigh demographic ones in predicting subscription

---

## 📁 File Structure

```
📦 decision-tree-bank-marketing/
├──  Task03_Decision_Tree_Bank_Marketing.ipynb   # Main Colab notebook
├──  README.md                                   # Project documentation
└──  bank-additional/
    └── bank-additional-full.csv                   # Dataset (auto-downloaded in notebook)
```

---

## 🚀 How to Run

1. Open [Google Colab](https://colab.research.google.com/)
2. Upload `SCT_DS_3.ipynb`
3. Run all cells — the dataset is **auto-downloaded** from UCI, no manual setup needed
4. All required libraries are pre-installed in Colab

---


⭐ *If you found this helpful, consider giving the repo a star!*
