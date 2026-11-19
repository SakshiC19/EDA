# Exploratory Data Analysis on Loan Approval Data

A Jupyter Notebook project covering the complete data-preprocessing and EDA workflow on a loan approval dataset.

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Repository Structure](#repository-structure)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Usage](#usage)
- [Analysis Workflow](#analysis-workflow)
- [Techniques Covered](#techniques-covered)
- [Contributing](#contributing)
- [Author](#author)

## Overview
- Takes a raw loan application dataset and prepares it for machine learning
- Handles missing values
- Detects and treats outliers
- Encodes categorical variables
- Applies statistical transformations
- Scales numeric features
- Every step is explained with comments and markdown notes, so it works as a learning reference

## Dataset
- **File:** `loan_approved.csv`
- **Size:** 600+ loan applicant records, 13 columns
- **Columns:**
  - `Loan_ID`: unique loan identifier
  - `Gender`: Male / Female
  - `Married`: Yes / No
  - `Dependents`: number of dependents
  - `Education`: Graduate / Not Graduate
  - `Self_Employed`: whether the applicant is self-employed
  - `ApplicantIncome`: applicant's income
  - `CoapplicantIncome`: co-applicant's income
  - `LoanAmount`: loan amount requested
  - `Loan_Amount_Term`: loan term in months
  - `Credit_History`: 1 = meets guidelines, 0 = does not
  - `Property_Area`: Urban / Semiurban / Rural
  - `Loan_Status (Approved)`: target variable (Y / N)

## Repository Structure
```
EDA/
├── EDA.ipynb           # Main analysis notebook
├── loan_approved.csv   # Loan approval dataset
└── README.md
```

## Tech Stack
- Python 3
- Pandas, NumPy
- Matplotlib, Seaborn
- SciPy
- Scikit-learn
- Jupyter Notebook

## Installation
1. Clone the repository
   ```bash
   git clone https://github.com/SakshiC19/EDA.git
   cd EDA
   ```
2. (Optional) Create a virtual environment
   ```bash
   python -m venv venv
   source venv/bin/activate        # Windows: venv\Scripts\activate
   ```
3. Install dependencies
   ```bash
   pip install pandas numpy matplotlib seaborn scipy scikit-learn jupyter
   ```

## Usage
1. Launch Jupyter
   ```bash
   jupyter notebook EDA.ipynb
   ```
2. Run the cells in order from top to bottom
3. Keep `loan_approved.csv` in the same folder as the notebook

## Analysis Workflow
1. **Data loading**
   - Read the CSV
   - Inspect with `head()`, `info()` and `isnull().sum()`
2. **Missing value imputation**
   - Mode for `Gender`, `Married`, `Dependents`, `Self_Employed` and `Loan_Amount_Term`
   - Median for `LoanAmount` (skewed numeric column)
   - Zero for missing `Credit_History`
3. **Outlier detection**
   - Boxplots for `LoanAmount` and `ApplicantIncome`
4. **Outlier treatment**
   - Winsorization
   - IQR method
5. **Categorical encoding**
   - Convert categories into numbers
6. **Feature transformation**
   - Reduce skewness of numeric features
7. **Feature scaling**
   - Bring numeric features onto comparable scales

## Techniques Covered
- **Missing values:** mode, median, constant imputation
- **Outlier handling:** boxplot visualization, Winsorization, IQR method
- **Encoding:** One-Hot Encoding (`get_dummies`), Label Encoding, Ordinal Encoding
- **Transformations:** Log, Exponential, Square Root, Box-Cox
- **Scaling:** StandardScaler, MinMaxScaler, RobustScaler

## Contributing
- Fork the repository
- Create a feature branch
- Open a pull request

## Author
**Sakshi**
- GitHub: [@SakshiC19](https://github.com/SakshiC19)
