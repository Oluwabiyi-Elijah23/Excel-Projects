# 🚴 Bike Sales Dashboard

![Bike Sales Dashboard](../Excel%20Projects%20Images/Bike%20Sales%20Project%20Images/Dashboard.png)
## Introduction

This project focuses on analyzing customer demographics and purchasing behavior to uncover factors that influence bike purchases. Using Microsoft Excel, the dataset was cleaned, transformed, analyzed, and visualized through an interactive dashboard.

The objective of this project was to identify patterns in customer income, commute distance, age groups, education levels, and geographic regions to better understand the characteristics of customers who are more likely to purchase bikes.

The project demonstrates the use of Excel for data cleaning, exploratory data analysis (EDA), dashboard development, and interactive reporting.

---

## Dataset Overview

The dataset contains customer demographic and behavioral information related to bike purchases.

### Dataset Fields

- Customer ID
- Marital Status
- Gender
- Income
- Children
- Education
- Occupation
- Home Owner Status
- Number of Cars
- Commute Distance
- Region
- Age
- Purchased Bike

The dataset was originally provided in Excel format and served as the foundation for the analysis.

---

## Project Workflow

The project was completed in four major phases:

1. Data Cleaning & Transformation
2. Exploratory Data Analysis (EDA)
3. Dashboard Development
4. Interactive Analysis using Slicers

---# 🧹 Data Cleaning & Transformation

Data quality improvements were performed before beginning the analysis.

## Raw Dataset

![Raw Dataset](../Excel%20Projects%20Images/Bike%20Sales%20Project%20Images/Raw_Data.png)

The original dataset contained customer demographic and purchasing information related to bike sales. Before conducting any analysis, the data was reviewed and cleaned to improve accuracy, consistency, and readability.

---

## Duplicate Removal

The dataset contained duplicate records that could potentially distort the analysis.

### Actions Performed

- Removed 26 duplicate records
- Ensured every record represented a unique customer
- Improved the reliability of subsequent analysis and visualizations

---

## Standardizing Marital Status

The original dataset used abbreviated values.

| Original Value | Updated Value |
|---------------|---------------|
| M | Married |
| S | Single |

The **Find and Replace** feature in Microsoft Excel was used to improve readability and ensure end users could easily understand the values contained within the dataset.

---

## Standardizing Gender Values

The Gender column originally contained abbreviated values.

| Original Value | Updated Value |
|---------------|---------------|
| M | Male |
| F | Female |

This transformation improved dashboard readability and user understanding.

---

## Income Formatting

The Income column was already formatted as a currency field.

Additional formatting included:

- Reducing decimal places
- Improving the visual presentation of financial values
- Making values easier to read during analysis and reporting

---

## Commute Distance Standardization

The commute distance categories were adjusted to improve logical ordering and readability.

| Original Value | Updated Value |
|---------------|---------------|
| 10+ Miles | More than 10 Miles |

This adjustment made the dataset more intuitive for end users and improved dashboard presentation.

---

## Creating Age Brackets

A new column called **Age Bracket** was created using a Nested IF Statement.

Customers were grouped into the following categories:

| Age Range | Age Bracket |
|------------|------------|
| Under 31 | Adolescent |
| 31 – 54 | Middle Age |
| 55 and Above | Old |

This transformation simplified demographic analysis and enabled easier comparison of purchasing behavior across age groups.

---

## Cleaned Dataset

![Cleaned Dataset](../Excel%20Projects%20Images/Bike%20Sales%20Project%20Images/Cleaned_Data.png)

The cleaned dataset provided a standardized and analysis-ready foundation for Exploratory Data Analysis (EDA), Pivot Tables, Pivot Charts, and Dashboard Development.

---

## Excel Skills Demonstrated During Data Cleaning

- Remove Duplicates
- Find and Replace
- Data Standardization
- Currency Formatting
- Nested IF Statements
- Data Transformation
- Dataset Preparation

---# 📊 Exploratory Data Analysis (EDA)

After completing the data cleaning process, Exploratory Data Analysis (EDA) was performed using Pivot Tables and Pivot Charts to identify trends and patterns within the dataset.

---

## 1️⃣ Average Income by Gender

The first analysis examined the average income of customers based on gender and whether they purchased a bike.

### Results

| Gender | No Purchase | Purchased |
|---------|------------|-----------|
| Female | $53,440 | $55,774 |
| Male | $56,208 | $60,124 |

### Insight

Customers who purchased bikes generally had higher average incomes than customers who did not purchase bikes.

This pattern was observed across both male and female customer groups, suggesting that income may play a role in purchasing decisions.

### Screenshot
![alt text](<../Excel Projects Images/Bike Sales Project Images/Pivot _Table_1.png>)


### Visualization

A column chart was used to visualize the average income comparison.

Formatting improvements included:

- Removal of gridlines
- Removal of field buttons
- Addition of a data table
- Improved chart readability

---

## 2️⃣ Purchase Count by Commute Distance

The second analysis investigated the relationship between commute distance and bike purchases.

### Results

| Commute Distance | No Purchase | Purchased |
|------------------|------------|-----------|
| 0–1 Miles | 166 | 200 |
| 1–2 Miles | 92 | 77 |
| 2–5 Miles | 67 | 95 |
| 5–10 Miles | 116 | 76 |
| More than 10 Miles | 78 | 33 |

### Insight

Customers with a commute distance of **0–1 miles** recorded the highest number of bike purchases.

Interestingly, bike purchases generally declined as commute distance increased.

