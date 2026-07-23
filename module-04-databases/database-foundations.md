# Database Foundations

> "Spreadsheets store data; databases *manage* it."

---

## 🎯 In This Section

- Define what a database is, and find the one already in your pocket
- See five predictable ways spreadsheets and flat files break down as data grows
- Trace the evolution of databases from 1950s flat files to today's vector stores
- Compare relational, NoSQL, graph, document, and vector databases
- Learn how AI systems use vector databases to "remember"

---

## What is a Database?

A **database** is an organized collection of data stored and accessed electronically. Think of it as a highly structured digital filing system.

You already carry one in your pocket. Your phone's contact list is a small database: each person is a record in a table called something like `Contacts`, and each record has fields for first name, last name, phone number, email, and so on. When you type "Mar" into the search bar and Maria pops up instantly, that's a database query. The structure (every contact has the same fields, in the same order) is what makes that instant retrieval possible.

### Why Not Just Use a Spreadsheet?

If a database is basically organized data, why not keep everything in a spreadsheet or a folder of files? For tiny amounts of data, you can. But as data grows, flat files and spreadsheets break down in predictable ways, and imagining life without databases makes the point vividly:

- **Retrieval becomes slow and painful.** A library without a catalog still has all its books; good luck finding one. Databases use indexes so that finding one record among millions takes a fraction of a second.
- **Integrity erodes.** In a spreadsheet, nothing stops you from typing a name three different ways or entering a birthday of February 30. Databases enforce rules about what data is allowed, and (as you'll see with [normalization](relational-databases.md)) their structure prevents contradictory copies of the same fact.
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

## Up Next

Most of the databases you'll actually meet are relational, and they have a precise vocabulary and logic all their own. Learn it in [Relational Database Design](relational-databases.md).
