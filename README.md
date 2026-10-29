# DATA-ANALYTICS-ABOUT-THE-DATASET

# AIM

To perform data analytics on a given dataset using Python and Pandas, understand the characteristics of the dataset, identify different types of data, examine missing values, and prepare the dataset for further analysis and machine learning.

# THEORY

Data analytics is the process of inspecting and organising data to identify its structure, quality, and useful patterns. Python's Pandas library provides tools for loading, examining, summarising, and cleaning tabular data.

A dataset can be loaded into a Pandas DataFrame, which stores data in rows and columns. Initial inspection uses methods such as `head()`, `shape`, `columns`, `info()`, and `dtypes` to view sample records, dataset dimensions, column names, non-null counts, and data types.

Columns may contain numerical data, categorical values, dates, or text. Descriptive statistics, obtained using methods such as `describe()`, help summarise numerical columns through measures such as count, mean, standard deviation, minimum, and maximum. Frequency counts can be used to examine categorical values.

Data quality is checked by identifying missing values with `isnull()` and counting them with `isnull().sum()`. Duplicate records can be detected using `duplicated()`. Depending on the dataset and the purpose of the analysis, missing values may be removed or filled using suitable values, and duplicates may be removed. Data types and inconsistent entries should also be checked before analysis.

These steps produce a clearer understanding of the dataset and help prepare reliable data for visualisation, statistical analysis, and machine-learning tasks. Any cleaning decision should preserve meaningful information and be appropriate to the data.

# RESULT

The dataset-analysis procedure using Python and Pandas was outlined. The dataset can be inspected for its dimensions, columns, data types, summary statistics, missing values, and duplicate records, providing a basis for data cleaning and further analysis.
