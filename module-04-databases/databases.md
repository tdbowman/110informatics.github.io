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

## What is a Database?

A **database** is an organized collection of data stored and accessed electronically. Think of it as a highly structured digital filing system.

You already carry one in your pocket. Your phone's contact list is a small database: each person is a record in a table called something like `Contacts`, and each record has fields for first name, last name, phone number, email, and so on. When you type "Mar" into the search bar and Maria pops up instantly, that's a database query. The structure (every contact has the same fields, in the same order) is what makes that instant retrieval possible.

### Why Not Just Use a Spreadsheet?

If a database is basically organized data, why not keep everything in a spreadsheet or a folder of files? For tiny amounts of data, you can. But as data grows, flat files and spreadsheets break down in predictable ways, and imagining life without databases makes the point vividly:

- **Retrieval becomes slow and painful.** A library without a catalog still has all its books; good luck finding one. Databases use indexes so that finding one record among millions takes a fraction of a second.
- **Integrity erodes.** In a spreadsheet, nothing stops you from typing a name three different ways or entering a birthday of February 30. Databases enforce rules about what data is allowed, and (as you'll see with normalization) their structure prevents contradictory copies of the same fact.
- **Multiple users cause chaos.** Two people editing the same spreadsheet can silently overwrite each other. Databases are built for thousands of simultaneous users, coordinating updates so nothing is lost.
- **Security is weak.** Physical files can be stolen and a spreadsheet is usually all-or-nothing, while databases offer encryption and fine-grained permissions (the registrar can see your grades; your classmates cannot).
- **Scale becomes impossible.** E-commerce as we know it simply could not exist on spreadsheets. Neither could real-time bank balances, airline reservations, or personalized recommendations.

In short, spreadsheets store data; databases *manage* it.

### A Brief History of Databases

Databases evolved through several eras, and each era solved a problem the previous one couldn't:

| Era | Approach | Key Idea |
|-----|----------|----------|
| 1950s–60s | **Flat files** | Data in simple files; every program had to know each file's exact layout |
| 1960s–70s | **Hierarchical & network models** | Data organized in tree-like parent-child structures (used in early mainframe systems) |
| 1970s–today | **Relational model** | Edgar F. Codd's 1970 insight: store data in simple tables and let a query language handle relationships |
| 2000s–today | **NoSQL** | Web-scale companies needed flexible structures and massive distribution; document, key-value, and graph databases emerged |
| 2020s–today | **Vector stores** | The AI era: databases that store meaning itself as numbers |

The relational model won the middle decades so thoroughly that "database" and "relational database" became almost synonymous, and its query language, SQL, is still one of the most in-demand skills in the job market half a century later. The NoSQL and vector eras didn't replace relational databases; they joined them. A modern company typically runs several kinds at once.

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

Most databases you'll encounter are **relational databases**. Before diving in, it helps to learn the vocabulary, because database people use these words precisely.

### Core Vocabulary

When you design a database, you start by thinking in terms of **entities** (the things or concepts your data describes; think *nouns* like Student, Course, Order), **attributes** (the properties of each entity, like a student's name or major), and **relationships** (how entities connect; think *verbs* like "enrolls in" or "teaches"). Then you translate that thinking into tables:

| Term | Meaning |
|------|---------|
| **Table** | An organized set of data about one kind of entity, arranged in rows and columns |
| **Row (record)** | One instance of the entity: one student, one transaction. (Also called a *tuple*.) |
| **Column (attribute/field)** | One property recorded for every row: name, email, date |
| **Primary key** | A column whose value uniquely identifies each row (no two students share a StudentID) |
| **Foreign key** | A primary key from one table stored in another table to link related records |
| **Index** | A behind-the-scenes lookup structure (like a book's index) that makes searching a column fast |
| **Query** | A question you ask the database, written in SQL |

The primary key deserves special attention. Names make terrible identifiers (two students can both be named James, and people change their names), so databases assign an arbitrary unique value, like StudentID 002, that never changes and never repeats. Foreign keys are what put the "relational" in relational databases: by storing a StudentID inside another table, you connect that table's records back to exactly one student, with no ambiguity.

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

Here `StudentID` is the primary key of Students, `CourseID` is the primary key of Courses, and the Enrollments table holds both as foreign keys. Keep this example in mind; we're about to see why it's structured this way.

### Relationships & Cardinality

**Cardinality** is a mathematical term for the number of elements in a set. In databases, it describes how many instances of one entity can relate to instances of another. There are three patterns:

| Cardinality | Meaning | Example |
|-------------|---------|---------|
| **One-to-one** | Each record in A matches at most one record in B | Each student has one campus ID card; each card belongs to one student |
| **One-to-many** | One record in A matches many in B, but each B matches only one A | One department offers many courses; each course belongs to one department |
| **Many-to-many** | Records on both sides can match many on the other | Students take many courses; courses contain many students |

One-to-many relationships are the everyday workhorse, and they're easy to build: put a foreign key on the "many" side (each course row carries its department's ID).

Many-to-many relationships are trickier, because relational tables can't directly store "many values in one cell." The solution is a **bridge table** (also called a *junction* or *linking* table): a third table whose rows each record one connection between the two sides. Look back at the example above. Students and Courses have a many-to-many relationship, and the Enrollments table is the bridge. Each Enrollments row says "this one student is in this one course," and can even carry attributes that belong to the relationship itself, like the grade. Neither the student nor the course "owns" the grade; the *enrollment* does. Once you spot this pattern, you'll see bridge tables everywhere: playlists linking users to songs, follows linking users to users, orders linking customers to products.

### Normalization: Organizing Data Well

**Normalization** is the technique of organizing data to reduce redundancy and improve data integrity. Two terms to hold onto:

- **Redundancy**: the same data repeated or duplicated in multiple places
- **Data integrity**: the accuracy and reliability of the data

Why do we care? Because we want efficient databases, and we need consistent data. The best way to see this is a worked example, so let's break our Students/Courses example on purpose. Suppose a well-meaning beginner records enrollments in one big table:

**One Big Table (not normalized!)**
| StudentID | Name | Major | CourseID | CourseTitle | Credits |
|-----------|------|-------|----------|-------------|---------|
| 001 | Maria | Informatics | INF110 | Foundations of Informatics | 3 |
| 002 | James | Data Science | INF110 | Foundations of Informatics | 3 |
| 001 | Maria | Informatics | INF220 | Database Design | 3 |

Every fact about Maria is repeated in every row about Maria, and every fact about INF110 is repeated for every student enrolled in it. This redundancy causes three classic problems:

- **Update anomaly**: If INF110's title changes, you must update it in every row where it appears. Miss one row and your database now contradicts itself: which title is correct? The database can't tell you.
- **Insert anomaly**: You can't add a brand-new course to the catalog until at least one student enrolls, because a course only exists here as part of an enrollment row.
- **Delete anomaly**: If Maria drops both her courses and her rows are deleted, the database forgets Maria exists at all, major and everything.

Normalization fixes this by splitting the big table into related tables, each about exactly one kind of entity: a Students table (each student stated once), a Courses table (each course stated once), and the Enrollments bridge table holding just the foreign keys and the grade, exactly the three-table design shown earlier. Now each fact lives in exactly one place. Changing a course title means editing one row, new courses can exist without students, and dropping enrollments never erases a person. Nothing is lost by splitting, because SQL's `JOIN` can reassemble the big picture whenever you need it.

There are formal levels of normalization (called *normal forms*) that you'd study in a database course, but the instinct is what matters at this stage: **one fact, one place.** If you find yourself typing the same information twice, your tables probably want to be split.

### Partitioning & Sharding: When Databases Get Huge

What happens when a table grows to billions of rows? Two related techniques keep giant databases fast, and they're easy to confuse:

- **Partitioning** means splitting a large table into smaller pieces, most often within a single database system. For example, an orders table might be partitioned by year, so a query about last month only touches the current partition instead of scanning a decade of history.
- **Sharding** is horizontal partitioning taken across machines: the data is distributed over many independent servers (shards), each holding a slice, for example users A–M on one server and N–Z on another. Sharding is how global apps serve hundreds of millions of users, at the cost of real added complexity, since queries that need data from several shards must coordinate across machines.

A handy way to remember it: all sharding is partitioning, but partitioning becomes sharding when the pieces live on different machines.

### Databases in the Wild: Inside a Social App

Take any large social media app and mentally peel back the interface, and you'll find a whole federation of databases working together. A plausible sketch of the backend:

| Function | What's Stored | Likely Database Style |
|----------|--------------|----------------------|
| User management | Profiles, settings, login credentials | Relational |
| Content | Videos/photos and their metadata, tags, search terms | Object storage plus document/relational databases |
| Social graph | Who follows whom | Graph database |
| Real-time features | Notifications, live streams, messages | Fast key-value/NoSQL stores |
| Analytics & recommendations | Every view, like, pause, and rewatch, feeding recommendation models | Massive analytical stores and ML pipelines |
| Monetization | Advertisements, in-app purchases | Relational (money demands strict integrity) |
| Security & compliance | Privacy preferences, consent records for laws like the EU's GDPR | Relational, with heavy auditing |

Behind the scenes, caching keeps hot content in fast memory, and sharding spreads users across data centers worldwide. The takeaway for this course: "the database" behind a real product is rarely one database. It's a carefully designed ecosystem, and the concepts you're learning this week (entities, keys, relationships, integrity) are the shared language that holds it together.

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

That last query is normalization paying off: it walks from Students through the Enrollments bridge table to Courses, reassembling the "one big table" view on demand, while the underlying data stays clean and duplicate-free.

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

:::{tip} Design Challenge
Try designing tables for a recreational sports league: teams have names, colors, and twelve players each; every player belongs to exactly one team; games have a home team, away team, scores, and a date. Which relationships are one-to-many? Where do you need a primary key? (Bonus: what happens to your design if the league later allows players to join two teams?)
:::

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

Normalization is one of your best defenses here: a well-normalized design makes several of these problems structurally difficult to create in the first place, because each fact has exactly one home.

This matters even more in the AI era: modern AI systems are trained on enormous databases, so the biases and errors in those databases become the biases and errors of the AI. (We'll dig into this in Modules 6 and 12.)

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

## Looking Ahead

Next week, we explore **accessibility**: designing information systems that work for everyone, regardless of ability.
