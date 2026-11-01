# Student Grade Analyzer 📊

A very simple, beginner-friendly Python project using **pandas** to manage, analyze, and export student grades. This project is designed for anyone just starting out with data analysis in Python.

---

## Features
* **DataFrame Creation:** Converts raw Python dictionaries into structured pandas DataFrames.
* **Data Exploration:** Uses built-in pandas methods like `.head()`, `.info()`, and `.describe()` to inspect data.
* **Row-wise Calculations:** Computes individual student averages across multiple subjects.
* **Conditional Filtering:** Filters and extracts top-performing students based on specific criteria.
* **Aggregation:** Calculates overall class averages for individual subjects.
* **File Export:** Saves the modified dataset into a new CSV file (`student_grades_analyzed.csv`).

---

## Prerequisites
Make sure you have Python and `pandas` installed on your machine. You can install pandas via terminal or command prompt:

```bash
pip install pandas
```

---

## How to Run
1. Clone or download this project repository.
2. Create a Python script (e.g., `analyzer.py`) and paste the analysis code.
3. Run the script using your terminal or IDE:

```bash
python analyzer.py
```

---

## Code Overview
```python
import pandas as pd

# 1. Create dataset
data = {
    'Student': ['Alice', 'Bob', 'Charlie', 'Diana', 'Ethan'],
    'Math': [85, 90, 78, 92, 65],
    'Science': [88, 76, 95, 89, 70],
    'English': [90, 85, 80, 95, 75]
}
df = pd.DataFrame(data)

# 2. Calculate student averages
df['Average'] = df[['Math', 'Science', 'English']].mean(axis=1)

# 3. Filter top students
top_students = df[df['Average'] > 85]

# 4. Export results
df.to_csv('student_grades_analyzed.csv', index=False)
```

---

## License
This project is open-source and free to use for educational purposes.