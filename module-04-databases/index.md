# Module 4: Database Design & Development 🗄️

**Week of January 27 | Data Storage & Organization**

---

## The Big Picture

Every time you search for a product, check your bank balance, or scroll through social media, you're interacting with a database. Databases are the backbone of our information systems—organizing, storing, and retrieving the data that powers our digital world.

This week, we explore how databases work and why they matter for informatics.

### 🎯 What You'll Learn

- Understand what databases are and why they're essential
- Learn about different types of databases
- Explore relational database concepts
- Get hands-on with SQL (Structured Query Language)
- Consider issues of data quality and integrity

### 🧠 Big Questions to Consider

- How is data organized to be useful?
- What happens when databases contain errors or biases?
- Who decides how information is categorized?
- What are the implications of massive data collection?

---

## What is a Database?

A **database** is an organized collection of data stored and accessed electronically. Think of it as a highly structured digital filing system.

### Types of Databases

| Type | Description | Example Use |
|------|-------------|-------------|
| **Relational** | Data in tables with relationships | Customer orders, inventory |
| **NoSQL** | Flexible, non-tabular structure | Social media, IoT data |
| **Graph** | Nodes and edges for relationships | Social networks, recommendations |
| **Document** | Stores data as documents (JSON) | Content management |

---

## Relational Databases

Most databases you'll encounter are **relational databases** organized into:

- **Tables**: Collections of related data (like spreadsheets)
- **Rows**: Individual records (one customer, one transaction)
- **Columns**: Attributes of each record (name, email, date)
- **Keys**: Unique identifiers that link tables together

### Example: A Simple Database

**Students Table**
| StudentID | Name | Major | Year |
|-----------|------|-------|------|
| 001 | Maria | Informatics | Junior |
| 002 | James | Data Science | Senior |
| 003 | Aisha | UX Design | Sophomore |

**Courses Table**
| CourseID | Title | Credits |
|----------|-------|---------|
| INF110 | Foundations of Informatics | 3 |
| INF220 | Database Design | 3 |

**Enrollments Table** (links students to courses)
| StudentID | CourseID | Grade |
|-----------|----------|-------|
| 001 | INF110 | A |
| 002 | INF110 | B+ |
| 001 | INF220 | A- |

---

## SQL: Structured Query Language

SQL is the language we use to communicate with relational databases.

### Basic SQL Commands

```sql
-- Select all students
SELECT * FROM Students;

-- Select specific columns
SELECT Name, Major FROM Students;

-- Filter with conditions
SELECT * FROM Students WHERE Year = 'Senior';

-- Join tables together
SELECT Students.Name, Courses.Title
FROM Students
JOIN Enrollments ON Students.StudentID = Enrollments.StudentID
JOIN Courses ON Enrollments.CourseID = Courses.CourseID;
```

:::{tip} Don't worry!
You don't need to memorize SQL. The goal is to understand what databases *do* and how they *think*. We'll practice together in class.
:::

---

## This Week's Journey

### 📚 Core Readings & Videos

| Resource | Type | Notes |
|----------|------|-------|
| What is a Database? | Video | Introduction to concepts |
| Relational Database Fundamentals | Reading | Core principles |
| SQL Basics Tutorial | Interactive | Hands-on practice |

### 🤔 Make You Think

- How do databases encode assumptions about identity? (Think: gender fields, name formats)
- What happens when categories don't fit real people?
- Who decides the structure of a database?

---

## Data Quality Matters

Databases are only as good as the data in them. Issues include:

| Problem | Description |
|---------|-------------|
| **Incomplete Data** | Missing values, empty fields |
| **Inconsistent Data** | "NYC" vs "New York" vs "New York City" |
| **Inaccurate Data** | Wrong information, typos |
| **Duplicate Data** | Same record entered multiple times |
| **Outdated Data** | Information that's no longer current |

> "Garbage in, garbage out" — A fundamental truth of computing

---

## 📝 This Week's Assignments

| Assignment | Due | Notes |
|------------|-----|-------|
| Weekly Reflection | Friday by class | Connect to database concepts |
| Usability Project | Continues | See assignment details |

:::{tip} Reflection Prompt
Think about the databases that contain information about YOU (school records, social media, shopping history, medical records). What do you know about how this data is organized? What might be inaccurate or missing?
:::

---

## Looking Ahead

Next week, we explore **accessibility**—designing information systems that work for everyone, regardless of ability.
