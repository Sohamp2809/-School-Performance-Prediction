# School Performance Prediction

Welcome, mate! This project focuses on **cleaning** and **transforming** a dataset of schools to ultimately help us **predict** their performance.

## Table of Contents

- [Overview](#overview)
- [Data Source](#data-source)
- [Preprocessing](#preprocessing)
- [Generated Files](#generated-files)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

We start with a **raw dataset** containing:
- **School Name, City**  
- **Academic Details** (Math Score, English Score, National & State Ranks)  
- **Demographics** (Race %, AP Classes, Electives, etc.)  
- **School Type** (Public or Private)  

We then **clean, transform, and prepare** the data for **ML** or **predictive** analyses.

## Data Source

- **`Final Raw Data.csv`**  
  A 481×17 CSV with missing values, duplicates, special characters, and unranked placeholders.

## Preprocessing

1. **Load Data**  
   - Read `Final Raw Data.csv` into a Pandas DataFrame.

2. **Clean Missing Values**  
   - Drop columns with the most missing values.  
   - Drop rows with any remaining missing values.

3. **Filter Invalid Ranks**  
   - Remove rows with “unranked”, “Not found”, or “na”.

4. **Remove Duplicates**  
   - Identify duplicates by `School Name + City` and keep the first occurrence.

5. **Transform**  
   - Remove special characters (`$`, `%`) from numeric columns.  
   - Convert `Yes/No` columns to **binary** `1/0`.

6. **Save**  
   - Export preprocessed data as `cleaned_and_transformed.csv`.  
   - Generate `transformed_data.csv` with further binary conversions, etc.

> **Note**: We **do not commit** these final CSV files to GitHub. They’re generated locally on your machine!

---

## Generated Files

- **`cleaned_and_transformed.csv`**  
  Contains partially cleaned data (no missing values, duplicates removed, special chars removed).

- **`transformed_data.csv`**  
  Final file with additional transformations (binary columns, etc.).

These files are **not** committed to the repo by default. If you want them on GitHub, remove them from `.gitignore` or upload manually.-

## Installation

1. **Clone the repository** (or download the ZIP):

   ```bash
   git clone https://github.com/YourUsername/School-Performance-Prediction.git
   cd School-Performance-Prediction

2. **Create and activate a virtual environment** (optional but recommended):

   ```bash
   # On Mac/Linux:
   python -m venv venv
   source venv/bin/activate

   # On Windows:
   python -m venv venv
   venv\Scripts\activate

3. **Install the required dependencies:**

  ```bash
  pip install pandas numpy

Or, if a `requirements.txt` file is provided:

```bash
pip install -r requirements.txt


## Project Structure

```bash
School-Performance-Prediction/
├── Final Raw Data.csv
├── .gitignore
├── README.md
├── <your_preprocessing_notebook_or_script>.ipynb   # or .py script
└── ...

## Contributing

1. **Fork** this repository.

2. **Create** a feature branch:
   ```bash
   git checkout -b feature/your-feature-name

3. **Commit** your changes:
   ```bash
   git commit -m "Add your feature description"

4. **Push** to your branch:
   ```bash
   git push origin feature/your-feature-name

5. **Open a Pull Request** on GitHub.




