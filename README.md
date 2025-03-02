# 🏎️ Formula 1 Database Analysis  

## 📌 Project Overview  
This project focuses on analyzing **Formula 1 race data** using SQL and relational database modeling. It involves **data modeling, ER diagram creation, data cleansing**, and **SQL-based analysis** to uncover insights about **drivers, teams, circuits, and race results** from **1950 to 2024**.  

## 📊 Dataset  
The dataset is sourced from:  
- **[Ergast API](http://ergast.com/mrd/) (Historical F1 data)**  
- **[Kaggle Formula 1 Dataset](https://www.kaggle.com/datasets/rohanrao/formula-1-world-championship-1950-2020)**  

It contains multiple tables, including:  
- **Drivers** 🏁 (driver details, nationality, etc.)  
- **Constructors** 🏎️ (team information)  
- **Circuits** 🌍 (track locations)  
- **Races** 🏆 (event details)  
- **Results** 📊 (finishing positions, points, etc.)  
- **Pit stops** ⛽ (timings, efficiency per team)  
- **Status** ⚠️ (race completion, DNFs, etc.)  

## 🏗️ Database Development  

### 1️⃣ **Entity-Relationship (ER) Diagram & Data Modeling**  
- An **ER Diagram** was created to visualize relationships between **Drivers, Races, Teams, and Results**.  
- **Normalization techniques** were used to ensure an efficient, structured schema.  
- **Relational schema** was defined to eliminate redundancy and ensure data integrity.  

### 2️⃣ **Data Cleaning & Transformation**  
- **Handled missing values** (e.g., missing driver numbers were set to NULL).  
- **Standardized column names** (e.g., `number` → `driverNumber` to avoid SQL conflicts).  
- **Validated foreign key relationships** to maintain consistency.  

### 3️⃣ **Database Implementation**  
- Tables were implemented in **Oracle SQL** with **Primary Keys (PKs)** and **Foreign Keys (FKs)**.  
- **SQL scripts** were written to load and structure the dataset.  
- Indexing was used for performance optimization.  

### 4️⃣ **Use of Window Functions**  
- **Ranking Analysis**: Used `RANK()` to determine driver rankings in each season.  
- **Cumulative Performance Trends**: Applied `SUM() OVER (PARTITION BY driverID ORDER BY year)` to track total points over time.  
- **Lag/Lead Functions**: Used `LAG()` and `LEAD()` to compare a driver's performance across consecutive races.  

## 🔍 Key Analyses  
✅ **Fastest pit stops by season & constructor**  
✅ **Driver performance trends over multiple seasons**  
✅ **Fastest lap times & records per year**  
✅ **Team-wise point distribution across seasons**  
✅ **Race completion & failure trends (DNFs, mechanical failures, etc.)**  


