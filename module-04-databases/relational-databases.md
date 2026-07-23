# Relational Database Design

> "One fact, one place."

---

## 🎯 In This Section

- Learn the core vocabulary: entities, tables, rows, columns, keys, and queries
- See how primary and foreign keys link tables together with no ambiguity
- Recognize one-to-one, one-to-many, and many-to-many relationships, and the bridge tables that make the last one work
- Understand normalization and why "one fact, one place" protects data integrity
- Find out how partitioning and sharding keep billion-row databases fast

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

```{figure} images/tables-and-keys.svg
:alt: Three database tables side by side. The Students table on the left has StudentID as its primary key; the Courses table on the right has CourseID as its primary key. Between them sits the Enrollments bridge table, whose StudentID and CourseID columns are foreign keys, with arrows pointing from each foreign key back to the matching primary key. A note explains that each Enrollments row records one student in one course, turning one many-to-many relationship into two one-to-many links.
:width: 100%
:name: fig-tables-and-keys

Foreign keys are the "relational" in relational databases: each value in the Enrollments bridge table points back to exactly one row in Students or Courses.
```

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

Normalization fixes this by splitting the big table into related tables, each about exactly one kind of entity: a Students table (each student stated once), a Courses table (each course stated once), and the Enrollments bridge table holding just the foreign keys and the grade, exactly the three-table design shown earlier. Now each fact lives in exactly one place. Changing a course title means editing one row, new courses can exist without students, and dropping enrollments never erases a person. Nothing is lost by splitting, because [SQL's `JOIN`](sql-and-data-quality.md) can reassemble the big picture whenever you need it.

```{figure} images/normalization-split.svg
:alt: Diagram of normalization. On the left, one big unnormalized table repeats Maria's name and major and the course title Foundations of Informatics across multiple rows; a warning box below lists the update, insert, and delete anomalies this redundancy causes. An arrow labeled normalize points to three clean tables on the right: Students with each student stated once, Enrollments holding just foreign keys plus the grade, and Courses with each course stated once. A note at the bottom says SQL's JOIN can reassemble the big picture whenever it is needed.
:width: 100%
:name: fig-normalization-split

Splitting the big table loses nothing and fixes everything: each fact gets exactly one home, and JOIN can rebuild the combined view on demand.
```

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

## Up Next

You've designed clean tables; now you need a way to talk to them. Meet the fifty-year-old language that still runs the world's data in [SQL & Data Quality](sql-and-data-quality.md).
