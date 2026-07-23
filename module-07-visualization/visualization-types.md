# Types of Visualizations

Not all visualizations are created equal, and choosing the wrong type can confuse your audience or even misrepresent your data. Let's explore the most common types and when to use each.

## 🎯 In This Section

- Match common chart types to the questions they answer best
- Learn a professional framework for classifying visualizations (Börner & Polley 2014)
- Understand graphic variables: the raw ingredients every chart is built from
- Use a decision guide to pick the right visualization
- Spot the most common charting mistakes, human- and AI-made

---

## A Framework Before the Zoo

Before touring individual chart types, it helps to have a map of the territory. In *Visual Insights*, Katy Börner and David Polley offer a practical framework used by professional visualization designers (Börner & Polley 2014). Their starting observation: visualizations can be grouped by the user's insight needs, by task type, or by the kind of data being visualized. In other words, classify by the *question*, not just the picture.

### Three Levels of Analysis: Micro, Meso, Macro

One axis of the framework is scale. How much of the world are you looking at?

| Level | Scale | Rough size | Example |
|-------|-------|-----------|---------|
| **Micro** | Individual level | Small datasets, up to about 100 records | One student's study hours across a semester |
| **Meso** | Group level | Up to about 10,000 records | All INF 110 sections over a decade |
| **Macro** | Global or population level | Beyond 10,000 records | Every course enrollment in US higher education |

Treat these cutoffs as **conventions, not laws of nature**. Nobody's chart breaks when a dataset hits record 101. The point is that different scales call for different designs: at micro scale you can label every data point by name; at macro scale individual points dissolve into density, and your job becomes showing the shape of the whole. Some of the most interesting visualizations deliberately connect levels, letting you see the population pattern and then zoom to your own dot in it.

### Five Types of Analysis

The other axis is the *kind of question* you're asking. Börner and Polley identify five, and almost any data question you'll ever ask falls into one (or a combination):

**1. Statistical analysis** asks "how much, how many, how do these compare?" It profiles a dataset: distributions, averages, outliers, correlations. Its natural visualizations are the workhorse charts: bar charts, histograms, box plots, scatter plots. Example: a histogram of exam scores showing that the class splits into two clusters.

**2. Temporal analysis** asks "when, and how is it changing?" Time is the organizing dimension. Its signature visualization is the line graph, along with timelines and area charts. Example: a line graph of a city's average temperature across 50 years, making a warming trend visible as a slope.

**3. Geospatial analysis** asks "where?" Data is anchored to physical locations using latitude and longitude. Its visualizations are maps: choropleth maps, dot maps, heat maps. Example: John Snow's cholera map (which you'll meet again below), where *where* the deaths were was the entire discovery.

**4. Topical analysis** asks "what is this about?" It works on text and themes: what topics appear, how often, and how they relate. Its visualizations include word clouds, topic maps, and thematic landscapes. Example: a map of thousands of research papers where papers on similar subjects cluster together, revealing the structure of a scientific field.

**5. Network analysis** asks "who or what is connected to whom?" The data is relationships. Its visualization is the network graph: nodes and edges. Example: a graph of who follows whom in a friend group, instantly revealing who bridges otherwise separate circles.

When you face a new dataset, running through this list ("is my question statistical? temporal? spatial? topical? relational?") does half the chart-choosing work for you. The decision guide later in this page is really this framework in disguise.

---

## Graphic Variables: The Alphabet of Charts

Every chart, no matter how fancy, is built from a small alphabet of visual encodings that Börner and Polley call **graphic variable types**:

- **Position**: where a mark sits along the x, y, or z axis
- **Form**: the mark's size and shape
- **Color**: its hue (which color), value (how light or dark), and saturation (how intense)
- **Texture**: pattern, orientation, or density of fill
- **Optics**: crispness, transparency, shading

A scatter plot is just position twice. A bubble chart adds size. A choropleth map is position (geographic) plus color value. Once you see charts as combinations of these ingredients, you can read unfamiliar visualizations by decoding one variable at a time.

