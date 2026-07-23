# How the Internet Works

> "The internet is physical infrastructure: cables, data centers, routers, and satellites that span the globe."

---

## 🎯 In This Section

- Meet the physical internet: submarine cables, data centers, exchange points, towers, and the last mile
- Follow packets, and the journey of a click, from your phone to a server and back
- Learn what DNS and IP addresses do, and how TCP and IP divide the labor
- Map the network hierarchy from your LAN to the backbone providers, and who owns it now
- Ride the mobile generations from 1G to 5G

---

## The Physical Internet

The internet is made of:

| Component | Description |
|-----------|-------------|
| **Submarine Cables** | Fiber optic cables crossing ocean floors carrying 99% of intercontinental data |
| **Data Centers** | Massive facilities housing servers (some use as much electricity as small cities) |
| **Internet Exchange Points** | Physical locations where networks connect and exchange traffic |
| **Cell Towers & Satellites** | Wireless connections to end users |
| **Last Mile Infrastructure** | The connection from the network to your home |

## What Is the Internet, Really?

The word "internet" is a compressed history lesson: it comes from *inter-network*, a network of interconnected networks. No single organization owns or runs it. Instead, thousands of independent networks (universities, companies, internet service providers, governments) agree to speak the same protocols and pass traffic to one another. High-speed data lines called the **internet backbone** carry traffic over long distances, and smaller networks connect to the backbone, which lets a user on any small network reach any other connected location on Earth.

The design is deliberately **redundant**: there are many possible paths between any two points, so if a cable is cut or a router fails, traffic reroutes around the damage. That resilience is inherited from the internet's Cold War era ancestry, and it is why the internet as a whole almost never goes down even though pieces of it fail constantly. Today this network of networks is the foundation for nearly all of computing: the web, apps, streaming, gaming, cloud services, and AI all ride on top of it.

## Packets: How Data Travels

The internet's core trick is **packet switching**. When you send anything (an email, a photo, a video call), your device does not open a dedicated line to the destination the way old telephone systems did. Instead, the data is chopped into small chunks called **packets**, typically around a thousand bytes each. Every packet is stamped with the address it's going to and the address it came from, then launched into the network to find its own way. Different packets from the same photo may take entirely different routes, and they may arrive out of order. At the destination, they are reassembled into the original file.

Why do it this way? Efficiency and resilience. Packets from millions of users can share the same cables, interleaved, with no one hogging a dedicated line. And if a route fails mid-transfer, later packets simply take a different path. When you watch a video "buffer," you are watching packet delivery fall behind playback; when it recovers, the network has found its flow again.

## The Journey of a Click

Trace what happens when you tap a link on your phone or laptop at home:

1. **Your device** builds a request. Its **network interface card (NIC)**, the hardware that speaks network protocols, hands the request to your local network.
2. **Your local area network (LAN)** carries it, either over an Ethernet cable or over Wi-Fi (a brand name for wireless networking based on the IEEE 802.11 standards).
3. **Your router and modem** pass the request out of your home: the router directs traffic between your LAN and the outside world, and the modem translates the signal for the physical line (cable, fiber, or DSL) that leaves your building.
4. **Your internet service provider (ISP)** receives the request and forwards it through its network toward the backbone.
5. **Backbone networks and exchange points** relay the packets, hop by hop, router by router, possibly across a submarine cable, to the data center where the destination server lives.
6. **The server** (or more likely a farm of servers) receives the reassembled request, prepares a response (the web page, the video chunk), and sends it back as packets, which retrace a path to your screen.

```{figure} images/journey-of-a-click.svg
:alt: Diagram of the six-step journey of a click. In the top row, your device builds the request, your home LAN carries it over Ethernet or Wi-Fi, and your router and modem send it out over cable, fiber, or DSL. The path continues in the bottom row: your ISP forwards it toward the backbone, backbone networks and exchange points relay it hop by hop, possibly across a submarine cable, and a data center server reassembles the request and sends the response back along a dashed return path to your device.
:width: 100%
:name: fig-journey-of-a-click

Six physical handoffs stand between your tap and the response, and every one of them is owned by someone, powered by electricity, and able to fail.
```

