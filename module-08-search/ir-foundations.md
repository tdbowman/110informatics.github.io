# Information Retrieval Foundations

> "The problem of finding the right information is as old as information itself."

---

## 🎯 In This Section

- Learn what information retrieval (IR) is and how searching differs from browsing
- Climb the ladder of knowledge organization, from metadata to ontologies
- Understand why "relevant" depends on who's asking: system vs. user relevance
- Meet precision and recall, the two measures that score every search system

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

Long before web search, librarians and information scientists were solving the same problem: how do you organize information so someone can find it later? Their tools form a kind of ladder, from lightweight and informal at the bottom to rigorous and expensive at the top. Every modern system, including search engines and the AI tools later in this module, still leans on these ideas.

**Metadata** is the foundation: data about data. A song file's metadata includes its title, artist, album, and length; a photo's includes when and where it was taken; a library record describes a book's author, subject, and publisher. Search engines rely heavily on metadata because it provides context the raw content may not: a page's title, description, and language tell a crawler a great deal before it reads a single sentence.

**Synonym rings** solve the "many words, one meaning" problem: a group of terms treated as semantically equivalent for retrieval purposes. If "car," "auto," and "automobile" are ringed together, a search for one finds documents using any of them. Search engines automate this idea as *query expansion*, which you'll meet in [How Search Engines Work](how-search-engines-work.md); synonym rings are the curated, human-built version.

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

## Up Next

Now that you know what retrieval is and how knowledge gets organized for it, let's open the hood on the systems that do it at web scale: [How Search Engines Work](how-search-engines-work.md).
