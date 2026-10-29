# DATA-ANALYTICS-ABOUT-THE-DATASET

## AIM

To analyse a dataset using Python and Pandas, examine its structure and data types, identify missing and duplicate records, and prepare the data for further analysis.

## THEORY

Pandas is a Python library used to organise and analyse tabular data. A DataFrame stores data in rows and columns. It provides methods to inspect dataset dimensions and data types, calculate summary statistics, identify missing values, detect duplicate records, and clean data before further analysis.

## ALGORITHM

1. Start the program and import Pandas.
2. Create a sample dataset and load it into a DataFrame.
3. Display the dataset and its dimensions.
4. Count missing values and identify duplicate records.
5. Remove duplicate rows.
6. Replace missing numerical values with the mean of the remaining valid values.
7. Display the cleaned dataset and stop.

## PYTHON PROGRAM

```python
import pandas as pd

data = {
    "Student": ["Anu", "Bala", "Charu", "Dev", "Anu"],
    "Age": [19, 20, 19, 21, 19],
    "Marks": [85, None, 92, 76, 85],
    "Department": ["EEE", "CSE", "EEE", "ECE", "EEE"]
}

df = pd.DataFrame(data)

print("Original Dataset:")
print(df)
print("\nDataset Shape:", df.shape)
print("\nMissing Values:")
print(df.isnull().sum())
print("\nDuplicate Records:", df.duplicated().sum())

df = df.drop_duplicates()
df["Marks"] = df["Marks"].fillna(round(df["Marks"].mean(), 1))

print("\nCleaned Dataset:")
print(df)
```

## OUTPUT

```text
Original Dataset:
  Student  Age  Marks Department
0     Anu   19   85.0        EEE
1    Bala   20    NaN        CSE
2   Charu   19   92.0        EEE
3     Dev   21   76.0        ECE
4     Anu   19   85.0        EEE

Dataset Shape: (5, 4)

Missing Values:
Student       0
Age           0
Marks         1
Department    0
dtype: int64

Duplicate Records: 1

Cleaned Dataset:
  Student  Age  Marks Department
0     Anu   19   85.0        EEE
1    Bala   20   84.3        CSE
2   Charu   19   92.0        EEE
3     Dev   21   76.0        ECE
```

## RESULT

The sample dataset was analysed using Pandas. One duplicate row was removed, and the missing Marks value was replaced with the mean of the valid marks after duplicate removal. The cleaned dataset was displayed successfully.
