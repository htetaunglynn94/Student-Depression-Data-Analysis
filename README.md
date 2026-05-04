# 📊 Student Depression Data Analysis (Tableau Project)

## Project Overview

This project analyzes **Student Depression Data** to identify key factors influencing mental health among students. The goal is to uncover patterns, correlations, and risk factors contributing to depression using interactive visualizations.

The analysis focuses on understanding how **academic pressure, lifestyle habits, financial stress, and study satisfaction** impact student well-being.

**Tableau Report**: [Student Depression Data Analysis.twb](https://public.tableau.com/shared/YRGK8CCQD?:display_count=n&:origin=viz_share_link)

---

## Objectives

- Enable interactive filtering across multiple dimensions (Gender, Age Group, Diet, Sleep, etc.)
- Analyze depression patterns by:
  - Academic Pressure
  - Study Satisfaction
  - Financial Stress
  - Sleep Duration
  - Dietary Habits
- Compare depression rates across demographic groups
- Identify high-risk student segments
- Provide actionable insights for improving student mental health

---

## Dataset Information

**Raw Data**: [Student Depression Data.xlsx](https://github.com/user-attachments/files/27337330/Student.Depression.Data.xlsx) 

- The dataset contains student-related mental health indicators
- Key attributes include:
  - Age
  - Gender
  - Academic Pressure
  - Study Satisfaction
  - Sleep Duration
  - Dietary Habits
  - Financial Stress
  - Depression Status

---

## Dashboard Structure

### Overview Dashboard

- KPI indicators (Total Students, Depression Rate)
- Interactive filters (Gender, Age Group, Lifestyle factors)
- Bar charts and percentage distributions
- Comparative analysis across categories

---

## Data Processing Steps

### 1️⃣ Data Preparation

- Imported dataset into Microsoft SQL Server for data manipulation purpose
- Verified and cleaned data types
- Created `Age Group` using SQL script:

```SQL
ALTER TABLE [Student Depression Data]
ADD [Age Group] AS
    CASE
        WHEN Age BETWEEN 18 AND 24 THEN 'A1'
        WHEN Age BETWEEN 25 AND 30 THEN 'A2'
        ELSE 'A3'
    END;
```
- Change `Depression` column from **boolean** to **categorical**

```SQL
UPDATE [Student Depression Data]
SET Depression = CASE
    WHEN Depression = '1' THEN 'Yes'
    ELSE 'No'
END
```

- Exported all result as `.xlsx` and imported to Tableau Public
- Created calculated fields where necessary

---

### 2️⃣ Feature Engineering

#### Age Group Segmentation

| Age Range | Group |
|----------|------|
| 18–24    | A1   |
| 25–30    | A2   |
| > 30     | A3   |

---

## Data Visualization & Analysis

### Key Insights

- The analysis reveals several important findings regarding student depression and its contributing factors.
- The overall depression rate is approximately 50 percent, indicating a significant prevalence of mental health challenges among students.
- Academic pressure is identified as the most influential factor affecting depression. As academic pressure increases, depression levels rise significantly, particularly among students with unhealthy lifestyle habits.
- Financial stress is the second most impactful factor, with higher levels of financial burden associated with increased depression rates.
- Dietary habits also play a meaningful role. Students with healthier diets tend to experience lower levels of depression, while those with unhealthy dietary patterns show higher depression rates.
- Sleep duration has a moderate influence on mental health. Students who sleep more than eight hours tend to have lower depression levels, while other sleep groups show relatively similar patterns.
- Gender-based analysis indicates that depression is slightly higher among male students; however, the difference between genders is not substantial.
- A key insight from the analysis is that depression is influenced by multiple factors simultaneously. Students experiencing high academic pressure, high financial stress, and unhealthy lifestyle habits are the most vulnerable to depression.

---

## Conclusion

The findings from this analysis demonstrate that student depression is a complex and multi-dimensional issue. Academic pressure emerges as the most critical factor, followed by financial stress and study dissatisfaction.

While lifestyle factors such as diet and sleep contribute to mental health outcomes, their impact is relatively secondary compared to academic and financial influences.

### Recommendations:
- Reduce excessive academic pressure
- Provide financial support mechanisms
- Improve study engagement and satisfaction
- Encourage healthy lifestyle habits

---

## Tools Used

- Tableau Public (Data Visualization & Dashboarding)
- Microsoft SQL Server (Data Preparation)
- Microsoft Excel (Data Source)

---

## Contact

If you have feedback or opportunities, feel free to connect:

* [LinkedIn](https://www.linkedin.com/in/htet-aung-lynn-64ba06146/)
* [GitHub](https://github.com/htetaunglynn94)

---
