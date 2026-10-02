# Lenskart India Data Analysis Project

## 1. Cover Page

**Project Title:** Lenskart India Sales and Customer Data Analysis  
**Subtitle:** Exploratory Data Analysis, Data Quality Assessment, Business Insights and Recommendations

**Prepared By:** ____________________  
**Organization / Institute:** ____________________  
**Date:** 2 October 2026

**Tools Used:** Microsoft Excel, Python, Jupyter Notebook / VS Code / Google Colab  
**Technologies Used:** Python, Pandas, NumPy, Matplotlib, Seaborn

---

## 2. Executive Summary

### Project Objective
This project analyzes the provided **Lenskart India** transaction dataset to understand sales performance, product categories, geographic contribution, customer characteristics, payment behavior, discounts and sales trends over time.

### Dataset Overview
The main analytical sheet, **“Lenskart India,” contains 150,000 transaction records and 14 columns** covering orders from **1 January 2022 to 31 December 2025**. The dataset contains order details, location, channel, store type, product category, quantity, price, discount, net sales, payment mode and customer demographics.

### Analysis Performed
The project includes:
- Data loading and validation
- Data type and structure checking
- Missing-value and duplicate checking
- Descriptive statistics
- Univariate analysis
- Bivariate and multivariate analysis
- GroupBy and pivot-style analysis
- Correlation analysis
- Outlier assessment
- Feature engineering using year, month, year-month and age groups
- Business-oriented visualizations
- Data-supported recommendations

### Major Findings
- Total recorded net sales are **₹784,355,989.95** across **150,000 transactions**.
- Total quantity sold is **300,064 units**.
- Average transaction net sales amount is **₹5,229.04**; the median is **₹4,290.80**.
- Online sales represent approximately **50.09%** of total net sales, while offline sales represent **49.91%**.
- **Eyeglasses** has the highest net sales among the four product categories, but category sales are closely distributed.
- **Kerala** records the highest state-level net sales in this dataset.
- The annual sales totals are relatively stable from 2022 through 2025, with year-over-year changes of approximately **+0.95% in 2023, −1.17% in 2024 and +0.86% in 2025**.
- Quantity and unit price have the strongest relationships with net sales amount among the numeric variables analyzed.
- There are **530 high-side net-sales observations under the IQR rule**. These are not automatically errors; they may represent legitimate larger orders.

### Important Data Quality Finding
A consistency check found **18,592 records where `store_type = Online Only` but `sales_channel = Offline`**. This should be validated with the business/data owner before using store type and sales channel together for operational conclusions.

### Business Value
The analysis can help a business understand where sales are coming from, which product groups contribute most, how sales are distributed across channels and locations, and where data-quality controls may be needed.

### Final Outcome
The project converts a large transaction dataset into a structured set of descriptive statistics, visual evidence, data-quality findings and actionable business questions. It can also serve as a foundation for a Power BI dashboard or future predictive analytics project.

---

## 3. Introduction

This project is a practical data-analysis study based on Lenskart India transaction data. The goal is to convert raw transactional information into understandable business information.

Data analysis is important because companies collect large amounts of information every day. Raw data alone does not clearly show what is happening. Analysis helps identify patterns, compare groups, measure performance and find data-quality problems.

For a retail business, this type of analysis can support questions such as:
- Which products generate the most sales?
- Which states contribute the most revenue?
- Is the business more dependent on online or offline transactions?
- How stable are sales over time?
- Which payment methods are commonly used?
- Are there unusual or inconsistent records?

The expected outcome is a clear, evidence-based report that a beginner can understand and that can also be presented as a college, internship or portfolio project.

---

## 4. Problem Statement

The dataset contains a large number of transaction records across multiple years, locations, product categories and customer attributes. Without analysis, it is difficult to identify important sales patterns and data-quality issues.

The business problem is therefore to **analyze transaction-level sales data and convert it into reliable business insights**.

The analysis is useful because organizations can use it to:
- Monitor sales performance.
- Compare products and markets.
- Understand customer and payment patterns.
- Identify unusual observations.
- Improve reporting and dashboard design.
- Validate the quality of operational data.

