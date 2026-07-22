# Search After Generative AI 🤖

> When the engine answers instead of linking, what do we gain, and what do we lose?

---

## 🎯 In This Section

- See how AI Overviews, answer engines, and zero-click search are reshaping the results page
- Understand retrieval-augmented generation (RAG), the fusion of this module's two topics
- Connect AI "hallucination" to plain old retrieval failure
- Follow *United States v. Google*, the antitrust case about who controls retrieval

---

## What Changed

Since 2023, search has changed more than in the previous twenty years combined:

| Development | What It Means |
|-------------|---------------|
| **AI Overviews / AI Mode** | Google now generates an AI answer *above* the traditional links for many queries (rolled out broadly starting May 2024) |
| **Answer engines** | Tools like Perplexity and ChatGPT's search mode answer questions directly, citing (some) sources |
| **Zero-click search** | More searches end without anyone clicking a website, raising hard questions about who sustains the sites the AI learned from |
| **Multimodal search** | Search by image, voice, or by [humming a song](https://blog.google/products/search/hum-to-search/) |

## RAG: Where This Module Meets AI

The technique behind AI search is called **retrieval-augmented generation (RAG)**, and it is literally this module's two topics fused together:

1. **Retrieve**: A classic IR system (like the ones described in [How Search Engines Work](how-search-engines-work.md), often powered by the vector databases from Module 4) finds documents relevant to your question.
2. **Generate**: An AI language model writes an answer *based on those retrieved documents*.

```{figure} images/rag-pipeline.svg
:alt: Diagram of retrieval-augmented generation. A user question flows to a retrieval step, which finds relevant documents from a search index or vector database. Those documents flow to a generation step, where an AI model writes an answer grounded in them, producing an answer with citations. A red dashed path warns that when retrieval fails, the model fills the gap by guessing, one source of hallucination.
:width: 100%
:name: fig-rag-pipeline

RAG is this module in one picture: classic information retrieval on the left, AI generation on the right — and hallucination is what leaks out when the left half fails.
```

This is why information retrieval concepts still matter in the ChatGPT era. When an AI gives a wrong answer, it's often an **IR failure**: the system retrieved the wrong documents, or none at all, and the model filled the gap by guessing. AI "hallucination" and bad search results are cousins.

:::{note} Discussion Point
When AI generates an answer instead of linking to sources, how do we verify accuracy? Who is responsible for errors? And what happens to the websites nobody clicks anymore?
:::

## 📌 Case Study: *United States v. Google*

The biggest tech antitrust case in a generation is about **search defaults**. In August 2024, a federal judge ruled that Google illegally maintained its search monopoly, largely through billions paid to be the default engine on phones and browsers. In September 2025 came the remedies: Google keeps Chrome and Android, but **exclusive default deals are banned** and Google must share certain search data with qualified competitors ([NPR](https://www.npr.org/2025/09/02/nx-s1-5478625/google-chrome-doj-antitrust-ruling)). Google is appealing.

*Why it belongs in this chapter:* everything you just learned (crawling, indexing, ranking, defaults, personalization) is what this case is about. Scale matters: whoever controls retrieval controls what billions of people find. *(Status as of mid-2026; check for appeal developments.)*

---

## Up Next

That wraps the module's content pages. Head back to the [module overview](search-and-retrieval.md) for this week's readings, reflection prompt, and assignments.
