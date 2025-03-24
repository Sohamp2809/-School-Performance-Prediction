# 🏫 School Performance Prediction

This project aims to predict and analyze school performance across Arizona using various features such as academic scores, racial demographics, school resources, and course offerings.

---

## 📂 Dataset Overview

- **Source File**: `Final Raw Data (1).csv`
- **Total Entries**: 481 schools
- **Columns**:
  - `School Name`, `City`
  - Course Offerings: `AP Classes?`, `Dual Enrollment?`, `Offers Electives?`
  - Performance: `Math Score`, `English Score`, `National Rank`, `AZ Rank`
  - Demographics: `Racial%-White`, `Racial%-Black`, `Racial%-Native`, `Racial%-Hispanic`, `Racial%-Asian`, `Racial%-Other`
  - School Info: `student_faculty_ratio`, `school_type`

---

## ⚙️ Preprocessing

- Cleaning categorical inconsistencies (`Yes` vs `yes`)
- Converting scores/ranks to numerical values
- Handling missing values appropriately
- Encoding categorical features for modeling

> ✅ **Note**: After running the `Pre-Processing.ipynb` notebook, a new preprocessed CSV file will be generated which is then used for modeling and analysis.

---

## 📁 Project Structure

```
School Performance Prediction/
├── Final Raw Data (1).csv             # Original dataset
├── Pre-Processing.ipynb               # Notebook for cleaning & preprocessing
├── School Performance Prediction.ipynb# Analysis, visualization, and modeling
├── README.md                          # This file
└── .git/                              # Git versioning folder
```

---

## 📊 Objectives

- Analyze correlations between performance and various features.
- Predict key outcomes like rank or score using regression/classification models.
- Explore how school offerings or demographics affect academic performance.

---

## 🚀 Getting Started

To run this project:
1. Open `Pre-Processing.ipynb` to clean the data and generate a new CSV.
2. Use the cleaned file in `School Performance Prediction.ipynb` to train models and visualize insights.

---

## 🧠 Future Enhancements

- Add more robust imputations or outlier handling
- Explore feature engineering with derived metrics
- Try ensemble models for better prediction

---

**Author**: *(Soham Patel)*  
**Last Updated**: March 2025