---

## 5. Project Objectives

1. Understand the structure of the dataset.
2. Load the data correctly into Python.
3. Check data types and data quality.
4. Identify missing and duplicate records.
5. Examine numerical and categorical variables.
6. Perform exploratory data analysis (EDA).
7. Compare products, channels, states, store types and customer groups.
8. Analyze sales trends over time.
9. Create meaningful visualizations.
10. Identify data-quality inconsistencies.
11. Generate only evidence-based business insights.
12. Provide practical recommendations.
13. Create a foundation for future dashboard and predictive-analysis work.

---

## 6. Dataset Description

### Dataset Name
**Lenskart India**

### Source
Provided Excel workbook: **Lenskart India.xlsx**

### Primary Analytical Sheet
**Lenskart India**

### Dataset Size
- Rows: **150,000**
- Columns: **14**
- Date range: **2022-01-01 to 2025-12-31**
- Cities: **23**
- States: **16**
- Sales channels: **2**
- Store types: **4**
- Product categories: **4**
- Payment modes: **5**
- Customer gender categories: **3**

### Column Description

| Column | Type | Description |
|---|---|---|
| order_id | Text | Unique order identifier. |
| order_date | Date/Time | Date on which the order was recorded. |
| city | Categorical | Customer/order city. |
| state | Categorical | Customer/order state. |
| sales_channel | Categorical | Online or Offline sales channel. |
| store_type | Categorical | Type of store/order location. |
| product_category | Categorical | Product group purchased. |
| quantity | Numerical | Number of units in the order. |
| unit_price | Numerical | Price per unit before discount. |
| discount_percent | Numerical | Discount percentage applied. |
| net_sales_amount | Numerical | Final sales amount after discount. |
| payment_mode | Categorical | Payment method used. |
| customer_gender | Categorical | Recorded customer gender category. |
| customer_age | Numerical | Customer age in years. |

### Data-Type Summary

| Data Type | Columns |
|---|---|
| Date/Time | order_date |
| Numerical | quantity, unit_price, discount_percent, net_sales_amount, customer_age |
| Categorical | city, state, sales_channel, store_type, product_category, payment_mode, customer_gender |
| Text / Identifier | order_id |

---

## 7. Business Questions

The following questions can be answered using the available columns:

1. What is the total net sales amount?
2. How many transactions and units were recorded?
3. How do annual sales compare from 2022 to 2025?
4. Which product category has the highest net sales?
5. How do online and offline sales compare?
6. Which states contribute the most net sales?
7. Which cities contribute the most net sales?
8. Which store types contribute the most recorded sales?
9. Which payment modes are most common by transaction count and sales?
10. How is sales distributed across customer gender categories?
11. Which customer age groups contribute the most sales?
12. What are the monthly sales patterns?
13. How do quantity and unit price relate to net sales?
14. Are there unusual net-sales observations?
15. Are there inconsistencies between store type and sales channel?

---

## 8. Tools and Technologies

| Tool / Technology | Purpose | Real-world use |
|---|---|---|
| Python | Main programming language | Data analysis and automation |
| Pandas | Data manipulation | Cleaning, filtering and grouping tables |
| NumPy | Numerical calculations | Statistical and mathematical operations |
| Matplotlib | Visualization | Business charts |
| Seaborn | Statistical visualization | Heatmaps, distributions and relationship charts |
| Jupyter Notebook | Interactive analysis | Learning, experimentation and documentation |
| VS Code | Code development | Building reusable Python projects |
| Google Colab | Cloud-based Python environment | Running notebooks without local setup |
| Excel | Source data / validation | Business data storage and quick checking |

---

## 9. Project Workflow

```text
Problem Statement
        ↓
Dataset Collection
        ↓
Import Libraries
        ↓
Load Dataset
        ↓
Data Exploration
        ↓
Data Cleaning
        ↓
Exploratory Data Analysis
        ↓
Univariate Analysis
        ↓
Bivariate Analysis
        ↓
Multivariate Analysis
        ↓
Feature Engineering
        ↓
Data Visualization
        ↓
Business Insights
        ↓
Recommendations
        ↓
Conclusion
```

