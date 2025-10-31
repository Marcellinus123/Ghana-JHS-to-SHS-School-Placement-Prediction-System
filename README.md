# Ghana JHS School Placement Prediction System  
### Built with PHP, MySQLi & Basic PHP-ML

A predictive academic placement system developed for **Junior High Schools (JHS) in Ghana**, designed to analyze student academic performance and estimate their most likely **Senior High School (SHS)** placement and programme allocation.  

The goal of this system is to assist schools, guidance counsellors, parents, and students with an **early insight into SHS placement outcomes**, using student performance data from **JHS1 to JHS3** plus **at least one mock examination**.

This solution is particularly aligned with the Ghana Education Service (GES) concept of the CSSPS style of selection, but in a **local, simplified, in-house prediction model**, built using **PHP-ML** and standard **PHP & MySQLi backend**.

---

## System Overview

Ghanaian JHS students have multiple academic records across three years, culminating in the BECE exam and national placement system.  
However, before official placement results are released, schools and parents often lack accurate, data-driven expectations.

This system fills that gap by:

- Collecting historical academic records of JHS students  
- Analyzing their academic performance curve  
- Applying basic ML classification and prediction  
- Providing insight into likely **SHS school category assignment** (A / B / C / D)  
- Suggesting likely **SHS programme** the student may qualify for  
- Helping stakeholders identify best-fit options and expectations early

It does **not replace official GES placement** but aids **prediction, counseling, planning, and student mentoring**.

---

## Key Features

### JHS Administrator Portal
- Secure login & account creation for schools/JHS admins  
- Student management dashboard  
- Upload student academic scores:  
  - JHS1 Term 1–3  
  - JHS2 Term 1–3  
  - JHS3 Term 1–2 + Mock score  
- Manual input or bulk upload (CSV/Excel)  
- Edit/update student records  
- View placement prediction reports  

### ML-Powered Placement Insight
- Predicts likely SHS category student could fall into  
- Suggests possible SHS programme such as:  
  - Science  
  - General Arts  
  - Business  
  - Technical Skills  
  - Home Economics  
  - Visual Arts  
- Flags students at risk academically  
- Performance trend analysis over 3 academic years  

###  Student Results Summary Dashboard
- Graph-based performance visualization  
- Average academic score computation  
- Weighted calculation for final year & mock results  
- Academic growth or decline score  
- ML score confidence indicator  

###  Admin Controls
- School user authentication  
- Manage school student dataset  
- Download PDF/Excel prediction reports  
- Generate advisory sheets for parents  
- Secure DB with multiple access checks  

---

## Machine Learning Logic (PHP-ML)

While lightweight, the ML logic applies:

- Basic classification models  
- Linear scoring & normalization of academic history  
- Weighted average processing  
- Pattern trend analysis (improvement vs decline)  
- Predictive approximation based on performance categories  

The engine uses **PHP-ML** library techniques and custom rules reflecting typical CSSPS-style evaluation logic.

### ML Input Data Considered

| Category | Description |
|---|---|
JHS1 Scores | Term 1–3 subject performance  
JHS2 Scores | Term 1–3 subject performance  
JHS3 Scores | Term 1–2 academic scores  
Mock Exam | Major weight factor  
Trend Factor | Consistency & improvement  
Subject Strength | Sciences, Business, Arts, etc.  

### Output Prediction

- **Likely SHS category** (A/B/C/D)
- **Likely programme** recommendation
- **Confidence level** indicator
- **Guidance remarks**

---

## Use Case & Value

###  For Schools
- Early student counselling  
- Improve SHS selection form accuracy  
- Identify strong & weak academic areas  
- Guide students with realistic expectations  

###  For Parents
- Understand child's placement potential  
- Early planning for school selection and fees  

###  For Teachers
- Track class performance trends  
- Provide targeted academic support  

### For Ghana Education Context
- Supplementary school-based CSSPS-like advisory  
- Encourages data-driven guidance culture  

---

## System Architecture

| Layer | Technology |
|------|-----------|
Frontend | HTML + CSS + JS |
Backend | PHP (XAMPP/LAMP environment) |
Database | MySQLi |
ML Engine | PHP-ML + custom calculation rules |
Export Tools | CSV / PDF reporting |
File Upload | CSV / Excel student records |

---

## Workflow

1. JHS Admin creates school account  
2. Admin enters/uploads student records (JHS1–JHS3 + Mock)  
3. System processes academic data  
4. ML model classifies based on patterns + historical weights  
5. Results displayed:  
   - Category prediction  
   - Programme recommendation  
   - Remarks + confidence score  
6. Admin downloads reports  
7. Expected placement guidance issued to students/parents  

---

## Folder Structure (Typical Example)
/school_placement_system
├── index.php
├── login.php
├── upload_records.php
├── students.php
├── predict.php
├── ml/
│ ├── train.php
│ ├── model.php
│ └── php-ml config files
├── db/
│ └── database.sql
├── css/
├── js/
├── reports/
├── pdf/
└── README.md


---

## Future Features

- AI-powered placement score visualization  
- BECE raw score upload support  
- API to integrate with SHS database for validation  
- Parental dashboard login  
- SMS notification module  
- Machine-learning model upgrade (Python micro-service)  

---

## Summary

This project brings **predictive analytics into Ghana JHS education** using accessible technologies.  
It empowers schools to guide students more effectively by analyzing academic history and making informed placement predictions — before official results are released.

The platform blends **education**, **data analysis**, and **ML logic** to support informed decisions in Ghana's school placement ecosystem.

> A smart educational advisory and placement prediction tool for Ghana JHS institutions — driven by PHP, MySQLi, and PHP-ML.

