# Robots, Games, and Embodied AI

> "A hallucinated sentence is embarrassing; a hallucinated grip on a coffee mug is a mess; a hallucinated lane change is a tragedy."

---

## 🎯 In This Section

- Meet Moravec's paradox: why AI aces chess but struggles to fold laundry
- Survey the state of robotics as of mid-2026, from warehouse arms to humanoid hype
- See how game engines double as "robot gyms" through sim-to-real transfer
- Trace game AI from Pac-Man's ghosts to the learned agents steering real robots
- Explore how generative AI is transforming game development, and where those skills lead

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

```{figure} images/sim-to-real-loop.svg
:alt: Diagram of sim-to-real transfer in three steps. First, a game engine such as Unity or Unreal simulates a world with realistic physics. Second, a robot practices at scale in that simulation, attempting tasks millions of times overnight, where failures are free and rare nightmare scenarios can be generated on demand. Third, the learned skills transfer to a physical robot in the real world. A warning arrow loops back from the real world to the simulator, labeled the reality gap: the messy physical world never quite matches the simulation, so robots return to training.
:width: 100%
:name: fig-sim-to-real-loop

Errors in a simulator are free; errors in the world are not, which is why every robot's road to reality now runs through what is, at bottom, a video game.
```

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
- **NPC dialogue and agents**: the same language models behind chatbots are being wired into game characters, so NPCs can hold unscripted conversations and pursue goals. A game populated by such characters is, quite literally, a society of AI agents in a sandbox, which makes games a preview of the agent questions in [AI Agents: Autonomy Without a Body](ai-agents.md): what may an NPC-agent do, and who is accountable when it goes off script?

### The Careers Bridge

For informatics students, games are also an accessible on-ramp to nearly every skill this course has touched: interface design and user experience (Module 3), data structures and databases for game state (Module 4), accessibility (Module 5), analytics on player behavior (Module 6), and the AI and agent design of this module. You do not need to code to start: visual, drag-and-drop tools like Construct 3, GameMaker, and Stencyl let you build playable games by wiring up events, while free engines like Godot and Unity scale from beginner visual scripting to professional development. And "games industry" undersells where these skills lead: the same engine skills power architectural visualization, film effects, training simulators, digital twins of factories, and the robot gyms described above.

:::{tip} 🛠️ Try It: Design (and Build) a Game About This Course
Pick the course topic that interested you most this semester, and design a small game around it: trivia, puzzle, exploration, or story. First storyboard it: the start and ending, the main character(s), the obstacles, the rewards and penalties, and the environment. Then, if you want the full experience, build a playable slice in a beginner-friendly tool (Construct 3, GameMaker, Stencyl, or Godot; all have free tiers). It does not need to be finished, just playable for a few minutes.

Past student projects turned course concepts into escape-the-facility robot stories, data-heist stealth games, and time-traveling AI-ethics adventures. The design questions are the informatics questions: what does the player learn, what behavior do your reward rules actually encourage, and (if you add AI-driven characters) how much autonomy do you give them? Which brings us to [agents](ai-agents.md).
:::

---

## Up Next

Robots give AI a body; agents give it an agenda. Continue to [AI Agents: Autonomy Without a Body](ai-agents.md).