### Step-by-Step Explanation

**1. Problem Statement:** Define what the analysis needs to understand.

**2. Dataset Collection:** Obtain the Excel transaction dataset.

**3. Import Libraries:** Load Python packages such as Pandas and NumPy.

**4. Load Dataset:** Read the Excel sheet into a Pandas DataFrame.

**5. Data Exploration:** Understand rows, columns, types and summary statistics.

**6. Data Cleaning:** Check missing values, duplicates, invalid values and inconsistencies.

**7. EDA:** Explore distributions, categories and relationships.

**8. Univariate Analysis:** Study one variable at a time.

**9. Bivariate Analysis:** Compare two variables.

**10. Multivariate Analysis:** Study several variables together.

**11. Feature Engineering:** Create useful analytical columns such as year and age group.

**12. Visualization:** Convert important findings into charts.

**13. Business Insights:** Translate numerical results into understandable findings.

**14. Recommendations:** Suggest actions that are directly connected to the evidence.

**15. Conclusion:** Summarize the analysis and its business value.

---

## 10. Data Loading

### What is a DataFrame?

A **DataFrame** is a table-like structure in Pandas. It has rows and columns, similar to an Excel worksheet.

### Basic Python Code

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

df = pd.read_excel("Lenskart India.xlsx", sheet_name="Lenskart India")

print(df.head())
```

### Verify Loading

```python
print(df.shape)
print(df.columns)
print(df.dtypes)
```

Expected shape:

```text
(150000, 14)
```

This confirms that the primary transaction sheet contains 150,000 rows and 14 columns.

---

## 11. Data Exploration

### `head()`

**Purpose:** Shows the first five rows.

```python
df.head()
```

**Business interpretation:** Useful for quickly checking whether the dataset was loaded correctly.

### `tail()`

**Purpose:** Shows the last five rows.

```python
df.tail()
```

**Business interpretation:** Helps confirm that the end of the dataset is also present.

### `shape`

**Purpose:** Returns number of rows and columns.

```python
df.shape
```

**Result:** `(150000, 14)`

### `columns`

**Purpose:** Displays column names.

```python
df.columns
```

### `dtypes`

**Purpose:** Shows the data type of each column.

```python
df.dtypes
```

The dataset contains:
- 1 date/time column
- 5 numerical columns
- 7 categorical columns
- 1 text/identifier column

### `info()`

```python
df.info()
```

**Result:** All 150,000 records are non-null in every primary column.

### `describe()`

```python
df.describe()
```

Important numerical results:

| Variable | Mean | Median | Min | Max |
|---|---:|---:|---:|---:|
| Quantity | 2.0004 | 2 | 1 | 3 |
| Unit Price | ₹2,895.17 | ₹2,889 | ₹799 | ₹4,998 |
| Discount % | 9.75% | 10% | 0% | 25% |
| Net Sales | ₹5,229.04 | ₹4,290.80 | ₹599.25 | ₹14,994 |
| Customer Age | 41.10 | 41 | 18 | 64 |

---

## 12. Data Cleaning

### 12.1 Missing Values

```python
df.isnull().sum()
```

**Result:** Every primary column has **0 missing values**.

**Why required:** Missing values can affect calculations and charts.

**Method used:** Missing-value count was checked before analysis.

**Advantage:** No imputation was required.

**Limitation:** A zero missing count does not prove that every value is logically correct.

**Business impact:** The dataset can be analyzed without filling missing cells.

### 12.2 Duplicate Rows

```python
df.duplicated().sum()
```

**Result:** **0 duplicate rows**.

This means no completely duplicated transaction rows were found.

### 12.3 Data Types

The `order_date` field is already stored as a datetime value.

```python
df["order_date"] = pd.to_datetime(df["order_date"])
```

This is useful for year, month and time-trend analysis.

### 12.4 Empty Strings and Extra Spaces

The primary sheet contains populated categorical fields. A production data pipeline should still use checks such as:

```python
for col in df.select_dtypes(include="object"):
    df[col] = df[col].str.strip()
