# The Law in Motion: AI Copyright and Net Neutrality

> When this course was first taught, every AI copyright question was "pending." That is no longer true.

---

## 🎯 In This Section

- Learn what courts have actually decided about AI authorship and training on copyrighted books
- Apply the four fair-use factors to the *Bartz v. Anthropic* facts yourself
- See how *Hachette v. Internet Archive* drew the line between owning and lending digital books
- Follow net neutrality's decade of whiplash: in force, repealed, restored, struck down
- Weigh both sides of the net neutrality debate, and its connection to the digital divide

---

## AI and Copyright: The Courts Have Started Answering

When this course was first taught, every AI copyright question was "pending." That is no longer true, because the last two years produced landmark rulings:

| Question | What's Been Decided |
|----------|---------------------|
| **Can AI-generated work be copyrighted?** | **No; this is settled law.** In *Thaler v. Perlmutter*, the D.C. Circuit affirmed (March 2025) that copyright requires a *human* author; the Supreme Court declined to hear the appeal in 2026 ([opinion](https://media.cadc.uscourts.gov/opinions/docs/2025/03/23-5233.pdf)). The [US Copyright Office's AI reports](https://www.copyright.gov/ai/) add nuance: works made *with* AI assistance can be protected to the extent of the human contribution, but a text prompt alone isn't enough. |
| **Can AI train on copyrighted books?** | **It depends how you got them.** In *Bartz v. Anthropic* (June 2025), a federal judge ruled that training on *lawfully purchased* books is transformative fair use, but that keeping a library of *pirated* copies is not. Anthropic then settled the piracy claims for **$1.5 billion**, the largest copyright settlement in US history ([analysis](https://legalblogs.wolterskluwer.com/copyright-blog/the-bartz-v-anthropic-settlement-understanding-americas-largest-copyright-settlement/)). *Kadrey v. Meta* (June 2025) also went Meta's way, but the judge pointedly left the door open to future "market dilution" arguments. |
| **Is it over?** | **No.** *The New York Times v. OpenAI*, the highest-profile case and the one with the strongest market-harm argument, is still being litigated as of mid-2026. The next few years will keep reshaping this table. |

It is worth appreciating how fast this moved. When authors including Michael Chabon first sued OpenAI in September 2023, scholars like Berkeley's Pamela Samuelson framed the core claim as untested: is ingesting copyrighted works as training data itself an infringing reproduction? Barely two years later, courts had answered "the ingestion can be fair use, the piracy cannot," and a $1.5 billion settlement had put a price on the difference. The [four factors you just learned](copyright-and-fair-use.md) are precisely the tool the judges used; the *Warhol* purpose-of-the-use lens shaped how they asked whether training "supersedes" books or does something genuinely different with them.

:::{tip} Apply the Four Factors Yourself
Take the *Bartz* facts: an AI company buys millions of books, scans them, and trains a model that doesn't reproduce the books but learned from all of them. Walk through purpose, nature, amount, and market effect. Would *you* have called it fair use? Now change one fact (the books were pirated) and see which factor flips. This is exactly how the court reasoned.
:::

### 📌 Case Study: *Hachette v. Internet Archive*

The Internet Archive scanned physical books it owned and lent the scans one-at-a-time, like a library: "controlled digital lending." Publishers sued. The Second Circuit ruled in September 2024 that this was **not** fair use, and the Archive [ended its appeal](https://blog.archive.org/2024/12/04/end-of-hachette-v-internet-archive/). For an information school, this case cuts close to home: it draws the current legal line between *owning* a book and *lending access* to it digitally. Do you think the line is in the right place?

### Personality, Voice, and Deepfakes

Two new laws extend "ownership" to your face and voice:
- **Tennessee's ELVIS Act (2024)**: the first state law protecting musicians' *voices* from unauthorized AI cloning
- **The TAKE IT DOWN Act (2025)**: federal criminal penalties for nonconsensual intimate images, explicitly including AI deepfakes ([Congress.gov](https://www.congress.gov/bill/119th-congress/senate-bill/146))

---

## Net Neutrality: A Case Study in Regulatory Whiplash

**Net Neutrality** is the principle that internet service providers (ISPs) should treat all internet traffic equally, without discriminating based on source, destination, or content.

### What Would ISPs Actually Do? The Vocabulary

The debate is easier to follow once the abstract principle is translated into the four specific behaviors the rules addressed:

- **Blocking**: the ISP refuses to carry certain traffic at all, such as a competitor's video app or a disfavored website. Under neutrality rules, if content is legal, the ISP must carry it.
- **Throttling**: the ISP deliberately slows particular traffic. The most vivid US example was not even about content: in 2018, Verizon throttled the data connection of the Santa Clara County Fire Department *while it was fighting the Mendocino Complex wildfire*, then told the department the fix was upgrading to a pricier plan. The incident (which Verizon called a customer-service error) became Exhibit A for why "just trust the ISPs" reassures few people.
- **Paid prioritization**: the ISP sells "fast lanes," delivering the traffic of companies that pay extra ahead of everyone else's. Netflix can afford the toll; the next startup competing with Netflix cannot. Critics argue this quietly reshapes who can compete on the internet.
- **Zero-rating**: certain services do not count against your data cap. It feels like a gift (free streaming!), but when the ISP zero-rates *its own* streaming service and not rivals', the "gift" steers your choices. Regulators worldwide have split on whether this counts as discrimination.

The point of the vocabulary: with no federal rules in force (see the timeline below), whether any of these practices is forbidden currently depends mostly on which state you live in.

### The Rise and Fall (and Rise and Fall)

| Year | What Happened |
|------|---------------|
| 2015 | FCC adopts the Open Internet Order: broadband reclassified under "Title II," net neutrality rules in force |
| 2017 | New FCC majority **repeals** the rules |
| April 2024 | FCC **restores** Title II net neutrality rules |
| January 2025 | The Sixth Circuit **strikes the rules down** (*Ohio Telecom Ass'n v. FCC*), ruling the FCC lacked authority to reclassify broadband; the court applied the Supreme Court's 2024 *Loper Bright* decision, which ended judicial deference to agencies ([opinion](https://law.justia.com/cases/federal/appellate-courts/ca6/24-3449/24-3449-2025-01-02.html)) |
| Today | **No federal net neutrality rules.** The FCC did not appeal. The action has moved to **state laws**, where California's SB 822 (upheld in court) leads a patchwork of state protections, and to the question of whether Congress will ever settle it |

A note on the "Title II" jargon in that timeline: reclassifying broadband under Title II of the Communications Act meant treating ISPs as **common carriers**, the same legal category as telephone companies, which must serve everyone on equal terms. That single classification question is what the entire decade-long fight was legally *about*, and it is what the Sixth Circuit ultimately said the FCC could not decide on its own.

### Why Teach a Dead Rule?

Because the *story* is the lesson. In ten years, net neutrality went in-force → repealed → restored → struck down, without the underlying technology or arguments changing much. What changed was politics and, crucially, **administrative law**: courts now defer far less to agencies like the FCC. For anyone working in tech policy, this whiplash, along with the shift of the battleground from Washington to state capitals, is the reality of how technology law gets made.

There is also a deeper stake than streaming speeds, one former FCC chair Tom Wheeler urged people not to lose sight of: the framing of "blocking and throttling" understates the question of whether a pathway so many Americans rely on should carry any public-interest obligations at all. Net neutrality connects directly to the **digital divide** (Module 2): if internet access shapes education, employment, and even health outcomes (public-health agencies now describe broadband as a "super determinant" of health, since telehealth, job applications, and schoolwork all run through it), then who controls the terms of access is a social question, not merely a commercial one. Equal treatment of traffic keeps costs predictable for low-income users, keeps the playing field level for small content creators, and keeps ISPs out of the business of deciding what information their subscribers encounter.

### The Debate (Still Worth Having)

| Pro-Net Neutrality | Against Net Neutrality |
|-------------------|----------------------|
| Protects free speech and innovation | Allows market-based solutions |
| Prevents ISPs from favoring their own content | Enables investment in infrastructure |
| Keeps internet open and fair | Different services have different needs |
| Supports small businesses and startups | Regulation stifles innovation |

The right-hand column deserves a fair hearing too: ISPs argue that some traffic genuinely is more time-sensitive (a video call suffers from delay; an email does not), that fast lanes could fund network buildout, and that twenty years of a mostly unregulated internet produced explosive innovation. The question to sit with: which side's risks worry you more, and who should bear the burden of proof?

---

## Up Next

That wraps the module's content pages. Head back to the [module overview](copyright-law.md) for this week's reflection prompt and assignments.
