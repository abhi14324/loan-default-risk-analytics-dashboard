# Loan Default Risk Analytics Dashboard

A multi-page financial analytics dashboard built using Power BI to analyze loan default behavior, applicant demographics, credit risk indicators, and financial trends.

This project transforms raw loan application data into business insights that help understand default probability, applicant financial profiles, and risk distribution across multiple dimensions.

---

## Project Objective

The objective of this project is to analyze loan applicant data and identify financial patterns that influence loan defaults.

The dashboard helps answer key business questions such as:

* How much total loan amount has been issued?
* What percentage of applicants are defaulting?
* Which employment groups have higher default risk?
* Which age groups receive larger loan values?
* How credit score categories affect lending patterns?
* How education and marital status influence loan distribution?

---

## Tools Used

* Power BI
* DAX Measures
* Power Query
* CSV Dataset
* Data Modeling
* Power BI Service

---

## Dataset Overview

The dataset contains applicant-level financial information including:

* Loan Amount
* Credit Score
* Default Status
* Employment Type
* Marital Status
* Age Group
* Education Level
* Income Bucket
* Loan Purpose
* Mortgage Status
* Dependents
* Application Year

The data was cleaned and transformed inside Power BI before visualization.

---

## Dashboard Structure

This project contains **3 analytical pages**.

---

# Page 1: Loan Default & Overview

This page provides executive-level KPI monitoring and loan risk overview.

## KPI Cards

* **Total Loan Amount:** 33bn
* **Default Rate:** 12%
* **Average Credit Score:** 574.26
* **Total Applications:** 255K

## Visuals Included

### Loan Amount by Purpose

Loan distribution across:

* Home
* Business
* Education
* Auto
* Other

### Average Income by Employment Type

Comparison across:

* Full-time
* Self-employed
* Part-time
* Unemployed

### Default Rate (%) by Employment Type

Employment-based default risk analysis.

### Average Loan Amount by Age Group

Age categories:

* Adult
* Middle Age Adults
* Senior Citizens
* Teen

### Default Rate (%) by Year

Year-wise default trend analysis.

---

# Page 2: Applicant Demographics & Financial Profile

This page focuses on applicant segmentation and financial behavior.

## Visuals Included

### Median Loan Amount by Credit Score Category

Credit score bins:

* Low
* Medium
* Very Low
* High

### Average Loan Amount by Age Group and Marital Status

Donut-based demographic analysis.

### Total Loan by Credit Score Bins

Adult applicant loan concentration by score category.

### Loan by Mortgage / Dependents

Middle-age applicant dependency analysis.

### Number of Loan by Education Type

Education categories:

* Bachelor's
* High School
* Master's
* PhD

---

# Page 3: Finance Risk Metrics

This page focuses on advanced financial movement and yearly loan trends.

## Visuals Included

### YOY Loan Amount Change by Year

Year-over-year loan movement.

### Risk Trend Comparison by Year

Financial trend fluctuations across years.

### YTD Loan Amount by Credit Score and Marital Status

Sankey flow analysis.

### Income Bucket vs Employment Type

Relationship between income and employment categories.

---

## DAX Measures Used

### Total Loan Amount

```DAX
Total Loan Amount = SUM(Loan[LoanAmount])
```

### Default Rate

```DAX
Default Rate =
DIVIDE(
    CALCULATE(COUNTROWS(Loan), Loan[Default] = TRUE()),
    COUNTROWS(Loan)
) * 100
```

### Average Credit Score

```DAX
Average Credit Score = AVERAGE(Loan[CreditScore])
```

### Total Applications

```DAX
Total Applications = COUNTROWS(Loan)
```

---

## Key Business Insights

* Home loans contribute the highest loan volume
* Unemployed applicants show higher default tendency
* Adults receive the highest average loan amount
* Default rate peaks around 2015–2016
* Low and medium credit score groups dominate loan distribution

---

## Power BI Service

This dashboard has also been published to **Power BI Service** for cloud-based reporting and online dashboard sharing.

---

## Repository Structure

```text
loan-default-risk-analytics-dashboard/
│
├── dataset/
│   └── Loan_default_dataset.csv
│
├── dax_measures/
│   └── measures.txt
│
├── screenshots/
│   ├── loan_default_overview.png
│   ├── applicant_demographics.png
│   └── finance_risk_metrics.png
│
├── documentation/
│   └── Loan_Project_Documentation.docx
│
├── Loan_Project.pbix
│
└── README.md
```

---

## Future Improvements

* Add SQL integration
* Add Python-based default prediction
* Add forecasting visuals
* Add borrower segmentation model
* Add drill-through applicant profile page

---

## Author

Abhi