```

### 12.5 Numerical Validation

The following variables have no zero or negative values where positive values are expected:
- Quantity: 1–3
- Unit price: ₹799–₹4,998
- Net sales: ₹599.25–₹14,994
- Customer age: 18–64

Discount percentage ranges from **0% to 25%**.

### 12.6 Net Sales Formula Validation

The dataset follows:

```text
Gross Sales = Quantity × Unit Price
Discount Amount = Gross Sales × Discount %
Net Sales = Gross Sales − Discount Amount
```

A calculation check found **no difference between the calculated value and the recorded `net_sales_amount`**.

### 12.7 Important Store/Channel Inconsistency

A cross-check found:

**18,592 records** with:

```text
store_type = Online Only
sales_channel = Offline
```

This is logically unusual because an “Online Only” store type would normally be expected to align with an online channel.

**Recommended treatment:** Do not delete these rows automatically. First confirm the business definition with the data owner.

**Business impact:** This inconsistency can distort analyses that compare store type and channel.

### 12.8 Outlier Handling

Using the IQR method on `net_sales_amount`, **530 observations** fall above the calculated upper IQR boundary.

These records were **not automatically deleted**.

Why? An outlier is not necessarily an error. A large transaction can be a genuine business transaction.

---

## 13. Exploratory Data Analysis (EDA)

EDA means **Exploratory Data Analysis**. It is the process of examining data to understand patterns before making conclusions.

### 13.1 Univariate Analysis – Numerical Variables

#### Quantity

- Mean: **2.0004**
- Median: **2**
- Minimum: **1**
- Maximum: **3**
- Standard deviation: **0.8175**

The quantity field is tightly bounded between 1 and 3 units.

#### Unit Price

- Mean: **₹2,895.17**
- Median: **₹2,889**
- Minimum: **₹799**
- Maximum: **₹4,998**
- Standard deviation: **₹1,213.29**

The price variable has a wider range than quantity, making it an important component of transaction value.

#### Discount Percentage

- Mean: **9.75%**
- Median: **10%**
- Minimum: **0%**
- Maximum: **25%**

The most frequent discount level is **10%**.

#### Net Sales Amount

- Mean: **₹5,229.04**
- Median: **₹4,290.80**
- Minimum: **₹599.25**
- Maximum: **₹14,994**
- Standard deviation: **₹3,230.05**

The mean is above the median, indicating that some higher-value transactions raise the average.

#### Customer Age

- Mean: **41.10 years**
- Median: **41 years**
- Minimum: **18 years**
- Maximum: **64 years**

The dataset covers adult customers from 18 to 64 years.

### 13.2 Categorical Analysis

#### Product Category

| Product Category | Orders | Quantity | Net Sales |
|---|---:|---:|---:|
| product_category   |   Orders |   Quantity |   Net Sales |   Average Order Value |
|:-------------------|---------:|-----------:|------------:|------------------:|
| Eyeglasses         |    37717 |      75501 | 1.97929e+08 |           5247.74 |
| Contact Lenses     |    37472 |      75000 | 1.95855e+08 |           5226.7  |
| Computer Glasses   |    37406 |      74716 | 1.95479e+08 |           5225.87 |
| Sunglasses         |    37405 |      74847 | 1.95093e+08 |           5215.69 |

The four product categories are relatively close in sales contribution. Eyeglasses has the highest recorded net sales.

#### Sales Channel

| sales_channel   |   Orders |   Quantity |   Net Sales |
|:----------------|---------:|-----------:|------------:|
| Offline         |    74810 |     149730 | 3.91498e+08 |
| Online          |    75190 |     150334 | 3.92858e+08 |

Online and offline transactions are almost evenly split.

#### Payment Mode

| payment_mode   |   Orders |   Net Sales |
|:---------------|---------:|------------:|
| Net Banking    |    30189 | 1.58211e+08 |
| Debit Card     |    30063 | 1.57667e+08 |
| Credit Card    |    30033 | 1.57515e+08 |
| Cash           |    29962 | 1.56883e+08 |
| UPI            |    29753 | 1.5408e+08  |

Payment-mode sales are also relatively close, with Net Banking recording the highest total in this dataset.

#### Customer Gender

| customer_gender   |   Orders |   Net Sales |
|:------------------|---------:|------------:|
| Male              |    50225 | 2.62803e+08 |
| Female            |    49931 | 2.60908e+08 |
| Other             |    49844 | 2.60644e+08 |

The three gender categories have very similar transaction and sales totals.

---

## 14. Bivariate Analysis

### 14.1 Product Category vs Net Sales

**Chart:** `02_category_sales.png`

**Objective:** Compare sales contribution by product category.

**Why selected:** A bar chart makes category comparisons easy.

**Observation:** Eyeglasses has the highest net sales, followed by Contact Lenses, Computer Glasses and Sunglasses. The differences are relatively small.

**Business interpretation:** The dataset does not show extreme dependence on one product category.

![Product Category Sales](02_category_sales.png)

### 14.2 Sales Channel vs Net Sales

**Chart:** `03_channel_sales.png`

**Observation:** Online contributes approximately **50.09%** of total net sales and Offline approximately **49.91%**.

**Business interpretation:** Recorded sales are highly balanced between the two sales channels.

![Sales Channel](03_channel_sales.png)

### 14.3 State vs Net Sales

**Chart:** `04_state_sales.png`

**Observation:** Kerala has the highest state-level net sales in the dataset at approximately **₹69.11 million**.

**Business interpretation:** Geographic sales are uneven across the states represented, although the top seven states are all relatively close to one another.

![State Sales](04_state_sales.png)

### 14.4 Quantity, Unit Price and Net Sales

The correlation matrix is:

| Variable | Quantity | Unit Price | Discount % | Net Sales | Age |
|---|---:|---:|---:|---:|---:|
| Quantity | 1.000 | 0.001 | 0.001 | 0.663 | 0.001 |
| Unit Price | 0.001 | 1.000 | -0.004 | 0.680 | 0.005 |
| Discount % | 0.001 | -0.004 | 1.000 | -0.131 | 0.004 |
| Net Sales | 0.663 | 0.680 | -0.131 | 1.000 | 0.005 |
| Age | 0.001 | 0.005 | 0.004 | 0.005 | 1.000 |

**Interpretation:** In this dataset, net sales has its strongest simple linear relationships with quantity and unit price. The relationship with discount percentage is negative and weaker.

**Important:** Correlation does not prove causation.

---

## 15. Multivariate Analysis

### 15.1 Correlation Matrix

The correlation matrix shows the strength and direction of linear relationships among numerical variables.

The most notable relationships are:
- Quantity ↔ Net Sales: **0.663**
- Unit Price ↔ Net Sales: **0.680**
- Discount % ↔ Net Sales: **−0.131**
- Customer Age ↔ Net Sales: **0.005**

This indicates that transaction size and price are much more directly associated with recorded net sales than customer age.

### 15.2 GroupBy Analysis

Pandas `groupby()` is useful for answering business questions.

Example:

```python
df.groupby("product_category")["net_sales_amount"].sum().sort_values(ascending=False)
```

Another example:

```python
df.groupby("state")["net_sales_amount"].sum().sort_values(ascending=False)
```

### 15.3 Pivot Table

```python
pd.pivot_table(
    df,
    values="net_sales_amount",
    index="state",
    columns="product_category",
    aggfunc="sum"
)
```

This can be used to compare product performance across states.

### 15.4 Pair Plot

A pair plot can be useful for smaller analytical samples, but with 150,000 rows it may be computationally heavy. A sampled dataset can be used:

```python
sample_df = df.sample(3000, random_state=42)
sns.pairplot(
    sample_df[[
        "quantity",
        "unit_price",
        "discount_percent",
        "net_sales_amount",
        "customer_age"
    ]]
)
plt.show()
```

---

## 16. Feature Engineering

Feature engineering means creating useful analytical columns from existing data.

### 16.1 Year

```python
df["year"] = df["order_date"].dt.year
```

**Purpose:** Compare yearly performance.

### 16.2 Month

```python
df["month"] = df["order_date"].dt.month
```

**Purpose:** Study monthly patterns.

### 16.3 Year-Month

```python
df["year_month"] = df["order_date"].dt.to_period("M")
```

**Purpose:** Create a continuous monthly time series.

### 16.4 Gross Sales

```python
df["gross_sales"] = df["quantity"] * df["unit_price"]
```

**Purpose:** Calculate sales before discount.

### 16.5 Discount Amount

```python
df["discount_amount"] = (
    df["gross_sales"] * df["discount_percent"] / 100
)
```

**Purpose:** Quantify the monetary discount.

### 16.6 Customer Age Group

```python
bins = [17, 24, 34, 44, 54, 64]
labels = ["18-24", "25-34", "35-44", "45-54", "55-64"]

