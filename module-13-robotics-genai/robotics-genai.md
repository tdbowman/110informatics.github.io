# Module 13: Robotics & Generative AI 🦾

**Week 13 | When AI Gets a Body (and an Agenda)**

---

## The Big Picture

We've seen AI that answers questions (Module 12) and vehicles that drive themselves (Module 11). This final content module looks at two frontiers where those threads converge: **robots** (AI embodied in the physical world) and **AI agents** (software that acts *for* you rather than only responding to you).

Both raise the same informatics question in its sharpest form yet: how much should we let systems *do things* on our behalf?

### 🎯 What You'll Learn

- Understand why physical robots are so much harder than chatbots
- Survey the current state of humanoid and industrial robotics
- Understand what "AI agents" are and how they differ from chatbots
- Consider the social and economic implications of embodied and agentic AI
- Connect the course's threads: data, systems, and society, one last time

### 🧠 Big Questions to Consider

- Why can AI write a sonnet but struggle to fold laundry?
- Would you let a robot care for a family member? Would you let an AI agent spend your money?
- Who is accountable when an autonomous *agent*, not a person, takes a harmful action?
- What does "human oversight" mean when systems act faster than humans can watch?

---

## Why Robots Are Hard: Moravec's Paradox

One of the strangest facts in AI is that the things humans find *hard* (chess, calculus, writing essays) turned out to be easy for machines, while the things toddlers find *easy* (walking, grasping a cup, folding a towel) remain frontier robotics problems. This is **Moravec's paradox**.

Roboticist Ken Goldberg's TED talk [Why Don't We Have Better Robots Yet?](https://www.ted.com/talks/ken_goldberg_why_don_t_we_have_better_robots_yet) is this week's anchor: the physical world is messy, unpredictable, and unforgiving of the small errors a chatbot gets away with. A hallucinated sentence is embarrassing; a hallucinated grip on a coffee mug is a mess; a hallucinated lane change is a tragedy.

---

## The State of Robotics *(as of mid-2026; expect this to age!)*

| Category | Where Things Stand |
|----------|--------------------|
| **Industrial & warehouse robots** | The quiet success story: over a million robots work in Amazon facilities alone; robotic arms dominate manufacturing |
| **Humanoid robots** | The hype frontier: Boston Dynamics' electric Atlas, Figure, Tesla's Optimus, and a wave of Chinese competitors (like Unitree) are racing toward general-purpose humanoids; the demos are impressive, but real deployments remain narrow pilots |
| **Robotaxis** | The proven case: Waymo's driverless service across ~10 metros (Module 11) |
| **Surgical & care robots** | Assistive rather than autonomous: robots steady surgeons' hands; eldercare robotics is a growing (and ethically loaded) field |
| **Generative AI in robotics** | The big shift: the same models behind chatbots are being used to let robots understand plain-language commands ("pick up the red cup") and learn tasks from video instead of hand-coded rules |

**Critical-eye exercise:** find a recent humanoid-robot demo video. What was *shown*? What was *claimed*? What was carefully not shown? (Remember the SAE-level lesson from Module 11: the gap between marketing and capability is where informatics thinking earns its keep.)

---

## AI Agents: Autonomy Without a Body

A **chatbot** answers your question. An **AI agent** pursues your *goal*: it can browse the web, fill out forms, write and run code, book appointments, or manage a workflow, taking many steps without asking permission for each one.

### The Autonomy Dial

Agents force a design decision you now have the vocabulary for (Modules 3, 11):

| Autonomy Level | Example |
|----------------|---------|
| **Suggest only** | "Here's a draft email; you send it" |
| **Act with confirmation** | "I found the flight. Book it? [Yes/No]" |
| **Act within limits** | "Book anything under $200 without asking" |
| **Fully autonomous** | The agent manages your inbox/calendar/purchases |

Every step down that table trades **oversight** for **convenience**. Where's your line? Does it move if the agent is 99% reliable? 99.9%?

### The Accountability Question

If your agent buys the wrong flight, whose mistake is it? Yours (you set it loose), the AI company's (their model erred), or the airline's website (it was confusing)? Courts and regulators are just beginning to face these questions. You'll recognize the pattern from Modules 9–11: *technology first, rules after*.

---

## 📌 Group Exercise: Design an Autonomous Agent

In groups, design an AI agent that acts on a user's behalf (not just a chatbot!). Work through:

1. **Tasks**: What does your agent do? What does it *never* do?
2. **Interaction**: How does the user direct it, and how do they interrupt it?
3. **Autonomy level**: Which rows of the autonomy dial apply to which actions? What requires confirmation?
4. **Trust & verification**: How does the agent show its work? How would a user catch its mistakes?
5. **Ethics**: Who could be harmed if it fails, or if it works exactly as designed? (Think beyond the user.)

Then find one *real* deployed agent or robot and grade it against your own framework. Present both to the class.

---

## This Week's Journey

### 📚 Readings & Videos

| Resource | Type | Notes |
|----------|------|-------|
| [Ken Goldberg: Why Don't We Have Better Robots Yet?](https://www.ted.com/talks/ken_goldberg_why_don_t_we_have_better_robots_yet) | TED Talk | This week's anchor |
| Current humanoid robotics coverage | Video/Article | Links on Canvas, refreshed each offering, because this field moves *fast* |
| [Hugging Face Spaces](https://huggingface.co/spaces) | Interactive | Try vision and robotics-adjacent models yourself |

### 🗝️ Key Terms This Week

*Robotics · Moravec's paradox · Humanoid robot · Embodied AI · AI agent · Agentic AI · Human-in-the-loop*; see the [Glossary](../glossary.md).

---

## 📝 This Week's Assignments

| Assignment | Due | Notes |
|------------|-----|-------|
| Weekly Reflection | Friday by class | Final reflection! |
| AI Journal | Due this week | Submit your complete journal + AI-generated podcast |
| Research Presentations | Next week | Final preparations: 6 minutes! |

:::{tip} Reflection Prompt
You've now spent a semester interacting with AI for your AI Journal. Based on that experience: would you delegate a real task to an AI agent: your email? your shopping? your calendar? Where exactly is your autonomy line, and what would move it?
:::

---

## Looking Ahead

Next week: **your** research presentations, and the [course wrap-up](../course-wrapup.md). Let's finish strong! 🎓
