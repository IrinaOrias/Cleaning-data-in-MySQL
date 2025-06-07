***Data Cleaning in MySQL – Layoffs Dataset Project***

Dataset: https://www.kaggle.com/datasets/swaptr/layoffs-2022

---

***Project Summary***

In this project, I worked with a real-world dataset that tracks company layoffs across different industries and countries. Using MySQL, I cleaned and organized the data to make it accurate, consistent, and ready for analysis. I created a staging environment to safely clean the data without affecting the original, removed duplicate entries, fixed inconsistent naming in fields like "industry" and "country," corrected date formats, and handled missing values.

After the cleaning process, the dataset became much easier to work with — now it's ready to be used for creating dashboards, spotting trends, or building models that help explain layoff patterns.

---

***Objective***

The goal of this project was to prepare a high-quality version of the layoffs dataset by:

- Removing duplicates  
- Fixing inconsistent values in company names, countries, and industries  
- Formatting date fields properly  
- Filling or removing missing values  
- Ensuring the dataset is reliable for analysis or visualization  

---

***Tools Used***

- MySQL – for writing queries and cleaning the data  
- SQL Workbench – as the main interface to work with the database  

---

***Key Cleaning Steps***

Step | Description  
-----|-------------  
**Table Duplication** | Created `layoffs_staging` and `layoffs_staging2` tables to safely clean data without altering the original.  
**Deduplication** | Used a `ROW_NUMBER()` function in a CTE (Common Table Expression) to identify and remove exact duplicate rows.  
**Trimming Values** | Cleaned extra spaces in company names using `TRIM()` to standardize values.  
**Standardizing Categories** | Corrected inconsistencies like “United States” vs. “United States.” or “Crypto” vs. “Cryptocurrency.”  
**Date Formatting** | Converted messy date fields into proper `DATE` format using `STR_TO_DATE()` and `ALTER TABLE`.  
**Handling Missing Values** | Identified and addressed missing values in important columns like `industry`, `total_laid_off`, and `percentage_laid_off`.  
**Manual Fixes** | Reassigned known industry values for companies like Airbnb, Juul, and Carvana.  
**Final Touches** | Removed temporary columns and checked that the dataset was clean and complete.  

---

***Results / Impact***

- The final cleaned table has no duplicate rows.  
- Categories like industry and country are now consistent and easy to group or filter.  
- The date column is properly formatted, allowing for time-based analysis.  
- The cleaned dataset can now be used to:  
  - Perform exploratory data analysis  
  - Create visual dashboards  
  - Build predictive models on layoff trends  

---
