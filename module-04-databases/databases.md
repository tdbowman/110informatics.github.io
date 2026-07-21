# Module 4: Database Design & Development 🗄️

**Week 4 | Data Storage & Organization**

---

## The Big Picture

Every time you search for a product, check your bank balance, or scroll through social media, you're interacting with a database. Databases are the backbone of our information systems, organizing, storing, and retrieving the data that powers our digital world.

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
| **Vector** | Stores meaning as lists of numbers ("embeddings") | AI search, chatbot memory |

:::{note} 🤖 Vector Databases: How AI Systems "Remember"
The newest member of the database family exists because of AI. A **vector database** stores text, images, or audio as *embeddings* (long lists of numbers that capture meaning) so a system can find items that are *similar in meaning*, not just items that match keywords.

This is how a company chatbot "remembers" thousands of internal documents: your question is converted to numbers, the database finds the most similar passages, and the AI writes an answer from them. (This technique is called **retrieval-augmented generation**, or RAG. Remember the term, because it connects this module directly to Module 8 on search and Module 12 on AI.)
:::

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
| [What is a Database?](https://www.oracle.com/database/what-is-database/) | Reading | Oracle's plain-language introduction |
| [Database Models](https://www.lucidchart.com/pages/database-diagram/database-models) | Reading | Visual guide to how databases are structured |
| [SQLBolt](https://sqlbolt.com/) | Interactive | Learn SQL by doing; work through Lessons 1–6 |

### 🤔 Make You Think

- How do databases encode assumptions about identity? (Think: gender fields, name formats)
- What happens when categories don't fit real people?
- Who decides the structure of a database?
- **AI twist:** Try asking an AI chatbot to design a database schema for a club you belong to. Then critique it: what did it get wrong or assume? (Being able to *evaluate* an AI's database design is quickly becoming more valuable than memorizing syntax.)

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

This matters even more in the AI era: modern AI systems are trained on enormous databases, so the biases and errors in those databases become the biases and errors of the AI. (We'll dig into this in Modules 6 and 12.)

### 🗝️ Key Terms This Week

*Database · Table · Primary key · SQL · NoSQL · Vector database · Embedding · RAG*: see the [Glossary](../glossary.md).

---

## 📝 This Week's Assignments

| Assignment | Due | Notes |
|------------|-----|-------|
| Weekly Reflection | Friday by class | Connect to database concepts |

:::{tip} Reflection Prompt
Think about the databases that contain information about YOU (school records, social media, shopping history, medical records). What do you know about how this data is organized? What might be inaccurate or missing?
:::

---

## Looking Ahead

Next week, we explore **accessibility**: designing information systems that work for everyone, regardless of ability.
