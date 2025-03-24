# School Performance Prediction

Welcome, mate! This project is all about **cleaning** and **transforming** a dataset of schools, ultimately helping us **predict** their performance.

## Table of Contents

- [Overview](#overview)  
- [Data Source](#data-source)  
- [Preprocessing](#preprocessing)  
- [Generated Files](#generated-files)  
- [How to Run](#how-to-run)  
- [Project Structure](#project-structure)  
- [Contributing](#contributing)  
- [License](#license)

---

## Overview

We start with a **raw dataset** that includes:
- **School Name, City**  
- **Academic Details** (Math Score, English Score, National & State Ranks)  
- **Demographic Info** (Race %, Offers Electives, etc.)  
- **School Type** (Public or Private)

We then clean, transform, and prepare the data for potential **ML** or **predictive** tasks.

---

## Data Source

- **`Final Raw Data.csv`**  
  A 481×17 CSV with missing values, duplicates, special characters, and unranked placeholders.

---

## Preprocessing

1. **Load Data**: Reads `Final Raw Data.csv` into a DataFrame.  
2. **Clean Missing Values**:  
   - Drops columns with the most missing values.  
   - Drops rows with **any** missing values remaining.  
3. **Invalid Ranks**: Filters out placeholders like `"unranked"`, `"Not found"`, `"na"`.  
4. **Remove Duplicates**: By `School Name` + `City`.  
5. **Transform**:  
   - Removes special characters (`$`, `%`) from numeric columns.  
   - Converts `Yes`/`No` columns to binary `1`/`0`.  
6. **Save**:  
   - Creates `cleaned_and_transformed.csv`  
   - Further transformations → `transformed_data.csv`

> **Note**: We **do not commit** these final CSV files to GitHub. They’re generated locally on your machine!

---

## Generated Files

- **`cleaned_and_transformed.csv`**: After dropping missing values, duplicates, special chars.  
- **`transformed_data.csv`**: Final, with `Yes/No → 1/0`.

Neither is included in the repo, so you won’t see them on GitHub. If you want them in your remote repo, just remove them from `.gitignore` or manually upload.

---




## Installation

1. **Clone the repository** (or download the ZIP):
   ```bash
   git clone https://github.com/YourUsername/School-Performance-Prediction.git
   cd School-Performance-Prediction
2. **Create and activate a virtual environment** (optional but recommended):
   
   python -m venv venv
   source venv/bin/activate  # On Mac/Linux
  # or
  ```bash
    venv\Scripts\activate     # On Windows
3. **Install the required dependencies:**
   ```bash
   pip install pandas numpy
4. **Check New CSV Files:**(in your local folder)
After running the preprocessing script or notebook, you’ll see:

- **cleaned_and_transformed.csv**
- **transformed_data.csv**

These files are generated locally and are not included in the repository by default.
