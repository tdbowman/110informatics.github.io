# What Is AI and How Does It Work?

> "Most modern AI uses machine learning: systems that learn from data rather than following explicit rules."

---

## 🎯 In This Section

- Define artificial intelligence and meet its three types: narrow, general, and superintelligent
- See how machine learning differs from writing explicit rules by hand
- Compare the three ways machines learn: supervised, unsupervised, and reinforcement learning
- Tour the generative AI landscape, from LLMs and reasoning models to image generators and agents
- Connect LLMs back to Shannon's prediction experiment, vector databases, and RAG

---

## What is Artificial Intelligence?

**Artificial Intelligence (AI)** is the simulation of human intelligence by machines: systems that can learn, reason, and make decisions.

### Types of AI

| Type | Description | Status |
|------|-------------|--------|
| **Narrow AI** | Designed for specific tasks | Exists today (Siri, chess engines) |
| **General AI** | Human-level intelligence across all domains | Doesn't exist yet (though the debate over how close we are has become very loud) |
| **Superintelligent AI** | Exceeds human intelligence | Hypothetical/theoretical |

```{figure} images/types-of-ai.svg
:alt: Three cards on a spectrum from narrower to broader intelligence. Narrow AI, designed for specific tasks like Siri and chess engines, is marked exists today. General AI, human-level intelligence across all domains, is marked doesn't exist yet. Superintelligent AI, exceeding human intelligence, is marked hypothetical. An arrow underneath points toward broader, more general intelligence.
:width: 100%
:name: fig-types-of-ai

Every AI system you have ever used lives in the green box; the other two are still forecast and philosophy.
```

### Machine Learning

Most modern AI uses **machine learning**: systems that learn from data rather than following explicit rules.

| Approach | How It Works | Example |
|----------|--------------|---------|
| **Supervised Learning** | Learns from labeled examples | Spam detection |
| **Unsupervised Learning** | Finds patterns in unlabeled data | Customer segmentation |
| **Reinforcement Learning** | Learns through trial and error | Game playing |

```{figure} images/rules-vs-learning.svg
:alt: Diagram contrasting rule-based systems, where humans write explicit rules and the system only knows what it was told, with machine learning, where the system learns patterns from data. Below the machine learning card, three branches show the three approaches: supervised learning learns from labeled examples such as spam detection, unsupervised learning finds patterns in unlabeled data such as customer segmentation, and reinforcement learning learns through trial and error such as game playing.
:width: 100%
:name: fig-rules-vs-learning

The shift that defines modern AI: instead of hand-coding the rules, we let the system find them in data, in three different ways.
```

---

## The Generative AI Landscape

**Generative AI** creates new content: text, images, music, code, and more. *(Landscape as of mid-2026. This table ages faster than any other page in this book; treat checking it as an exercise!)*

| Technology | What It Does | Examples |
|------------|--------------|---------|
| **Large Language Models (LLMs)** | Generate and understand text | ChatGPT (OpenAI), Claude (Anthropic), Gemini (Google), Llama (Meta, open-weight) |
| **Reasoning Models** | LLMs that "think step by step" before answering, making them much stronger at math, science, and planning | Newer versions of the models above |
| **Image & Video Generators** | Create images and video from text descriptions | DALL-E, Midjourney, Stable Diffusion, Sora |
| **Code Assistants** | Write and explain code | GitHub Copilot, Claude Code |
| **AI Agents** | Go beyond answering to *act*: browse, book, buy, and complete multi-step tasks | The frontier, covered in Module 13 |
| **Voice Synthesis** | Create realistic speech | ElevenLabs |

Remember Module 1? LLMs are Shannon's next-word prediction experiment made industrial, and Module 4's vector databases plus Module 8's RAG are how they're connected to real knowledge.

---

## Up Next

Now that you know what AI is and how it learns, the harder questions: what could go wrong, and who gets to decide? Continue to [AI Ethics, Law, and Policy](ai-ethics-law-policy.md).
