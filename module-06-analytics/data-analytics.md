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
- Review the statistics vocabulary that analysis is built on: variables, levels of measurement, samples, and populations
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

A useful working definition of data science: it combines math and statistics, programming, advanced analytics, artificial intelligence, and machine learning with subject-matter expertise to uncover actionable insights hidden in an organization's data. Data analysis, meanwhile, is the process of inspecting, cleaning, transforming, and modeling data with the goal of discovering useful information and supporting decision making. The two overlap heavily, and in smaller organizations one person often does both.

---

## The People Behind the Titles: Analyst vs. Scientist

The table above compares the *work*. What about the *jobs*? If you browse job postings (a genuinely useful habit even as a first-year student), you'll notice the two roles ask for different mixes of skills.

**A data analyst** spends most of the day close to the data itself. Surveys of employers repeatedly identify eight skills they want from analysts:

1. Data cleaning and preparation (often the majority of the job!)
2. Data analysis and exploration
3. Statistical knowledge
4. Creating data visualizations
5. Building dashboards and reports
6. Writing and communication
7. Domain knowledge (understanding the business or field the data comes from)
8. Problem solving

If you watch a "day in the life" video of a working analyst, you'll see a lot of meetings, a lot of Excel and SQL, and a lot of translating between "what the data says" and "what the marketing team asked." Analysts typically come from a wide range of backgrounds: business, economics, psychology, information science, and yes, informatics.

**A data scientist** does much of the above *plus* builds things that predict. A data scientist must be able to:

- Know enough about the organization to ask pertinent questions and identify pain points
- Apply statistics and computer science, along with business sense, to data analysis
- Use a wide range of tools for preparing and extracting data, from databases and SQL to data mining and integration methods
- Extract insights from big data using predictive analytics and AI, including machine learning, natural language processing, and deep learning
- Write programs that automate data processing and calculations
- Tell, and illustrate, stories that convey the meaning of results to decision makers at every level of technical understanding
- Collaborate with analysts, engineers, architects, and developers

| Aspect | Data Analyst | Data Scientist |
|--------|--------------|----------------|
| **Typical background** | Business, statistics, social science, informatics | Statistics, computer science, or a quantitative graduate degree |
| **Daily tools** | Excel, SQL, Tableau or Power BI | Python or R, SQL, machine learning libraries |
| **Core question** | "What does our data say happened?" | "What will happen, and can we build a system that acts on it?" |
| **Typical output** | Reports, dashboards, presentations | Models, algorithms, data products |

Neither role is "better." Analysts are often closer to real decisions; scientists are often closer to the engineering. Many people start as analysts and grow into data science as they add programming and modeling skills.

---

## A Statistics Refresher: The Vocabulary of Data

Before anyone can analyze data, they have to agree on what the pieces are called. **Statistics** is the study of how to collect, organize, analyze, and interpret numerical information from data. Four terms do most of the work:

- **Data**: pieces of carefully and precisely acquired information, formatted in a particular way
- **Individuals**: the people, objects, or instances represented in the data (each row in a spreadsheet, roughly)
- **Variables**: the attributes or features observed about each individual (each column)
- **Values**: what actually gets recorded for each individual on each variable

Values come in two broad flavors. **Quantitative** data is about numeric variables: height, price, number of followers. **Qualitative** (categorical) data records *types*, represented by a name, symbol, or code: your major, your phone's operating system, the color of a car.

### The Four Levels of Measurement (NOIR)

Statisticians classify variables into four levels of measurement, remembered by the acronym **NOIR**: Nominal, Ordinal, Interval, Ratio. This sounds like trivia, but it quietly determines which analyses and which charts are even *legal* for a given dataset.

| Level | What it is | Student-friendly examples | What you can do with it |
|-------|-----------|---------------------------|--------------------------|
| **Nominal** | Categories or labels with no natural order | Your major; favorite streaming service; jersey numbers | Count and compare frequencies. You cannot average majors. |
| **Ordinal** | Categories with a meaningful order, but unknown gaps between them | Class standing (first-year, sophomore, junior, senior); 1-to-5 star ratings; T-shirt sizes | Rank and compare order. The gap between 4 and 5 stars may not equal the gap between 1 and 2. |
| **Interval** | Numeric, with equal gaps between values, but no true zero | Temperature in Fahrenheit; calendar years; standardized test scores | Add and subtract meaningfully. But 80°F is *not* "twice as hot" as 40°F, because 0°F doesn't mean "no temperature." |
| **Ratio** | Numeric, with equal gaps *and* a true zero | Height; money; time spent studying; number of TikTok followers | Everything, including ratios: someone with 2,000 followers really does have twice as many as someone with 1,000. |

