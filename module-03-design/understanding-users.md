# Understanding Users: Sense-Making & Norman's Principles

> "Users act on their beliefs about how a system works, not on how it actually works."

---

## 🎯 In This Section

- Meet Brenda Dervin's **sense-making** and the "gap" every user is trying to bridge
- Learn what **mental models** are and why flawed ones still drive every decision users make
- Master Don Norman's five concepts: affordance, signifier, feedback, mapping, and constraints
- Understand why shoving a "Norman door" is the design's failure, not yours

---

## How People Make Sense of Information

Before we talk about designing technology, it helps to understand what people are doing when they use it. A useful starting point is **sense-making**, a concept developed by communication researcher Brenda Dervin. Sense-making describes human experience as an active, socially rooted process of creating meaning out of the information problems, discontinuities, and disconnections we run into in daily life.

The core image in Dervin's methodology is a **gap**. You are moving through your day and something changes: your usual route is closed, an app updates its layout, a professor assigns a tool you've never used. Suddenly there is a gap between what you know and what you need to know, and you have to build a bridge across it. The questions you ask, the searches you run, and the people you turn to are all bridge-building materials. Meaning, in this view, is not something you passively receive; it is something you construct, negotiate, and revise through interaction with the world.

```{figure} images/sense-making-gap.svg
:alt: Diagram of Dervin's sense-making metaphor. On the left, a card labeled "Your situation" holds what you know now. On the right, a card labeled "Your goal" holds what you need to know. Between them is a gap, and a bridge spans it, built from the questions you ask, the searches you run, and the people you turn to. A note underneath says good design meets people at their gaps.
:width: 100%
:name: fig-sense-making-gap

Dervin's gap: every user arrives mid-journey, and the questions, searches, and people they turn to are the materials they bridge it with.
```

Why does this matter for design? Because every user who opens your app arrives mid-journey, standing at some gap, trying to get somewhere. Good design meets people at their gaps. It asks: what situation is this person in, what are they trying to accomplish, and what would actually help them move forward? Bad design assumes everyone arrives with the same knowledge, the same goal, and the same patience.

### Mental Models

Closely related to sense-making is the idea of a **mental model**: your internal explanation of how something works in the world. A mental model is a representation of a system, the relationships between its parts, and your intuitive sense of what your own actions will cause it to do. You have a mental model of how your refrigerator works, how a search engine finds results, and how "the cloud" stores your photos. Some of those models are quite accurate. Others are wildly wrong, and that's normal, because mental models are built from experience, not from engineering diagrams.

Researchers describe mental models in several ways (Westbrook, 2006, offers a helpful overview and a preliminary study of how library users model information systems):

| Perspective | What it emphasizes |
|-------------|-------------------|
| **Reason-centered** | We use models to infer relationships, predict outcomes, understand systems, and decide what actions to take |
| **Physically-centered** | We carry limited internal diagrams of physical processes (how water flows through pipes, how heat moves) |
| **Socio-cognitive** | Our models are shaped by social context, personal situation, and emotion, not just logic |

The design lesson is fundamental: **users act on their beliefs about how a system works, not on how it actually works.** If a user believes the trash can icon deletes files instantly, they will hesitate to use it even if there's an undo. If a user believes an AI chatbot "looks things up" the way a search engine does, they will trust its answers in ways the system may not deserve. Westbrook's study found that users' models of information systems were often fragmentary and mistaken, yet those flawed models still drove every decision the users made. Great designers don't fight mental models; they discover what models users already hold and either design to match them or gently teach a better one.

:::{tip} Try This
Ask a friend to explain, in their own words, what happens between hitting "send" on a text message and it appearing on someone else's phone. You'll hear a mental model. Is it accurate? Does it need to be?
:::

---

## Don Norman: The Design of Everyday Things

Don Norman is a pioneer in design thinking. His key concepts:

| Concept | Definition |
|---------|------------|
| **Affordance** | The relationship between object properties and user capabilities that suggests how something can be used |
| **Signifier** | Visual cues that communicate how something works |
| **Feedback** | Communication about the results of an action |
| **Mapping** | The relationship between controls and their effects |
| **Constraints** | Limitations that guide proper use (including cultural constraints) |

> "Design is concerned with how things work, how they are controlled, and the nature of the interaction between people and technology." — Don Norman

These five ideas are easiest to grasp through everyday objects, which is exactly why Norman wrote about doors, faucets, and stovetops rather than software.

**Affordances** are about the relationship between an object and a person. A flat metal plate on a door affords pushing; there is simply nothing to grab. A vertical handle affords grasping and pulling. A chair affords sitting for an adult but might afford climbing for a toddler; affordances depend on the user's capabilities, not just the object.

**Signifiers** are the perceivable clues that communicate the affordance. The word "PUSH" engraved on a plate is a signifier. So is the shading on a button that makes it look pressable. The famous **Norman door** is a door whose signifiers contradict its affordances: it has a graspable pull handle, but it only opens if you push. When you shove a pull door or yank a push door, you haven't failed; the design has. (The Vox video in [this week's resources](design-thinking.md) shows this delightfully.)

**Feedback** tells you your action registered. An elevator button that lights up, a phone that vibrates on a tap, a progress bar that fills: all feedback. Systems with no feedback leave users jabbing buttons repeatedly; systems with delayed feedback make users doubt themselves.

**Mapping** describes how controls relate to their effects. A stovetop where the four knobs are arranged in the same spatial pattern as the four burners has natural mapping; you never turn on the wrong burner. A stovetop with four knobs in a straight row makes you read tiny labels every time.

**Constraints** prevent errors before they happen. A SIM card that only fits its slot one way is a physical constraint. A form that grays out the "Submit" button until required fields are filled is a logical constraint. Cultural constraints work too: you know red means stop without being told.

Once you learn these five concepts, you cannot unsee them. Every frustrating interaction you have this week is a failure of one of them.

---

## Up Next

Now that you can see users' gaps and mental models, let's look at the process designers use to meet them there: [Design Thinking & the UX Family](design-thinking-and-ux.md).
