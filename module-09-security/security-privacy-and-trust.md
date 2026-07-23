# Security, Privacy, and Trust

> "Security is necessary for privacy, but it is never sufficient."

---

## 🎯 In This Section

- Define information security and see why it is a practice, not a product
- Meet the CIA triad: confidentiality, integrity, and availability
- Distinguish security (protection) from privacy (governance)
- See how digital trust emerges where security and privacy overlap
- Watch all three fail at once in the 23andMe case study

---

## What Is Information Security?

**Information security** is the practice of protecting digital information from unauthorized access, corruption, or theft throughout its entire lifecycle. That definition (adapted from IBM's) is worth unpacking, because each phrase carries weight. "Throughout its entire lifecycle" means security covers far more than the moment a hacker attacks: it includes how data is collected, stored, transmitted, used, and eventually deleted. And "practice" means security is something organizations *do* continuously, not a product they buy once. It spans the physical security of hardware and storage devices, administrative rules about who may access what, the technical security of software, and the organizational policies and procedures that hold it all together. The weakest of those layers, very often the human one, sets the real level of protection.

### The CIA Triad

Security professionals summarize their goals with three properties, remembered by the acronym **CIA** (no relation to the agency):

| Property | The Question It Asks | Example Failure |
|----------|---------------------|-----------------|
| **Confidentiality** | Can only authorized people see this data? | A breach exposes customer records |
| **Integrity** | Is the data accurate and unaltered? | An attacker (or a bug) silently changes grades in a registrar database |
| **Availability** | Can authorized people get to the data when they need it? | Ransomware locks a hospital out of its own patient files |

```{figure} images/cia-triad.svg
:alt: Triangle diagram of the CIA triad. Three cards sit at the corners of a triangle labeled Security. Confidentiality asks whether only authorized people can see the data, with a breach exposing customer records as the example failure. Integrity asks whether the data is accurate and unaltered, with silently changed grades as the example failure. Availability asks whether authorized people can reach the data when needed, with ransomware locking a hospital out of patient files as the example failure.
:width: 100%
:name: fig-cia-triad

Security is the whole triangle: a system that never leaks data but corrupts it, or one that goes down when you need it, has still failed.
```

The triad is useful because it shows that security is more than secrecy. A system that never leaks data but corrupts it, or one that is perfectly confidential but goes down during finals week, has still failed. When you read about a security incident, try asking which of the three properties was violated. Ransomware, for instance, is primarily an attack on *availability*; a deepfake is an attack on *integrity* of information itself.

---

## Security vs. Privacy

These terms are related but different:

| Concept | Definition | Focus |
|---------|------------|-------|
| **Security** | Protecting information from unauthorized access | Keeping data safe from attackers |
| **Privacy** | Controlling who has access to your information | Deciding what to share and with whom |

You can have security without privacy (your data is safe but shared widely), and privacy concerns even when security is strong (companies legally collecting your data).

The privacy profession's own definition, from the International Association of Privacy Professionals (IAPP), traces back to a famous 1890 law review phrase: privacy is "the right to be let alone," freedom from interference or intrusion. **Information privacy** is the narrower, modern version: the right to have some control over how your personal information is collected and used. Privacy is about *governance* (policies ensuring personal information is collected, shared, and used appropriately), while security is about *protection* (defending data from attack and exploitation). Security is necessary for privacy, but it is never sufficient. A company can encrypt your data flawlessly and still sell it to anyone who pays.

### The Third Corner: Trust

Where security and privacy overlap, a third concept emerges: **digital trust**. Frameworks from IBM, KPMG, and the World Economic Forum all converge on a similar idea: trust sits at the intersection of security and privacy, reinforced by transparency and honesty, ethics and integrity, accountability, quality, availability, and resiliency. In plain terms, you trust a system when it protects your data (security), respects your choices about that data (privacy), tells you honestly what it is doing (transparency), and answers for its failures (accountability).

Why does this matter beyond feelings? Because trust is measurable economic infrastructure. McKinsey's research on digital trust finds that consumers increasingly change providers, abandon purchases, and pay premiums based on data practices. For the systems you will build or manage in your career, trust is a design requirement, not a public relations afterthought. Keep this triangle in mind as you read the case study below: it is a story about all three corners failing at once.

:::{important} 📌 Case Study: 23andMe, or When the Company Holding Your DNA Goes Bankrupt
In 2023, attackers used **credential stuffing** (trying passwords stolen from *other* breaches) to access millions of 23andMe accounts and scrape genetic-ancestry data. Then in 2025, 23andMe filed for bankruptcy, and its most valuable asset was the DNA data of some 15 million customers, which came up for sale as part of the proceedings. State attorneys general publicly urged customers to delete their data.

This one story contains the whole module: a security failure (weak authentication + reused passwords), a privacy question (who should be able to buy genetic data?), and a trust question nobody had thought to ask (what does "we protect your data" mean when the company itself can be sold?). Your DNA identifies more than you alone; it partially identifies your relatives, who never signed up at all.
:::

---

## Up Next

Now that the concepts are straight, let's look at how attacks actually work, and how to stop them: [Common Security Threats and Defenses](threats-and-defenses.md).
