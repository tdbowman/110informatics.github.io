# Types of Visualizations

Not all visualizations are created equal, and choosing the wrong type can confuse your audience or even misrepresent your data. Let's explore the most common types and when to use each.

## 🎯 In This Section

- Match common chart types to the questions they answer best
- Use a decision guide to pick the right visualization
- Spot the most common charting mistakes, human- and AI-made

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
