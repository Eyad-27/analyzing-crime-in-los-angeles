# Analyzing Crime in Los Angeles 🚨

Explore crime patterns in Los Angeles using historical crime data to help the LAPD allocate resources effectively.  
This project leverages pandas and visualization to answer questions about peak crime hours, high-risk areas at night, and crime frequency by age group.

---

## ❓ Guiding Questions
1. Which hour has the **highest frequency of crimes**?  
   - Stored as `peak_crime_hour`.  

2. Which **area has the largest frequency of night crimes** (10pm–3:59am)?  
   - Stored as `peak_night_crime_location`.  

3. How many crimes were committed against victims of different **age groups**?  
   - Stored as a pandas Series `victim_ages` with age group labels: `"0-17"`, `"18-25"`, `"26-34"`, `"35-44"`, `"45-54"`, `"55-64"`, `"65+"`.  

---

## 📊 The Data

### **crimes.csv**
| Column             | Description |
|-------------------|-------------|
| `DR_NO`           | Division of Records Number (2-digit year, area ID, 5 digits). |
| `Date Rptd`       | Date reported (MM/DD/YYYY). |
| `DATE OCC`        | Date of occurrence (MM/DD/YYYY). |
| `TIME OCC`        | Time of occurrence in 24-hour military format. |
| `AREA NAME`       | Name of the patrol area or division responsible for the location. |
| `Crm Cd Desc`     | Description of the crime committed. |
| `Vict Age`        | Age of the victim in years. |
| `Vict Sex`        | Sex of the victim (`F`, `M`, `X`). |
| `Vict Descent`    | Victim’s descent (A–Z codes, e.g., `B` = Black, `H` = Hispanic). |
| `Weapon Desc`     | Weapon used in the crime, if applicable. |
| `Status Desc`     | Current status of the crime report. |
| `LOCATION`        | Street address of the crime. |

---

## 🔎 How I Approached the Project  

### 1. Peak crime hour  
Extracted the hour from `TIME OCC`, converted to integer, counted frequencies, and stored the highest as `peak_crime_hour`.  

### 2. Area with most night crimes  
Filtered records for hours 22:00–03:59, grouped by `AREA NAME`, and identified the area with the highest frequency as `peak_night_crime_location`.  

### 3. Crimes by age group  
Created bins and labels for victim ages, added a new column with the age group, and counted crimes per group to create the pandas Series `victim_ages`.  

---

## 📌 Key Deliverables
- Extracted peak crime hours using **pandas** and Boolean filtering.  
- Identified high-risk night crime areas with aggregation.  
- Binned victim ages to compute crime counts per age group.  
- Applied filtering, grouping, and counting to generate actionable insights for LAPD.  

---

## 🛠️ Skills Used
- **Python**: pandas, matplotlib  
- Data wrangling & filtering  
- Grouping, aggregation, and counting  
- Boolean logic & conditional filtering  
- Data visualization for frequency analysis  
