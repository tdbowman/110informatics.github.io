# The Analysis Process, AI, and Bias

> "Garbage in, garbage out. Analysis is only as good as the data it's based on."

---

## 🎯 In This Section

- Walk through the six-step data analysis process, from Ask to Act
- Learn the data-quality questions every analyst should ask before trusting a dataset
- See what AI copilots can and can't do, and why statistical literacy matters more than ever
- Recognize four ways bias creeps into data, and how AI automates it
- Try beginner-friendly practice datasets yourself

---

## The Data Analysis Process

A widely-taught six-step framework (popularized by Google's Data Analytics Certificate):

1. **Ask**: Define the question you're trying to answer
2. **Collect**: Gather relevant data from various sources
3. **Clean**: Fix errors, handle missing values, standardize formats
4. **Analyze**: Apply statistical methods and explore patterns
5. **Visualize**: Create charts and graphs to communicate findings
6. **Act**: Make decisions based on insights

```{figure} images/data-analysis-process.svg
:alt: Flow diagram of the six-step data analysis process arranged in two rows. The top row flows left to right through step one, Ask, define the question; step two, Collect, gather relevant data; and step three, Clean, fix errors and missing values. An arrow drops to the bottom row, which flows right to left through step four, Analyze, apply statistics and explore patterns; step five, Visualize, create charts that communicate findings; and step six, Act, make decisions based on insights.
:width: 100%
:name: fig-data-analysis-process

Six steps from question to decision. The analysis itself is only one step, sandwiched between asking well and communicating clearly.
```

:::{warning} Data Quality
Remember: "Garbage in, garbage out." Analysis is only as good as the data it's based on. Always question:
- Where did this data come from?
- What's missing?
- What assumptions were made?
:::

---

## 🤖 The AI Copilot Era

The biggest change in this field since this course was first taught: **AI assistants can now do much of the mechanical work of analysis**. You can hand ChatGPT or Claude a spreadsheet and get charts and summaries in seconds; Microsoft Copilot lives inside Excel; Google's Gemini works in Sheets.

So is statistical literacy obsolete? Exactly the opposite:

| The AI can... | Only you can... |
|---------------|-----------------|
| Write the code to compute a correlation | Know that correlation isn't causation |
| Produce a confident-sounding summary | Notice the summary ignores missing data |
| Chart whatever you ask for | Ask whether it's the *right* question |
| Analyze the data it's given | Ask where the data came from and who's excluded |

AI copilots make analysis *faster*, including faster at being wrong. The analyst's job is shifting from writing code to **framing questions and verifying answers**. That's why the concepts in this module (bias, sampling, the analysis process) matter *more* in the AI era, not less.

**Try it:** Give an AI assistant a small dataset (like the practice datasets below) and ask for an analysis. Then fact-check it. What did it do well? Where did it overreach?

---

## Bias in Data

Data can perpetuate and amplify existing biases:

| Type of Bias | Description | Example |
|--------------|-------------|---------|
| **Selection Bias** | Data doesn't represent the full population | Surveys only in English exclude non-English speakers |
| **Historical Bias** | Past discrimination embedded in data | Criminal justice data reflecting biased policing |
| **Measurement Bias** | How data is collected affects results | Fitness trackers designed for one skin tone |
| **Algorithm Bias** | Model amplifies patterns including biased ones | Hiring algorithms that favor male applicants |

These biases don't disappear when AI does the analysis; they get *automated*. Every large AI model was trained on data collected by someone, somewhere, with all the gaps and biases that implies.

---

## Practice Datasets

Want to explore data analysis yourself? Try these beginner-friendly datasets:

| Dataset | Source | What You Can Explore |
|---------|--------|---------------------|
| Titanic | [Kaggle](https://www.kaggle.com/c/titanic) | Survival factors (we use this in the Module 7 notebook!) |
| Netflix Shows | [Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows) | Entertainment trends |
| World Happiness | [Kaggle](https://www.kaggle.com/unsdsn/world-happiness) | Quality of life factors |

---

## Up Next

That wraps the module's content pages. Head back to the [module overview](data-analytics.md) for this week's readings, reflection prompt, and assignments.
