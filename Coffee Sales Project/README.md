# ☕ Coffee Sales Dashboard

![Coffee Sales Dashboard](../Excel%20Projects%20Images/Coffee%20Sales%20Project%20Images/Dashboard.png)

## Introduction

This project focuses on analyzing coffee sales data to uncover trends in customer purchasing behavior, product performance, and revenue generation across different countries.

The dataset was provided in an Excel workbook containing multiple related tables. Using Microsoft Excel, the data was gathered, transformed, analyzed, and visualized through an interactive dashboard.

The project demonstrates the use of Excel for data gathering, data cleaning, exploratory data analysis (EDA), dashboard development, and interactive reporting through slicers and timelines.

---

## Dataset Overview

The dataset was provided in an Excel workbook containing three worksheets:

### Orders Table

The Orders table served as the primary fact table for the project. It contained transactional information such as:

- Order ID
- Order Date
- Customer ID
- Product ID
- Quantity

Several customer and product-related fields were present but initially unpopulated.

### Customers Table

The Customers table contained customer-related information including:

- Customer Name
- Email
- Country
- Loyalty Card Status

### Products Table

The Products table contained product-related information including:

- Coffee Type
- Roast Type
- Size
- Unit Price
- Profit

### Raw Dataset

#### Orders Table

![Raw Orders Table](../Excel%20Projects%20Images/Coffee%20Sales%20Project%20Images/Raw_Orders_Table.png)

#### Customers Table

![Raw Customers Table](../Excel%20Projects%20Images/Coffee%20Sales%20Project%20Images/Raw_Customers_Table.png)

#### Products Table

![Raw Products Table](../Excel%20Projects%20Images/Coffee%20Sales%20Project%20Images/Raw_Products_Table.png)

---

## Project Workflow

The project was completed in four major phases:

1. Data Gathering
2. Data Cleaning & Transformation
3. Exploratory Data Analysis (EDA)
4. Dashboard Development

---

# 📥 Data Gathering

The first phase of the project involved gathering data from multiple worksheets and consolidating it into the Orders table.

The Orders table originally contained several empty columns that required information from both the Customers and Products tables.

To populate the missing fields, the **XLOOKUP** function was used extensively.

### Customer Information Retrieval

Using XLOOKUP, the following fields were retrieved from the Customers table:

- Customer Name
- Email
- Country

This ensured that each order was associated with the correct customer information.

### Product Information Retrieval

Using XLOOKUP, the following fields were retrieved from the Products table:

- Coffee Type
- Roast Type
- Size
- Unit Price

This allowed each order to be linked to its corresponding product details.

### Sales Calculation

After populating the customer and product information, a new **Sales** column was created.

The Sales column was calculated using:

```excel
= Unit Price * Quantity
```

This calculation provided the total revenue generated from each order based on the quantity purchased.

The result of the data gathering process was a single consolidated dataset containing customer, product, and transaction information, making it suitable for further analysis and reporting.

### Data Gathering Result

![Cleaned Dataset Part 1](../Excel%20Projects%20Images/Coffee%20Sales%20Project%20Images/Cleaned_Data_1.png)

![Cleaned Dataset Part 2](../Excel%20Projects%20Images/Coffee%20Sales%20Project%20Images/Cleaned_Data_2.png)

---
## 🧹 Data Cleaning & Transformation

After consolidating the data into a single analytical table, several cleaning and transformation steps were performed to improve data quality, readability, and reporting effectiveness.

### Creating Coffee Type Names

The original **Coffee Type** column contained abbreviated values:

| Abbreviation | Coffee Type |
|-------------|------------|
| Ara | Arabica |
| Exc | Excelsa |
| Lib | Liberica |
| Rob | Robusta |

A new column called **Coffee Type Name** was created using a Nested IF statement to convert the abbreviations into their full names.

This transformation improved readability and ensured that dashboard users could easily understand the different coffee categories.

### Creating Roast Type Names

The original **Roast Type** column contained abbreviated values:

| Abbreviation | Roast Type |
|-------------|-----------|
| D | Dark |
| M | Medium |
| L | Light |

A new column called **Roast Type Name** was created using a Nested IF statement to display the full roast type names.

This transformation enhanced reporting clarity and improved dashboard usability.

### Date Formatting

The **Order Date** column was reformatted to improve readability.

| Original Format | Updated Format |
|----------------|---------------|
| 05/03/26 | 5-March-2026 |

This formatting change reduced the likelihood of confusion between day and month values.

### Size Formatting

The **Size** column was standardized by:

- Formatting values to one decimal place
- Appending the unit **kg** to each value

Examples:

- 0.2 kg
- 0.5 kg
- 1.0 kg
- 2.5 kg

