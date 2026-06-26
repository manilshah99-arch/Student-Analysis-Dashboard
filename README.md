# Student Performance Dashboard – Academic & Behavioral Insights

## Project Overview

This project is an interactive Power BI Dashboard that analyzes student academic performance, attendance patterns, and behavioral insights.

The dashboard helps understand student progress across different classes, subjects, sections, and terms using data visualization, DAX calculations, and interactive reporting features.

---

## Objective

Build an interactive Power BI report that provides insights into:

- Student academic performance
- Subject-wise score analysis
- Attendance trends
- Behavioral patterns
- Student-level performance details

This project demonstrates skills in:

- Data Cleaning
- Data Modeling
- DAX Measures
- Data Visualization
- Dashboard Design
- Storytelling with Data

---

## Dataset Used

The project uses four CSV files:

### 1. Students.csv

Contains student information:

- StudentID
- Name
- Gender
- Class
- Section


### 2. Scores.csv

Contains academic records:

- StudentID
- Subject
- ExamType
- Score
- MaxScore
- Term


### 3. Attendance.csv

Contains attendance details:

- StudentID
- Date
- Status
- Reason


### 4. Behavior.csv

Contains student behavior records:

- StudentID
- Date
- BehaviorType
- Notes

---

# Data Model

A star-schema style relationship model was created.

Relationships:

Students → Scores

Students → Attendance

Students → Behavior


Relationship type:

One-to-Many

---

# Data Cleaning

Performed cleaning steps:

- Corrected column data types
- Removed duplicate records
- Trimmed text values
- Handled missing values
- Created attendance flag column


Attendance Flag Logic:

Present = 1

Absent = 0

---

# DAX Measures Created

## Total Students

Counts unique students.

```DAX
Total Students =
DISTINCTCOUNT(Students[StudentID])
