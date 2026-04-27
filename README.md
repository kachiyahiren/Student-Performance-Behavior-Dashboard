# 🎓 Student Performance & Behavior Dashboard (Power BI)

## 🚀 Project Overview
This project is an interactive **Power BI dashboard** designed to analyze student academic performance, attendance, and behavioral patterns.

It helps educators and administrators monitor student progress, identify performance gaps, and take data-driven actions to improve outcomes.

---

## 🎯 Objectives
- Track student academic performance across subjects
- Analyze performance trends over different terms
- Monitor student behavior patterns
- Evaluate attendance and engagement
- Identify high-performing and at-risk students

---

## 📊 Dashboard Structure

### 🟢 Student Dashboard (Performance Overview)

#### 📈 Key Visuals:
- **Average Score by Term** → Tracks performance trend across terms
- **Average Score by Subject** → Compares subject-wise performance
- **Student Performance Table**:
  - Name
  - Subject
  - Total Score
  - % Score
  - Performance Category (High/Medium/Low)

#### 📌 Insights:
- Most students fall under **High performance category**
- Slight **decline in average score across terms**
- Math shows relatively higher average performance

---

### 🟣 Behavior Dashboard

#### 📊 Key Visuals:
- **Behavior Distribution (Donut Chart)**:
  - Disruptive
  - Late
  - Helpful
  - Participative
  - Absent without notice

- **Behavior Count by Class**
- **Detailed Behavior Log Table**

#### 🎛 Filters:
- Subject Filter
- Section Filter (A, B, C)
- Class Filter

#### 📌 Insights:
- Behavior distribution is relatively balanced
- “Absent without notice” is a significant concern
- Some classes show higher behavioral issues than others

---

### 🔵 Student Profile Dashboard

#### 📊 Key Metrics:
- 📅 **Attendance Rate:** 90.05%

#### 📋 Key Visuals:
- Student Information Table (Class, Section, Gender)
- Detailed Behavior History with Notes

#### 📌 Insights:
- Attendance is generally strong (>90%)
- Behavioral records provide qualitative insights for each student
- Enables individual-level tracking

---

## 🛠️ Tools & Technologies
- **Power BI Desktop**
- Power Query (Data Cleaning)
- DAX (Data Analysis Expressions)
- Data Modeling

---

## ⚙️ Data Model
- Fact Table: Student Records
- Dimension Tables:
  - Students
  - Subjects
  - Behavior
  - Date


## SHREENSHORT
MAIN DASHBOARD:https://github.com/kachiyahiren/Student-Performance-Behavior-Dashboard/blob/main/Main%20Dashboard.png

BEHAVIOR DASHBOARD:https://github.com/kachiyahiren/Student-Performance-Behavior-Dashboard/blob/main/Behavior%20Dashboard.png

STUDENT PROFILE DASHBOARD:
---

## 🧮 Key DAX Measures

```DAX
Average Score = AVERAGE(Scores[Score])

% Score = 
DIVIDE(
    SUM(Scores[Score]),
    SUM(Scores[MaxScore])
)

Performance Category =
SWITCH(
    TRUE(),
    [% Score] >= 90, "High",
    [% Score] >= 60, "Medium",
    "Low"
)

Attendance % =
DIVIDE(
    SUM(Attendance[PresentDays]),
    SUM(Attendance[TotalDays])
)# Student-Performance-Behavior-Dashboard
