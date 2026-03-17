# Analysis-of-a-telecommunications-company
# ConnectaTel – Customer Usage Analysis

An exploratory data analysis project focused on understanding **mobile service usage patterns** for ConnectaTel customers.

The project analyzes **calls and SMS behavior**, detects **outliers**, and builds **customer segments based on usage patterns** to support data-driven business decisions.

Identify usage patterns, detect atypical behaviors, and understand which customer segments show differentiated needs, in order to optimize the commercial offering and improve the user experience.

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-orange)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-green)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Charts-yellow)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-red)

---

# Project Objective

The goal of this project is to analyze how customers actually use mobile services in order to:

- Identify **usage patterns** in calls and text messages
- Detect **outliers or abnormal behavior**
- Understand how usage varies by **age and plan type**
- Create **customer segments based on usage**
- Generate **business insights to improve mobile plans**

---

# Datasets

The project uses three datasets.

### `plans.csv`
Plan catalog including:

- monthly price
- included minutes
- included data
- extra usage costs

---

### `users_latam.csv`
Customer information.

Main variables:

- `user_id`
- `age`
- `city`
- `plan`
- `reg_date`
- `churn_date`

Data quality issues detected:

- missing values in `city`
- invalid age values (`-999`)
- registration dates outside expected range

---

### `usage.csv`
User activity records.

Includes:

- phone calls (`duration`)
- text messages (`length`)

This dataset allows the analysis of **actual service consumption**.

Data quality issues detected:

- 0.125% Empty values in `Date`
- 55.19% Call Duration: 45% of users have made calls.
- 44.74% SMS Length: 55% of users have used messages included in the plan.
- Possible outliers were identified in message length `length` that could be explored further (e.g., concatenated messages, atypical records, potential outliers).

---

# Analysis Workflow

The project follows a structured data analysis process.

## 1️. Data Exploration
- dataset inspection
- variable types review
- identification of missing values

---

## 2️. Data Cleaning
- handling missing values
- fixing invalid age values
- converting date columns
- correcting inconsistent records

---

## 3️. User Usage Profile
Usage metrics were aggregated per user:

- total calls
- total messages
- total call minutes

This created a **user-level usage profile**.

---

## 4️. Exploratory Data Analysis (EDA)

Distribution analysis for:

- age
- number of calls
- number of messages
- call minutes

Distributions were compared **between Basic and Premium plans**.

---

## 5️. Outlier Detection

Outliers were identified using:

- **boxplots**
- **IQR method**

Variables analyzed:

- age
- call counts
- message counts
- call minutes

This helps detect:

- abnormal usage
- potential data errors
- extreme user behavior.

---

## 6️. Customer Segmentation

Users were classified into three usage segments:

- **Low usage**
- **Medium usage**
- **High usage**

Segmentation was based on the number of **calls and messages per user**.

This allows identifying **high-value customer groups**.

---

# Example Visualizations

Example visual outputs generated during the analysis.

### Distribution of call minutes by plan
![Call minutes distribution](images/minutes_distribution.png)
### Message usage by plan
![Messages distribution](images/messages_distribution.png)
### Customer usage segmentation
![Usage segmentation](images/usage_segmentation.png)

# How to Run the Project

Requirements

Install dependencies:

`pip install pandas numpy matplotlib seaborn jupyter`

Run in Google Colab

1. Open Google Colab
2. Upload the notebook

`connectatel_analysis.ipynb`

3. Upload datasets:

`plans.csv
users_latam.csv
usage.csv`

4. Run the notebook cells sequentially.

---

## Run Locally

Clone the repository:

`git clone https://github.com/yourusername/connectatel-analysis.git`

Navigate to the project folder:

`cd connectatel-analysis`

Launch Jupyter Notebook:

`jupyter notebook`

---

### Reproducibility

To reproduce the full analysis:

1. Load datasets
2. Execute data cleaning steps
3. Generate user usage profile
4. Perform exploratory data analysis
5. Detect outliers
6. Build customer segmentation
7. Review insights

The notebook is organized sequentially for easy replication.

---

## Key Skills Demonstrated

- Data Cleaning
- Exploratory Data Analysis (EDA)
- Data Visualization
- Outlier Detection
- Customer Segmentation
- Business Insight Generation

---

Author

Gerardo Olmedo – ConnectaTel
