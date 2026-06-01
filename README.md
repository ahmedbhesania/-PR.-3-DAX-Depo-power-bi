# Power BI DAX Analysis Project

**Author:** Ahmed

---

## Project Overview

This project focuses on implementing DAX (Data Analysis Expressions) in Power BI to perform business calculations, time intelligence analysis, filter context evaluation, and data modeling enhancements.

The objective is to demonstrate understanding of calculated columns, measures, quick measures, DAX functions, filter behavior, relationships, and matrix-based reporting.

---

## Dataset Tables

The following tables were used in the project:

### Fact Tables

* Sales_Fact
* Returns_Fact

### Dimension Tables

* Customer_Dim
* Product_Dim
* Date_Dim
* Region_Dim

---

## Calculated Columns Created

### Profit

Calculated profit for each sales transaction.

```DAX
Profit = Sales_Fact[SalesAmount] - Sales_Fact[Cost]
```

### ReturnFlag

Identifies whether a transaction was returned.

```DAX
ReturnFlag = "Returned" / "Not Returned"
```

### Customer Full Name

Combines customer first and last names.

```DAX
Customer Full Name =
Customer_Dim[FirstName] & " " & Customer_Dim[LastName]
```

---

## Measure Table

A dedicated MeasureTable was created to organize all DAX measures and improve model readability.

---

## Measures Created

### Sales Metrics

* Total Sales
* Total Cost
* Total Profit
* Return Rate
* Average Sale Per Transaction

### Statistical Measures

* Revenue Sum
* Revenue Average
* Revenue Maximum
* Transaction Count
* Unique Customers

### Iterator Functions

* SUMX
* AVERAGEX

---

## Quick Measures

The following quick measures were implemented:

* Year-over-Year Sales Growth
* Difference Between Current and Previous Month Sales

---

## Filter Context Analysis

The project demonstrates filter behavior using:

### ALL()

Removes filters and returns overall results.

### FILTER()

Applies custom filtering conditions.

### CALCULATE()

Modifies filter context for calculations.

These measures were compared using Matrix visuals.

---

## DAX Functions Used

### Mathematical Functions

* SUM()
* AVERAGE()
* MAX()

### Counting Functions

* COUNTX()
* DISTINCTCOUNT()

### Logical Functions

* IF()
* SWITCH()
* AND()
* OR()

### Text Functions

* CONCATENATE()
* UPPER()
* LEFT()

### Date Functions

* YEAR()
* MONTH()
* EOMONTH()

### Relationship Function

* RELATED()

---

## Time Intelligence Functions

The following time intelligence calculations were implemented:

### TOTALYTD()

Used to calculate Year-To-Date sales.

### SAMEPERIODLASTYEAR()

Used for year-over-year comparison.

### DATESINPERIOD()

Used for rolling period analysis.

### DATESBETWEEN()

Used to create running total calculations.

---

## Sales Categorization

Sales transactions were categorized using SWITCH():

* Low
* Medium
* High

This enables easier business analysis of revenue segments.

---

## Matrix-Based Verification

As required by the project instructions, all outputs were displayed using Matrix visuals only.

### Matrix Reports

#### Sales by Region

Displayed:

* Total Sales
* Total Profit
* Return Rate

#### Sales by Month

Displayed:

* Sales YTD
* Sales Last Year
* Running Total

#### Sales by Product Category

Displayed:

* Total Sales
* Average Sale Per Transaction

#### Sales by Customer Segment

Displayed:

* Total Sales
* Total Profit

---

## Challenges Faced

### 1. Understanding Measures vs Columns

Initially it was difficult to understand the difference between calculated columns and measures.

**Solution:**

* Used calculated columns for row-level calculations.
* Used measures for aggregated calculations displayed in visuals.

### 2. Time Intelligence Errors

Some time intelligence functions required a proper Date table and active relationships.

**Solution:**

* Verified Date table structure.
* Ensured correct relationship configuration.

### 3. Filter Context Confusion

Results changed unexpectedly when slicers and filters were applied.

**Solution:**

* Practiced using ALL(), FILTER(), and CALCULATE() to understand filter propagation.

### 4. Measure Organization

Managing multiple measures became difficult.

**Solution:**

* Created a dedicated MeasureTable to store all measures in one location.

---

## Project Outcome

Successfully implemented a complete DAX-based Power BI solution including:

* Calculated Columns
* Measures
* Quick Measures
* Filter Context Analysis
* Time Intelligence
* Iterator Functions
* Relationship-Based Calculations
* Matrix-Based Reporting

The project demonstrates practical understanding of DAX and analytical modeling techniques in Power BI.

---

## Tools Used

* Microsoft Power BI Desktop
* DAX (Data Analysis Expressions)
* Microsoft Excel

---
