Exploratory Data Analysis on Loan Approval Data

A Jupyter Notebook project that walks through the complete data-preprocessing and exploratory data analysis (EDA) workflow on a loan approval dataset: handling missing values, detecting and treating outliers, encoding categorical variables, applying statistical transformations, and scaling features.

Table of Contents
Overview
Dataset
Repository Structure
Tech Stack
Installation
Usage
Analysis Workflow
Techniques Covered
Contributing
Author
Overview

Raw data is rarely ready for modeling. This project demonstrates how to take a loan application dataset from its raw form to a clean, numeric, well-scaled dataset that is ready for machine learning. Each step in the notebook is explained with comments and markdown notes, making it useful as a learning reference for data preprocessing.

Dataset

File: loan_approved.csv: 600+ loan applicant records with 13 columns.

Column	Description
Loan_ID	Unique loan identifier
Gender	Applicant gender (Male / Female)
Married	Marital status (Yes / No)
Dependents	Number of dependents
Education	Graduate / Not Graduate
Self_Employed	Whether the applicant is self-employed
ApplicantIncome	Applicant's income
CoapplicantIncome	Co-applicant's income
LoanAmount	Loan amount requested
Loan_Amount_Term	Loan term (in months)
Credit_History	Credit history (1 = meets guidelines, 0 = does not)
Property_Area	Urban / Semiurban / Rural
Loan_Status (Approved)	Target variable: loan approved (Y / N)
Repository Structure
EDA/
├── EDA.ipynb           # Main analysis notebook
├── loan_approved.csv   # Loan approval dataset
└── README.md
Tech Stack
Python 3
Pandas, NumPy
Matplotlib, Seaborn
SciPy
Scikit-learn
Jupyter Notebook
Installation
bash
# Clone the repository
git clone https://github.com/SakshiC19/EDA.git
cd EDA

# (Optional) create a virtual environment
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate

# Install dependencies
pip install pandas numpy matplotlib seaborn scipy scikit-learn jupyter
Usage
bash
jupyter notebook EDA.ipynb

Run the cells in order from top to bottom. Make sure loan_approved.csv is in the same folder as the notebook.

Analysis Workflow
Data loading: read the CSV and inspect it with head(), info(), and isnull().sum().
Missing value imputation: fill gaps using the most appropriate statistic for each column.
Mode for categorical columns (Gender, Married, Dependents, Self_Employed) and Loan_Amount_Term
Median for skewed numeric columns (LoanAmount)
Zero for missing Credit_History values
Outlier detection: visualize LoanAmount and ApplicantIncome with boxplots.
Outlier treatment: apply Winsorization and the IQR method.
Categorical encoding: convert categories into numbers.
Feature transformation: reduce skewness of numeric features.
Feature scaling: bring numeric features onto comparable scales.
Techniques Covered
Category	Methods
Missing values	Mode, median, constant imputation
Outlier handling	Boxplot visualization, Winsorization, IQR method
Encoding	One-Hot Encoding (get_dummies), Label Encoding, Ordinal Encoding
Transformations	Log, Exponential, Square Root, Box-Cox
Scaling	StandardScaler, MinMaxScaler, RobustScaler
Contributing

Suggestions and improvements are welcome. Fork the repository, create a feature branch, and open a pull request.

Author

Sakshi GitHub: @SakshiC19
