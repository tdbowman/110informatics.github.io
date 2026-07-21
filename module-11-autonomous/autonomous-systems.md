# Module 11: Autonomous Systems 🚗

**Week 11 | Machines That Operate Themselves**

---

## The Big Picture

From self-driving taxis to delivery drones, autonomous systems are reshaping our world. These technologies can perform tasks with little or no human intervention, but they also raise profound questions about safety, employment, and responsibility.

This week, we explore what autonomous systems are, how they work, and what they mean for society. And we'll examine a remarkable natural experiment: two companies that bet billions on the same technology and met opposite fates.

### 🎯 What You'll Learn

- Understand what makes a system "autonomous"
- Explore different areas where autonomous systems are used
- Learn how AI enables autonomous behavior
- Consider the ethical implications of autonomous systems
- Evaluate the benefits and risks of autonomous technology

### 🧠 Big Questions to Consider

- When is it safe to remove human control?
- Who is responsible when an autonomous system causes harm?
- How will autonomous systems affect employment?
- Why did one robotaxi company succeed where another collapsed?

---

## What Are Autonomous Systems?

**Autonomous systems** are technologies capable of performing tasks with little or no human intervention, using sensors, processors, and software to perceive, decide, and act.

### Automated, Autonomous, or "AI"? Three Words That Get Confused

These three terms get used interchangeably in headlines, but they name different things, and telling them apart is a genuinely useful skill:

- **Automated** systems execute a fixed procedure. A dishwasher, a traffic light on a timer, an assembly-line arm repeating one weld: each does exactly what it was programmed to do, every time, in a controlled environment. Surprise the system and it fails (or just keeps welding).
- **Autonomous** systems handle *uncertainty* without a human stepping in. The environment is not fully predictable, so the system must sense what is actually happening, decide among options, and act, adjusting as conditions change. A robot vacuum that maps your apartment and reroutes around the shoes you left out is (modestly) autonomous; a fan on a timer is merely automated.
- **AI** is a family of techniques (machine learning above all) that many autonomous systems use to achieve autonomy, but the terms are not synonyms. A chess program is AI with no autonomy in the physical world; an old thermostat has a sliver of autonomy (it senses and reacts) with no AI at all.

The working distinction: automation replaces human *muscle* on a known task, autonomy replaces human *judgment* on an uncertain one. That is why autonomy is the harder and more consequential step, and why this module's questions are mostly about judgment: whose, encoded how, accountable to whom?

You interact with simple sense-decide-act loops every day without noticing. A motion-sensor faucet senses your hands, decides water should flow, and actuates the valve. An elevator senses button presses and load, decides which floors to serve in which order, and actuates motors and doors. Once you see the pattern, you will find it everywhere.

### Why Build Autonomy at All? The Four D's

Roboticists have a shorthand for the tasks worth automating: the **dangerous, dull, dirty, and distant**.

- **Dangerous**: bomb disposal, mine inspection, disaster-zone search. Every task a robot does in a collapsed building is a task no firefighter has to.
- **Dull**: monitoring hundreds of security feeds, driving the same highway lane for eleven hours. Humans are terrible at sustained vigilance; machines never get bored, which is precisely why long-haul trucking is a leading target for autonomy.
- **Dirty**: sewer inspection, hazardous-waste handling, crop spraying.
- **Distant**: the clearest case for *full* autonomy. A rover on Mars cannot be remote-controlled in real time, because radio signals take roughly 4 to 24 minutes each way depending on the planets' positions. By the time a human driver on Earth saw the cliff edge, the rover would be over it. NASA's Curiosity and Perseverance rovers therefore drive themselves between waypoints: cameras and sensors perceive the terrain, onboard processing builds a local map and picks a safe path, and actuators (wheels, arms, drills) execute it, with humans setting goals rather than steering. Perseverance's self-driving system routinely covers hundreds of meters per day of hazard-strewn ground no human has ever seen up close.

Communication delay, hostile environments, and human fatigue are all versions of the same argument: sometimes the human *cannot* be in the loop, so the judgment has to ride along in the machine.

### Levels of Autonomy

The standard framework is SAE International's six levels of driving automation:

