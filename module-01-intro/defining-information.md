# Defining Information

> "Engineering can move messages, but only people make meaning."

---

## 🎯 In This Section

- Untangle Buckland's three senses of "information": process, knowledge, and thing
- See why information *systems* can only ever store and retrieve information-as-thing
- Trace a text message through Shannon's communication model, noise and all
- Distinguish a single act of transmission from the full information lifecycle

---

## How Do We Define Information?

"Information" might be the most-used and least-examined word in this whole field. This week's readings offer two classic attempts to pin it down, and they approach the problem from opposite directions.

### Buckland's Three Senses of Information

Michael Buckland, in "Information as Thing" (Buckland, 1991), points out that when people say "information" they usually mean one of three different things:

1. **Information-as-process**: the act of informing, of becoming informed. When a friend tells you your class is canceled, the *telling* (and your change in knowledge) is information in this sense. It is an event that happens to a person.
2. **Information-as-knowledge**: the intangible stuff that gets communicated. What you now know (class is canceled) is information in this sense. It lives in minds, and you cannot touch it or measure it directly.
3. **Information-as-thing**: the physical objects that carry or represent information: documents, books, files, databases, photographs, even museum specimens. The text message on your screen is information in this sense.

Buckland's provocative argument is that the third sense deserves serious attention, because *things* are the only form of information that systems can actually store, retrieve, and process. A library cannot shelve knowledge; it shelves books. A database cannot hold your understanding; it holds records. Whenever we build information systems, we are inevitably working with information-as-thing, and hoping that the things we deliver will spark the process that produces knowledge. Keep this three-way distinction in your pocket; it will clarify many muddled conversations about technology, in this course and beyond.

### Shannon's Communication Model

Where Buckland asks *what information is*, Claude Shannon asked *how it moves*. In his landmark 1948 paper "A Mathematical Theory of Communication," Shannon (1948) wrote:

> "The fundamental problem of communication is that of reproducing at one point either exactly or approximately a message selected at another point."

Shannon's model breaks every act of communication into a chain of parts:

| Component | Role | Example (a text message) |
|-----------|------|--------------------------|
| **Sender** | Originates the message | You, deciding what to say |
| **Encoder** | Converts the message into a transmittable signal | Your phone turning text into radio waves |
| **Channel** | The medium the signal travels through | The cellular network |
| **Noise** | Anything that distorts the signal | Interference, a weak connection, a typo |
| **Decoder** | Converts the signal back into a message | Your friend's phone rendering the text |
| **Receiver** | The destination of the message | Your friend, reading it |

```{figure} images/shannon-model.svg
:alt: Diagram of Shannon's communication model as a chain of five boxes: a sender (you, deciding what to say) passes a message to an encoder (your phone turning text into radio waves), which sends a signal through a channel (the cellular network), which a decoder (your friend's phone rendering the text) turns back into a message for the receiver (your friend, reading it). A noise box above the channel distorts the signal, and a dashed feedback arrow runs from the receiver back to the sender.
:width: 100%
:name: fig-shannon-model

One text message, six moving parts: Shannon's chain describes a noisy room, an undersea cable, and a DNA strand with the same six boxes, plus the feedback loop later scholars added.
```

Later communication scholars added **feedback** (the receiver's response flowing back to the sender) to describe conversations rather than one-way transmissions. The model's genius is its generality: it describes talking across a noisy room, a fiber-optic cable under the ocean, and a DNA strand copying itself. Shannon deliberately set *meaning* aside ("frequently the messages have meaning," he noted dryly) so that information could be measured and engineered. That move made the digital world possible, and it is also why informatics needs Buckland too: engineering can move messages, but only people make meaning.

Separate from Shannon's transmission model, information professionals also describe an **information lifecycle**: information is *created*, *disseminated*, *stored, indexed, and retrieved*, *consumed*, and eventually *archived or disposed of*. This lifecycle model comes from the information management tradition, not from Shannon; it tracks what happens to documents and data over time, while Shannon's model captures a single act of transmission. You'll use both lenses in this course: the lifecycle when we discuss databases, archives, and retention; the communication chain when we discuss networks, noise, and encoding.

---

## Up Next

With the field mapped and "information" defined, meet this week's authors in depth: [Key Concepts from the Readings](key-concepts.md).
