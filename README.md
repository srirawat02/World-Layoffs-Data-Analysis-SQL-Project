# World-Layoffs-Data-Analysis-SQL-Project

## 📌 Project Overview
   
This project analyzes global layoffs across different years using SQL.
The goal of this project is to clean raw layoff data and perform exploratory data analysis (EDA) to uncover trends, patterns, and business insights related to workforce reductions worldwide.

This project demonstrates practical SQL skills including:

- Data cleaning

- Data transformation

- Window functions

- Aggregations

- Common Table Expressions (CTEs)

- Ranking and rolling totals

## 🎯 Purpose of the Project

Layoffs have significantly impacted the global economy in recent years. This project aims to:

- Understand layoff patterns across years

- Identify industries and companies most affected

- Analyze trends over time

- Extract insights that could help businesses, analysts, and policymakers understand workforce dynamics

## 📊 Data Source

The dataset used for this project is a public World Layoffs dataset, which includes:

- Company

- Location

- Industry

- Total laid off

- Percentage laid off

- Date

- Funding stage

- Country

- Funds raised (in millions)

The dataset contains global layoff events across multiple years.

## 🧹 Phase 1: Data Cleaning (SQL)

A complete data cleaning process was performed before analysis.

✔ Steps Performed:

1. Removed Duplicates

- Used ROW_NUMBER() with PARTITION BY

- Created a staging table to safely remove duplicate rows

2. Standardized Data

- Trimmed company names

- Standardized industry names (e.g., all variations of “crypto” → “Crypto”)

- Cleaned country names (e.g., removed trailing dots in “United States.”)

- Converted date column from text to proper DATE format

3. Handled Null and Blank Values

- Converted blank industries to NULL

- Used self-join technique to populate missing industry values

- Removed rows where both total_laid_off and percentage_laid_off were NULL

4. Removed Unnecessary Columns

- Dropped helper column (row_num) after duplicate removal

This ensured the dataset was accurate, consistent, and analysis-ready.

## 📈 Phase 2: Exploratory Data Analysis (EDA)

After cleaning, several business questions were answered.

## 🔎 Key Questions Answered

- Which companies completely shut down?

- Which company had the highest total layoffs?

- When did the layoffs start?

- Which industry had the most layoffs?

- Which country had the most layoffs?

- Which year recorded the highest layoffs?

- Which funding stage had the most layoffs?

- How many layoffs occurred per month each year?

- What is the rolling progression of layoffs over time?

- Who were the top 5 companies with the most layoffs each year?

## 💡 Key Insights

Here are some major insights discovered from the analysis:

- Certain companies reported 100% layoffs, indicating complete shutdowns.

- Layoffs peaked during specific years, showing economic downturn impact.

- A few industries consistently dominated total layoffs.

- Some countries contributed disproportionately to global layoffs.

- Rolling monthly totals revealed clear upward and downward layoff waves.

- Large late-stage or well-funded companies were not immune to layoffs.

- The top 5 companies per year showed that layoffs were concentrated among major tech-driven firms.

## 🏢 Business Problem

Organizations, investors, and analysts often struggle to:

- Track workforce reductions globally

- Understand industry-specific downturns

- Identify macroeconomic impact periods

- Compare startup stages with layoff trends

This project transforms raw data into structured insights that support:

- Workforce trend analysis

- Industry risk evaluation

- Economic cycle interpretation

- Strategic decision-making

## 📊 Impact

This analysis can help:

- Analysts identify high-risk industries

- Investors evaluate funding-stage vulnerability

- Companies benchmark workforce stability

## 🧠 SQL Concepts Used

- ROW_NUMBER()

- DENSE_RANK()

- Window Functions (SUM() OVER)

- CTEs (Common Table Expressions)

- Aggregate Functions (SUM, MAX, MIN)

- Date Functions (STR_TO_DATE, YEAR)

- Data Standardization

- Self Joins

- Data Cleaning Techniques

## 📌 Conclusion

This project demonstrates an end-to-end SQL workflow:

Raw Dataset → Data Cleaning → Data Transformation → Exploratory Data Analysis → Business Insights

The analysis highlights how global layoffs evolved over time, which industries and countries were most impacted, and how workforce reductions progressed month by month.