The whole round trip routinely completes in under a couple hundred milliseconds. Every element in that chain is physical, owned by someone, powered by electricity, and capable of failing. Keep this journey in mind while you look at [this week's data center photo essays](information-infrastructure.md): you are looking at steps 5 and 6.

## DNS: The Internet's Phone Book

There's a missing step in the journey above. You typed a *name* (like `example.com`), but packets are addressed to *numbers*. The **Domain Name System (DNS)** is the internet's phone book: a globally distributed directory that translates human-friendly domain names into machine-usable IP addresses. Before your request can go anywhere, your device quietly asks a DNS server, "what is the address for this name?" and gets back a number to stamp on its packets.

DNS is a hierarchy: root servers know who manages each top-level domain (`.com`, `.org`, `.edu`), those registries know which name servers handle each domain, and so on down. Because DNS sits in front of everything, it is also a pressure point: when a major DNS provider has an outage, huge swaths of the web become unreachable at once, even though the servers themselves are fine. The names stop resolving, and unresolvable is indistinguishable from offline.

## IP Addresses: Numbering Every Device

Every device on the internet needs a unique address to send and receive packets. That address is an **Internet Protocol (IP) address**. The original scheme, **IPv4**, uses four numbers (like `172.16.254.1`), which allows about 4.3 billion unique addresses. That sounded limitless in the 1980s; it stopped being enough once phones, TVs, cars, and doorbells all wanted addresses. The world has effectively run out of fresh IPv4 addresses, and networks stretch the supply with workarounds like sharing one public address among many home devices.

The long-term fix is **IPv6**, which uses eight groups of hexadecimal digits and provides 2^128 addresses: roughly 340 undecillion, or 340 trillion trillion trillion. That is enough to give every grain of sand on Earth its own address many times over. The two systems run side by side today, and the decades-long transition between them is a lesson in how hard it is to renovate infrastructure that can never be turned off.

## TCP and IP: A Division of Labor

You'll constantly see the abbreviation **TCP/IP**, the protocol pair at the heart of the internet since 1983. They are two separate protocols with a clean division of labor:

- **IP (Internet Protocol)** handles *addressing and routing*: it defines the addresses that identify every device and gets individual packets forwarded, hop by hop, toward their destination. IP makes no promises; packets can arrive late, out of order, or not at all.
- **TCP (Transmission Control Protocol)** handles *reliability*: it establishes a connection between sender and receiver, numbers the packets so they can be reassembled in the correct order, confirms what arrived, and retransmits anything that got lost.

A useful analogy: IP is the postal address system plus the trucks; TCP is a meticulous shipping clerk who numbers every box, tracks confirmations, and re-sends missing ones. The genius of the design is that the network's middle stays simple and dumb (routers just forward packets) while the intelligence lives at the edges, in the sending and receiving devices. That "dumb middle" is a big part of why the internet could grow without central coordination and why new applications can be invented without asking anyone's permission.

## Internet, Intranet, Extranet

Not every network that behaves like the internet *is* the internet:

| Network | Who can access it | Typical use |
|---------|-------------------|-------------|
| **Internet** | Anyone, globally | Public web, email, apps, everything |
| **Intranet** | Members of one organization only | Internal documents, HR portals, staff tools |
| **Extranet** | An organization plus selected outsiders | Vendor portals, partner dashboards, client access |

All three use the same technologies (TCP/IP, web browsers, servers); the difference is purely about *who is allowed in*. Your university runs an intranet (try reaching some campus systems from off campus), and companies use extranets to share restricted information with suppliers and customers without opening it to the world.

## The Network Hierarchy: Who Connects Whom

The internet's networks form a rough hierarchy. At the bottom are LANs: homes, dorms, offices. These connect to **ISPs**, the retail companies that sell connectivity. ISPs in turn connect to one another and to **backbone providers**: large network operators (companies such as AT&T, Verizon, NTT, Lumen, and Cogent) whose long-haul fiber crisscrosses continents and oceans. Where networks meet and swap traffic, they do so at **Internet Exchange Points (IXPs)**, physical facilities, like Chicago's 350 E. Cermak from [this week's reading](information-infrastructure.md), where hundreds of networks plug into shared switching fabric.

One major recent shift: the traditional telecom giants no longer own this map alone. Hyperscale content companies, notably Google, Meta, Amazon, and Microsoft, now own or lease a large share of the world's backbone and submarine cable capacity, building private cables to connect their own data centers. When one company owns the app, the data centers, *and* the cables in between, questions about competition, resilience, and power stop being hypothetical. Keep that in mind when we discuss net neutrality later in the course.

## Going Mobile: From 1G to 5G

Most of your internet use probably travels the last stretch through the air. Mobile networks have evolved in roughly decade-long generations. **1G** (1980s) carried analog voice only. **2G** (1990s) went digital and gave us text messaging; this was the era of competing standards like GSM and CDMA, terms you may still see in older articles. **3G** (2000s) brought usable mobile data and the first smartphones; US carriers retired their 3G networks in 2022, which is why some older phones, medical alert devices, and even car systems abruptly stopped connecting. **4G LTE** (2010s) made mobile video, ride-sharing, and app economies practical. **5G** (2020s) adds higher speeds, lower latency, and capacity for huge numbers of devices; today's phones use 4G LTE and 5G.

The generational story is an infrastructure story: each "G" means new radios on hundreds of thousands of towers, new spectrum licenses, and new fiber connecting it all back to the wired internet. A cell tower is really an on-ramp: from the tower onward, your cat video travels the same cables and exchange points as everyone else's traffic.

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

---

## Up Next

All of this hardware runs on electricity, water, land, and minerals, and not everyone gets to use it. Next: [Costs and the Digital Divide](costs-and-the-digital-divide.md).
