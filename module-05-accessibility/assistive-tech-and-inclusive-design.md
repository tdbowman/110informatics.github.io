# Assistive Technology & Inclusive Design

> "Design for one and you help all three."

---

## 🎯 In This Section

- Survey the major types of disabilities and the assistive technologies that serve them
- Learn how screen readers, switch access, and eye tracking actually work
- Weigh AI's promise and peril as assistive technology
- Distinguish accessible design from inclusive design
- Meet the curb-cut effect and universal design

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

**Switch access** serves people with very limited mobility. A switch can be a large button pressed with a hand, foot, or head, or even a sip-and-puff device operated by breath. The system highlights options in sequence and the user activates the switch to select. **Eye tracking** goes further, letting users point and click with their gaze alone. Both technologies share one requirement: everything on screen must be reachable and activatable without a mouse, which is why keyboard operability (coming up in [POUR](wcag-testing-and-etiquette.md)) is such a foundational test.

**Captioning and transcripts** make audio content available to Deaf and hard-of-hearing users, and visual alerts replace sounds like notification chimes. Quality matters: auto-generated captions have improved dramatically but still mangle names, technical terms, and accented speech, so human review remains part of real accessibility work.

For cognitive and learning disabilities, the most powerful "assistive technology" is often the design itself: plain language, predictable layouts, consistent navigation, and freedom from time pressure and distracting motion.

```{figure} images/assistive-tech-landscape.svg
:alt: Four cards mapping disability types to assistive technologies. Visual disabilities pair with screen readers such as JAWS, NVDA, VoiceOver, and TalkBack, plus magnifiers, high-contrast modes, and refreshable braille. Auditory disabilities pair with captions, transcripts, and visual alerts. Motor disabilities pair with keyboard navigation, voice control, switch access including sip-and-puff devices, and eye tracking. Cognitive disabilities pair with the design itself: plain language, predictable layouts, consistent navigation, and no time pressure. A bottom note states the shared requirement that everything on screen must work without a mouse.
:width: 100%
:name: fig-assistive-tech-landscape

Four kinds of disability, four families of assistive technology, and one shared demand on every designer: nothing on screen can require a mouse.
```

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

```{figure} images/curb-cut-effect.svg
:alt: Diagram of the curb-cut effect. On top, a card labeled "designed for one group" describes curb cuts won by disability activists so wheelchair users could cross the street; an arrow leads to a card labeled "used by nearly everyone" listing parents with strollers, travelers with luggage, delivery workers, kids on bikes, and older adults. Below, three pairs show the same pattern in technology: captions built for Deaf viewers now serve noisy gyms, quiet libraries, and language learners; text-to-speech built for blind users became audiobooks and voice assistants; OXO Good Grips designed for arthritic hands took over everyone's kitchen drawers.
:width: 100%
:name: fig-curb-cut-effect

The curb-cut effect: a solution won for one excluded group keeps turning into a benefit for nearly everybody, on sidewalks and in software alike.
```

### Universal Design: From Buildings to Software

The philosophy behind all of this predates the web. **Universal design** was coined by architect **Ronald Mace** at North Carolina State University: the design of products and environments to be usable by all people, to the greatest extent possible, *without the need for adaptation or specialized design*. Mace, who used a wheelchair himself, argued that ramps, wide doorways, and lever handles shouldn't be special accommodations bolted onto buildings afterward; they should simply be how buildings are made.

Carry that idea into software and it becomes a design ethic: build the ramp into the product from the start. A website that is keyboard-navigable, well-structured, and captioned from day one doesn't need a costly "accessibility retrofit," and it never sends anyone around back to a separate entrance. Retrofitting accessibility, like retrofitting a ramp onto a finished building, is always more expensive and always more awkward than designing it in.

---

## Up Next

You know the who and the why; now for the how. The international standard that turns these ideas into testable rules: [WCAG, Testing & Everyday Etiquette](wcag-testing-and-etiquette.md).
