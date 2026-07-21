# Module 5: Accessibility & Inclusion ♿

**Week 5 | Designing for Everyone**

---

## The Big Picture

An estimated 1.3 billion people worldwide (about 16% of everyone alive) experience significant disability ([WHO](https://www.who.int/news-room/fact-sheets/detail/disability-and-health)). When technology isn't designed with accessibility in mind, it creates barriers that exclude people from education, employment, and social connection.

This week, we explore how to design information systems that work for everyone.

### 🎯 What You'll Learn

- Understand why accessibility matters (legally, ethically, and practically)
- Learn how disability is defined, and why the definition you choose changes what you build
- Learn about different types of disabilities and assistive technologies
- Explore accessibility guidelines and standards, and how US laws relate to them
- Distinguish between accessible design and inclusive design
- Evaluate the accessibility of real-world technologies

### 🧠 Big Questions to Consider

- What assumptions do we make about how users interact with technology?
- Is accessibility a feature or a fundamental right?
- How does designing for disability benefit everyone?
- What barriers exist in technologies you use daily?

---

## What Do We Mean by "Disability"?

Before designing for disability, it's worth asking what disability actually is, because the answer is less obvious than it seems, and it shapes everything downstream.

**The legal definition (ADA).** The Americans with Disabilities Act defines an individual with a disability as a person who has a physical or mental impairment that substantially limits one or more major life activities, a person who has a history or record of such an impairment, or a person who is perceived by others as having such an impairment. The ADA deliberately does not list every covered condition. It prohibits discrimination on the basis of disability in employment, state and local government, public accommodations, commercial facilities, transportation, and telecommunications.

**The WHO framing.** The World Health Organization describes persons with disabilities as those who have long-term physical, mental, intellectual, or sensory impairments which *in interaction with various barriers* may hinder their full and effective participation in society on an equal basis with others. Read that carefully: in this framing, disability is not located solely in a person's body. Disability is the *outcome of an interaction* between an individual with a health condition and their personal and environmental context: negative attitudes, inaccessible buildings and transportation, limited social support.

This shift in perspective is often described as moving from a **medical model** (disability is a problem inside a person, to be treated) toward a **social model** (disability arises when environments are built for only some bodies and minds). Consider: a wheelchair user is not "disabled" by stairs in a building that has a ramp. A Deaf viewer is not "disabled" by a video that has accurate captions. The impairment is real, but the *barrier* is a design choice, and design choices can be changed. That is why this module belongs in an informatics course: as a builder of information systems, you will be one of the people deciding, screen by screen, who encounters barriers and who doesn't.

There's even a name for studying this intersection: **disability informatics**, an emerging field examining how people with disabilities use information technology to get things done, improve their self-efficacy, and live as independently as anyone else (Appleyard, 2005).

---

## Why Accessibility Matters

### The Numbers

- **1 in 4** US adults has a disability ([CDC](https://www.cdc.gov/disability-and-health/articles-documents/disability-impacts-all-of-us-infographic.html))
- **1.3 billion people / 16%** of the world's population experiences significant disability ([WHO, 2023](https://www.who.int/news-room/fact-sheets/detail/disability-and-health))
- **100%** of us will likely experience temporary or situational disability

A few more facts put these numbers in context. In the US, older adults are significantly more likely than younger adults to have a disability, the most common disabilities involve mobility, independent living, and cognition, and Americans with disabilities tend to earn less and adopt some technologies at lower rates than those without (Pew Research Center, 2023). Globally, the WHO reports that persons with disabilities face steep health inequities driven not by their conditions alone but by stigma, discrimination, poverty, exclusion from education and employment, and barriers within systems themselves. Inaccessible technology is one of those barriers, and it's one we can fix.

### It's the Law

- **Section 508**: US federal agencies must make technology accessible
- **ADA Title II web rule (2024)**: In April 2024, the Department of Justice issued a landmark rule requiring state and local governments, including public universities, to make their web content and mobile apps conform to **WCAG 2.1 Level AA** ([ADA.gov](https://www.ada.gov/resources/2024-03-08-web-rule/)). Compliance deadlines were extended in 2026 to **April 2027** (larger entities) and **April 2028** (smaller ones). In other words, this is being implemented *right now*, and people who understand it are in demand.
- **WCAG**: Web Content Accessibility Guidelines, the international standard. The current version is **WCAG 2.2** ([W3C](https://www.w3.org/TR/WCAG22/)), though US regulations reference 2.1 AA.

#### How Section 508, the ADA, and WCAG Fit Together

Students often mix these three up, so here is the relationship in one breath: **WCAG is a technical standard, while Section 508 and the ADA are laws that increasingly point at it.**

| Instrument | What it is | Who it covers | Connection to WCAG |
|-----------|-----------|---------------|--------------------|
| **WCAG** | Voluntary technical guidelines from the W3C (an international standards body, not a government) | Anyone who adopts them | It *is* the standard; versions 2.0, 2.1, 2.2 |
| **Section 508** | US federal procurement law | Federal agencies and technology bought with federal money | Its 2017 refresh incorporates WCAG 2.0 AA as the benchmark |
| **ADA** | US civil rights law (1990) | Employment, government services, public accommodations | The 2024 Title II rule requires WCAG 2.1 AA for state/local government web content |

So a web developer at a public university might satisfy the ADA rule, Section 508 obligations, and good practice all at once by building to WCAG. And because WCAG versions are backward-compatible (2.2 includes 2.1's requirements and adds more), building to the current version is the safest strategy: you meet today's legal benchmarks and tomorrow's likely ones.

### It's Good Design

Accessible design often benefits everyone:
- Captions help in noisy environments
- High contrast helps in bright sunlight
- Simple navigation helps everyone find things faster

---

## Types of Disabilities & Assistive Technologies

| Disability Type | Examples | Assistive Technologies |
|----------------|----------|----------------------|
| **Visual** | Blindness, low vision, color blindness | Screen readers, magnifiers, high contrast |
| **Auditory** | Deafness, hard of hearing | Captions, transcripts, visual alerts |
| **Motor** | Limited mobility, tremors | Keyboard navigation, voice control, switches |
| **Cognitive** | Learning disabilities, attention disorders | Simple layouts, clear language, consistent navigation |

The table is a starting point; the technologies deserve a closer look, because you will design *for* them whether you know it or not.

**Screen readers** convert on-screen content into synthesized speech or refreshable braille. The major ones are JAWS (a commercial Windows program), NVDA (a free, open-source Windows alternative), and VoiceOver (built into every Mac and iPhone; Android's equivalent is TalkBack). A skilled screen reader user doesn't listen to a page top to bottom; they jump between headings, skim link lists, and navigate by landmarks, which is exactly why well-structured headings and meaningful link text matter so much. A page that is a visual masterpiece but a structural soup is unreadable this way.

**Switch access** serves people with very limited mobility. A switch can be a large button pressed with a hand, foot, or head, or even a sip-and-puff device operated by breath. The system highlights options in sequence and the user activates the switch to select. **Eye tracking** goes further, letting users point and click with their gaze alone. Both technologies share one requirement: everything on screen must be reachable and activatable without a mouse, which is why keyboard operability (coming up in POUR) is such a foundational test.

**Captioning and transcripts** make audio content available to Deaf and hard-of-hearing users, and visual alerts replace sounds like notification chimes. Quality matters: auto-generated captions have improved dramatically but still mangle names, technical terms, and accented speech, so human review remains part of real accessibility work.

For cognitive and learning disabilities, the most powerful "assistive technology" is often the design itself: plain language, predictable layouts, consistent navigation, and freedom from time pressure and distracting motion.

:::{note} 🤖 AI as Assistive Technology: Promise and Peril
AI has produced some of the most meaningful accessibility advances in decades: apps that describe the visual world aloud for blind users (like Be My Eyes' AI mode), real-time AI captioning of any conversation, and voice interfaces that give hands-free control of devices.

But AI has also enabled a shortcut industry. "Accessibility overlay" widgets promised to make any website compliant with one line of code, and in 2025 the FTC ordered overlay vendor accessiBe to pay **$1 million** for falsely claiming its widget could make any site WCAG-compliant ([FTC](https://www.ftc.gov/news-events/news/press-releases/2025/04/ftc-approves-final-order-requiring-accessibe-pay-1-million)). Real accessibility is a design practice, not a product you bolt on.
:::

---

## Accessible vs. Inclusive Design

These terms are related but different:

### Accessible Design
Designing an experience that **meets the needs** of everyone within your audience, including those with disabilities.

*Example: Adding alt text to images so screen readers can describe them*

### Inclusive Design
Creating content that is **mindful of a broad range** of users, their abilities, environments, situations, and contexts.

*Example: Designing a form that doesn't assume binary gender, specific name formats, or physical addresses*

> Inclusiveness doesn't only question if a user CAN use something; it goes further to consider if they WANT to use something.

Inclusive design doesn't necessarily target one specific need; instead it provides a spectrum of tools and features users can choose to fit their own context. As designer Cameron Chapman puts it, every designer should step away from preconceived notions of a "typical" user and instead see people as unique individuals with differing abilities at different times in their lives.

Microsoft's [Inclusive Design toolkit](https://inclusive.microsoft.design/) offers the classic illustration: disability can be **permanent** (one arm), **temporary** (arm injury), or **situational** (holding a baby). Design for one and you help all three.

### The Curb-Cut Effect

The deepest argument for inclusive design has a name borrowed from the sidewalk. **Curb cuts**, the small ramps carved into street corners, were fought for by disability activists (famously in Berkeley, California in the 1970s, where activists poured makeshift cement ramps in protest) so wheelchair users could cross the street. Then something remarkable happened: everyone started using them. Parents with strollers, travelers with rolling luggage, delivery workers with carts, kids on bikes, older adults who appreciated the gentler transition. A feature designed for a "small" group turned out to serve nearly everybody.

The **curb-cut effect** is the general pattern: solutions designed for people with disabilities routinely become universal benefits ([The Curb Cut Effect](https://ssir.org/articles/entry/the_curb_cut_effect)). Technology is full of examples. Captions, created for Deaf viewers, are now used by millions watching videos in noisy gyms and quiet libraries, and they help language learners besides. Text-to-speech, built for blind users, became audiobooks and voice assistants. OXO's Good Grips kitchen tools were designed for arthritic hands and took over everyone's kitchen drawers. The typewriter itself traces back to helping a blind countess write letters. The lesson for your career: accessibility work is not charity at the margins. It is very often where the next mainstream feature comes from.

### Universal Design: From Buildings to Software

The philosophy behind all of this predates the web. **Universal design** was coined by architect **Ronald Mace** at North Carolina State University: the design of products and environments to be usable by all people, to the greatest extent possible, *without the need for adaptation or specialized design*. Mace, who used a wheelchair himself, argued that ramps, wide doorways, and lever handles shouldn't be special accommodations bolted onto buildings afterward; they should simply be how buildings are made.

Carry that idea into software and it becomes a design ethic: build the ramp into the product from the start. A website that is keyboard-navigable, well-structured, and captioned from day one doesn't need a costly "accessibility retrofit," and it never sends anyone around back to a separate entrance. Retrofitting accessibility, like retrofitting a ramp onto a finished building, is always more expensive and always more awkward than designing it in.

---

## Web Accessibility Guidelines (WCAG)

WCAG is organized around four principles, known as **POUR**:

| Principle | Meaning |
|-----------|---------|
| **Perceivable** | Information must be presentable in ways users can perceive |
| **Operable** | Interface components must be operable by all users |
| **Understandable** | Information and operation must be understandable |
| **Robust** | Content must work with current and future assistive technologies |

Each principle breaks down into concrete, testable **success criteria**. A few examples make the abstract principles vivid:

**Perceivable** means information can't be invisible to all of a user's senses. Concretely: every meaningful image needs a **text alternative** (alt text) so screen readers can convey it; prerecorded video needs **captions**; and text must have sufficient **color contrast** against its background (the familiar AA benchmark is a 4.5:1 contrast ratio for normal-size text). Light gray text on white may look sleek, but for many users it simply is not there.

**Operable** means no interaction can require abilities a user may not have. Concretely: all functionality must work from the **keyboard alone**, with no mouse required and no "keyboard traps" you can tab into but not out of; users need **enough time**, so time limits must be extendable; and content must not **flash more than three times per second**, a criterion that exists because flashing content can trigger seizures in people with photosensitive epilepsy. This last one is a good reminder that accessibility failures can cause physical harm, not just inconvenience.

**Understandable** means users must be able to comprehend both the information and the interface. Concretely: form inputs need clear, programmatically attached **labels and instructions** (a floating placeholder that vanishes when you click is not a label); when a user makes an **error**, the system should identify it in text and *suggest* how to fix it ("Password must include a number" beats a red border and silence); and navigation should behave **consistently and predictably** from page to page.

**Robust** means content must be interpretable by a wide variety of user agents, including assistive technologies, as they evolve. Concretely: valid, standards-following markup, and correctly exposed names, roles, and values for custom controls, so a screen reader can tell a user that your fancy custom toggle is a switch and whether it's on. If any one of the four principles fails, users with disabilities will not be able to use the web content; that's why POUR is the test, not a wish list.

### Common Accessibility Issues

- Missing alt text on images
- Poor color contrast
- No keyboard navigation
- Videos without captions
- Complex forms without labels
- Time limits without extensions

---

## Disability Etiquette & Language

Designing with and for people with disabilities also means talking about, and with, people respectfully. Two language conventions are in active use, and informed people disagree about which to prefer, so you should understand both:

- **Person-first language** puts the person before the condition: "a person with a disability," "a student who is blind." The intent is to emphasize that a person is not defined by a diagnosis. This convention dominates in medical, legal, and much academic writing (the ADA itself is written person-first).
- **Identity-first language** puts the identity first: "a disabled person," "a Deaf student," "an autistic adult." Many people, notably in Deaf and autistic communities, prefer this framing because they consider disability an integral part of who they are, not an unfortunate accessory, and person-first phrasing can imply disability is something shameful to distance from the person.

Neither convention is wrong, and the actual rule is simple: **individual preference wins.** When you're writing generally, many organizations mix or alternate the two; when you're referring to a specific person or community, use what they use. Beyond wording, everyday etiquette follows the same logic of respect: speak directly to the person (not to their interpreter or companion), don't touch someone's wheelchair, cane, or service animal without permission (they function as extensions of personal space), ask before helping instead of assuming help is wanted, and never demand that someone explain their disability to justify a need. If you're unsure what someone needs, there is a time-tested technique: ask.

---

## This Week's Journey

### 📚 Core Readings & Videos

| Resource | Type | Notes |
|----------|------|-------|
| [W3C: Introduction to Web Accessibility](https://www.w3.org/WAI/fundamentals/accessibility-intro/) | Reading | The standard-setters' overview |
| [WCAG 2.2 Guidelines](https://www.w3.org/TR/WCAG22/) | Reference | The current international standard |
| [DOJ fact sheet: ADA web rule](https://www.ada.gov/resources/2024-03-08-web-rule/) | Reading | The 2024 rule, in plain language |
| [Microsoft Inclusive Design](https://inclusive.microsoft.design/) | Interactive | The inclusive design toolkit |

### 🤔 Make You Think

- [The Curb Cut Effect](https://ssir.org/articles/entry/the_curb_cut_effect): How designing for disability benefits everyone
- How do algorithms perpetuate ableism?
- Voice assistants struggle far more with some accents and speech patterns than others. What does "accessible AI" require?

---

## Testing for Accessibility

Quick tests you can do:

1. **Keyboard Only**: Can you navigate without a mouse?
2. **Screen Reader**: Does it make sense when read aloud?
3. **Zoom**: Does it work at 200% magnification?
4. **Color**: Is information conveyed without relying on color alone?
5. **Captions**: Do videos have accurate captions?

Each of these maps back to POUR: the keyboard test checks Operable, the screen reader and color tests check Perceivable, and reading your interface aloud is a surprisingly effective test of Understandable. Automated checker tools can catch some issues (missing alt text, low contrast), but they cannot judge whether alt text is *meaningful* or a page truly makes sense, so human testing stays essential. Recall the accessiBe case above: anyone promising fully automated compliance is selling something.

:::{tip} Try It!
Turn on VoiceOver (Mac) or Narrator (Windows) and try navigating a website you use frequently. What works? What's frustrating?
:::

### 🗝️ Key Terms This Week

*Accessibility · Assistive technology · Screen reader · WCAG · Section 508 · POUR · Alt text · Inclusive design · Universal design · Curb-cut effect*; see the [Glossary](../glossary.md).

---

## 📝 This Week's Assignments

| Assignment | Due | Notes |
|------------|-----|-------|
| Weekly Reflection | Friday by class | Connect to accessibility concepts |

:::{tip} Reflection Prompt
Choose a website or app you use regularly. Evaluate its accessibility using the concepts from this module. What works well? What could be improved? How might someone with a disability experience this technology differently than you do?
:::

---

## Looking Ahead

Next week, we dive into **Data Analytics & Data Science**: how we extract meaning and insights from data.
