---
banner: images/module-07-banner.png
thumbnail: images/module-07-banner.png
---

# Module 7: Data Visualization & Infographics 📊

**Week 7 | Communicating with Data**

---

## The Big Picture

Have you ever looked at a spreadsheet full of numbers and felt your eyes glaze over? You're not alone! Raw data can be overwhelming, but when we transform it into visual form, patterns emerge, stories unfold, and insights become clear.

This week, we're diving into the art and science of **data visualization**. You'll discover why a well-designed chart can communicate in seconds what might take paragraphs to explain, and why a *poorly* designed one can mislead even the most careful reader.

### 🎯 What You'll Learn

- Why visualizations are powerful tools for communication
- How professionals design visualizations around a user's question, not just the data
- The difference between **infographics** and **data visualizations**
- How to recognize (and avoid!) misleading charts, including AI-generated ones
- The building blocks: charts, graphs, maps, and networks
- Hands-on practice creating your own visualizations

### 🧠 Big Questions to Consider

- When is a visualization more effective than words?
- How can the same data tell completely different stories?
- What responsibility do we have when creating visualizations?
- Now that AI can generate a chart from a sentence, who checks the chart?

---

## This Week's Journey

:::{note} Before Class
Complete the readings and videos below before our class session. Come ready to discuss what surprised you, confused you, or made you think differently!
:::

### 📚 Core Readings & Videos

