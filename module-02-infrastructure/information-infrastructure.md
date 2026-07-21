# Module 2: Information Infrastructure & Society 🏗️

**Week 2 | Technology Embedded in Society**

---

## The Big Picture

Have you ever wondered where the internet actually *lives*? Spoiler: it's not floating in a cloud. The internet is physical infrastructure: cables, data centers, routers, and satellites that span the globe.

This week, we explore the massive technological infrastructure that makes our connected world possible, and consider its consequences for society.

### 🎯 What You'll Learn

- Understand that technology and infrastructure exists and has consequences at multiple levels
- Acknowledge the importance of thinking of informatics as an intersection between information, people, and technology
- Recognize the environmental, economic, and social costs of digital infrastructure
- Consider the digital divide and its implications for equity

### 🧠 Big Questions to Consider

- What is the environmental cost of our digital lives?
- Who has access to technology, and who doesn't?
- How does physical infrastructure shape digital possibilities?
- What happens when the infrastructure fails?

---

## Thinking in Systems

Before we dive into cables and data centers, we need a habit of mind: **systems thinking**. A system is a set of parts that interact to produce something none of the parts could produce alone. Your body is a system; so is a university, a supply chain, and the internet. Systems thinking means resisting the urge to study parts in isolation and instead asking how the parts connect, where the feedback loops are, and what happens elsewhere in the system when you change one piece.

Systems thinking matters in informatics because information technologies never operate alone. A hospital's records software fails or succeeds based on the nurses who type into it, the procedures that govern it, and the network it runs on. When we look at the internet this week, we'll see the same lesson at planetary scale: your ability to stream a video depends on an unbroken chain of parts, from the chip in your phone to a cable on the ocean floor, and a failure anywhere in the chain is a failure for you.

### The Six Components of an Information System

Textbooks on information systems, such as Stair and Reynolds' *Principles of Information Systems*, break any information system into six interacting components. Every one of them has to work for the system to work:

| Component | What it is | Example in a campus course system |
|-----------|-----------|----------------------------------|
| **Hardware** | The physical devices that process, store, and move data | Servers, laptops, phones, network switches |
| **Software** | The programs that tell hardware what to do | Canvas, the database engine behind it, your browser |
| **Data** | The raw facts the system stores and processes | Grades, submissions, due dates, rosters |
| **Procedures** | The rules and steps people and machines follow | How assignments are submitted, how grades are entered, backup schedules |
| **People** | Everyone who builds, runs, and uses the system | Students, instructors, IT staff, developers |
| **Networks / Telecommunications** | The connections that let components communicate | Campus Wi-Fi, the university network, the internet itself |

Two observations. First, only half of these components are technological; data, procedures, and people are just as essential as hardware and software, which is why "the system is down" is sometimes a people problem or a procedures problem wearing a technical disguise. Second, networks earn their place as a separate component because modern systems are *distributed*: the hardware running Canvas is not on your campus, and without telecommunications the other five components could never find each other.

### Hardware, Then and Now

The hardware component deserves a closer look, because it has changed dramatically. The classic categories still apply: **input devices** (keyboards, touchscreens, microphones, sensors), **processing devices** (the central processing unit, or CPU), **storage** (drives and memory), and **output devices** (screens, speakers, printers). But two modern additions matter enormously.

The first is **cloud computing**: instead of owning servers, organizations rent computing power and storage from providers like Amazon Web Services, Microsoft Azure, and Google Cloud, which run it in the giant data centers we study this week. "The cloud" is a comforting metaphor for what is really *someone else's hardware, somewhere else*, reachable only through networks.

The second is the rise of **GPUs and other accelerators**. Graphics processing units were designed to draw video-game imagery, but their talent for doing thousands of simple calculations at once turned out to be exactly what machine learning needs. Today's AI boom is, at the hardware level, a GPU boom: the data centers making headlines are being filled with racks of accelerator chips, and access to them has become a strategic resource for companies and countries alike.

:::{note} 🔬 Spotlight on Bioinformatics: Infrastructure Meets Biology
Want proof that hardware, software, data, and people can change a science? Consider bioinformatics. For fifty years, predicting how a protein folds into its 3D shape was one of biology's grand challenges. Then DeepMind's AlphaFold system, trained on decades of shared protein data using massive GPU infrastructure, essentially solved it, releasing predicted structures for hundreds of millions of proteins. In 2024, the Nobel Prize in Chemistry went to David Baker for computational protein design and to Demis Hassabis and John Jumper of DeepMind for AlphaFold. A chemistry Nobel awarded largely for software and data is a milestone worth pausing on: careers in bioinformatics now sit exactly at the data-systems-society intersection this course is about, and the field is hiring.
:::

---

## Technology Isn't Cost Neutral

