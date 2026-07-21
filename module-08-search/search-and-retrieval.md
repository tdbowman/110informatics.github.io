# Module 8: Search Engines & Information Retrieval 🔍

**Week 8 | Finding Information**

---

## The Big Picture

How does Google find exactly what you're looking for among billions of web pages in less than a second? The answer lies in **information retrieval**—the science of finding relevant information from large collections.

This week, we explore how search engines work and how AI has transformed the way we find information.

### 🎯 What You'll Learn

- Understand the fundamentals of information retrieval
- Learn the difference between searching and browsing
- Explore how search engines are designed and developed
- Understand how generative AI has reshaped search — and the new questions it raises
- Evaluate the quality and bias of search results

### 🧠 Big Questions to Consider

- What determines which results appear first?
- How do search engines shape what we know?
- What's the difference between finding information and understanding it?
- When an AI *answers* your question instead of linking to sources, what do we gain — and what do we lose?

---

## Information Retrieval Basics

**Information Retrieval (IR)** is the process of obtaining relevant information from a collection of resources.

### Searching vs. Browsing

| Activity | Description | Example |
|----------|-------------|---------|
| **Searching** | Looking for specific information | Typing a query into Google |
| **Browsing** | Exploring without a specific goal | Scrolling through Netflix |

Good information systems support both!

---

## How Search Engines Work

### The Three Steps

1. **Crawling**: Automated "spiders" visit web pages and follow links
2. **Indexing**: Pages are analyzed and stored in a massive database
3. **Ranking**: When you search, results are ordered by relevance

### What Makes Something "Relevant"?

Search engines consider:
- **Keywords**: Does the page contain your search terms?
- **Quality**: Is the page authoritative and trustworthy?
- **Freshness**: Is the content recent and updated?
- **Personalization**: Your location, history, and preferences
- **Link Analysis**: How many other pages link to this one?

---

## Search After Generative AI

Since 2023, search has changed more than in the previous twenty years combined:

| Development | What It Means |
|-------------|---------------|
| **AI Overviews / AI Mode** | Google now generates an AI answer *above* the traditional links for many queries (rolled out broadly starting May 2024) |
| **Answer engines** | Tools like Perplexity and ChatGPT's search mode answer questions directly, citing (some) sources |
| **Zero-click search** | More searches end without anyone clicking a website — raising hard questions about who sustains the sites the AI learned from |
| **Multimodal search** | Search by image, voice, or by [humming a song](https://blog.google/products/search/hum-to-search/) |

### RAG: Where This Module Meets AI

The technique behind AI search is called **retrieval-augmented generation (RAG)** — and it is literally this module's two topics fused together:

1. **Retrieve**: A classic IR system (like the ones described above, often powered by the vector databases from Module 4) finds documents relevant to your question.
2. **Generate**: An AI language model writes an answer *based on those retrieved documents*.

This is why information retrieval concepts still matter in the ChatGPT era. When an AI gives a wrong answer, it's often an **IR failure** — the system retrieved the wrong documents, or none at all, and the model filled the gap by guessing. AI "hallucination" and bad search results are cousins.

:::{note} Discussion Point
When AI generates an answer instead of linking to sources, how do we verify accuracy? Who is responsible for errors? And what happens to the websites nobody clicks anymore?
:::

### 📌 Case Study: *United States v. Google*

The biggest tech antitrust case in a generation is about **search defaults**. In August 2024, a federal judge ruled that Google illegally maintained its search monopoly, largely through billions paid to be the default engine on phones and browsers. In September 2025 came the remedies: Google keeps Chrome and Android, but **exclusive default deals are banned** and Google must share certain search data with qualified competitors ([NPR](https://www.npr.org/2025/09/02/nx-s1-5478625/google-chrome-doj-antitrust-ruling)). Google is appealing.

*Why it belongs in this chapter:* everything you just learned — crawling, indexing, ranking, defaults, personalization — is what this case is about. Scale matters: whoever controls retrieval controls what billions of people find. *(Status as of mid-2026; check for appeal developments.)*

---

## This Week's Journey

:::{note} Before Class
Complete the readings below. Pay attention to how search shapes information access!
:::

### 📚 Core Readings

| Resource | Type | Notes |
|----------|------|-------|
| [How does Google's monopoly hurt you? Try these searches.](https://www.washingtonpost.com/technology/2020/10/19/google-search-results-monopoly/) | Article | Fowler's search bias investigation (written before the ruling that agreed) |
| [Information Retrieval Systems Explained](https://www.elastic.co/what-is/information-retrieval) | Article | Technical foundations |
| [Song stuck in your head? Just hum to search](https://blog.google/products/search/hum-to-search/) | Article | Multimodal search in action |

### 🤔 Make You Think (Optional)

- Ask the same question to a traditional Google search, Google's AI Overview, and an answer engine like Perplexity. Compare: Which sources did each rely on? Which answer would you trust — and how would you check?

---

## Key Concepts

### TF-IDF: How Search Engines Measure Relevance

**Term Frequency - Inverse Document Frequency** is a classic algorithm:

- **Term Frequency (TF)**: How often does the word appear in this document?
- **Inverse Document Frequency (IDF)**: How rare is this word across all documents?

Words that appear frequently in one document but rarely overall are probably important!

(Modern AI search adds **semantic search**: instead of matching words, it matches *meanings*, using the embeddings you met in Module 4. "How do I fix a flat?" can retrieve a page about "repairing punctured bicycle tires" even with zero words in common.)

### The Filter Bubble

When search results are personalized based on your history and preferences, you may only see information that confirms what you already believe.

:::{warning} Consider This
Two people searching the same term might get completely different results based on their location, search history, and browsing behavior. What are the implications for shared understanding? Does an AI-generated answer make this better — or just less visible?
:::

### SEO and SEM

| Term | Meaning |
|------|---------|
| **SEO** (Search Engine Optimization) | Improving a website to rank higher in organic results |
| **SEM** (Search Engine Marketing) | Paying for ads to appear in search results |

Understanding these helps you recognize what's organic vs. paid. (A new cousin has emerged: optimizing content so *AI systems* cite it — sometimes called "GEO," generative engine optimization.)

### 🗝️ Key Terms This Week

*Information retrieval · Crawling · Indexing · Ranking · TF-IDF · Semantic search · RAG · Hallucination · Filter bubble · SEO* — see the [Glossary](../glossary.md).

---

## 📝 This Week's Assignments

| Assignment | Due | Notes |
|------------|-----|-------|
| Weekly Reflection | Friday by class | Connect to search engine concepts |
| Research Questions | Due this week | Send to Professor for approval |

:::{tip} Reflection Prompt
Try searching for the same controversial topic on a traditional search engine, an AI answer engine (Perplexity, ChatGPT search), and a privacy-focused engine (DuckDuckGo). Do you get different results and framings? Why might that be? What does this tell you about information access in the AI era?
:::

---

## Looking Ahead

Spring Break is coming! After the break, we'll explore **Security & Privacy**—how to protect yourself and your data in the digital age.
