# UCL Research Fellow Technical Test – Hypertension Data Analysis

This repository contains a Python-based data cleaning and exploratory analysis pipeline for synthetic primary care data generated using [Synthea](https://synthetichealth.github.io/synthea/). The project was completed as part of the UCL Research Fellow technical assessment (Ref: B02 08645).

## 📁 Contents

- `Sabrina Research fellow project.ipynb` – Main notebook with code and outputs
- `test_data_2.zip` – Cleaned and compressed dataset for reproducibility
- `docs/` – Includes data dictionary and term definitions
- `data/dest/` – Raw input files: conditions, observations, patients, medications (compressed)

## 🎯 Objective

To simulate and evaluate typical electronic health record (EHR) workflows using synthetic patient data, with a focus on cleaning, descriptive statistics, and epidemiological estimates related to hypertension.

---

## 📌 Tasks Overview

### 1. **Data Cleaning**
- Loaded and validated 5 core datasets: `patients`, `conditions`, `observations`, `encounters`, `medications`.
- Implemented rigorous exclusion criteria to filter records with:
  - Implausible birth/death dates
  - Negative ages
  - Invalid gender values
- Cleaned and relinked `conditions`, `observations`, and `medications` to valid patient IDs.

### 2. **Descriptive Statistics**
- Summarised:
  - Total number of unique patients
  - Most frequent SNOMED conditions
  - Top LOINC observations and RxNorm medications
- Visualised top concepts using bar plots.

### 3. **Hypertension Subgroup Analysis**
- Identified hypertensive patients using SNOMED concept `59621000`.
- Examined distributions of:
  - Systolic and diastolic blood pressure (SBP, DBP)
  - Body Mass Index (BMI)
- Produced stratified boxplots by hypertension and sex.

### 4. **Prevalence Estimation**
- Calculated crude hypertension prevalence: `25.2%` (95% CI: 22.7–27.8%)
- Performed direct age standardisation using 2020 UK population weights:
  - Adjusted prevalence: `25.1%`
  - Sex-adjusted prevalence: Female `24.0%`, Male `26.3%`
- Compared results with national estimates (~30%) and discussed underdiagnosis.

---

## 📊 Key Findings

- Over 85% of hypertensive patients were overweight or obese.
- Mean SBP and BMI were notably higher in hypertensive individuals.
- Age and obesity were the strongest predictors of hypertension.
- Sex differences were modest after adjusting for age and BMI.

---

## 🛠 Tools & Libraries

- Python 3.10
- pandas, numpy, matplotlib, seaborn
- Jupyter Notebook

---

## 🧪 How to Reproduce

1. Clone this repo:
   ```bash
   git clone https://github.com/sabrinaansarey25/Research-Fellow---B02-08645---Technical-Test.git
   cd Research-Fellow---B02-08645---Technical-Test