The crucial fact: **we do not read all graphic variables equally well.** Decades of perception research (the same tradition as Ware's work in the previous section) give a rough accuracy ranking:

1. **Position** on a common scale (most accurate: this is why scatter plots and dot plots work so well)
2. **Length** (bar charts live here)
3. **Angle and slope** (pie chart slices; line steepness)
4. **Area** (bubble sizes: people consistently misjudge these)
5. **Color value and saturation** (fine for showing "more vs. less," bad for exact values)
6. **Color hue** (great for *categories*, nearly useless for *quantities*)

This ranking explains most chart advice you'll ever hear. "Prefer bar charts to pie charts" is just "length beats angle." "Don't encode quantity with rainbow colors" is just "hue can't carry numbers." Design isn't about decorating data; it's about spending your most accurate encodings on your most important variables.

---

## The Big Five

### 📊 Charts (Bar, Column, Pie)

**Best for**: Comparing categories or showing parts of a whole

| Type | Use When... |
|------|-------------|
| **Bar Chart** | Comparing values across categories (horizontal orientation good for long labels) |
| **Column Chart** | Similar to bar, but vertical; works well for time-based categories |
| **Pie Chart** | Showing proportions of a whole (**use sparingly!** Hard to compare slices accurately) |

:::{tip} Pro Tip
Pie charts are often overused. If you have more than 5-6 categories, or if the slices are similar in size, consider a bar chart instead; it's much easier to compare lengths than angles!
:::

---

### 📈 Line Graphs

**Best for**: Showing change over time (trends)

Line graphs connect data points to emphasize continuity and direction. They're perfect for:
- Stock prices over months
- Temperature changes through a day
- Website traffic over a year

:::{warning} When NOT to use
Don't use line graphs for categorical data that doesn't have a natural order. A line connecting "apples" to "oranges" to "bananas" implies a progression that doesn't exist!
:::

---

### 📋 Tables

**Best for**: Precise values and detailed comparisons

Sometimes the best visualization is... not a visualization at all. Tables shine when:
- Exact numbers matter more than patterns
- You have a small amount of data
- Your audience needs to look up specific values

| Quarter | Sales | Growth |
|---------|-------|--------|
| Q1 2024 | $1.2M | +12% |
| Q2 2024 | $1.4M | +17% |
| Q3 2024 | $1.3M | -7% |
| Q4 2024 | $1.6M | +23% |

---

### 🗺️ Geospatial Maps

**Best for**: Data with a geographic component

Maps use our intuitive understanding of physical space to display data. Types include:

- **Choropleth maps**: Regions colored by value (e.g., election maps)
- **Dot maps**: Individual points on a map (e.g., store locations)
- **Heat maps**: Density of occurrences (e.g., crime hotspots)

:::{note} Real-World Example
Remember John Snow's 1854 cholera map? By plotting deaths on a London street map, he discovered they clustered around a contaminated water pump, a breakthrough in epidemiology that came from visualization.
:::

---

### 🕸️ Network Graphs

**Best for**: Relationships and connections

Network graphs show how things are connected. Nodes represent entities, and edges (lines) represent relationships.

Common uses:
- Social networks (who follows whom)
- Organizational structures
- How websites link to each other
- Character relationships in literature

---

## Choosing the Right Visualization

Here's a quick decision guide. Ask yourself: **"What's my goal?"**

- **Comparison?** → Bar/Column Chart
- **Composition (parts of a whole)?** → Pie Chart or Stacked Bar
- **Distribution?** → Histogram or Box Plot
- **Relationship between variables?** → Scatter Plot or Network
- **Location-based data?** → Map

```{figure} images/chart-chooser.svg
:alt: Decision guide for choosing a visualization, fanning out from a starting question, "What's my goal?", to eight goal-and-chart pairings. Comparing values across categories points to a bar or column chart. Showing change over time points to a line graph. Showing parts of a whole points to a pie chart with under six parts or a stacked bar. Seeing a distribution points to a histogram or box plot. A relationship between variables points to a scatter plot. Geographic patterns point to a map. Connections or networks point to a network graph. Presenting exact values points to a table.
:width: 100%
:name: fig-chart-chooser

Chart choice starts with your goal, not your data: name the question first and the chart type mostly picks itself.
```

### Quick Reference Table

| Your Goal | Suggested Chart Type |
|-----------|---------------------|
| Compare values across categories | Bar or column chart |
| Show change over time | Line graph |
| Display parts of a whole | Pie chart (if <6 parts) or stacked bar |
| Show geographic patterns | Map |
| Reveal relationships between variables | Scatter plot |
| Display connections/networks | Network graph |
| Present exact values | Table |

---

## Common Mistakes to Avoid

| Mistake | Why It's a Problem |
|---------|-------------------|
| ❌ **Too Many Colors** | Using rainbow palettes makes it hard to distinguish categories. Stick to 3-5 colors max. |
| ❌ **Unlabeled Axes** | Never assume your audience knows what the numbers mean. Label everything! |
| ❌ **Missing Context** | A chart without a title, source, or date leaves readers guessing. |
| ❌ **Chartjunk** | 3D effects, unnecessary icons, and decorative elements distract from the data. |
| ❌ **Color-Only Encoding** | If the meaning disappears in grayscale, colorblind readers never had it. Use position, shape, or labels too. |

:::{note} ♿ Accessible Charts
Everything from Module 5 applies to charts: use colorblind-safe palettes (search "ColorBrewer"), never rely on color alone to carry meaning, write alt text that states the chart's *takeaway* (not just "a bar chart"), and check that text is readable at a glance. Accessibility is part of choosing the right visualization, not an afterthought.
:::

---

## Activity: Chart Detective 🔍

Look at the visualizations you encounter today in news articles, social media, or apps. For each one, ask:

1. What type of visualization is this?
2. Is it the right choice for this data?
3. What story is it trying to tell?
4. Is anything confusing or potentially misleading?

**Bonus round** 🤖: Ask an AI assistant to create a chart from some data you give it (or the quarterly sales table above). Then play detective on the *AI's* chart with the same four questions, plus one more: did it choose the chart type you would have? AI tools often default to the wrong chart type or add misleading styling; catching that is the skill.

Share an interesting example in this week's reflection!

---

## Next Up

We've covered traditional data visualizations, but there's a special category designed specifically for communication: [Infographics](infographics.md). Let's explore what makes them different.