This suggests that customers with shorter commuting requirements may find bicycles to be a practical transportation option.

### Screenshot
![alt text](<../Excel Projects Images/Bike Sales Project Images/Pivot_Table_2.png>)


### Visualization

A line chart was used to visualize the relationship between commute distance and bike purchases.

Formatting improvements included:

- Removal of field buttons
- Addition of chart titles
- Axis formatting
- Improved readability

---

## 3️⃣ Bike Purchases by Age Bracket

The final analysis explored bike purchasing behavior across different age groups.

### Results

| Age Bracket | No Purchase | Purchased |
|------------|------------|-----------|
| Adolescent | 71 | 39 |
| Middle Age | 318 | 383 |
| Old | 130 | 59 |

### Insight

The **Middle Age** category recorded the highest number of bike purchases.

The **Adolescent** category recorded the lowest number of purchases.

This indicates that middle-aged customers represent the strongest customer segment within the dataset.

### Screenshot

![Age Bracket Analysis](../Excel%20Projects%20Images/Bike%20Sales%20Project%20Images/Pivot_Table_3.png)







### Visualization

A line chart was used to visualize purchasing behavior across age groups.

Formatting improvements included:

- Chart title customization
- Gridline removal
- Data table addition
- Axis formatting

---

## Excel Skills Demonstrated

This project showcases several Excel skills including:

### 📊 Pivot Tables

Used to summarize customer purchasing behavior and identify trends across multiple dimensions.

### 📉 Pivot Charts

Created visual representations of analytical findings and transformed Pivot Table outputs into meaningful business insights.

### 🧮 Formulas and Functions

- Nested IF Statements
- Find & Replace
- Currency Formatting
- Data Transformation

### 🎛️ Slicers

Added interactivity to the dashboard and enabled dynamic filtering.

### 🔗 Report Connections

Connected slicers to multiple Pivot Tables and Pivot Charts for synchronized dashboard filtering.

### 🧹 Data Cleaning

- Duplicate Removal
- Data Standardization
- Category Transformation
- Data Preparation

---# 📊 Dashboard Development

After completing the exploratory analysis, an interactive dashboard was developed to provide a centralized view of customer purchasing behavior.

The dashboard was designed to allow users to quickly identify trends and patterns while also providing the ability to perform deeper analysis through interactive filtering.

---

## Dashboard Features

### Dashboard Design

The dashboard was developed on a separate worksheet to provide a clean and professional reporting interface.

Key design improvements included:

- Removal of worksheet gridlines
- Dashboard title creation and formatting
- Proper chart alignment and spacing
- Consistent visual design
- Improved dashboard readability

### Dashboard Screenshot

![Age Bracket Analysis](../Excel%20Projects%20Images/Bike%20Sales%20Project%20Images/dashboard.png)


---

## Interactive Features

Three slicers were implemented to improve dashboard usability and enable deeper analysis of customer purchasing behavior.

### Marital Status

Available options:

- Married
- Single

### Region

Available options:

- Europe
- North America
- Pacific

### Education

Available options:

- Bachelors
- Graduate Degree
- High School
- Partial College
- Partial High School

---

### Report Connections

Initially, the slicers only interacted with a single Pivot Table and Pivot Chart.

To ensure all visualizations responded simultaneously to user selections, the **Report Connections** feature in Microsoft Excel was used to connect all Pivot Tables and Pivot Charts to the dashboard slicers.

This created a fully interactive dashboard experience and improved the ability to explore the data dynamically.

---

# 💡 Additional Insights

After completing the dashboard, additional analysis was performed using the slicers and filters to uncover deeper insights.

---

## Regional Analysis

The dashboard revealed notable differences in bike purchasing behavior across regions.

### Bike Purchases by Region

| Region | Purchases |
|----------|-----------|
| North America | 220 |
| Europe | 148 |
| Pacific | 113 |

### Insight

North America recorded the highest number of bike purchases with **220 purchases**.

Europe recorded the second-highest number of purchases with **148 purchases**.

The Pacific region recorded the lowest number of purchases with **113 purchases**.

This suggests that North America represented the strongest market within the dataset.

---

## Education Analysis

A deeper analysis was conducted on customers within the North America region.

### Insight

Among customers who purchased bikes in North America:

- Bachelor's Degree holders recorded the highest number of purchases
- Graduate Degree holders recorded the second-highest number of purchases
- Partial College customers recorded the third-highest number of purchases

These findings suggest that customers with higher educational attainment represented a significant portion of bike purchasers within the dataset.

---



# 🛠️ Tools Used

- Microsoft Excel
- Pivot Tables
- Pivot Charts
- Slicers
- Report Connections
- Data Cleaning Techniques
- Dashboard Design
- Data Visualization
- Exploratory Data Analysis (EDA)

---

# Conclusion

This project demonstrates how Microsoft Excel can be used to transform raw customer data into meaningful business insights.

Through data cleaning, exploratory analysis, Pivot Tables, Pivot Charts, and interactive dashboard development, the project identified relationships between income levels, commute distance, age groups, geographic regions, and bike purchasing behavior.

Key findings from the analysis revealed that:

- Customers who purchased bikes generally earned higher incomes.
- Customers with shorter commute distances recorded the highest number of bike purchases.
- Middle-aged customers represented the largest purchasing segment.
- North America recorded the highest number of bike purchases among all regions.
- Customers with Bachelor's Degrees represented a significant proportion of bike purchasers.

The resulting dashboard provides a user-friendly interface for exploring customer trends and supports data-driven decision-making through interactive filtering and visual analytics.

🚴📊