df["age_group"] = pd.cut(
    df["customer_age"],
    bins=bins,
    labels=labels
)
```

**Business benefit:** Age groups are easier to compare than individual ages.

---

## 17. Data Visualization

Only charts connected to useful business questions were selected.

### Chart 1 – Annual Sales

**File:** `01_annual_sales.png`

**Objective:** Compare yearly sales.

**Observation:** Annual sales are relatively stable across 2022–2025.

**Business interpretation:** The dataset does not show a large year-over-year structural change in total recorded sales.

![Annual Sales](01_annual_sales.png)

### Chart 2 – Product Category Sales

**File:** `02_category_sales.png`

**Objective:** Compare product categories.

**Observation:** Eyeglasses is the highest category, but the four categories are close.

**Business interpretation:** Sales are diversified across the four product categories.

![Category Sales](02_category_sales.png)

### Chart 3 – Channel Sales

**File:** `03_channel_sales.png`

**Objective:** Compare online and offline sales.

**Observation:** The split is approximately 50/50.

**Business interpretation:** Both channels represent significant recorded sales volume.

![Channel Sales](03_channel_sales.png)

### Chart 4 – State Sales

**File:** `04_state_sales.png`

**Objective:** Compare geographic contribution.

**Observation:** Kerala has the highest recorded state-level net sales.

**Business interpretation:** Geographic reporting can help identify markets for deeper investigation.

![State Sales](04_state_sales.png)

### Chart 5 – Age Group Sales

**File:** `05_age_sales.png`

**Objective:** Compare sales across age groups.

**Observation:** The 55–64 group records the highest total sales among the defined age groups.

**Business interpretation:** The dataset contains meaningful sales contribution across all age groups, so age segmentation can be useful for further customer analysis.

![Age Sales](05_age_sales.png)

### Chart 6 – Monthly Trend

**File:** `06_monthly_trend.png`

**Objective:** Examine monthly sales movement.

**Observation:** Monthly sales fluctuate, but the overall four-year annual totals remain relatively stable.

**Business interpretation:** Monthly monitoring may reveal short-term changes that annual totals can hide.

![Monthly Trend](06_monthly_trend.png)

---

## 18. Business Insights

### Insight 1 – Large Overall Transaction Base
The dataset contains **150,000 transactions** and approximately **300,064 units**, generating **₹784.36 million** in recorded net sales.

### Insight 2 – Annual Sales Are Stable
Annual net sales are approximately:
- 2022: **₹195.43 million**
- 2023: **₹197.29 million**
- 2024: **₹194.98 million**
- 2025: **₹196.66 million**

The highest annual total is in 2023.

### Insight 3 – Product Categories Are Closely Distributed
Eyeglasses contributes about **25.23%** of total net sales. Contact Lenses contributes **24.97%**, Computer Glasses **24.92%**, and Sunglasses **24.87%**.

### Insight 4 – Online and Offline Are Nearly Balanced
Online accounts for about **50.09%** of recorded net sales, while Offline accounts for **49.91%**.

### Insight 5 – Kerala Has the Highest State Sales
Kerala records approximately **₹69.11 million** in net sales, followed closely by Madhya Pradesh and Odisha.

### Insight 6 – Online Only Is the Largest Store-Type Group
The `Online Only` store type accounts for approximately **62.45%** of total recorded net sales. However, its presence in offline channel records requires validation before using this field for channel/store operational conclusions.

### Insight 7 – Customer Gender Totals Are Similar
The recorded sales for Male, Female and Other categories are close to one another. The dataset therefore does not show a large sales concentration in a single recorded gender category.

### Insight 8 – Age Has Very Little Linear Relationship with Net Sales
The correlation between customer age and net sales is approximately **0.005**, which is effectively very weak in a simple linear-correlation sense.

### Insight 9 – Transaction Size Matters
Quantity and unit price have the strongest correlations with net sales among the numerical variables. This is consistent with the structure of the sales formula.

### Insight 10 – Data Quality Needs Attention
The store type/channel mismatch is the main notable structural inconsistency found in the primary dataset.

---

## 19. Recommendations

### Recommendation 1 – Validate Store Type and Sales Channel Definitions
**Why:** 18,592 records show `Online Only` with `Offline`.

**Expected benefit:** Better channel reporting and more reliable operational dashboards.

### Recommendation 2 – Monitor Product Categories Separately
**Why:** The four product categories contribute similar levels of sales.

**Expected benefit:** Management can track category performance without assuming that one category dominates the business.

### Recommendation 3 – Use State-Level Reporting
**Why:** State sales vary across the dataset, with Kerala recording the highest total.

**Expected benefit:** Regional dashboards can help teams investigate market differences and plan local initiatives.

### Recommendation 4 – Track Monthly Sales Instead of Only Annual Sales
**Why:** Annual totals are stable while individual months vary.

**Expected benefit:** Monthly monitoring can identify short-term changes that annual summaries may hide.

### Recommendation 5 – Do Not Automatically Remove High-Value Transactions
**Why:** 530 records are above the IQR upper boundary for net sales, but they may be legitimate transactions.

**Expected benefit:** Prevents valid business records from being removed simply because they are statistically unusual.

### Recommendation 6 – Add Automated Data-Quality Rules
Recommended checks include:
- Store type vs sales channel consistency.
- Valid date range.
- Positive quantity.
- Valid price range.
- Valid discount percentage.
- Unique order ID.
- Valid customer age.

**Expected benefit:** Data errors can be detected before entering dashboards or reports.

---

## 20. Challenges Faced

### Challenge 1 – Large Dataset
150,000 rows are difficult to inspect manually.

**Solution:** Pandas was used for automated calculations and grouping.

### Challenge 2 – Multiple Excel Sheets
The workbook contains multiple sheets, including report/pivot-style sheets.

**Solution:** The transaction-level **Lenskart India** sheet was selected as the primary analytical source.

### Challenge 3 – Store/Channel Inconsistency
The Online Only / Offline combination appears in 18,592 records.

**Solution:** The records were retained but flagged for business validation.

### Challenge 4 – Outlier Identification
Some net-sales values are statistically high.

**Solution:** IQR analysis was performed, but observations were not deleted automatically.

### Challenge 5 – Business Interpretation
A statistical relationship does not automatically mean one variable causes another.

**Solution:** Findings are described as associations and dataset observations rather than causal claims.

---

## 21. Conclusion

This project analyzed the Lenskart India transaction dataset containing **150,000 records and 14 columns** covering 2022–2025.

The analysis examined:
- Overall sales
- Product categories
- Sales channels
- Store types
- States and cities
- Payment methods
- Customer demographics
- Annual and monthly trends
- Numerical relationships
- Data quality

The dataset contains approximately **₹784.36 million in recorded net sales** and **300,064 units**.

The product categories are closely balanced, online and offline sales are nearly evenly split, and annual sales remain relatively stable across the four years. Quantity and unit price show the strongest simple relationships with net sales among the numerical variables.

The most important data-quality observation is the mismatch between `Online Only` store type and `Offline` sales channel in **18,592 records**. This should be investigated before operational decisions are based on those two fields together.

Overall, the project demonstrates a complete beginner-friendly data-analysis workflow: loading data, exploring it, validating quality, analyzing patterns, visualizing results and converting findings into business-oriented recommendations.

---

## 22. Future Scope

### 22.1 Power BI Dashboard
Build an interactive dashboard containing:
- KPI cards
- Sales trend
- State map
- Product category analysis
- Channel comparison
- Payment analysis
- Customer age analysis

### 22.2 Predictive Analytics
Future projects could predict:
- Monthly sales
- Product demand
- High-value transactions
- Regional sales

### 22.3 Machine Learning
Potential models include:
- Regression for sales prediction
- Classification for customer segmentation
- Clustering for customer groups

### 22.4 Recommendation System
A future project could analyze product purchasing behavior and develop product recommendations.

### 22.5 Automation
Python scripts can automate:
- Excel ingestion
- Data-quality checks
- KPI calculation
- Report generation
- Dashboard data preparation

### 22.6 Real-Time Reporting
A production system could connect transaction data to a database and refresh business dashboards automatically.

---

## 23. References

### Dataset
- Lenskart India.xlsx — dataset supplied for this project.

### Python
- Python Documentation: https://docs.python.org/

### Pandas
- Pandas Documentation: https://pandas.pydata.org/docs/

### NumPy
- NumPy Documentation: https://numpy.org/doc/

### Matplotlib
- Matplotlib Documentation: https://matplotlib.org/stable/

### Seaborn
- Seaborn Documentation: https://seaborn.pydata.org/

---

# Beginner Python Analysis Code

The following code provides a simple starting point for reproducing the analysis.

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# Load data
df = pd.read_excel(
    "Lenskart India.xlsx",
    sheet_name="Lenskart India"
)

# Basic inspection
print(df.head())
print(df.tail())
print(df.shape)
print(df.columns)
print(df.dtypes)
df.info()
print(df.describe())

# Missing values
print(df.isnull().sum())

# Duplicates
print(df.duplicated().sum())

# Date conversion
df["order_date"] = pd.to_datetime(df["order_date"])

# Feature engineering
df["year"] = df["order_date"].dt.year
df["month"] = df["order_date"].dt.month
df["year_month"] = df["order_date"].dt.to_period("M")

# Gross sales
df["gross_sales"] = df["quantity"] * df["unit_price"]

# Discount amount
df["discount_amount"] = (
    df["gross_sales"] *
    df["discount_percent"] / 100
)

# Product analysis
product_sales = (
    df.groupby("product_category")["net_sales_amount"]
      .sum()
      .sort_values(ascending=False)
)

print(product_sales)

# State analysis
state_sales = (
    df.groupby("state")["net_sales_amount"]
      .sum()
      .sort_values(ascending=False)
)

print(state_sales)

# Channel analysis
channel_sales = (
    df.groupby("sales_channel")["net_sales_amount"]
      .sum()
)

print(channel_sales)

# Annual analysis
annual_sales = (
    df.groupby("year")["net_sales_amount"]
      .sum()
)

print(annual_sales)

# Correlation
numeric_cols = [
    "quantity",
    "unit_price",
    "discount_percent",
    "net_sales_amount",
    "customer_age"
]

print(df[numeric_cols].corr())

# Example chart
annual_sales.plot(kind="bar")
plt.title("Annual Net Sales")
plt.xlabel("Year")
plt.ylabel("Net Sales")
plt.show()
```

---

# Final Project Checklist

- [x] Cover Page
- [x] Executive Summary
- [x] Introduction
- [x] Problem Statement
- [x] Project Objectives
- [x] Dataset Description
- [x] Business Questions
- [x] Tools and Technologies
- [x] Project Workflow
- [x] Data Loading
- [x] Data Exploration
- [x] Data Cleaning
- [x] EDA
- [x] Bivariate Analysis
- [x] Multivariate Analysis
- [x] Feature Engineering
- [x] Data Visualization
- [x] Business Insights
- [x] Recommendations
- [x] Challenges
- [x] Conclusion
- [x] Future Scope
- [x] References
- [x] Beginner-friendly Python code
- [x] Dataset-supported findings only
