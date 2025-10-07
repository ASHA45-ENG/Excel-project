## README NOTE – Excel Assignment

### Overview
This Excel workbook contains data cleaning, transformation, and analysis tasks completed as part of the Excel Assignment.  
The work was mainly done on two sheets:  
- **Data** – Original dataset provided.  
- **Staging** – Cleaned and transformed dataset used for analysis and reporting.  

---

### Part A – Data Preparation
In this section, the raw dataset from the **Data** sheet was reviewed and cleaned.  
Key actions included:  
1. **Removing duplicates** and ensuring all rows had valid entries.  
2. **Converting the dataset to a table** to enable structured referencing.  
3. **Formatting columns** (dates, currency, percentages) for consistency.  
4. **Adding helper columns** to support later analysis.  

---

### Part B – Data Transformation (Staging Sheet)
This section involved creating calculated columns in the **Staging** sheet to prepare the dataset for insights and pivot analysis.

| Step | Column Name | Description | Formula Summary |
|------|--------------|--------------|-----------------|
| 1 | **Corrected Unit Price** | Calculates accurate unit price based on gross revenue and quantity. | `=GrossRevenue / Quantity` |
| 2 | **Unit Price Check** | Flags suspicious unit prices differing greatly from corrected prices. | `=IF(ABS([@UnitPrice]-[@CorrectedUnitPrice])>1,"Suspicious","OK")` |
| 3 | **Discount Pct Check** | Computes discount percentage applied on the item. | `=([@UnitPrice]/[@ListPrice])` |
| 4 | **High Discount Pct** | Classifies discounts above 30% as HIGH, others as NORMAL. | `=IF([@DiscountPct]>0.3,"HIGH","NORMAL")` |
| 5 | **Price Band** | Categorises products into LOW, MEDIUM, or HIGH based on corrected price. | Custom logic |

---

### Part C – Pivot Analysis
(If included in your assignment)  
A pivot table was created in a new sheet named **Q4_Cohort** to summarise and analyse the data based on:  
- Customer segment  
- Price Band  
- Cohort Month  
- Profit and Revenue Metrics  

---

### Notes
All formulas were implemented using **structured table references** in Excel.  
The **Staging** sheet serves as the foundation for all analysis and pivot tables.  

Formatting standards applied:  
- Percentages: 2 decimal places  
- Dates: `dd-mmm-yyyy`  
- Currency: 2 decimal places  

---

### Author
Prepared by: **Asha**  
Date: **October 2025**  
File: *Copy of Excel_1_assignment.xlsx*