| Resource | Type | Time | Notes |
|----------|------|------|-------|
| [A Short History of Data Visualisation](https://medium.com/data-science/a-short-history-of-data-visualisation-de2f81ed0b23) | Article | ~15 min | Where did this all begin? |
| [W.E.B. Du Bois's Data Visualizations](https://www.smithsonianmag.com/history/web-du-bois-visualized-black-experience-180976253/) | Article | ~10 min | Beautiful, powerful, and over 100 years old |
| [Chart Wars: The Political Power of Data Visualization](https://www.youtube.com/watch?v=N9Mqu2Hp2pg) | Video | ~18 min | How charts shape our political views |

### 🔍 Explore These Examples

Spend some time clicking around these galleries. Notice what catches your eye and what makes certain visualizations effective.

- [Information is Beautiful: Showcase](https://informationisbeautiful.net/visualizations/)
- [One Dataset, Visualized 25 Ways](https://flowingdata.com/2017/01/24/one-dataset-visualized-25-ways/)
- [Mapping Police Violence](https://mappingpoliceviolence.org/)
- [The Deadliest Animal in the World](https://www.gatesnotes.com/Health/Most-Lethal-Animal-Mosquito-Week)

### 🤔 Make You Think (Optional but Fascinating)

These go deeper into the ethics and challenges of visualization:

- [Graphics That Seem Clear Can Easily Be Misread](https://www.scientificamerican.com/article/graphics-that-seem-clear-can-easily-be-misread/) – Scientific American
- [It's Time for Data Visualizations to Be More Inclusive of Gender](https://www.poynter.org/reporting-editing/2021/its-time-for-data-visualizations-to-be-more-inclusive-of-gender-information/) – Poynter
- [Information Overload Helps Fake News Spread](https://www.scientificamerican.com/article/information-overload-helps-fake-news-spread-and-social-media-knows-it/) – Scientific American

---

## Start with the Question, Not the Data

Here is the most common beginner mistake in visualization: opening a dataset and asking "what charts can I make from this?" Professionals work in the opposite direction. Börner and Polley call this a **needs-driven workflow** (Börner & Polley 2014): the process begins with a *user* and an *insight need*, not with the data.

The workflow runs roughly like this:

1. **Identify the stakeholder and their question.** Who will look at this, and what decision or curiosity drives them? "The residence hall director wants to know when the laundry rooms are busiest" is a question; "I have laundry data" is not.
2. **Acquire and prepare the data** that can actually answer that question (and be honest when it can't).
3. **Analyze** using whichever of the five analysis types fits: statistical, temporal, geospatial, topical, or network (you'll meet these in [Types of Visualizations](visualization-types.md)).
4. **Design the visualization**, choosing encodings that make the answer visible at a glance.
5. **Deploy and interpret with the user**, then watch what they actually do with it.

```{figure} images/needs-driven-workflow.svg
:alt: Flowchart of the needs-driven visualization workflow in five steps. Step one, the question, asks who the stakeholder is and what they need to know. Step two acquires and prepares data that can answer it. Step three analyzes the data using statistical, temporal, geospatial, topical, or network analysis. Step four designs the visualization with encodings that make the answer visible. Step five deploys the visualization and interprets it with the user. A dashed arrow loops from step five back to step one, labeled "iterate: version one teaches you what version two should be."
:width: 100%
:name: fig-needs-driven-workflow

The needs-driven workflow starts with a person's question, not a dataset. The dashed arrow is the step beginners skip.
```

And then, almost always, you go around again. As Börner and Polley put it, information visualization is an **iterative process**. The first version of a chart teaches you what the second version should be: the stakeholder squints at a legend, asks a question the chart can't answer, or spots something you didn't expect (Tukey would be pleased). Treat version one as a conversation starter, not a deliverable.

Keep this workflow in mind through the whole module. Every technique in the following pages, from chart choice to color, is in service of step 1: someone's actual question.

---

## 🛠️ Tools of the Trade

Curious about what professionals use? Here are some industry-standard tools:

| Tool | Description |
|------|-------------|
| [Tableau](https://www.tableau.com/) | Industry-leading visualization platform |
| [Power BI](https://powerbi.microsoft.com/) | Microsoft's business intelligence tool |
| [Looker Studio](https://lookerstudio.google.com/) | Google's free reporting tool |
| [Datawrapper](https://www.datawrapper.de/) | Simple, clean chart creation (used by major newsrooms) |
| [Flourish](https://flourish.studio/) | Interactive data stories |
| **AI assistants** 🤖 | ChatGPT, Claude, and Copilot can now generate charts from a plain-language request |

:::{warning} AI-Generated Charts: Powerful, and Perilous
AI can produce a chart in seconds, and it can just as confidently produce the *wrong* chart: a misleading axis, a poor chart type, or in the worst case, **invented data**. AI-fabricated infographics with made-up statistics now circulate widely on social media. Everything you learn this week about honest visualization applies double when the chart came from a machine: check the axes, check the source, check the numbers exist. (You'll practice exactly this in the hands-on notebook.)
:::

Don't worry: we'll be using **Python** in this course, which is free and incredibly powerful. The [Hands-On Charts](hands-on-charts.ipynb) notebook will walk you through it step by step.

### ♿ Accessible Charts (Bridge to Module 5!)

Visualization has its own accessibility rules: don't encode meaning in color alone (about 1 in 12 men has some color-vision deficiency), use colorblind-safe palettes, write real alt text for charts, and make sure the takeaway survives in grayscale. A chart nobody can read isn't communication.

---

## 📝 This Week's Assignments

| Assignment | Due | Points |
|------------|-----|--------|
| Weekly Reflection (Module 7) | Friday by class | Part of Reflection grade |
| Continue: Research Questions | See syllabus | Part of research grade |

:::{tip} Reflection Prompt
For this week's reflection, focus on **one** of the readings above. Consider: How does visualization relate to the themes we've explored in informatics: the intersection of data, technology, and people? Include an image or visualization in your post that helps illustrate your point!
:::

---

## Module Contents

This module contains several sections:

1. **[Why Visualize Data?](why-visualize.md)** - The power and purpose of visualization
2. **[Types of Visualizations](visualization-types.md)** - Charts, graphs, maps, and networks
3. **[Infographics](infographics.md)** - Visualization for communication
4. **[Hands-On: Creating Charts](hands-on-charts.ipynb)** - Build your own visualizations with Python

---

## Let's Get Started!

Ready to see the world through a new lens? Start with [Why Visualize Data?](why-visualize.md) to understand the "why" behind data visualization, then explore the different [Types of Visualizations](visualization-types.md) you'll encounter in the wild.

When you're ready to get hands-on, the [Hands-On Charts](hands-on-charts.ipynb) notebook will guide you through creating your own visualizations (no prior coding experience required!).
