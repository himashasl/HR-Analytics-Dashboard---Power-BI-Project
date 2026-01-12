
# HR Analytics Dashboard – Strategic Workforce Insights

## 📋 Project Overview

This Power BI project provides a comprehensive analysis of a workforce comprising **1,470 employees**. Unlike standard HR reports, this dashboard focuses on **Workforce Planning**, specifically identifying employees **Due for Promotion** and those at risk of **Retrenchment**. It serves as a strategic tool for HR managers to make data-driven decisions regarding talent development and organizational restructuring.

### 🎯 Key Business Questions Addressed:

* **Workforce Composition:** What is the gender distribution and total headcount? (Current: **60% Male, 40% Female**) .
* **Promotion Pipeline:** How many employees are eligible for promotion (**4.9% of the workforce**)?
* **Risk Assessment:** Which employees are identified for retrenchment (**7.96%**) and in which departments?
* **Employee Stability:** How do factors like **Service Years**, **Job Satisfaction**, and **Distance from Office** impact the workforce?

---

## 🔧 Tools & Technologies Used

* **Power BI Desktop:** Dashboard design and interactive reporting.
* **Power Query:** Data cleaning and transformation.
* **DAX:** For custom KPIs such as **Promotion Due %** and **Retrenchment Rates**.
* **Navigation UI:** Custom side-menu navigation for **Home, Action, and Detail** views.
---

## 🛠️ Project Workflow

### 1. Data Cleaning & Transformation

* Processed employee records to categorize **Job Levels** and **Job Satisfaction** scores.
* Created logical flags to determine "Due for Promotion" based on years since last promotion and performance.
* Handled categorical data for **OverTime** and **Department**-wise analysis.



### 2. Interactive Navigation & UI

* **Home Page:** High-level summary of headcount, gender split, and tenure.
* **Action Page:** Focuses on decision-making metrics—who needs to be promoted or retired.
* **Detail Page:** Granular table views showing individual employee names (e.g., Walton S Keim, Taylor Thill) and their specific status.

### 3. DAX Measures Used

* **Total Employees:** Total Emp = COUNTROWS('HR Analytics Data') .
* **On Service:** `% On service = DIVIDE([On Service],[Total Emp],0)`.
* **Due for Promotion:** `Due for promotion = CALCULATE([Total Emp],'HR Analytics Data'[Promotion Status]="due for promotion")`.
* **Will be retreanche:** `IF(ISBLANK(CALCULATE([Total Emp],'HR Analytics Data'[Retreanchment Status]="Will be retreanched")),0,CALCULATE([Total Emp],'HR Analytics Data'[Retreanchment Status]="Will be retreanched"))`.

---

## 📊 Dashboard Insights

* **Service Year Trends:** A significant portion of the workforce has high tenure, as seen in the **Service Year** bar chart.


* **Departmental Impact:** The **Manager** role has the highest number of employees **Due for Promotion (22)** and **Retrenchment (44)**, indicating a high-turnover leadership tier.


* **Work-Life Balance:** **28.3%** of employees are working **OverTime**, which may correlate with satisfaction levels.


* **Job Satisfaction:** The dashboard tracks satisfaction across "High," "Medium," and "Low" categories to monitor morale.



---

## 🚀 How to Use

1. **Navigate:** Use the sidebar to toggle between the **Summary (Home)**, **Actionable Insights**, and **Employee Details**.


2. **Filter:** Click on the **Department** or **Job Level** charts to cross-filter the promotion and retrenchment lists.


3. **Analyze:** Review the **Distance from Office** donut chart to see if commuting distance impacts employee retention.