This improved consistency throughout the dataset and dashboard.

### Currency Formatting

The following columns were formatted using the Accounting data type:

- Unit Price
- Sales

This ensured that all monetary values were displayed consistently using the US Dollar currency format.

### Loyalty Card Population

The Orders table originally contained an empty Loyalty Card field.

Using **XLOOKUP**, Loyalty Card information was retrieved from the Customers table and populated into the Orders table.

This enabled further customer segmentation and dashboard filtering.

### Duplicate Check

The dataset was checked for duplicate records using Excel's **Remove Duplicates** feature.

**Result:**

- No duplicate records were found.

### Converting Data to an Excel Table

The final dataset was converted into an Excel Table using:

```excel
CTRL + T
```

The table was renamed to:

```excel
Orders
```

Converting the dataset into a structured table improved formula consistency, filtering capabilities, and data management.

---
# 📊 Exploratory Data Analysis (EDA)

After completing the data gathering and data transformation stages, Pivot Tables and Pivot Charts were used to explore the dataset and uncover meaningful business insights.

All Pivot Tables used in this project were created on a dedicated worksheet called **Pivot Tables**.

---

## 1️⃣ Total Sales Over Time

The first analysis focused on understanding how coffee sales changed over time and how each coffee type contributed to overall revenue.

To perform this analysis, a Pivot Table was created using:

- Order Date (Years and Months)
- Sales
- Coffee Type Name

The objective was to track revenue generated by each coffee type between **2019 and 2022**.

### Screenshot

![Total Sales Over Time](../Excel%20Projects%20Images/Coffee%20Sales%20Project%20Images/Pivot_Table_1.png)

### Key Insights

- Revenue remained relatively stable across the years, indicating consistent customer demand for coffee products.

- The highest monthly revenue observed in the analysis occurred in **February 2020**, generating approximately **$1,798** in sales.

- Several months across different years generated more than **$1,500** in revenue, suggesting that strong sales performance was not limited to a single period.

- Revenue performance was distributed across all four coffee types rather than being driven by a single product category.

- **Liberica**, **Arabica**, and **Excelsa** consistently contributed significant portions of total revenue across multiple years.

- The sales data for **2022** covered only the period between **January and August**. As a result, the lower annual revenue observed for 2022 should not be interpreted as a decline in business performance because the year does not contain a complete twelve-month sales cycle.

- The analysis suggests that the business maintained a relatively balanced product portfolio, with multiple coffee varieties contributing to overall sales performance.

### Visualization

A Line Chart was used to visualize the sales trend over time and compare the performance of the different coffee types.

---

## 2️⃣ Sales by Country

The second analysis examined revenue generated across different countries.

The dataset contained sales records from three countries:

- United States
- Ireland
- United Kingdom

### Results

| Country | Total Sales |
|----------|------------:|
| United Kingdom | $2,799 |
| Ireland | $6,697 |
| United States | $35,639 |

### Screenshot

![Sales by Country](../Excel%20Projects%20Images/Coffee%20Sales%20Project%20Images/Pivot_Table_2.png)

### Key Insights

- The **United States** generated the highest revenue, contributing approximately **79%** of total sales.

- **Ireland** contributed approximately **15%** of total sales.

- The **United Kingdom** contributed approximately **6%** of total sales.

- The significant difference between the United States and the other two countries suggests that the business has a much larger customer base or stronger market presence within the United States.

- The results indicate that Ireland and the United Kingdom may represent potential growth opportunities for future expansion and marketing efforts.

- Despite generating the lowest revenue, the United Kingdom still contributed meaningful sales and may benefit from targeted promotional campaigns.

### Visualization

A Bar Chart was used to compare sales performance across the three countries.

---

## 3️⃣ Top Five Customers

The final analysis identified the highest revenue-generating customers.

### Results

| Customer | Total Sales |
|-----------|-----------:|
| Allis Wilmore | $317 |
| Brenn Dundredge | $307 |
| Terri Farra | $289 |
| Nealson Cuttler | $282 |
| Don Flintiff | $278 |

### Screenshot

![Top Five Customers](../Excel%20Projects%20Images/Coffee%20Sales%20Project%20Images/Pivot_Table_3.png)

### Key Insights

- **Allis Wilmore** generated the highest revenue among all customers with total purchases of **$317**.

- The difference between the highest-performing customer and the fifth-ranked customer was only **$39**, indicating that revenue is not heavily concentrated in a single customer.

- A relatively small gap between the top customers suggests a healthy distribution of revenue across multiple customers.

- Further investigation revealed that **four of the top five customers were from the United States**, while **one customer was from the United Kingdom**.

- This finding aligns with the country-level analysis, which showed that the United States is the company's strongest market.

