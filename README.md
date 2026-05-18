# Netflix Data Analysis using PostgreSQL

<p align="center">
  <img src="https://i.pcmag.com/imagery/reviews/05cItXL96l4LE9n02WfDR0h-5.fit_lim.size_1200x630.v1582751026.png" width="800" >
</p>

## Project Overview
This project focuses on analyzing the Netflix dataset using PostgreSQL.  
The goal of this project is to perform data exploration and solve real-world business problems using SQL queries.

The project includes:
- Database creation
- Data exploration
- Business problem solving
- SQL concepts like:
  - CTEs
  - Window Functions
  - Aggregate Functions
  - String Functions
  - Date Functions
  - Filtering & Grouping

---

## Tools & Technologies
- PostgreSQL
- SQL

---

## Dataset Information
The dataset contains Netflix content information such as:

- Show ID
- Type (Movie / TV Show)
- Title
- Director
- Cast
- Country
- Date Added
- Release Year
- Rating
- Duration
- Genre
- Description

---

# Database Schema

```sql
DROP TABLE IF EXISTS netflix;

CREATE TABLE netflix
(
    show_id        VARCHAR(6),
    type           VARCHAR(10),
    title          VARCHAR(150),
    director       VARCHAR(250),
    casts          VARCHAR(1000),
    country        VARCHAR(150),
    date_added     VARCHAR(50),
    release_year   INT,
    rating         VARCHAR(10),
    duration       VARCHAR(15),
    listed_in      VARCHAR(100),
    description    VARCHAR(250)
);
```

---

# Business Problems Solved

## 1. Count the number of Movies vs TV Shows
- Used `GROUP BY`
- Content type distribution analysis

---

## 2. Find the most common rating for Movies and TV Shows
- Used:
  - `CTE`
  - `RANK() Window Function`

---

## 3. List all movies released in a specific year
- Filtering movies released in 2020

---

## 4. Find the Top 5 countries with the most Netflix content
- Used:
  - `STRING_TO_ARRAY()`
  - `UNNEST()`

---

## 5. Identify the longest movie
- Used `MAX()` function

---

## 6. Find content added in the last 5 years
- Used:
  - `TO_DATE()`
  - `INTERVAL`

---

## 7. Find all content by director 'Rajiv Chilaka'
- Used `ILIKE`

---

## 8. List TV Shows with more than 5 seasons
- Used:
  - `SPLIT_PART()`
  - Type Casting

---

## 9. Count content items in each genre
- Genre analysis using:
  - `UNNEST()`
  - `STRING_TO_ARRAY()`

---

## 10. Analyze yearly average content release in India
- Used:
  - `EXTRACT()`
  - Aggregate Functions
  - Percentage calculations

---

## 11. Find all documentary movies
- Genre filtering using `ILIKE`

---

## 12. Find content without a director
- Handling `NULL` values

---

## 13. Find Salman Khan movies released in the last 10 years
- Actor-based filtering

---

## 14. Find Top 10 actors in Indian movies
- Actor frequency analysis

---

## 15. Categorize content as Good or Bad
- Used:
  - `CASE WHEN`
  - Keyword-based classification

---

# SQL Concepts Used

- SELECT Statements
- WHERE Clause
- GROUP BY
- ORDER BY
- LIMIT
- Aggregate Functions
- Common Table Expressions (CTEs)
- Window Functions
- CASE Statements
- Date Functions
- String Functions
- Type Casting

---

# Project Learning Outcomes

Through this project, I improved my understanding of:

- Writing complex SQL queries
- Solving business problems using SQL
- Data cleaning and exploration
- Query optimization basics
- Real-world data analysis workflows

---

# How to Run This Project

1. Install PostgreSQL
2. Create a database
3. Run the table creation query
4. Import the Netflix dataset
5. Execute the SQL queries

---

# Future Improvements

- Build an interactive dashboard using:
  - Power BI
  - Tableau
- Add advanced SQL analysis
- Perform trend analysis and visualizations

---

# Author

Abhi  
BCA Student | Aspiring Data Analyst

---


```