Why care? Because a lot of bad analysis comes from treating one level like another. Averaging star ratings treats an ordinal variable as interval (everyone does it, but it's technically on thin ice). Computing "average zip code" treats nominal as ratio (pure nonsense). When you meet a suspicious statistic, asking "what level of measurement is this variable, and does the math being done to it make sense?" is a surprisingly powerful filter.

### Describing vs. Inferring: Two Jobs for Statistics

There are two fundamentally different things you can do with statistics:

- **Descriptive analysis** summarizes and describes the data you actually have: averages, percentages, counts, spreads. "The average quiz score in this class was 84%."
- **Inferential analysis** uses a sample to draw conclusions about a larger group you *didn't* fully measure. "Based on a poll of 1,200 voters, we estimate 52% of the state supports the measure."

That distinction rests on two more terms:

- **Population**: the entire group you want to know about (all voters, all students, all customers)
- **Sample**: the smaller, hopefully representative group you actually collected data from

The accuracy of inferential statistics relies *heavily* on the sample being representative of the population. If a "student opinion" survey only reaches students who check email at 8 a.m., the inference is built on sand, no matter how fancy the math. This is exactly the selection bias you'll meet again later in this chapter.

Beyond these two, analysts sometimes distinguish further types: **predictive analysis** (use current and historical data to forecast future events), **causal analysis** (determine what happens to one variable when another is changed, usually requiring an experiment), and **mechanistic analysis** (understand exactly *how* changes in one variable produce changes in another). Each answers a stronger question than the last, and each requires stronger evidence.

### Correlation Is Not Causation

Here is the single most important sentence in this module: **two things moving together does not mean one causes the other.**

The classic example: ice cream sales and drowning deaths are strongly correlated. Months with high ice cream sales are months with more drownings. Does ice cream cause drowning? Obviously not. A third variable, summer weather, drives both: hot weather sends people to buy ice cream *and* sends people swimming. Summer is what statisticians call a **confounding variable** (or "lurking variable").

Whenever you see "A is linked to B," there are at least four possibilities:

1. A causes B
2. B causes A (the arrow points the other way)
3. Some hidden C causes both A and B
4. Coincidence (with enough variables, some will correlate by pure chance)

Establishing actual causation usually requires a controlled experiment, where you change one variable on purpose and hold everything else steady. Most of the data in the world comes from *observation*, not experiment, which is why honest analysts say "associated with" far more often than "causes." When a headline skips that caution, you now know what question to ask.

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

## Analytics in Your Daily Life

Analytics can feel abstract until you notice how much of your ordinary day is quietly shaped by it. Match these everyday encounters to the four types of analytics defined below (descriptive, diagnostic, predictive, prescriptive):

**Recommendations.** Every time Netflix suggests a show, Spotify builds you a playlist, or TikTok decides what's next on your For You page, a recommendation engine is at work. These systems are machine learning applied to your behavior: what you watched, skipped, replayed, and when. They're also a preview of this module's ethics questions, because the same engine that "knows what you like" is deciding what you never see.

**Predictions everywhere.** The weather forecast, the estimated arrival time in a maps app, a retailer stocking up before a holiday rush, a streaming service deciding which show to fund next: all predictive analytics, telling us what is *most likely* to happen based on previous data.

**Sports.** Modern professional sports run on analytics, from which shots are worth taking to which players are undervalued. The optional reading below on Liverpool FC shows data analysis helping win a Champions League.

**Logistics.** Why do UPS trucks famously avoid left turns? Because analysts modeled millions of routes and found that minimizing left turns saves fuel and time at massive scale (see the optional Big Think reading). One small insight, multiplied across a fleet, becomes millions of dollars.

**Prescriptions, not just predictions.** Prescriptive analytics goes one step further: run simulations of the possible options and recommend the best one. During clinical trials, for example, prescriptive methods can suggest which patient groups and testing methods are most likely to yield successful results.

One analyst described the raw material this way: data is like a pile of disjointed Lego pieces, or a jigsaw puzzle dumped on the table. Scattered, it makes little sense. Bring it together from various sources, put a framework around it, find the pattern, and suddenly you have a compelling story to tell. That framing skill, more than any single tool, is what this module is trying to build.

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
