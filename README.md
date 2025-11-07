# 🧠 Data Analyst Practical Exam: Product Sales Analysis
## 📊 Project Overview

This project was completed as part of the Data Analyst Certification (DataCamp) practical exam.
It analyzes six weeks of sales data from Pens and Printers, an office-supply company that recently launched a creative stationery line.

The objective is to identify which sales method — Email, Call, or Email and Call — generated the highest revenue and customer engagement, and to provide actionable insights for future sales strategy.

## 🎯 Business Problem

The company tested three different outreach methods during the launch campaign.
Management needs to know:

Which sales method led to the highest average revenue.

How revenue trends evolved over time (Week 1–6).

Whether customer characteristics (years as customer, site visits, etc.) correlate with sales results.

## 🧩 Objectives

Validate and clean the dataset to ensure reliable insights.

Visualize trends in sales performance by week and by method.

Quantify the relationship between online engagement and revenue.

Summarize key findings in clear, business-friendly language.

## 🛠️ Tools & Libraries

Python 3.11+

pandas – data manipulation and aggregation

numpy – numeric operations

matplotlib / seaborn – data visualization

Jupyter Notebook – interactive analysis environment

## 🧹 Data Validation
Check	Description	Result
Missing Values	Checked for nulls in all columns	revenue contained missing values
Consistency	Normalized variations in sales_method (e.g. “email”, “Email + Call”)	Standardized to 3 categories
Range Validity	Verified week 1–6, reasonable revenue/nb_sold values	Valid
Uniqueness	Checked for duplicate customer_id entries	None found
Outliers	IQR method on revenue	634 outliers (≈4.6%)
Correlation	nb_site_visits ↔ revenue	r = 0.32 (weak–moderate positive)

All results were exported to product_sales_validation_flags.csv for traceability.

## 📈 Exploratory Analysis & Visualization

Key plots generated:

Average Revenue per Week by Sales Method
– Seaborn lineplot (sorted x-axis, hue by method, markers for readability)

Distribution of Revenue per Sales Method
– Boxplots to visualize variability and outliers

Revenue vs. Site Visits
– Scatterplot with trend line to illustrate positive correlation

Example code snippet:

sns.lineplot(
    data=weekly, 
    x='week', 
    y='revenue', 
    hue='sales_method_clean', 
    marker='o', 
    linewidth=2, 
    ci=None
)

## 💡 Key Insights

“Email and Call” produced the highest overall average revenue.

Week 5 showed the peak performance for all methods.

Customers with higher site visit frequency generated more revenue.

Outliers represented legitimate high-value customers rather than errors.

## 🧾 Deliverables

product_sales.csv – original dataset

product_sales_validation_flags.csv – validated dataset with flags

product_sales_analysis.ipynb – full analysis notebook

presentation.pdf – executive summary slides (optional for GitHub)

## 📚 Skills Demonstrated

Data Validation & Cleaning — handling missing values, outliers, and inconsistencies

Data Visualization — communicating trends through clear, business-relevant charts

Statistical Thinking — using correlation and aggregation to support decisions

Data Storytelling — framing insights for non-technical audiences

## 🏁 Conclusion

This analysis demonstrates how data-driven insights can guide business strategy by revealing which sales approaches generate the best outcomes.
The project emphasizes reproducibility, clarity, and actionable storytelling — core competencies for a certified Data Analyst.
