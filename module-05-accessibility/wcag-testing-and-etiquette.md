# WCAG, Testing & Everyday Etiquette

> "POUR is the test, not a wish list."

---

## 🎯 In This Section

- Break WCAG down into its four POUR principles
- Connect each principle to concrete, testable success criteria
- Spot the most common accessibility failures
- Learn person-first vs. identity-first language, and the rule that settles the debate
- Run five quick accessibility tests on any website

---

## Web Accessibility Guidelines (WCAG)

WCAG is organized around four principles, known as **POUR**:

| Principle | Meaning |
|-----------|---------|
| **Perceivable** | Information must be presentable in ways users can perceive |
| **Operable** | Interface components must be operable by all users |
| **Understandable** | Information and operation must be understandable |
| **Robust** | Content must work with current and future assistive technologies |

```{figure} images/pour-principles.svg
:alt: Four cards showing the WCAG POUR principles with concrete examples. Perceivable: users can perceive it with the senses they have; alt text on images, captions on video, 4.5 to 1 color contrast. Operable: no interaction requires abilities a user may not have; keyboard-only use, extendable time limits, no rapid flashing. Understandable: content and controls make sense; clear form labels, errors explained in text, predictable navigation. Robust: works with assistive technologies present and future; valid markup, names, roles, and values exposed to screen readers. A note beneath states that if any one principle fails, users with disabilities cannot use the content.
:width: 100%
:name: fig-pour-principles

POUR works like a chain, not a checklist: content is only accessible while all four principles hold, so a single failure breaks the whole experience.
```

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

## Testing for Accessibility

Quick tests you can do:

1. **Keyboard Only**: Can you navigate without a mouse?
2. **Screen Reader**: Does it make sense when read aloud?
3. **Zoom**: Does it work at 200% magnification?
4. **Color**: Is information conveyed without relying on color alone?
5. **Captions**: Do videos have accurate captions?

Each of these maps back to POUR: the keyboard test checks Operable, the screen reader and color tests check Perceivable, and reading your interface aloud is a surprisingly effective test of Understandable. Automated checker tools can catch some issues (missing alt text, low contrast), but they cannot judge whether alt text is *meaningful* or a page truly makes sense, so human testing stays essential. Recall the accessiBe case from [Assistive Technology & Inclusive Design](assistive-tech-and-inclusive-design.md): anyone promising fully automated compliance is selling something.

:::{tip} Try It!
Turn on VoiceOver (Mac) or Narrator (Windows) and try navigating a website you use frequently. What works? What's frustrating?
:::

---

## Up Next

That wraps the module's content pages. Head back to the [module overview](accessibility-inclusion.md) for this week's readings, reflection prompt, and assignments.
