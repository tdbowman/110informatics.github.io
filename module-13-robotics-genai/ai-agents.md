# AI Agents: Autonomy Without a Body

> "A chatbot answers your question. An AI agent pursues your *goal*."

---

## 🎯 In This Section

- Learn what makes an AI agent different from a chatbot
- Step through the autonomy dial, from suggest-only to fully autonomous
- Weigh the trade every agent design makes: oversight for convenience
- Confront the accountability question: whose mistake is the agent's mistake?
- Design your own autonomous agent, then grade a real one against your framework

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

```{figure} images/autonomy-dial.svg
:alt: Diagram of the autonomy dial as four levels from left to right. Level one, suggest only: the agent drafts, the human acts, for example a draft email you send yourself. Level two, act with confirmation: the agent asks before each action, for example booking a flight only after a yes. Level three, act within limits: the agent acts freely inside preset bounds, for example booking anything under two hundred dollars without asking. Level four, fully autonomous: the agent runs the whole workflow, such as managing your inbox, calendar, and purchases. A two-headed arrow underneath shows that moving right trades oversight for convenience.
:width: 100%
:name: fig-autonomy-dial

Each step to the right hands the agent more of your judgment. The dial sets what the agent may do and how much of its work you will ever see.
```

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

## Up Next

That wraps the module's content pages. Head back to the [module overview](robotics-genai.md) for this week's readings, reflection prompt, and assignments.
