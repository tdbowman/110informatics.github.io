# Evaluating Interfaces & Design Ethics

> "Studying good design and studying manipulation turn out to be the same curriculum read in opposite directions."

---

## 🎯 In This Section

- Use Nielsen's ten usability heuristics as a fast, cheap interface checklist
- Walk an interface step by step with the **cognitive walkthrough**'s four questions
- See why emotion steers cognition, and why usable-but-flat designs lose
- Confront the new design questions raised when the interface is a conversation with an AI
- Recognize **deceptive patterns** and the ten-figure legal consequences of using them

---

## Nielsen's Usability Heuristics

Jakob Nielsen, co-founder (with Don Norman) of the Nielsen Norman Group, distilled decades of usability research into ten heuristics: broad rules of thumb for good interface design ([Nielsen Norman Group](https://www.nngroup.com/articles/ten-usability-heuristics/)):

1. Visibility of system status
2. Match between system and real world
3. User control and freedom
4. Consistency and standards
5. Error prevention
6. Recognition rather than recall
7. Flexibility and efficiency of use
8. Aesthetic and minimalist design
9. Help users recognize and recover from errors
10. Help and documentation

The heuristics echo everything in [Understanding Users](understanding-users.md). "Visibility of system status" is Norman's feedback. "Match between system and real world" is designing to users' mental models. "Recognition rather than recall" respects the limits of human memory: showing options is kinder than making people remember commands. Evaluators use these heuristics as a checklist when reviewing an interface, a method called heuristic evaluation, which is fast and cheap because it doesn't require recruiting users.

## The Cognitive Walkthrough

Heuristic evaluation is one way to judge an interface without users; the **cognitive walkthrough** is another, and it's more focused. In a cognitive walkthrough, one or more evaluators work through a series of realistic tasks while asking questions from the user's perspective at every single step.

The method has a preparatory phase (choose the users to simulate, the tasks to test, and the exact sequence of correct actions) and an analysis phase, where the evaluators walk each step asking, in effect:

1. The user sets a goal to be completed within the system. *Will the user know what to try to do at this point?*
2. The user determines the currently available actions. *Will they see that the correct action is available?*
3. The user selects the action they think will move them toward the goal. *Will they connect the correct action with what they're trying to do?*
4. The user performs the action and evaluates the system's feedback. *Will they understand from the feedback whether they made progress?*

```{figure} images/cognitive-walkthrough.svg
:alt: Diagram of the four steps of a cognitive walkthrough, repeated for every step of every task. Step one, the user sets a goal: will the user know what to try to do? Step two, the user scans available actions: will they see that the correct action is available? Step three, the user selects an action: will they connect it with their goal? Step four, the user acts and reads the feedback: will they know they made progress? A red box below notes that a "probably not" answer at any step means a usability problem has been found before a single real user got confused.
:width: 100%
:name: fig-cognitive-walkthrough

Four questions asked at every single step: any "probably not" is a usability problem caught before it ever reaches a real user.
```

If the answer at any step is "probably not," you've found a usability problem, and you found it before a single real user got confused. The cognitive walkthrough is especially good at catching problems for first-time users, because it forces the evaluator to abandon their expert knowledge and simulate a newcomer's mental model, step by step.

## Affective Computing

**Affective computing** is computing that relates to, arises from, or deliberately influences emotion or other affective phenomena. The field, pioneered at the MIT Media Lab, studies systems that can detect emotion (from your face, voice, or typing rhythm) and systems that express or respond to it. UX focuses on the human side of this equation rather than the computing side, and it cares about emotion in two directions:

- **Emotions as consequences of product use**: how a product makes you feel during and after use
- **Emotions as antecedents of use and judgments**: how the mood you bring to a product changes what you do and how you evaluate it

Why does emotion matter so much in design? Because emotion is not decoration on top of "real" cognition; it steers cognition. A frustrated user stops exploring, blames themselves, and remembers the product bitterly. A delighted user forgives small flaws, tries more features, and tells friends. Emotion also arrives first: people form aesthetic and emotional judgments of an interface in a fraction of a second, long before they've evaluated whether it actually works. And emotion is what turns interactions into *experiences* (recall the [experiential perspective](design-thinking-and-ux.md)): the moments you remember from technology are the ones that made you feel something. A design that is usable but emotionally flat is a design that will be replaced by one that is both.

## Designing With (and For) AI

A new frontier for UX: when the interface is a chat box or a voice, most of Norman's visual vocabulary disappears. Designers of AI products wrestle with new questions:

- **Discoverability**: How does a user know what an AI assistant *can* do? (There are no buttons to see!)
- **Feedback & trust**: How should a system communicate *confidence*, and admit when it might be wrong?
- **Signifiers for the invisible**: What cues tell you content is AI-generated?
- **Agency**: When an AI acts on your behalf, how much control should you keep?

Try applying Nielsen's heuristics to an AI chatbot you've used; you'll find several are surprisingly hard to satisfy. Mental models make this even trickier: most users' models of how AI works are borrowed from search engines or from science fiction, and both lead to predictable mistakes about what the system can and cannot be trusted to do.

---

## Value-Sensitive Design

Design isn't neutral: it embeds values. Consider:

- **Who benefits** from design decisions?
- **Who is excluded** by design choices?
- **What behaviors** does the design encourage or discourage?
- **What assumptions** does the design make about users?

:::{warning} Deceptive Patterns (formerly "Dark Patterns")
Some designs intentionally manipulate users; the field now calls these **deceptive patterns**. Examples include:
- Trick questions in forms
- Hidden costs revealed at checkout
- Difficult unsubscribe or cancellation processes
- Shame-based opt-outs ("No thanks, I don't want to save money")

This debate has moved beyond design ethics and into law. The FTC sued Amazon over its Prime enrollment and cancellation flow (the internally-named "Iliad" process), and in September 2025 Amazon settled for **\$2.5 billion**: a \$1 billion penalty plus \$1.5 billion in customer refunds ([FTC](https://www.ftc.gov/news-events/news/press-releases/2025/09/ftc-secures-historic-25-billion-settlement-against-amazon)). In the EU, the Digital Services Act now explicitly bans deceptive interface design. Design decisions have consequences, sometimes ten-figure ones.
:::

There's a useful connection here to everything in this module: deceptive patterns work precisely by *weaponizing* the concepts in this module. They exploit users' mental models (making a paid option look like the only option), corrupt signifiers (making the "decline" link tiny and gray), and abuse emotional design (using shame or urgency to rush decisions). Studying good design and studying manipulation turn out to be the same curriculum read in opposite directions, which is exactly why designers carry real ethical responsibility.

### 📌 Case Study Box

Pick one pattern from [deceptive.design](https://www.deceptive.design/) and find a live example in an app or site you use. What value is the design serving: yours, or the company's? *(Swap in a fresh enforcement case each year; there will be one.)*

---

## Up Next

That wraps the module's content pages. Head back to the [module overview](design-thinking.md) for this week's readings, reflection prompt, and assignments.
