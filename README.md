This project involves a complete data cleaning pipeline for the Netflix dataset using Python (Pandas). The goal is to transform the raw CSV into a clean, structured, and analysis-ready format.

Internship Task – ElevateLabs | Task 1

Tool Used: Google Colab

DATASET: netflix.csv | Rows: 8807 | Columns: 12

-------------------

UPLOADED FILES :

'Task 1.ipynb - Colab' = CODE FILE IN PDF FORMAT

GOOGLE COLAB CODE LINK :
( https://colab.research.google.com/drive/1IKx8bS2vD1bt_w-GRZskorUv61-cP9AS?usp=sharing )

'altered_file'         = FINAL OUTPUT FILE IN CSV FORMAT

-----------------------

TASK PERFORMED :

1. Handling Missing Values
Identified missing values using .isnull() and .sum().

Dropped rows where director or cast were missing.

Filled missing values in the country column with "Unknown".

Filled missing values in the rating column with the mode.

Dropped remaining missing rows.

2. Removing Duplicates
Removed exact duplicate rows using .drop_duplicates().

Removed partial duplicates (ignoring show_id) using .drop_duplicates(subset=...).

3. Standardizing Text Values
Applied consistent formatting across key columns

Removed incorrect values in rating (like "66 MIN").

Split duration into numeric and unit components.

Converted listed_in into lists for multi-genre support.

4. Date Formatting


Converted date_added to a uniform format (dd-mm-yyyy) using pd.to_datetime().

5. Renaming Column Headers

Renamed all column headers to lowercase with underscores (snake_case).

6. Data Type Correction

Optimized data types using .convert_dtypes().

---

NOTE:

"You can't store a column in a DataFrame as both a true datetime64[ns] and in 'dd-mm-yyyy' format. This is because datetime columns store raw timestamps internally, while formatting like 'dd-mm-yyyy' turns them into strings (object dtype). Formatting is only for display—not storage in datetime type."

---

FINAL OUTPUT:

Cleaned dataset has 5695 rows and no missing or malformed values.

Output file saved as altered_file.csv.
