# Module 8: Search Engines & Information Retrieval 🔍

**Week 8 | Finding Information**

---

## The Big Picture

How does Google find exactly what you're looking for among billions of web pages in less than a second? The answer lies in **information retrieval**, the science of finding relevant information from large collections.

This week, we explore how search engines work and how AI has transformed the way we find information.

### 🎯 What You'll Learn

- Understand the fundamentals of information retrieval
- Learn the difference between searching and browsing
- See how knowledge is organized for retrieval, from metadata and taxonomies to folksonomies and ontologies
- Explore how search engines are designed and developed: crawling, indexing, query processing, and ranking
- Understand how generative AI has reshaped search, and the new questions it raises
- Evaluate the quality and bias of search results

### 🧠 Big Questions to Consider

- What determines which results appear first?
- How do search engines shape what we know?
- What's the difference between finding information and understanding it?
- When an AI *answers* your question instead of linking to sources, what do we gain and what do we lose?

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

## Organizing Knowledge So It Can Be Found

Long before web search, librarians and information scientists were solving the same problem: how do you organize information so someone can find it later? Their tools form a kind of ladder, from lightweight and informal at the bottom to rigorous and expensive at the top. Every modern system, including search engines and the AI tools later in this chapter, still leans on these ideas.

**Metadata** is the foundation: data about data. A song file's metadata includes its title, artist, album, and length; a photo's includes when and where it was taken; a library record describes a book's author, subject, and publisher. Search engines rely heavily on metadata because it provides context the raw content may not: a page's title, description, and language tell a crawler a great deal before it reads a single sentence.

**Synonym rings** solve the "many words, one meaning" problem: a group of terms treated as semantically equivalent for retrieval purposes. If "car," "auto," and "automobile" are ringed together, a search for one finds documents using any of them. You saw this idea moments ago as query expansion; synonym rings are the curated, human-built version.

**Controlled vocabularies** go a step further: a predefined list of terms that everyone entering or searching data must use. Instead of some records saying "heart attack" and others "myocardial infarction," a controlled vocabulary picks one official term. As one classic description puts it, a controlled vocabulary inserts an interpretive layer of semantics between the term the user enters and the underlying database, to better represent what the user meant. Controlled vocabularies often mark relationships between terms: **BT** (broader term) and **NT** (narrower term). "Dogs" has the broader term "Mammals" and narrower terms like "Retrievers," which lets a system widen or tighten a search on demand.

**Taxonomies** organize those terms into a full hierarchical classification: categories and subcategories, from general to specific. Biology's kingdom-phylum-class system is the famous one, but you use taxonomies daily: an online store's Electronics > Audio > Headphones > Wireless path is a taxonomy you navigate every time you shop.

**Authority files** handle names. Is the author "J.K. Rowling," "Joanne Rowling," or "Robert Galbraith" (her pen name)? An authority file establishes one authoritative form for each name and subject, with cross-references from the variants, so a catalog search finds everything by a person no matter which form a record used.

**Folksonomies** are what happens when you skip all that structure and let users tag things themselves. Hashtags on TikTok, Instagram, and X are folksonomies: classification from the bottom up, by folks. The upside is speed, scale, and vocabulary that matches how people actually talk. The downside is visible in any TikTok tag stream:

- Misspellings and variations split one topic across many tags
- Many posts have missing or inconsistent tags
- Synonyms scatter related content ("#thrifting" vs. "#secondhandfashion")
- Deliberate mistagging: trolling (tagging unrelated content to hijack a trend) and marketing (stuffing popular tags onto ads to ride their reach)

A folksonomy trades precision for participation. Whether that trade is worth it depends on the system; for a social feed it mostly works, for a medical database it would be a disaster.

**Ontologies** sit at the top of the ladder: a formal representation of knowledge that defines not just concepts and categories but the *relationships* between them, in a form machines can reason over. A taxonomy can say "Aspirin is a Drug." An ontology can also say "Aspirin *treats* Headache, *interacts with* Warfarin, and *belongs to* the class Anti-inflammatory." Ontologies power AI systems, the Semantic Web, and biomedical research, anywhere software needs to draw conclusions rather than just retrieve documents.