Technology comes with costs that involve:
- **Energy**: Data centers consume enormous amounts of electricity
- **Physical Resources**: Rare earth minerals, water for cooling, land
- **Infrastructure**: A vast technological network spanning the globe
- **Social Changes**: Shifts in how we work, communicate, and live

:::{important} 📌 Case Study: The AI Data Center Boom
The rise of generative AI has turned data centers into front-page news. Training and running AI models requires enormous computing power, and the International Energy Agency projects that global data centre electricity use could roughly double by 2030, approaching the annual electricity consumption of Japan ([IEA, *Energy and AI*](https://www.iea.org/reports/energy-and-ai/energy-demand-from-ai)). Communities across the US are now debating the water, power, land, and noise costs of proposed AI campuses ([Pew Research: energy use at U.S. data centers](https://www.pewresearch.org/short-reads/2025/10/24/what-we-know-about-energy-use-at-us-data-centers-amid-the-ai-boom/)).

*Discussion:* Every AI answer you get has a physical footprint somewhere. Who bears those costs, and who reaps the benefits? *(Case study current as of mid-2026; check for newer figures!)*
:::

---

## This Week's Journey

:::{note} Before Class
Complete the readings and videos below. Pay attention to the *physical* nature of the internet!
:::

### 📚 Core Readings & Videos

| Resource | Type | Notes |
|----------|------|-------|
| [Bridging the Digital Divide](https://www.pbs.org/video/bridging-the-digital-divide-36dhyl/) | Video (26 min) | PBS documentary on access inequality |
| [Inside the New York 'Hotels' Where the Internet Lives](https://time.com/4276215/internet-hotels/) | Photo Essay | TIME feature with Peter Garritano's photos of carrier hotels |
| [Chicago's Data Fortress for the Digital Economy](https://www.datacenterknowledge.com/business/chicago-s-data-fortress-for-the-digital-economy) | Article | 350 E. Cermak, one of the world's largest carrier hotels, right here in Chicago |
| [What we know about energy use at U.S. data centers](https://www.pewresearch.org/short-reads/2025/10/24/what-we-know-about-energy-use-at-us-data-centers-amid-the-ai-boom/) | Article | Pew Research on the AI-era energy question |

### 🗺️ Explore: Internet Maps

- [40 Maps That Explain the Internet](https://www.vox.com/a/internet-maps)
- [Submarine Cable Map](https://www.submarinecablemap.com/) – Telegeography
- [Infrapedia](https://www.infrapedia.com/) – Infrastructure mapping

### 🤔 Make You Think (Optional)

- [Impact of the Digital Divide](https://ctu.ieee.org/impact-of-the-digital-divide-economic-social-and-educational-consequences/) – IEEE
- [The Case for Investing in Digital Public Infrastructure](https://hbr.org/2023/05/the-case-for-investing-in-digital-public-infrastructure) – Harvard Business Review
- [Experts Say the 'New Normal' in 2025 Will Be Far More Tech-Driven](https://www.pewresearch.org/internet/2021/02/18/experts-say-the-new-normal-in-2025-will-be-far-more-tech-driven-presenting-more-big-challenges/) – Pew Research. **Time-capsule exercise:** these predictions were made in early 2021, *about a year the world has now lived through*. Which predictions held up? Which missed completely? What does that teach us about forecasting technology?

---

## Key Concepts

### The Physical Internet

The internet is made of:

| Component | Description |
|-----------|-------------|
| **Submarine Cables** | Fiber optic cables crossing ocean floors carrying 99% of intercontinental data |
| **Data Centers** | Massive facilities housing servers (some use as much electricity as small cities) |
| **Internet Exchange Points** | Physical locations where networks connect and exchange traffic |
| **Cell Towers & Satellites** | Wireless connections to end users |
| **Last Mile Infrastructure** | The connection from the network to your home |

### What Is the Internet, Really?

The word "internet" is a compressed history lesson: it comes from *inter-network*, a network of interconnected networks. No single organization owns or runs it. Instead, thousands of independent networks (universities, companies, internet service providers, governments) agree to speak the same protocols and pass traffic to one another. High-speed data lines called the **internet backbone** carry traffic over long distances, and smaller networks connect to the backbone, which lets a user on any small network reach any other connected location on Earth.

The design is deliberately **redundant**: there are many possible paths between any two points, so if a cable is cut or a router fails, traffic reroutes around the damage. That resilience is inherited from the internet's Cold War era ancestry, and it is why the internet as a whole almost never goes down even though pieces of it fail constantly. Today this network of networks is the foundation for nearly all of computing: the web, apps, streaming, gaming, cloud services, and AI all ride on top of it.

### Packets: How Data Travels

The internet's core trick is **packet switching**. When you send anything (an email, a photo, a video call), your device does not open a dedicated line to the destination the way old telephone systems did. Instead, the data is chopped into small chunks called **packets**, typically around a thousand bytes each. Every packet is stamped with the address it's going to and the address it came from, then launched into the network to find its own way. Different packets from the same photo may take entirely different routes, and they may arrive out of order. At the destination, they are reassembled into the original file.

Why do it this way? Efficiency and resilience. Packets from millions of users can share the same cables, interleaved, with no one hogging a dedicated line. And if a route fails mid-transfer, later packets simply take a different path. When you watch a video "buffer," you are watching packet delivery fall behind playback; when it recovers, the network has found its flow again.

### The Journey of a Click

Trace what happens when you tap a link on your phone or laptop at home:

1. **Your device** builds a request. Its **network interface card (NIC)**, the hardware that speaks network protocols, hands the request to your local network.
2. **Your local area network (LAN)** carries it, either over an Ethernet cable or over Wi-Fi (a brand name for wireless networking based on the IEEE 802.11 standards).
3. **Your router and modem** pass the request out of your home: the router directs traffic between your LAN and the outside world, and the modem translates the signal for the physical line (cable, fiber, or DSL) that leaves your building.
4. **Your internet service provider (ISP)** receives the request and forwards it through its network toward the backbone.
5. **Backbone networks and exchange points** relay the packets, hop by hop, router by router, possibly across a submarine cable, to the data center where the destination server lives.
6. **The server** (or more likely a farm of servers) receives the reassembled request, prepares a response (the web page, the video chunk), and sends it back as packets, which retrace a path to your screen.

The whole round trip routinely completes in under a couple hundred milliseconds. Every element in that chain is physical, owned by someone, powered by electricity, and capable of failing. Keep this journey in mind while you look at this week's data center photo essays: you are looking at steps 5 and 6.

### DNS: The Internet's Phone Book

There's a missing step in the journey above. You typed a *name* (like `example.com`), but packets are addressed to *numbers*. The **Domain Name System (DNS)** is the internet's phone book: a globally distributed directory that translates human-friendly domain names into machine-usable IP addresses. Before your request can go anywhere, your device quietly asks a DNS server, "what is the address for this name?" and gets back a number to stamp on its packets.

DNS is a hierarchy: root servers know who manages each top-level domain (`.com`, `.org`, `.edu`), those registries know which name servers handle each domain, and so on down. Because DNS sits in front of everything, it is also a pressure point: when a major DNS provider has an outage, huge swaths of the web become unreachable at once, even though the servers themselves are fine. The names stop resolving, and unresolvable is indistinguishable from offline.

### IP Addresses: Numbering Every Device

Every device on the internet needs a unique address to send and receive packets. That address is an **Internet Protocol (IP) address**. The original scheme, **IPv4**, uses four numbers (like `172.16.254.1`), which allows about 4.3 billion unique addresses. That sounded limitless in the 1980s; it stopped being enough once phones, TVs, cars, and doorbells all wanted addresses. The world has effectively run out of fresh IPv4 addresses, and networks stretch the supply with workarounds like sharing one public address among many home devices.

The long-term fix is **IPv6**, which uses eight groups of hexadecimal digits and provides 2^128 addresses: roughly 340 undecillion, or 340 trillion trillion trillion. That is enough to give every grain of sand on Earth its own address many times over. The two systems run side by side today, and the decades-long transition between them is a lesson in how hard it is to renovate infrastructure that can never be turned off.

### TCP and IP: A Division of Labor

You'll constantly see the abbreviation **TCP/IP**, the protocol pair at the heart of the internet since 1983. They are two separate protocols with a clean division of labor:

- **IP (Internet Protocol)** handles *addressing and routing*: it defines the addresses that identify every device and gets individual packets forwarded, hop by hop, toward their destination. IP makes no promises; packets can arrive late, out of order, or not at all.
- **TCP (Transmission Control Protocol)** handles *reliability*: it establishes a connection between sender and receiver, numbers the packets so they can be reassembled in the correct order, confirms what arrived, and retransmits anything that got lost.

A useful analogy: IP is the postal address system plus the trucks; TCP is a meticulous shipping clerk who numbers every box, tracks confirmations, and re-sends missing ones. The genius of the design is that the network's middle stays simple and dumb (routers just forward packets) while the intelligence lives at the edges, in the sending and receiving devices. That "dumb middle" is a big part of why the internet could grow without central coordination and why new applications can be invented without asking anyone's permission.

### Internet, Intranet, Extranet

Not every network that behaves like the internet *is* the internet:

| Network | Who can access it | Typical use |
|---------|-------------------|-------------|
| **Internet** | Anyone, globally | Public web, email, apps, everything |
| **Intranet** | Members of one organization only | Internal documents, HR portals, staff tools |
| **Extranet** | An organization plus selected outsiders | Vendor portals, partner dashboards, client access |

All three use the same technologies (TCP/IP, web browsers, servers); the difference is purely about *who is allowed in*. Your university runs an intranet (try reaching some campus systems from off campus), and companies use extranets to share restricted information with suppliers and customers without opening it to the world.

### The Network Hierarchy: Who Connects Whom

The internet's networks form a rough hierarchy. At the bottom are LANs: homes, dorms, offices. These connect to **ISPs**, the retail companies that sell connectivity. ISPs in turn connect to one another and to **backbone providers**: large network operators (companies such as AT&T, Verizon, NTT, Lumen, and Cogent) whose long-haul fiber crisscrosses continents and oceans. Where networks meet and swap traffic, they do so at **Internet Exchange Points (IXPs)**, physical facilities, like Chicago's 350 E. Cermak from this week's reading, where hundreds of networks plug into shared switching fabric.

One major recent shift: the traditional telecom giants no longer own this map alone. Hyperscale content companies, notably Google, Meta, Amazon, and Microsoft, now own or lease a large share of the world's backbone and submarine cable capacity, building private cables to connect their own data centers. When one company owns the app, the data centers, *and* the cables in between, questions about competition, resilience, and power stop being hypothetical. Keep that in mind when we discuss net neutrality later in the course.

### Going Mobile: From 1G to 5G

Most of your internet use probably travels the last stretch through the air. Mobile networks have evolved in roughly decade-long generations. **1G** (1980s) carried analog voice only. **2G** (1990s) went digital and gave us text messaging; this was the era of competing standards like GSM and CDMA, terms you may still see in older articles. **3G** (2000s) brought usable mobile data and the first smartphones; US carriers retired their 3G networks in 2022, which is why some older phones, medical alert devices, and even car systems abruptly stopped connecting. **4G LTE** (2010s) made mobile video, ride-sharing, and app economies practical. **5G** (2020s) adds higher speeds, lower latency, and capacity for huge numbers of devices; today's phones use 4G LTE and 5G.

The generational story is an infrastructure story: each "G" means new radios on hundreds of thousands of towers, new spectrum licenses, and new fiber connecting it all back to the wired internet. A cell tower is really an on-ramp: from the tower onward, your cat video travels the same cables and exchange points as everyone else's traffic.

### The Digital Divide

The gap between those who have access to modern information and communication technology and those who don't:

- **Access Divide**: Physical availability of internet and devices
- **Skills Divide**: Ability to effectively use technology
- **Usage Divide**: How people use technology (entertainment vs. empowerment)

:::{warning} Policy Snapshot: The Affordable Connectivity Program
The ACP, a federal subsidy that helped over 23 million US households afford internet access, ran out of funding and ended on June 1, 2024, after Congress declined to renew it ([FCC](https://www.fcc.gov/affordable-connectivity-program)). Millions of households lost their broadband subsidy overnight. As you watch the digital divide documentary, consider: what happens to the divide when support programs disappear?
:::

---

## 🔗 Interesting Links: Internet History

| Year | Milestone |
|------|-----------|
| 1969 | ARPANET launched |
| 1971 | First email sent (Ray Tomlinson) |
| 1983 | TCP/IP adopted, unified internet |
| 1991 | [First website](https://info.cern.ch/) goes live at CERN |
| 1993 | CERN releases the World Wide Web into the public domain; the web goes public |
| 2005 | [First YouTube video](https://www.youtube.com/watch?v=jNQXAC9IVRw) |
| 2006 | [First tweet](https://web.archive.org/web/2023/https://twitter.com/jack/status/20) (via Internet Archive; Twitter is now X) |
| 2010 | [First Instagram photo](https://web.archive.org/web/2023/https://www.instagram.com/p/G/) (via Internet Archive) |
| 2022 | ChatGPT launches; generative AI goes mainstream |

### 🗝️ Key Terms This Week

*Infrastructure · Data center · Internet Exchange Point · Digital divide · Bandwidth*: see the [Glossary](../glossary.md).

---

## 📝 This Week's Assignments

| Assignment | Due | Notes |
|------------|-----|-------|
| Intro Video | This week | Must be completed |
| Name Coach | This week | Must be completed |
| Weekly Reflection | Friday by class | Connect to infrastructure readings |

:::{tip} Reflection Prompt
Consider the physical infrastructure that enables your digital life. What surprised you about where the internet "lives"? How does understanding this infrastructure change how you think about the digital divide?
:::

---

## Looking Ahead

Now that we understand the physical infrastructure, next week we'll explore how technology is *designed*, and why design decisions matter for everyone who uses them.
