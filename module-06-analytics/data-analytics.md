# Module 6: Data Analytics & Data Science 📊

**Week 6 | Making Sense of Data**

---

## The Big Picture

We generate a staggering amount of data every day. But raw data isn't useful on its own. Data analytics and data science transform this flood of information into insights that drive decisions.

This week, we explore how organizations extract meaning from data.

:::{warning} 🧟 Zombie Statistic Alert
You may have heard that humanity creates "2.5 quintillion bytes of data every day." That number traces back to an IBM marketing page from around 2017, and it has been copy-pasted ever since, usually with no date and no source. It's a perfect example of a **zombie statistic**: a number that keeps shambling around the internet long after its evidence died.

An informatics student's move: when you meet a dramatic statistic, ask *who measured it, how, and when?* (Current estimates of global data creation are tracked by firms like IDC, and they're wildly larger than the zombie number. The honest answer is "hundreds of zettabytes per year, and growing fast.")
:::

### 🎯 What You'll Learn

- Understand the difference between data analytics and data science
- Learn the data analysis process
- Explore how organizations use data to make decisions
- Consider the ethical implications of data-driven decision making
- Understand how AI copilots are changing analytical work, and why statistical literacy matters more than ever

### 🧠 Big Questions to Consider

- What can data tell us? What can't it tell us?
- How do biases in data lead to biased outcomes?
- Who benefits from data analysis? Who might be harmed?
- What's the difference between correlation and causation?
- If an AI can write the analysis code for you, what's left for the human to do?

---

## Data Science vs. Data Analytics

| Aspect | Data Analytics | Data Science |
|--------|----------------|--------------|
| **Focus** | Understanding past data | Predicting future outcomes |
| **Question** | "What happened?" | "What will happen?" |
| **Methods** | Statistics, visualization | Machine learning, algorithms |
| **Output** | Reports, dashboards | Predictive models |

Both are essential for turning raw data into actionable insights! And both remain strong career paths: the US Bureau of Labor Statistics projects data scientist employment to grow about **34% this decade**, among the fastest of any occupation ([BLS Occupational Outlook](https://www.bls.gov/ooh/math/data-scientists.htm)).

---

## The Data Analysis Process

A widely-taught six-step framework (popularized by Google's Data Analytics Certificate):

1. **Ask**: Define the question you're trying to answer
2. **Collect**: Gather relevant data from various sources
3. **Clean**: Fix errors, handle missing values, standardize formats
4. **Analyze**: Apply statistical methods and explore patterns
5. **Visualize**: Create charts and graphs to communicate findings
6. **Act**: Make decisions based on insights

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

## This Week's Journey

### 📚 Core Readings & Videos

| Resource | Type | Notes |
|----------|------|-------|
| [What Do Data Scientists Do?](https://www.youtube.com/watch?v=qrhRfPY4F4w) | Video | Overview of the field |
| [The Secret Data Collected by Dockless Bikes](https://www.technologyreview.com/2018/09/28/139983/the-secret-data-collected-by-dockless-bikes-is-helping-cities-map-your-movement/) | Article | MIT Technology Review on real-world data collection |
| [Data Scientists: Occupational Outlook](https://www.bls.gov/ooh/math/data-scientists.htm) | Reference | What the job actually pays and requires (BLS) |

### 🤔 Make You Think (Optional)

- [How Data (and Some Breathtaking Soccer) Brought Liverpool to the Cusp of Glory](https://www.nytimes.com/2019/05/22/magazine/soccer-data-liverpool.html) – NYT Magazine on sports analytics
- [The Science Behind Why UPS Trucks Avoid Making Left Turns](https://bigthink.com/technology-innovation/the-science-behind-why-ups-trucks-avoid-making-left-turns/) – Big Think on logistics optimization

---

## Key Concepts

### Types of Analytics

| Type | Question | Example |
|------|----------|---------|
| **Descriptive** | What happened? | Sales last quarter were $1.2M |
| **Diagnostic** | Why did it happen? | Sales dropped because of supply issues |
| **Predictive** | What will happen? | Next quarter sales will be $1.4M |
| **Prescriptive** | What should we do? | Increase inventory by 20% |

### Common Data Science Terms

- **Big Data**: Datasets too large for traditional processing
- **Algorithm**: A set of rules for solving a problem
- **Machine Learning**: Systems that learn from data
- **Feature**: A measurable property used in analysis
- **Model**: A mathematical representation of patterns in data

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

### 🗝️ Key Terms This Week

*Data analytics · Data science · Big data · Algorithm · Machine learning · Bias · Correlation vs. causation*: see the [Glossary](../glossary.md).

---

## 📝 This Week's Assignments

| Assignment | Due | Notes |
|------------|-----|-------|
| Weekly Reflection | Friday by class | Connect to data analytics concepts |

:::{tip} Reflection Prompt
Think about a decision you've seen made based on data (in news, at work, in your life). What data was used? What might have been missing? How could bias have affected the conclusions?
:::

---

## Looking Ahead

Next week, we explore **Data Visualization**: how to communicate data insights effectively through visual representations.