| Rung | Structure | Cost to build | Example |
|------|-----------|---------------|---------|
| Metadata | Descriptive fields | Low | Song title, artist, year |
| Synonym ring | Equivalent terms | Low | car = auto = automobile |
| Controlled vocabulary | Approved terms, BT/NT links | Medium | Medical subject headings |
| Taxonomy | Full hierarchy | Medium-high | Store category tree |
| Authority file | Canonical names | Medium | One official form per author |
| Folksonomy | User tags, no control | Nearly free | TikTok hashtags |
| Ontology | Concepts plus formal relationships | High | Drug-interaction knowledge bases |

The pattern to notice: as you climb the ladder (folksonomies excepted, they're the ladder's free-spirited cousin), retrieval gets more precise and more consistent, but building and maintaining the system gets more expensive. Every real-world system picks its rung based on how much wrong-answer it can tolerate.

---

## How Search Engines Work

### The Three Steps

1. **Crawling**: Automated "spiders" visit web pages and follow links
2. **Indexing**: Pages are analyzed and stored in a massive database
3. **Ranking**: When you search, results are ordered by relevance

Those three words carry a lot of machinery, so let's open the hood on each.

### Crawling: How a Spider Explores the Web

Nobody hands a search engine a list of every page on the web; there is no such list. Instead, a **web crawler** (also called a spider or bot) discovers the web by walking it, link by link. The process looks like this:

1. **Seed URLs.** The crawler starts from an initial list of known addresses, drawn from previous crawls, sitemaps submitted by website owners, and other sources.
2. **Fetching and parsing.** It visits each URL, downloads the page, and parses it to extract text, metadata, and, crucially, links to other pages.
3. **The URL queue.** Every newly discovered link joins a queue of pages to visit next. The crawler works through the queue, and each visited page feeds it more links. This is why a crawl never really finishes: the frontier keeps growing.
4. **Filtering and deduplication.** Crawlers decide which URLs are worth visiting and skip pages they've already seen, unless the content has changed and the index copy needs updating.
5. **Politeness.** Well-behaved crawlers respect a site's **robots.txt** file, a small text file where site owners say "please don't crawl these pages." They also throttle their request rates so they don't overwhelm a site's server. A crawler hitting a small site thousands of times per second would be indistinguishable from an attack.

A few strategic choices shape a crawl:

- **Depth versus breadth.** A depth-first crawler burrows deep into one site before moving on; a breadth-first crawler skims across many sites at the same level before going deeper. Real crawlers blend the two, prioritizing pages likely to matter.
- **Dynamic content.** Much of the modern web is generated by JavaScript after the page loads. Some crawlers can execute scripts to see that content; many can't, which is one reason plain HTML is still the most reliably searchable web.
- **Freshness.** The web changes constantly, so crawlers run continuously, revisiting pages to catch updates and deletions. News sites get recrawled far more often than a decade-old personal homepage.
- **Distribution.** At web scale, no single machine can do this. Large search engines run many crawlers in parallel, coordinated by a central system that divides up the web and prevents duplication.

### Indexing: The World's Biggest Book Index

Once pages are fetched, the search engine builds its **index**: a database of all the text, metadata, and other information extracted from those pages, organized for fast lookup.

The core trick is called an **inverted index**, and you have used one your whole life: it's the index at the back of a book. A book's pages run in order, and the index *inverts* that: for each important word, it lists the pages where the word appears. A search engine does the same at web scale. Instead of storing "page X contains the words A, B, C," it stores "word A appears on pages X, Y, Z."

Why bother? Speed. When you search for "octopus intelligence," the engine does not read billions of pages looking for those words (that would take days). It looks up "octopus" in the inverted index, looks up "intelligence," and intersects the two lists, all in milliseconds. Nearly everything magical about search speed comes down to this one data structure, prepared ahead of time so your query doesn't have to do the work.

