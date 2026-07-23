# Analytics vs. Data Science

> "Data is like a pile of disjointed Lego pieces, or a jigsaw puzzle dumped on the table... find the pattern, and suddenly you have a compelling story to tell."

---

## 🎯 In This Section

- Compare data analytics ("what happened?") with data science ("what will happen?")
- Meet the people behind the titles: what analysts and data scientists actually do all day
- Spot descriptive, diagnostic, predictive, and prescriptive analytics in your everyday life
- Pick up the field's core vocabulary: big data, algorithms, machine learning, features, and models

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

```{figure} images/analytics-vs-data-science.svg
:alt: Venn diagram of two overlapping ellipses. The left, labeled Data Analytics, asks what happened and lists understanding past data, statistics and visualization, reports and dashboards, and tools like Excel, Tableau, and Power BI. The right, labeled Data Science, asks what will happen and lists predicting future outcomes, machine learning and AI, predictive models, and tools like Python, R, and machine learning libraries. The shared middle region lists SQL and data cleaning, statistical thinking, domain knowledge, and communicating results. A note underneath says that in smaller organizations one person often does both.
:width: 100%
:name: fig-analytics-vs-data-science

Analytics looks backward, data science looks forward, and the overlap (cleaning, statistics, domain knowledge, communication) is where most of the actual work lives.
```

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

## Analytics in Your Daily Life

Analytics can feel abstract until you notice how much of your ordinary day is quietly shaped by it. Match these everyday encounters to the four types of analytics defined below (descriptive, diagnostic, predictive, prescriptive):

**Recommendations.** Every time Netflix suggests a show, Spotify builds you a playlist, or TikTok decides what's next on your For You page, a recommendation engine is at work. These systems are machine learning applied to your behavior: what you watched, skipped, replayed, and when. They're also a preview of this module's ethics questions, because the same engine that "knows what you like" is deciding what you never see.

**Predictions everywhere.** The weather forecast, the estimated arrival time in a maps app, a retailer stocking up before a holiday rush, a streaming service deciding which show to fund next: all predictive analytics, telling us what is *most likely* to happen based on previous data.

**Sports.** Modern professional sports run on analytics, from which shots are worth taking to which players are undervalued. The optional reading on Liverpool FC (on the [module overview page](data-analytics.md)) shows data analysis helping win a Champions League.

**Logistics.** Why do UPS trucks famously avoid left turns? Because analysts modeled millions of routes and found that minimizing left turns saves fuel and time at massive scale (see the optional Big Think reading on the [module overview page](data-analytics.md)). One small insight, multiplied across a fleet, becomes millions of dollars.

**Prescriptions, not just predictions.** Prescriptive analytics goes one step further: run simulations of the possible options and recommend the best one. During clinical trials, for example, prescriptive methods can suggest which patient groups and testing methods are most likely to yield successful results.

One analyst described the raw material this way: data is like a pile of disjointed Lego pieces, or a jigsaw puzzle dumped on the table. Scattered, it makes little sense. Bring it together from various sources, put a framework around it, find the pattern, and suddenly you have a compelling story to tell. That framing skill, more than any single tool, is what this module is trying to build.

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

## Up Next

Before anyone can analyze data, they have to agree on what the pieces are called. Build that shared vocabulary in [Statistics Foundations](statistics-foundations.md).
