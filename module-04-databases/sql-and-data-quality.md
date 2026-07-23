# SQL & Data Quality

> "Garbage in, garbage out."

---

## 🎯 In This Section

- Read your first SQL: `SELECT`, `WHERE`, and `JOIN`
- Watch a `JOIN` walk across tables and reassemble the "one big table" view on demand
- Identify five common data quality problems, from missing values to duplicates
- See why normalization is a structural defense against bad data
- Connect data quality to bias in AI systems trained on databases

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

That last query is [normalization](relational-databases.md) paying off: it walks from Students through the Enrollments bridge table to Courses, reassembling the "one big table" view on demand, while the underlying data stays clean and duplicate-free.

```{figure} images/sql-join-path.svg
:alt: Diagram of the path a SQL JOIN query takes. At the top is the query selecting student names and course titles. Below it, arrows trace the path from the Students table, across a join on StudentID to the Enrollments bridge table, then across a join on CourseID to the Courses table. The path ends at a result row reading Maria, Foundations of Informatics, labeled as the one-big-table view rebuilt on demand.
:width: 100%
:name: fig-sql-join-path

A JOIN is a guided walk across foreign keys: from Students, through the Enrollments bridge, to Courses, ending in a combined view that never has to be stored.
```

:::{tip} Don't worry!
You don't need to memorize SQL. The goal is to understand what databases *do* and how they *think*. We'll practice together in class.
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

[Normalization](relational-databases.md) is one of your best defenses here: a well-normalized design makes several of these problems structurally difficult to create in the first place, because each fact has exactly one home.

This matters even more in the AI era: modern AI systems are trained on enormous databases, so the biases and errors in those databases become the biases and errors of the AI. (We'll dig into this in Modules 6 and 12.)

---

## Up Next

That wraps the module's content pages. Head back to the [module overview](databases.md) for this week's readings, reflection prompt, and assignments.
