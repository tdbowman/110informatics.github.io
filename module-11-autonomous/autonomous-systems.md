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