### Visualization

A Bar Chart was used to compare the sales performance of the top five customers.

---
# 📊 Dashboard Development

After completing the exploratory data analysis, an interactive dashboard was developed to provide a centralized view of coffee sales performance.

The dashboard was designed to enable users to explore sales trends, customer performance, and geographic performance through interactive filtering and visual analytics.

### Dashboard Screenshot

![Coffee Sales Dashboard](../Excel%20Projects%20Images/Coffee%20Sales%20Project%20Images/Dashboard.png)

---

## Dashboard Features

The dashboard was designed using several formatting and visualization techniques to improve usability and presentation.

### Layout and Design

The following improvements were made during dashboard creation:

- Created and formatted a dashboard title section
- Applied a consistent color theme throughout the dashboard
- Removed worksheet gridlines for a cleaner appearance
- Organized charts, slicers, and timelines into a structured layout
- Applied chart titles across all visualizations
- Added data labels where appropriate
- Formatted chart axes for improved readability
- Customized chart backgrounds and dashboard styling
- Used alignment tools to maintain a professional dashboard layout

---

## Interactive Features

To enhance user interaction and data exploration, both Timelines and Slicers were incorporated into the dashboard.

### Timeline

A Timeline was added based on the **Order Date** field.

The timeline enables users to:

- Filter sales data by year and month
- Analyze performance across different periods
- Explore revenue trends over time

This provides greater flexibility when examining historical sales performance.

### Roast Type Slicer

The Roast Type slicer allows users to filter the dashboard by:

- Dark Roast
- Medium Roast
- Light Roast

This feature enables users to identify which roast categories contribute most to sales performance.

### Size Slicer

The Size slicer allows users to filter dashboard results by package size:

- 0.2 kg
- 0.5 kg
- 1.0 kg
- 2.5 kg

Additional analysis revealed that **0.5 kg** was the most frequently purchased coffee size within the dataset.

### Loyalty Card Slicer

The Loyalty Card slicer enables comparisons between:

- Customers with a loyalty card
- Customers without a loyalty card

This feature allows users to explore the relationship between customer loyalty and purchasing behavior.

---

## Report Connections

The **Report Connections** feature was used to connect all Pivot Tables and Pivot Charts to the dashboard's slicers and timeline.

This ensured that:

- All charts respond dynamically to filters
- Dashboard components remain synchronized
- Users can perform interactive analysis across multiple dimensions simultaneously

This functionality transformed the dashboard from a static report into an interactive analytical tool.

---

## Additional Insights

Several additional observations were identified while interacting with the dashboard.

### Balanced Customer Revenue Distribution

The relatively small difference between the top five customers indicates that revenue is distributed across multiple customers rather than being concentrated in one individual.

This reduces the risk associated with dependence on a single high-value customer.

### Diverse Product Performance

Multiple coffee varieties contributed significantly to overall revenue.

Rather than relying on one dominant product, the business benefits from a diversified product portfolio.

### Potential Expansion Opportunities

Ireland and the United Kingdom generated lower sales compared to the United States.

These markets may represent opportunities for targeted marketing campaigns and future business growth.

---

## 🛠️ Excel Skills Demonstrated

This project showcases several Microsoft Excel skills and techniques including:

### 📥 Data Gathering

- XLOOKUP
- Multi-table data integration
- Data consolidation

### 🧹 Data Cleaning & Transformation

- Data standardization
- Date formatting
- Currency formatting
- Duplicate validation
- Category transformation

### 🧮 Formulas & Functions

- XLOOKUP
- Nested IF Statements
- Arithmetic Calculations

### 📊 Data Analysis

- Pivot Tables
- Data aggregation
- Trend analysis
- Customer analysis
- Geographic analysis

### 📈 Data Visualization

- Pivot Charts
- Line Charts
- Bar Charts

### 🎛️ Dashboard Development

- Slicers
- Timelines
- Report Connections
- Dashboard formatting
- Interactive filtering



















## 🛠️ Tools Used

- Microsoft Excel
- XLOOKUP
- Nested IF Statements
- Pivot Tables
- Pivot Charts
- Slicers
- Timelines
- Report Connections
- Data Cleaning Techniques
- Dashboard Design

---

## Conclusion

This project demonstrates how Microsoft Excel can be used to gather, transform, analyze, and visualize data from multiple related tables.

Through the use of XLOOKUP, data cleaning techniques, Pivot Tables, Pivot Charts, and interactive dashboard features, the project transformed raw coffee sales data into meaningful business insights.

The final dashboard provides a user-friendly reporting interface that enables users to explore sales trends, customer performance, product preferences, and geographic performance through dynamic filtering and visual analytics.