### Query Processing: What Happens When You Hit Enter

Between your keystrokes and the results page, your query goes through its own pipeline. In roughly the order it happens:

1. **Tokenization.** The query string is broken into individual components (words or phrases) called tokens.
2. **Stop word removal.** Very common words like "and," "or," and "the" usually add little meaning and may be dropped.
3. **Normalization.** Terms are standardized: lowercased, then reduced by **stemming** (chopping words to a root form, so "running" and "runs" both become "run") or **lemmatization** (mapping words to their dictionary form, so "better" becomes "good"). This lets a search for "swimming lessons" match a page that says "swim lesson."
4. **Phrase detection.** Words in quotation marks, or words that commonly travel together ("New York"), are treated as a single unit so their meaning isn't scattered.
5. **Query expansion.** The engine may quietly add synonyms, acronyms, and related terms so relevant pages using different words still surface.
6. **Spelling correction.** "Restaraunt" gets fixed before it ever reaches the index, which is why typos rarely break your searches.
7. **Disambiguation.** Does "jaguar" mean the cat, the car, or the operating system? The engine uses contextual clues and the behavior of past searchers to guess the most likely meaning.
8. **Personalization.** Your location, language, and search history may adjust both interpretation and results. Searching "pizza near me" would be useless without it; the trade-offs come up in the filter bubble discussion below.
9. **Query classification.** The engine categorizes your intent: **informational** (you want to learn something), **navigational** (you want a specific site), or **transactional** (you want to do or buy something). Different intents trigger different result layouts, which is why "weather" gets a forecast box and "facebook login" gets one dominant link.

Only after all this does the refined query go to the index, and ranking begins. There's also a **feedback loop**: which results people click, and how long they stay, feeds back into improving both query understanding and ranking over time.

### Ranking: What Makes Something "Relevant"?

The index may return millions of matching pages. Ranking decides what you actually see, and factors include:

| Factor | The question it asks |
|--------|----------------------|
| **Keyword matching** | Does the page contain (or mean) what the query says? |
| **Link analysis** | How many other quality pages link to this one? |
| **User engagement** | When this page appears in results, do people click it and stay? |
| **Page quality** | Is the source authoritative and reliable? |
| **Freshness** | Is the content current, for queries where that matters? |
| **Location** | Is the page relevant to where the searcher is? |

The most famous of these is link analysis, and the intuition behind Google's original **PageRank** algorithm is worth knowing. Treat every link from one page to another as a **vote**: page A linking to page B is A vouching that B is worth visiting. But not all votes count equally. A vote from a page that itself has many votes carries more weight. So an obscure blog linking to your site helps a little; a major university linking to it helps a lot. This recursive idea ("you're important if important pages point to you") let early Google surface trustworthy pages far better than keyword matching alone, and it's why an entire industry of link-buying and link-swapping sprang up to game it. Modern ranking blends hundreds of signals, but the votes intuition still explains a lot of what floats to the top.

---

## Relevant to Whom? Measuring Search Success

We've used the word "relevant" a lot. Information retrieval researchers noticed decades ago that it hides an ambiguity:

- **System-oriented relevance**: the document matches the *query*. The words (or meanings) line up; the algorithm scores it highly.
- **User-oriented relevance**: the document actually satisfies the *person*. It answers their real need, at their level, in a form they can use.

These come apart constantly. Search "python" wanting programming help and a perfectly system-relevant page about snakes is user-irrelevant. A technically accurate medical paper is system-relevant to a worried parent's query and user-irrelevant if it's unreadable to them. This gap is why evaluation methods split the same way: system-oriented evaluation tests ranking algorithms against pre-judged document sets (bypassing real users entirely), while user-oriented evaluation watches or asks actual people whether they found what they needed. Describing your information need in words a system can act on is genuinely hard, and it's half the challenge of IR.

### Precision and Recall, in Plain Language

How do we score a search system? Two measures do most of the work, and they pull against each other:

- **Precision**: of the results the system returned, what fraction were actually relevant? High precision means little junk in your results.
- **Recall**: of all the relevant documents that *exist* in the collection, what fraction did the system find? High recall means little treasure left behind.

