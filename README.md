# 👔 HR Analytics Dashboard — Power BI & Excel

![POWERBI](https://img.shields.io/badge/PowerBI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black) ![EXCEL](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white) ![HR Analytics](https://img.shields.io/badge/HR-Analytics-blue?style=for-the-badge)
> An end-to-end HR analytics project analyzing employee attrition patterns using Power BI, Excel, and DAX measures with custom visualizations.

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Business Problem](#-business-problem)
- [Dataset](#-dataset)
- [Tools & Technologies](#%EF%B8%8F-tools--technologies)
- [Project Structure](#%EF%B8%8F-project-structure)
- [Data Cleaning & Preparation](#-data-cleaning--preparation)
- [Exploratory Data Analysis (EDA)](#-exploratory-data-analysis-eda)
- [Research Questions & Key Insights](#-research-questions--key-insights)
- [Dashboard](#-dashboard)
- [How to Run This Project](#-how-to-run-this-project)
- [Final Recommendations](#-final-recommendations)
- [Dashboard Screenshots](#-dashboard-screenshots)
- [Author & Contact](#-author--contact)

---

## 📖 Overview

This project analyzes **HR Analytics** data covering 1,470 employees to understand attrition patterns, demographics, salary distribution, and employee tenure. The goal is to help HR managers and business leaders make data-driven decisions to improve employee retention and workforce planning.

The dashboard was built in **Power BI Desktop** with custom **DAX measures**, covering:
- Employee attrition trends by demographics
- Salary slab and education level analysis
- Job role and department-wise attrition
- Years at company and age group patterns
- Gender-based attrition insights

---

## 💼 Business Problem

HR departments struggle with understanding why employees leave and which factors contribute most to attrition. This project addresses the following business challenges:

- **No centralized attrition tracking** — HR lacks a single dashboard to monitor overall attrition rate and key metrics
- **Lack of demographic insights** — It's unclear which age groups, genders, or education levels have higher attrition
- **No salary-attrition correlation** — The relationship between compensation and employee turnover is not analyzed
- **Department-specific blindspots** — Certain departments may have higher attrition but go unnoticed
- **Difficulty tracking tenure patterns** — No visibility into whether employees leave early or after long tenures
- **Decision-making gaps** — HR cannot proactively identify at-risk employee groups or implement targeted retention strategies

---

## 📁 Dataset

- **Source:** HR Employee Data (Sample Dataset)
- **File:** `HR_Analytics-1.csv`
- **Rows:** 1,470 employee records
- **Attrition:** 237 employees left (16.1% attrition rate)

### Key Columns:

| Column | Description |
|--------|-------------|
| `EmpID` | Unique employee identifier |
| `Age` | Employee age |
| `AgeGroup` | Age grouped into ranges (18-25, 26-35, etc.) |
| `Attrition` | Whether employee left (Yes/No) |
| `Department` | Department (Research & Development, Sales, HR) |
| `DistanceFromHome` | Distance from home in km |
| `Education` | Education level (1-5 scale) |
| `EducationField` | Field of education |
| `Gender` | Male/Female |
| `JobRole` | Specific job role |
| `JobSatisfaction` | Job satisfaction level (1-4) |
| `MaritalStatus` | Single/Married/Divorced |
| `MonthlyIncome` | Monthly salary |
| `SalarySlab` | Salary grouped (Upto 5k, 5k-10k, etc.) |
| `YearsAtCompany` | Total years at company |
| `YearsInCurrentRole` | Years in current role |
| `OverTime` | Whether works overtime (Yes/No) |

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|----------|
| **Power BI Desktop** | Dashboard building & interactive visualizations |
| **Microsoft Excel** | Data cleaning, preprocessing & exploration |
| **DAX** | Custom KPI calculations and measures |
| **GitHub** | Version control & project documentation |

---

## 🗂️ Project Structure

```
hr-analytics-dashboard-powerbi-excel/
│
├── 📁 assets/              ← Dashboard screenshots
├── 📁 dashboard/           ← Power BI .pbix file
├── 📁 data/                ← Raw CSV dataset
└── README.md
```

---

## 🧹 Data Cleaning & Preparation

Before building the dashboard, the raw dataset was cleaned and structured in **Microsoft Excel**:

✅ Removed duplicate employee records  
✅ Handled missing values in `JobSatisfaction` and `EnvironmentSatisfaction`  
✅ Created **AgeGroup** column by binning ages (18-25, 26-35, 36-45, 46-55, 55+)  
✅ Created **SalarySlab** column to categorize monthly income (Upto 5k, 5k-10k, 10k-15k, 15k+)  
✅ Standardized `EducationField` values (Life Sciences, Medical, Marketing, etc.)  
✅ Converted `Attrition` and `OverTime` to binary Yes/No for easy filtering  
✅ Validated `YearsAtCompany` against `YearsInCurrentRole` for data consistency  

---

## 🔍 Exploratory Data Analysis (EDA)

### Employee Demographics
- **Total Employees:** 1,470
- **Total Attrition:** 237 employees
- **Attrition Rate:** 16.1%
- **Average Age:** 37 years
- **Average Salary:** ₹6,500/month
- **Average Tenure:** 7.0 years at company

### Attrition by Gender
- **Male Attrition:** 140 employees (59%)
- **Female Attrition:** 79 employees (33%)
- Men show slightly higher attrition rates, possibly due to higher representation in certain high-turnover roles

### Attrition by Education Level
- **Life Sciences:** 38% of attrition
- **Medical:** 27% of attrition
- **Marketing:** 15% of attrition
- **Technical Degree:** 14% of attrition
- **Other:** 6%

Life Sciences and Medical backgrounds dominate attrition, suggesting these roles may face higher market competition or dissatisfaction.

### Attrition by Age Group
- **26-35 years:** Highest attrition count (116 employees)
- **18-25 years:** 44 employees
- **36-45 years:** 43 employees
- **46-55 years:** 26 employees
- **55+ years:** 8 employees

Mid-career professionals (26-35) are most likely to leave, often seeking better opportunities or career growth.

### Attrition by Salary Slab
- **Upto 5k:** 163 employees (highest attrition)
- **5k-10k:** 49 employees
- **10k-15k:** 20 employees
- **15k+:** 5 employees

Lower salary ranges correlate strongly with attrition, indicating compensation is a major factor.

### Attrition by Years at Company
- **Peak attrition at 0-5 years:** Most employees leave within the first few years
- Gradual decline after 10+ years, showing long-tenured employees are more loyal

### Attrition by Job Role
- **Laboratory Technician:** 62 employees (highest)
- **Sales Executive:** 57 employees
- **Research Scientist:** 47 employees
- **Sales Representative:** 33 employees

These roles show high turnover, possibly due to job stress, limited growth, or market demand.

---

## 💡 Research Questions & Key Insights

### 1. What is the overall attrition rate?
**Finding:** The attrition rate is **16.1%** (237 out of 1,470 employees), which is above the industry average of 10-15%. This indicates retention challenges.

### 2. Which age group has the highest attrition?
**Finding:** Employees aged **26-35** have the highest attrition (116 employees), representing nearly half of all attrition. This group is typically seeking career advancement and better opportunities.

### 3. Does salary impact attrition?
**Finding:** **Yes.** Employees earning **Upto ₹5k/month** show the highest attrition (163 employees). Salary dissatisfaction is a critical driver of turnover.

### 4. Which departments face the most attrition?
**Finding:** **Research & Development** has the highest attrition count, followed by Sales. Both departments require targeted retention programs.

### 5. Do employees with more years at the company stay longer?
**Finding:** **Yes.** Attrition peaks in the first 5 years and drops significantly after 10 years. Early retention programs are crucial.

### 6. Is there a gender difference in attrition?
**Finding:** **Males** show higher attrition (140) compared to females (79). This could be due to role distribution or workplace factors.

### 7. Which job roles have the highest turnover?
**Finding:** **Laboratory Technicians, Sales Executives, and Research Scientists** have the most attrition, suggesting these roles face higher stress or limited growth opportunities.

---

## 📊 Dashboard

The Power BI dashboard provides **interactive visualizations** across key HR metrics:

### Key Metrics (KPI Cards)
- Count of Employees: **1,470**
- Attrition: **237**
- Attrition Rate: **16.1%**
- Average Age: **37**
- Average Salary: **₹6.5k**
- Average Years at Company: **7.0**

### Visualizations

| Visualization | Description |
|---------------|-------------|
| **Attrition by Gender** | Donut chart showing male vs female attrition |
| **Attrition by Education** | Donut chart breaking down by education field |
| **Attrition by Age** | Bar chart showing attrition across age groups |
| **Attrition by Salary Slab** | Horizontal bar chart of salary-based attrition |
| **Attrition by Years at Company** | Line chart showing tenure-based trends |
| **Attrition by Job Role** | Horizontal bar chart of role-wise attrition |
| **Job Role Table** | Detailed table with attrition counts by job role |

---

## 🚀 How to Run This Project

### Prerequisites
- [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)
- Microsoft Excel or any CSV viewer
- Git (optional, for cloning)

### Steps

**1. Clone the repository:**
```bash
git clone https://github.com/AkarshKumarM05/hr-analytics-dashboard-powerbi-excel.git
```

**2. Navigate to the project folder:**
```bash
cd hr-analytics-dashboard-powerbi-excel
```

**3. Open the dataset:**
- Locate `data/HR_Analytics-1.csv`
- Open in Excel to preview or verify data structure

**4. Open the Power BI Dashboard:**
- Open `dashboard/HR_Analytics_Dashboard.pbix` in **Power BI Desktop**
- If prompted, update the data source path to point to `data/HR_Analytics-1.csv` on your local machine

**5. Refresh the data:**
- Go to **Home → Refresh** in Power BI Desktop to load the latest data

**6. Explore the dashboard:**
- Use slicers to filter by department, gender, education, or salary slab
- Hover over visuals for detailed tooltips and insights

---

## ✅ Final Recommendations

Based on the HR analytics findings:

1. **Address salary concerns immediately** — The highest attrition occurs in the Upto 5k salary range. Consider salary reviews and market benchmarking.

2. **Implement early retention programs** — Most employees leave within 0-5 years. Focus on onboarding, mentorship, and career path clarity in the first few years.

3. **Target the 26-35 age group** — This group shows the highest attrition. Offer career development opportunities, leadership training, and clear growth paths.

4. **Review high-attrition roles** — Laboratory Technicians, Sales Executives, and Research Scientists need role-specific retention strategies (better comp, work-life balance, growth opportunities).

5. **Improve departmental engagement** — Research & Development and Sales departments should be prioritized for employee satisfaction surveys and retention initiatives.

6. **Analyze gender-specific factors** — With higher male attrition, explore if certain roles or workplace factors disproportionately affect men.

7. **Invest in Life Sciences & Medical talent** — These education backgrounds show high attrition. Partner with universities and offer competitive packages to retain this talent pool.

---

## 📸 Dashboard Screenshots

**Full Dashboard View**

![Dashboard View**](assets/Screenshot%202026-03-26%20232944.png)
---

## 👨‍💻 Author & Contact

**Akarsh Kumar Pandey**  
B.Com (Hons) | Data Analytics Enthusiast

[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:tulnama02@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/akarshkpandey)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AkarshKumarM05)
---

> ⭐ If you found this project useful, please give it a star — it helps a lot!
