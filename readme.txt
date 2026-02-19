POWER BI STUDENT PERFORMANCE DASHBOARD
======================================

Project Overview
----------------
This dashboard analyzes student academic performance, attendance, and behavior 
using Power BI. The dataset includes Students, Scores, Attendance, and Behavior tables.

Tables Used
-----------
1. Students
2. Scores
3. Attendance
4. Behavior

Data Modeling
-------------
Relationships Created:
- Students[StudentID] -> Scores[StudentID] (One to Many)
- Students[StudentID] -> Attendance[StudentID] (One to Many)
- Students[StudentID] -> Behavior[StudentID] (One to Many)

Students table is used as the Dimension table.

Key Measures (DAX)
------------------

1. Percentage Score:
   % Score = DIVIDE(SUM(Scores[Score]), SUM(Scores[MaxScore]))

2. Average Score:
   Average Score = AVERAGE(Scores[Score])

3. Attendance Percentage:
   Attendance % =
   DIVIDE(
       CALCULATE(COUNT(Attendance[Status]), Attendance[Status] = "Present"),
       COUNT(Attendance[Status])
   )

4. Behavior Count:
   Behavior Count = COUNT(Behavior[BehaviorType])

5. Total Students:
   Total Students = DISTINCTCOUNT(Students[StudentID])

Visualizations Used
-------------------
- KPI Cards (Total Students, Average Score, Attendance %)
- Bar Chart (Subject vs Average Score)
- Line Chart (Performance Trend by Term)
- Donut Chart (Behavior Distribution)
- Table (Student Details with Conditional Formatting)
- Slicers (Class, Section, Subject, Term)

Dashboard Features
------------------
- Interactive filtering using slicers
- Drillthrough page for Student Profile
- Conditional formatting for performance highlighting
- Clean and professional layout

Steps to Build
--------------
1. Load data into Power BI.
2. Check and correct data types in Power Query.
3. Create relationships in Model view.
4. Create required DAX measures.
5. Design visuals and format dashboard.
6. Add slicers and drillthrough functionality.
7. Apply theme and finalize layout.

Prepared For: Exam Submission
Tool Used: Microsoft Power BI
"""