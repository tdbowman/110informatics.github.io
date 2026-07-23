# Thinking in Systems

> "A system is a set of parts that interact to produce something none of the parts could produce alone."

---

## 🎯 In This Section

- Pick up the habit of mind called systems thinking: study the connections, not just the parts
- Meet the six components of an information system, from hardware to people
- See why "the system is down" is sometimes a people or procedures problem in disguise
- Trace how cloud computing and GPUs rewrote the hardware story
- Watch infrastructure change a science in the bioinformatics spotlight

---

Before we dive into [cables and data centers](how-the-internet-works.md), we need a habit of mind: **systems thinking**. A system is a set of parts that interact to produce something none of the parts could produce alone. Your body is a system; so is a university, a supply chain, and the internet. Systems thinking means resisting the urge to study parts in isolation and instead asking how the parts connect, where the feedback loops are, and what happens elsewhere in the system when you change one piece.

Systems thinking matters in informatics because information technologies never operate alone. A hospital's records software fails or succeeds based on the nurses who type into it, the procedures that govern it, and the network it runs on. When we look at the internet this week, we'll see the same lesson at planetary scale: your ability to stream a video depends on an unbroken chain of parts, from the chip in your phone to a cable on the ocean floor, and a failure anywhere in the chain is a failure for you.

## The Six Components of an Information System

Textbooks on information systems, such as Stair and Reynolds' *Principles of Information Systems*, break any information system into six interacting components. Every one of them has to work for the system to work:

| Component | What it is | Example in a campus course system |
|-----------|-----------|----------------------------------|
| **Hardware** | The physical devices that process, store, and move data | Servers, laptops, phones, network switches |
| **Software** | The programs that tell hardware what to do | Canvas, the database engine behind it, your browser |
| **Data** | The raw facts the system stores and processes | Grades, submissions, due dates, rosters |
| **Procedures** | The rules and steps people and machines follow | How assignments are submitted, how grades are entered, backup schedules |
| **People** | Everyone who builds, runs, and uses the system | Students, instructors, IT staff, developers |
| **Networks / Telecommunications** | The connections that let components communicate | Campus Wi-Fi, the university network, the internet itself |

```{figure} images/six-components.svg
:alt: Diagram of the six components of an information system arranged in two groups. Hardware, software, and networks form the technical half; data, procedures, and people form the human half. Arrows from all six components feed into a single box labeled one working information system, noting that when the system is down the culprit may be people or procedures rather than technology.
:width: 100%
:name: fig-six-components

Only half of an information system is technology: data, procedures, and people are load-bearing components too.
```

Two observations. First, only half of these components are technological; data, procedures, and people are just as essential as hardware and software, which is why "the system is down" is sometimes a people problem or a procedures problem wearing a technical disguise. Second, networks earn their place as a separate component because modern systems are *distributed*: the hardware running Canvas is not on your campus, and without telecommunications the other five components could never find each other.

## Hardware, Then and Now

The hardware component deserves a closer look, because it has changed dramatically. The classic categories still apply: **input devices** (keyboards, touchscreens, microphones, sensors), **processing devices** (the central processing unit, or CPU), **storage** (drives and memory), and **output devices** (screens, speakers, printers). But two modern additions matter enormously.

The first is **cloud computing**: instead of owning servers, organizations rent computing power and storage from providers like Amazon Web Services, Microsoft Azure, and Google Cloud, which run it in the giant data centers we study this week. "The cloud" is a comforting metaphor for what is really *someone else's hardware, somewhere else*, reachable only through networks.

The second is the rise of **GPUs and other accelerators**. Graphics processing units were designed to draw video-game imagery, but their talent for doing thousands of simple calculations at once turned out to be exactly what machine learning needs. Today's AI boom is, at the hardware level, a GPU boom: the data centers making headlines are being filled with racks of accelerator chips, and access to them has become a strategic resource for companies and countries alike.

:::{note} 🔬 Spotlight on Bioinformatics: Infrastructure Meets Biology
Want proof that hardware, software, data, and people can change a science? Consider bioinformatics. For fifty years, predicting how a protein folds into its 3D shape was one of biology's grand challenges. Then DeepMind's AlphaFold system, trained on decades of shared protein data using massive GPU infrastructure, essentially solved it, releasing predicted structures for hundreds of millions of proteins. In 2024, the Nobel Prize in Chemistry went to David Baker for computational protein design and to Demis Hassabis and John Jumper of DeepMind for AlphaFold. A chemistry Nobel awarded largely for software and data is a milestone worth pausing on: careers in bioinformatics now sit exactly at the data-systems-society intersection this course is about, and the field is hiring.
:::

---

## Up Next

You now have the systems lens. Time to point it at the largest system humans have ever built: [How the Internet Works](how-the-internet-works.md).