| Level | Description | Example |
|-------|-------------|---------|
| **0 - No Automation** | Human does everything | Traditional car |
| **1 - Driver Assistance** | System assists with one task | Cruise control |
| **2 - Partial Automation** | System controls multiple tasks, human must supervise | Tesla Autopilot / "Full Self-Driving (Supervised)" |
| **3 - Conditional Automation** | System handles most driving in certain conditions | Traffic jam pilot |
| **4 - High Automation** | System handles all driving in defined conditions | Waymo robotaxi |
| **5 - Full Automation** | System handles all driving in all conditions | Doesn't exist yet |

The marketing name of a product ("Full Self-Driving") and its actual SAE level (2, human must supervise) can be very different. Evaluating that gap between claim and capability is an informatics skill.

The same spectrum applies far beyond cars. A light switch is fully human-controlled; a thermostat is semi-autonomous (it acts on its own within parameters a human set); a Level-4 robotaxi senses, decides, and acts with nobody in the loop, inside a defined territory. Most systems you meet daily sit in the middle, and the interesting design question is always *where* on the spectrum a given task belongs, not whether autonomy is good or bad in general.

---

## 📌 Case Study: Waymo vs. Cruise (Same Bet, Opposite Outcomes)

Two companies spent billions building Level-4 robotaxis. As of mid-2026:

**Waymo** expanded methodically: safety drivers first, small geofenced areas, gradual growth. It now operates paid, fully driverless service in roughly **ten US metro areas** (Phoenix, San Francisco, LA, Austin, Atlanta, Miami, and several Texas cities), delivering hundreds of thousands of rides per week ([TechCrunch](https://techcrunch.com/2026/02/24/waymo-robotaxis-are-now-operating-in-10-us-cities/)).

**Cruise** (GM's robotaxi arm) raced to scale. In October 2023, one of its vehicles struck a pedestrian who had been thrown into its path by another car, and then *dragged her about 20 feet* while attempting to pull over. Regulators found Cruise had withheld the full video. California suspended its permits within weeks, and in December 2024 GM shut down the robotaxi program entirely, writing off roughly $10 billion.

**Tesla**, meanwhile, launched a small robotaxi service in Austin in June 2025, still operating at modest scale with safety monitors in many vehicles ([Electrek](https://electrek.co/2026/06/03/tesla-robotaxi-expands-entire-austin-metro-only-20-vehicles/)).

*The lesson here is not that "robotaxis are good" or "robotaxis are bad."* The lesson is that **trust is an engineering requirement**. Cruise's technology and Waymo's were comparable; what differed was safety culture, transparency with regulators, and pacing. One incident, handled badly, ended a $10 billion program. *(Status as of mid-2026.)*

---

## Areas of Autonomous Systems

| Area | Examples |
|------|----------|
| **Transportation** | Self-driving cars, trucks, ships, aircraft |
| **Robotics** | Manufacturing robots, surgical robots, warehouse robots |
| **Information Systems** | Automated trading, content moderation, AI agents (see Module 13!) |
| **Home Automation** | Smart thermostats, robot vacuums |
| **Agriculture** | Autonomous tractors, drones for crop monitoring |
| **Military** | Drones, autonomous weapons systems |

### Beyond the Robotaxi: Where Autonomy Is Quietly Winning

Robotaxis get the headlines, but the less glamorous deployments are often further along, because their environments are more controlled:

- **Agriculture** may be the most autonomous industry you never think about. GPS-guided tractors have steered themselves down crop rows for two decades; fully driverless models now plow and seed with no cab occupant, and John Deere sells autonomy as a product line. Overhead, camera-equipped drones survey fields and feed imagery to models that spot pest outbreaks, irrigation failures, and nutrient deficiencies plant-by-plant, enabling "precision agriculture": spraying the sick square meter instead of the whole field. A farm field is a great robotics environment: private land, no pedestrians, forgiving speeds.
- **Warehouses**: hundreds of thousands of robots shuttle shelves to human pickers in fulfillment centers, coordinated by fleet software that solves a continuous traffic-management problem. The humans and robots each do what they are best at; the choreography is the autonomy.
- **Mining**: enormous autonomous haul trucks have run around the clock at remote Australian iron mines for years. Dangerous, dull, dirty, *and* distant: the four D's in one industry, which is why mining adopted autonomy early.
- **Maritime**: crewless cargo vessels and autonomous ferries are in trials, and uncrewed survey ships already map the seafloor for weeks at a time.
- **Sidewalk delivery**: cooler-sized robots roll across many US college campuses delivering food, an example chosen because you can analyze one in person: watch how it handles a crowded crosswalk, and ask what it senses, what it decides, and when a remote human takes over.

The pattern across all five: autonomy arrives fastest where the environment is *structured* (fields, mines, warehouses) and slowest where it is chaotic (city streets). Uncertainty, again, is the whole game.

---

## How Autonomous Systems Work

### Key Components

| Component | Function | Example |
|-----------|----------|---------|
| **Sensors** | Detect/measure physical environment | Cameras, LIDAR, radar |
| **Actuators** | Move or control mechanisms | Motors, steering, brakes |
| **Control System** | Manages commands and behavior | Computer processors |
| **Algorithms** | Rules for decision-making | Path planning software |
| **Machine Learning** | Improves through experience | Object recognition |
| **Data Fusion** | Integrates multiple data sources | Combining sensor inputs |

### From Sensing to Acting: The Pipeline

Those components are not a parts list so much as a *pipeline*, a loop the system runs many times per second. Following one cycle through a self-driving car makes the architecture concrete:

1. **Perception**: raw sensor data becomes a description of the world. Cameras provide rich color imagery (good for reading signs and lane paint), radar measures speed and distance through rain and fog, and LIDAR sweeps lasers to build a precise 3D point cloud. **Data fusion** merges these overlapping, partly contradictory streams into one coherent picture: *that* cluster of points plus *that* camera blob is a cyclist, moving at 15 km/h. Fusion exists because every sensor fails somewhere (cameras at night, LIDAR in heavy rain), and the failures must not overlap.
2. **Localization and mapping**: the system answers "where exactly am I?" by matching what it perceives against a map, often one it is building or refining as it goes (roboticists call this SLAM, simultaneous localization and mapping). GPS alone is meters off; a car needs centimeters.
3. **Planning**: given the world-picture and a goal, the system chooses what to do, at several timescales at once: the route (which streets), the maneuver (change lanes now or after the intersection?), and the trajectory (the exact curve and speed for the next few seconds). Prediction lives here too: the planner has to anticipate what that cyclist will *probably* do next.
4. **Control**: the chosen trajectory becomes low-level commands to the actuators: steering angle, throttle, braking pressure, issued and corrected continuously.

Then the loop repeats. A Mars rover, a warehouse robot, and a robotaxi all run some version of this same perceive → localize → plan → act cycle; what differs is how messy each stage's problem is. And every stage can fail differently: perception can misclassify (a white truck against a bright sky), localization can drift, planning can freeze between bad options, control can respond too slowly. Safety engineering means asking "what happens next?" at each stage's failure, which is a good lens to bring to the readings below.

### AI in Autonomous Systems

AI enables autonomous systems to:

- **Perception**: Process sensor data to understand the environment
- **Decision-Making**: Make choices based on processed information
- **Learning**: Improve performance over time
- **Predictive Analysis**: Anticipate outcomes based on data
- **Adaptability**: Adjust to new or changing environments

---

## This Week's Journey

:::{note} Before Class
Choose at least ONE reading from the list below (links on Canvas). Come ready to discuss the implications!
:::

### 📚 Core Readings (Choose 1+; posted on Canvas)

| Resource | Topic |
|----------|-------|
| How a Self-Driving Uber Killed a Pedestrian in Arizona | The 2018 tragedy that first forced the accountability question |
| 'I'm the Operator': The Aftermath of a Self-Driving Tragedy | Human responsibility |
| Coverage of the Cruise incident and shutdown | The case study above, in depth |
| Waymo expansion reporting | [TechCrunch: Waymo in 10 cities](https://techcrunch.com/2026/02/24/waymo-robotaxis-are-now-operating-in-10-us-cities/) |
| Trucks Move Past Cars on the Road to Autonomy | Commercial applications |

### 🎥 Videos

- [Ken Goldberg: Why Don't We Have Better Robots Yet?](https://www.ted.com/talks/ken_goldberg_why_don_t_we_have_better_robots_yet) – TED talk on why physical autonomy is *hard*
- [Beyond Driverless Trucks: Building Autonomous EV Systems](https://www.youtube.com/watch?v=j69mhky2S_4)

:::{tip} 🛠️ Try It: The Autonomous Systems Hunt
Walk around campus (or your neighborhood, or a grocery store) and find five autonomous or semi-autonomous systems hiding in plain sight: automatic doors, motion-sensor lights and faucets, elevators, self-checkout kiosks, adaptive traffic signals, a robot vacuum. For each one, identify its **sensors**, its **actuators**, its **control logic**, and where it sits on the autonomy spectrum (human-controlled, semi-autonomous, fully autonomous). Then ask the ethics questions from this module: does it collect data about people? Could it treat some users differently? What happens when it fails? The exercise sounds trivial until you try the last question on an automatic door with a wheelchair user in mind.
:::

---

## The Six Challenges Every Autonomous System Faces

The Waymo/Cruise story is one instance of a general pattern. Whether the system is a robotaxi, a crop drone, or a surgical robot, deployment runs the same gauntlet of six challenge categories:

1. **Technical robustness**: handling the "long tail" of rare situations. Driving is easy 99% of the time; the last fraction of a percent (a couch on the freeway, a police officer waving traffic *through* a red light) is where a decade of engineering goes. A system that is 99.9% reliable still fails once per thousand encounters, and autonomy at scale means millions of encounters.
2. **Regulation**: rules written for human operators map badly onto machines, and they vary by state and country. Companies must navigate a moving patchwork, and (as Module 10's net-neutrality saga showed) the patchwork itself keeps shifting.
3. **Liability**: when a human driver crashes, insurance and courts know what to do. When a Level-4 vehicle crashes, is the fault the manufacturer's, the software supplier's, the fleet operator's, or the passenger's? Legal systems are working this out case by painful case.
4. **Public acceptance**: surveys consistently find most people hesitant to ride in driverless vehicles, and one vivid failure moves opinion more than a million quiet successes. Cruise's collapse was an acceptance failure as much as anything: not the crash itself, but the withheld video.
5. **Ethics**: value-laden choices get encoded in software, from the dramatic (harm tradeoffs) to the mundane-but-consequential (whose neighborhoods get served first, what data the sensors retain).
6. **Workforce**: the employment implications below, which arrive on a different timescale than the technology does.

Keep this list; it applies almost unchanged to the AI agents of Module 13.

---

## Ethical Considerations

### The Trolley Problem, Revisited

If an autonomous vehicle must choose between two harmful outcomes, how should it decide?

- Protect the passengers at all costs?
- Minimize total harm?
- Follow traffic laws regardless of consequences?

:::{warning} No Easy Answers
These decisions encode values into software. Who should make these choices? Engineers? Lawmakers? Society? (The *real* Cruise failure wasn't a trolley-problem edge case; it was organizational: what the company did *after* the crash. Ethics in autonomy is mostly about institutions, not just algorithms.)
:::

### Employment Implications

Autonomous systems could displace workers in:
- Transportation (trucking, taxi, delivery)
- Manufacturing
- Retail (automated stores)
- Agriculture

But they may also create new jobs in:
- System development and maintenance
- Supervision, monitoring, and remote assistance
- New industries we haven't imagined

### 🗝️ Key Terms This Week

*Autonomous system · SAE levels · Sensor · Actuator · LIDAR · Data fusion · Geofencing*: see the [Glossary](../glossary.md).

---

## 📝 This Week's Assignments

| Assignment | Due | Notes |
|------------|-----|-------|
| Weekly Reflection | Friday by class | Connect to autonomous systems |
| Research Presentation | Coming soon | Final preparations |
| Research Report | Due soon | See syllabus for date |

:::{tip} Reflection Prompt
Would you ride in a fully autonomous vehicle today? Does your answer change knowing the Waymo/Cruise story? What would need to be true, technically, legally, and institutionally, for you to trust these systems more (or less)?
:::

---

## Looking Ahead

Next week, we explore **Artificial Intelligence** more broadly: its capabilities, limitations, and implications for society.
