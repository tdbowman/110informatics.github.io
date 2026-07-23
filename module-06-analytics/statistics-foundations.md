# Statistics Foundations

> "Here is the single most important sentence in this module: two things moving together does not mean one causes the other."

---

## 🎯 In This Section

- Learn the four words statistics is built on: data, individuals, variables, and values
- Classify any variable with the four levels of measurement (NOIR), and see why it decides which math is legal
- Distinguish descriptive from inferential analysis, and populations from samples
- Understand why correlation is not causation, and how confounding variables fool us

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

```{figure} images/population-vs-sample.svg
:alt: Diagram of a large box labeled Population, containing a grid of dots representing the entire group you want to know about, and a smaller box labeled Sample containing the few highlighted dots you actually collected data from. A solid arrow from population to sample is labeled sampling, must be representative. A dashed arrow from sample back to population is labeled inference, conclusions about the whole group. Below, two cards define descriptive analysis as summarizing the data you actually have and inferential analysis as using a sample to draw conclusions about the population.
:width: 100%
:name: fig-population-vs-sample

Inference runs the arrow backward: you measure the few and conclude about the many, which only works if the few genuinely resemble the many.
```

The accuracy of inferential statistics relies *heavily* on the sample being representative of the population. If a "student opinion" survey only reaches students who check email at 8 a.m., the inference is built on sand, no matter how fancy the math. This is exactly the selection bias you'll meet again in [The Analysis Process, AI, and Bias](analysis-process-and-bias.md).

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

## Up Next

With the vocabulary in place, see how analysts actually put it to work, and where it breaks down, in [The Analysis Process, AI, and Bias](analysis-process-and-bias.md).
