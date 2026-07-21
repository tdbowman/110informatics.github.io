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
- See how games and simulation connect to robotics, AI, and informatics careers
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

## Games, Simulation, and Embodied AI 🎮

An unexpected thread runs through everything above: **video games**. The technology, the algorithms, and even the career paths of modern robotics and AI are tangled up with game development, and the connection runs in both directions.

### Game Engines as Robot Gyms

If the physical world is unforgiving of small errors (Moravec's paradox again), one solution is to practice somewhere errors are free. That somewhere is a **game engine**. Engines like Unity and Unreal, built to render believable worlds with realistic physics for players, turn out to be exactly what roboticists need: a simulated environment where a robot can attempt a task millions of times overnight, fail catastrophically, and reset instantly. Autonomous-vehicle companies drive billions of *simulated* miles for every real one, deliberately generating the rare nightmare scenarios (a child chasing a ball at dusk in the rain) that a real test fleet might encounter once a decade. Warehouse robots, robotic arms, and humanoids are increasingly trained the same way, in physics simulators that are, at bottom, video games with no human player. The approach even has a name, *sim-to-real transfer*, and its central problem, the "reality gap" between simulation and the messy world, is Moravec's paradox meeting you on the way out. Simulation is also where much of the safety work of Module 11 happens: you do not discover how a robotaxi handles a couch on the freeway by waiting for one.

### A Short History of Game AI (and Why It Matters)

Games have been AI's proving ground since before "AI" was a career. The ghosts in Pac-Man ran simple pursuit rules; decades of games since have driven real algorithmic advances that escaped into the wider world:

- **Pathfinding**: the A* search algorithm, the workhorse that moves every unit in every strategy game around every obstacle, is the same family of algorithms a warehouse robot or a Mars rover uses to plan a route. If you have watched a game character navigate a maze, you have watched robot motion planning.
- **Behavior trees**: game developers needed non-player characters (NPCs) whose behavior was complex but *debuggable*, so they organized decisions into hierarchical trees (if enemy visible → attack branch; else → patrol branch). Behavior trees jumped species and are now a standard control architecture in robotics.
- **Learned agents**: the modern era inverted the relationship. Instead of hand-authoring behavior, researchers train agents that *learn* to play, and games became the benchmark: checkers, then chess, then Go, then video games like StarCraft II, each a milestone on the road to the learning systems now steering physical robots. Games are ideal training grounds for the same reason they are ideal robot gyms: clear goals, fast feedback, and unlimited safe practice.

The through-line: the "game AI vs. modern AI" story is really the hand-coded-rules vs. learned-behavior story, the same shift described in the robotics table above.

### Generative AI Comes for Game Development

Game development is also one of the industries generative AI is transforming fastest, which makes it a compact case study of everything in Modules 10, 12, and 13:

- **Asset generation**: image and 3D models draft textures, concept art, and environment objects that once took artists weeks. Studios save time; artists ask the Module 10 questions about what those models trained on, and game platforms now wrestle with disclosure policies for AI-generated content.
- **Procedural content generation (PCG)**: algorithmically generating game worlds is actually decades old (the classic space-trading game *Elite* generated whole galaxies in the 1980s; *Minecraft* builds a unique world from a random seed). Generative AI supercharges the idea: instead of clever randomness within hand-built rules, models can generate levels, quests, and dialogue with semantic coherence.
- **NPC dialogue and agents**: the same language models behind chatbots are being wired into game characters, so NPCs can hold unscripted conversations and pursue goals. A game populated by such characters is, quite literally, a society of AI agents in a sandbox, which makes games a preview of the agent questions in the next section: what may an NPC-agent do, and who is accountable when it goes off script?

### The Careers Bridge

For informatics students, games are also an accessible on-ramp to nearly every skill this course has touched: interface design and user experience (Module 3), data structures and databases for game state (Module 4), accessibility (Module 5), analytics on player behavior (Module 6), and the AI and agent design of this module. You do not need to code to start: visual, drag-and-drop tools like Construct 3, GameMaker, and Stencyl let you build playable games by wiring up events, while free engines like Godot and Unity scale from beginner visual scripting to professional development. And "games industry" undersells where these skills lead: the same engine skills power architectural visualization, film effects, training simulators, digital twins of factories, and the robot gyms described above.

:::{tip} 🛠️ Try It: Design (and Build) a Game About This Course
Pick the course topic that interested you most this semester, and design a small game around it: trivia, puzzle, exploration, or story. First storyboard it: the start and ending, the main character(s), the obstacles, the rewards and penalties, and the environment. Then, if you want the full experience, build a playable slice in a beginner-friendly tool (Construct 3, GameMaker, Stencyl, or Godot; all have free tiers). It does not need to be finished, just playable for a few minutes.

Past student projects turned course concepts into escape-the-facility robot stories, data-heist stealth games, and time-traveling AI-ethics adventures. The design questions are the informatics questions: what does the player learn, what behavior do your reward rules actually encourage, and (if you add AI-driven characters) how much autonomy do you give them? Which brings us to agents.
:::

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
