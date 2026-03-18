📊 KPMG Data Analysis Project

-------------------------------------------
📌 Overview:

This project focuses on analyzing transactional data from the KPMG dataset to extract meaningful insights. The primary goal is to clean, transform, and prepare the data for further analysis and visualization.

--------------------------------------------
📂 Dataset:

File: `KPMG_VI_New_raw_data_update_final.xlsx`
Sheet Used: `Transactions`
Key Columns:
  `customer_id`
  `transaction_date`

--------------------------------------------

⚙️ Technologies Used:

  Python 🐍
  Pandas 📊
  Jupyter Notebook 📓
  Visual Studio Code(VS Code)

--------------------------------------------

🔧 Data Preprocessing Steps

1. Load Dataset:
   Save the given file into the local to ide this will ease in loading the date, if the files are saved local disk you need to provide the     exact path.

```python

df1 = pd.read_excel('KPMG_VI_New_raw_data_update_final.xlsx', sheet_name='Transactions')

```

2. Fix Column Headers

* First row contained column names, so it was reassigned as header.

```python
df1.columns = df1.iloc[0]
df1 = df1[1:].reset_index(drop=True)
df1.columns = df1.columns.str.strip()
```

3. Select Required Columns

Extracted only relevant fields for analysis.

```python
df2 = df1[['customer_id', 'transaction_date']].copy()
```

--------------------------------------------

🧠 Key Concepts Applied

 **Data Cleaning**

  1. Handling incorrect headers
  2. Removing unwanted rows
  3. Stripping column names

 **Data Selection**

  1. Filtering relevant columns for focused analysis

 **Deep Copy in Pandas**

  1. Used `.copy()` to avoid unintended modifications to the original dataset



## 📈 Possible Analysis (Next Steps)

  1. Customer transaction frequency analysis
  2. Cohort analysis
  3. Time-based trend analysis
  4. Customer segmentation

--------------------------------------------

🚀 How to Run

1. Clone the repository

```bash
git clone <your-repo-link>
```

2. Install dependencies

```bash
pip install pandas openpyxl jupyter
```

3. Run Jupyter Notebook

```bash
jupyter notebook
```

--------------------------------------------

