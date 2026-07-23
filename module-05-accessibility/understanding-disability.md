# Understanding Disability & Why It Matters

> "The impairment is real, but the *barrier* is a design choice, and design choices can be changed."

---

## 🎯 In This Section

- Compare the ADA's legal definition of disability with the WHO's interaction-based framing
- Trace the shift from the medical model to the social model of disability
- Put numbers on disability in the US and worldwide
- Learn how Section 508, the ADA, and WCAG fit together
- See why accessible design is simply good design

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

## Up Next

Now that you know why accessibility matters, meet the people and tools at the center of it: [Assistive Technology & Inclusive Design](assistive-tech-and-inclusive-design.md).
