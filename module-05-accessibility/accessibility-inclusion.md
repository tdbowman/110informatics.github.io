# Module 5: Accessibility & Inclusion ♿

**Week 5 | Designing for Everyone**

---

## The Big Picture

An estimated 1.3 billion people worldwide (about 16% of everyone alive) experience significant disability ([WHO](https://www.who.int/news-room/fact-sheets/detail/disability-and-health)). When technology isn't designed with accessibility in mind, it creates barriers that exclude people from education, employment, and social connection.

This week, we explore how to design information systems that work for everyone.

### 🎯 What You'll Learn

- Understand why accessibility matters (legally, ethically, and practically)
- Learn about different types of disabilities and assistive technologies
- Explore accessibility guidelines and standards
- Distinguish between accessible design and inclusive design
- Evaluate the accessibility of real-world technologies

### 🧠 Big Questions to Consider

- What assumptions do we make about how users interact with technology?
- Is accessibility a feature or a fundamental right?
- How does designing for disability benefit everyone?
- What barriers exist in technologies you use daily?

---

## Why Accessibility Matters

### The Numbers

- **1 in 4** US adults has a disability ([CDC](https://www.cdc.gov/disability-and-health/articles-documents/disability-impacts-all-of-us-infographic.html))
- **1.3 billion people / 16%** of the world's population experiences significant disability ([WHO, 2023](https://www.who.int/news-room/fact-sheets/detail/disability-and-health))
- **100%** of us will likely experience temporary or situational disability

### It's the Law

- **Section 508**: US federal agencies must make technology accessible
- **ADA Title II web rule (2024)**: In April 2024, the Department of Justice issued a landmark rule requiring state and local governments, including public universities, to make their web content and mobile apps conform to **WCAG 2.1 Level AA** ([ADA.gov](https://www.ada.gov/resources/2024-03-08-web-rule/)). Compliance deadlines were extended in 2026 to **April 2027** (larger entities) and **April 2028** (smaller ones). In other words, this is being implemented *right now*, and people who understand it are in demand.
- **WCAG**: Web Content Accessibility Guidelines, the international standard. The current version is **WCAG 2.2** ([W3C](https://www.w3.org/TR/WCAG22/)), though US regulations reference 2.1 AA.

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

Microsoft's [Inclusive Design toolkit](https://inclusive.microsoft.design/) offers the classic illustration: disability can be **permanent** (one arm), **temporary** (arm injury), or **situational** (holding a baby). Design for one and you help all three.

---

## Web Accessibility Guidelines (WCAG)

WCAG is organized around four principles, known as **POUR**:

| Principle | Meaning |
|-----------|---------|
| **Perceivable** | Information must be presentable in ways users can perceive |
| **Operable** | Interface components must be operable by all users |
| **Understandable** | Information and operation must be understandable |
| **Robust** | Content must work with current and future assistive technologies |

### Common Accessibility Issues

- Missing alt text on images
- Poor color contrast
- No keyboard navigation
- Videos without captions
- Complex forms without labels
- Time limits without extensions

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

:::{tip} Try It!
Turn on VoiceOver (Mac) or Narrator (Windows) and try navigating a website you use frequently. What works? What's frustrating?
:::

### 🗝️ Key Terms This Week

*Accessibility · Assistive technology · WCAG · POUR · Alt text · Inclusive design · Universal design*; see the [Glossary](../glossary.md).

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