A fishing analogy: precision asks "how much of what's in the net is fish?" and recall asks "how many of the lake's fish ended up in the net?" You can max out recall by dragging the whole lake (you'll get every fish, plus boots and tires: terrible precision). You can max out precision by keeping only the one fish you're certain about (and miss the rest: terrible recall).

Which matters more depends on the task. A student wanting one good source for a discussion post cares about precision: the first page of results should be good. A lawyer searching for every precedent, or a doctor checking every known drug interaction, needs recall: missing one relevant document can be catastrophic. Web search engines tune hard for precision at the top of the results, because almost nobody reads page two, a fact worth remembering the next time you stop at result number three.

---

## Search After Generative AI

Since 2023, search has changed more than in the previous twenty years combined:

| Development | What It Means |
|-------------|---------------|
| **AI Overviews / AI Mode** | Google now generates an AI answer *above* the traditional links for many queries (rolled out broadly starting May 2024) |
| **Answer engines** | Tools like Perplexity and ChatGPT's search mode answer questions directly, citing (some) sources |
| **Zero-click search** | More searches end without anyone clicking a website, raising hard questions about who sustains the sites the AI learned from |
| **Multimodal search** | Search by image, voice, or by [humming a song](https://blog.google/products/search/hum-to-search/) |

### RAG: Where This Module Meets AI

The technique behind AI search is called **retrieval-augmented generation (RAG)**, and it is literally this module's two topics fused together:

1. **Retrieve**: A classic IR system (like the ones described above, often powered by the vector databases from Module 4) finds documents relevant to your question.
2. **Generate**: An AI language model writes an answer *based on those retrieved documents*.

This is why information retrieval concepts still matter in the ChatGPT era. When an AI gives a wrong answer, it's often an **IR failure**: the system retrieved the wrong documents, or none at all, and the model filled the gap by guessing. AI "hallucination" and bad search results are cousins.

:::{note} Discussion Point
When AI generates an answer instead of linking to sources, how do we verify accuracy? Who is responsible for errors? And what happens to the websites nobody clicks anymore?
:::

### 📌 Case Study: *United States v. Google*

The biggest tech antitrust case in a generation is about **search defaults**. In August 2024, a federal judge ruled that Google illegally maintained its search monopoly, largely through billions paid to be the default engine on phones and browsers. In September 2025 came the remedies: Google keeps Chrome and Android, but **exclusive default deals are banned** and Google must share certain search data with qualified competitors ([NPR](https://www.npr.org/2025/09/02/nx-s1-5478625/google-chrome-doj-antitrust-ruling)). Google is appealing.

*Why it belongs in this chapter:* everything you just learned (crawling, indexing, ranking, defaults, personalization) is what this case is about. Scale matters: whoever controls retrieval controls what billions of people find. *(Status as of mid-2026; check for appeal developments.)*

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

- Ask the same question to a traditional Google search, Google's AI Overview, and an answer engine like Perplexity. Compare: Which sources did each rely on? Which answer would you trust, and how would you check?

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
Two people searching the same term might get completely different results based on their location, search history, and browsing behavior. What are the implications for shared understanding? Does an AI-generated answer make this better, or just less visible?
:::

### SEO and SEM

| Term | Meaning |
|------|---------|
| **SEO** (Search Engine Optimization) | Improving a website to rank higher in organic results |
| **SEM** (Search Engine Marketing) | Paying for ads to appear in search results |

Understanding these helps you recognize what's organic vs. paid. (A new cousin has emerged: optimizing content so *AI systems* cite it, sometimes called "GEO," generative engine optimization.)

### 🗝️ Key Terms This Week

*Information retrieval · Crawling · Indexing · Ranking · TF-IDF · Semantic search · RAG · Hallucination · Filter bubble · SEO*: see the [Glossary](../glossary.md).

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

Spring Break is coming! After the break, we'll explore **Security & Privacy**: how to protect yourself and your data in the digital age.
