---
banner: images/module-04-banner.png
thumbnail: images/module-04-banner.png
---

# Module 4: Database Design & Development 🗄️

**Week 4 | Data Storage & Organization**

---

## The Big Picture

Every time you search for a product, check your bank balance, or scroll through social media, you're interacting with a database. Databases are the backbone of our information systems, organizing, storing, and retrieving the data that powers our digital world.

This week, we explore how databases work and why they matter for informatics.

### 🎯 What You'll Learn

- Understand what databases are and why they're essential
- Learn about different types of databases and how they evolved
- Explore relational database concepts: tables, keys, relationships, and normalization
- Get hands-on with SQL (Structured Query Language)
- Consider issues of data quality and integrity

### 🧠 Big Questions to Consider

- How is data organized to be useful?
- What happens when databases contain errors or biases?
- Who decides how information is categorized?
- What are the implications of massive data collection?

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

:::{tip} Design Challenge
Try designing tables for a recreational sports league: teams have names, colors, and twelve players each; every player belongs to exactly one team; games have a home team, away team, scores, and a date. Which relationships are one-to-many? Where do you need a primary key? (Bonus: what happens to your design if the league later allows players to join two teams?)
:::

---

## Module Contents

This module contains three sections:

1. **[Database Foundations](database-foundations.md)** - What a database is, why spreadsheets break down as data grows, and how databases evolved from flat files to vector stores
2. **[Relational Database Design](relational-databases.md)** - Tables, keys, relationships, normalization, and how billion-row databases stay fast
3. **[SQL & Data Quality](sql-and-data-quality.md)** - The language we use to talk to relational databases, and why a database is only as good as the data in it

### 🗝️ Key Terms This Week

*Database · Table · Primary key · Foreign key · Cardinality · Bridge table · Normalization · Index · SQL · NoSQL · Sharding · Vector database · Embedding · RAG*: see the [Glossary](../glossary.md).

---

## 📝 This Week's Assignments

| Assignment | Due | Notes |
|------------|-----|-------|
| Weekly Reflection | Friday by class | Connect to database concepts |

:::{tip} Reflection Prompt
Think about the databases that contain information about YOU (school records, social media, shopping history, medical records). What do you know about how this data is organized? What might be inaccurate or missing?
:::

---

## Let's Get Started!

Begin with [Database Foundations](database-foundations.md) to see what databases are and why spreadsheets can't do their job, then learn how tables, keys, and normalization fit together in [Relational Database Design](relational-databases.md), and finish with [SQL & Data Quality](sql-and-data-quality.md) to see how we query databases and why the data inside them matters.

---

## Looking Ahead

Next week, we explore **accessibility**: designing information systems that work for everyone, regardless of ability.
