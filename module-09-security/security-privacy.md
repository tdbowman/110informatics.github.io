# Module 9: Security & Privacy 🔐

**Week 9 | Protecting Information**

---

## The Big Picture

Every day, you share personal information, sometimes knowingly, sometimes not. Your location, browsing history, purchases, and social connections create a detailed digital portrait. Who has access to this information? How is it protected? What are your rights?

This week, we explore the crucial intersection of security and privacy in the digital age.

### 🎯 What You'll Learn

- Understand the difference between security and privacy
- Learn common cybersecurity threats and how to protect yourself
- Explore data collection practices and privacy policies
- Consider the trade-offs between convenience and privacy
- Evaluate your own digital privacy practices

### 🧠 Big Questions to Consider

- What personal data do you share without realizing it?
- Who benefits from collecting your data?
- Is privacy a right or a privilege?
- When is surveillance acceptable?
- What happens to your data when a company dies?

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

## Common Security Threats

### Types of Attacks

| Threat | Description | Protection |
|--------|-------------|------------|
| **Phishing** | Fake emails/websites tricking you into sharing info | Verify sender, don't click suspicious links |
| **Malware** | Software that damages or gains access to systems | Use antivirus, keep software updated |
| **Social Engineering** | Manipulating people to reveal information | Be skeptical, verify requests |
| **Password Attacks** | Guessing, stealing, or reusing passwords (see 23andMe above!) | Use strong, unique passwords |
| **Data Breaches** | Companies losing your data to hackers | Use different passwords, monitor accounts |
| **AI-Enabled Scams** 🤖 | Deepfake video calls, cloned voices of family members, flawlessly written phishing | Verify through a second channel; agree on family "code words" |

The table is the summary. The subsections below slow down and look at how the most common attacks actually work, because understanding the mechanism is what makes the defenses make sense.

### How Phishing Actually Works

Phishing succeeds not because victims are foolish but because the attack is engineered around how busy people read email. A typical phishing attack unfolds in five steps:

1. **The lure.** You receive a message that appears to come from an organization you trust: your bank, your university IT department, a delivery service, a streaming account. Attackers copy real logos, footers, and writing style, and they often *spoof* the sender name so the "From" line looks right even when the underlying address is not.
2. **The hook.** The message gives you an urgent reason to act: your account will be suspended, a package could not be delivered, someone signed in from an unknown device, a document needs your signature today. Urgency is the point; it short-circuits the pause in which you would normally get suspicious.
3. **The fake page.** The link leads to a counterfeit login page, often pixel-perfect, at an address that is *almost* right (think `university-login-verify.com` instead of your university's real domain). Your browser dutifully renders it; nothing "looks hacked."
4. **The harvest.** You type your username and password. The page may even forward you to the real site afterward so nothing seems wrong. Sophisticated kits now capture two-factor codes in real time too, replaying them before they expire.
5. **The exploitation.** Within minutes to days, the attacker logs in as you: reading email, resetting other accounts (your inbox is the master key to everything), moving money, or using your account to phish your contacts, who trust messages from you.

The defense follows from the mechanism: never log in from a link in a message. If your bank emails you about a problem, close the email and type the bank's address yourself or use its app. That one habit defeats the entire attack chain.

### The Psychology of Social Engineering

Phishing is one instance of **social engineering**: manipulating people, rather than machines, to defeat security. Social engineers are applied psychologists, and they lean on a small set of reliable levers:

- **Urgency**: "Act in the next 30 minutes or lose access." Time pressure suppresses skepticism, which is precisely why legitimate organizations rarely impose it.
- **Authority**: Messages impersonate bosses, professors, IT departments, the IRS, or the police, because most people comply with authority reflexively. The classic campus version is the "gift card scam": an email seemingly from a department chair asking a student worker to urgently buy gift cards.
- **Familiarity and trust**: Attacks arrive through hijacked accounts of friends, or reference real details about you scraped from social media, so the request feels personal. This is also why AI voice cloning is so dangerous: familiarity is exactly what it counterfeits.
- **Fear and greed**: Threats ("your account was used for fraud") and windfalls ("you've been selected for a scholarship refund") both work, because strong emotion in either direction crowds out careful reading.

The countermeasure is procedural, not emotional: verify through a **different channel**. If "your bank" calls, hang up and call the number on your card. If "your grandmother" needs money urgently by voice call, call her back on her known number. No legitimate institution objects to verification; attackers depend on your not doing it.

### Password Attacks

Attackers rarely "guess" passwords the way movies depict. They use three industrial-scale techniques:

- **Brute force**: software tries every possible combination. Length is the defense; each added character multiplies the search space, which is why a 16-character passphrase is astronomically harder to crack than an 8-character one, no matter how many symbols the short one has.
- **Dictionary attacks**: instead of every combination, the software tries millions of *likely* passwords: real words, names, dates, keyboard patterns, and previously leaked passwords, along with common mutations (`P@ssw0rd1!` fools no one; the mutation rules are in the cracking software).
- **Credential stuffing**: the attack that hit 23andMe. Attackers take username-password pairs leaked from one breach and automatically try them on hundreds of other sites. It works because people reuse passwords. If your streaming-service password is also your email password, then a breach at the weakest site you ever signed up for becomes a breach of everything.

Understanding these three explains the standard advice. Long beats complex (defeats brute force). Random beats memorable-pattern (defeats dictionaries). *Unique per site beats everything* (defeats credential stuffing), and since no human can memorize a hundred unique random passwords, a password manager is not a convenience but the actual defense.

### Ransomware in Plain Language

**Ransomware** is malware that encrypts the victim's files and demands payment for the key. In effect, the attacker steals nothing and instead locks you out of your own data: an availability attack, in CIA-triad terms. Modern ransomware gangs run "double extortion": before encrypting, they copy the data and threaten to publish it, so even victims with good backups face pressure to pay. Targets are chosen for desperation, which is why hospitals, school districts, city governments, and small businesses appear so often in the headlines; they can least afford downtime. Ransomware usually arrives through the doors this module has already described: a phishing email, a reused password on a remote-access system, or unpatched software. For individuals, the defense is the same boring toolkit as everything else, with one addition: **backups you have actually tested**, kept somewhere the malware cannot reach (offline, or in a versioned cloud service).

:::{warning} The AI Twist
Generative AI has industrialized old scams. Phishing emails no longer have telltale typos; a scammer needs only seconds of audio to clone a loved one's voice; and deepfake video calls have been used to authorize multimillion-dollar corporate transfers. The defenses are old-fashioned: verify identity through a *different channel*, and be suspicious of urgency.
:::

### Protecting Yourself: Defense in Depth

Security professionals design systems on the assumption that any single defense will eventually fail, so they layer defenses: **defense in depth**. The same principle scales down to your personal digital life. Each layer below covers for the failure of the ones above it:

1. **Strong, unique passwords** (a password manager makes this practical): so one breached site cannot cascade into all your accounts.
2. **Multi-factor authentication (MFA/2FA)** on anything important, especially email: so a stolen password alone is not enough to get in. An authenticator app or hardware key is stronger than texted codes, but any second factor beats none.
3. **Software updates**, applied promptly: most malware exploits holes that were patched months earlier; updating closes the door before opportunistic attackers arrive.
4. **Backups** of anything you cannot afford to lose: so ransomware, theft, or plain hardware failure becomes an inconvenience rather than a catastrophe.
5. **Skepticism** as the always-on outer layer: verify unexpected requests through a second channel, type addresses instead of clicking links, and treat urgency itself as a red flag.

**Password Best Practices:**
- Use long, unique passwords for each account
- Consider a password manager
- Enable two-factor authentication (2FA)
- Never share passwords

**Online Safety:**
- Check for HTTPS in the browser
- Be cautious on public WiFi
- Keep software updated
- Back up important data

No single layer is heroic, and none is optional. Notably, everything on this list is free or nearly free; the barrier is habit, not money.

---

## This Week's Journey

### 📚 Core Readings & Videos

| Resource | Type | Notes |
|----------|------|-------|
| [Have I Been Pwned?](https://haveibeenpwned.com/) | Interactive | Check whether your accounts appear in known breaches |
| [I Used Apple AirTags, Tiles and a GPS Tracker to Watch My Husband's Every Move](https://www.nytimes.com/2022/02/11/technology/airtags-gps-surveillance.html) | Article | Kashmir Hill on consumer tracking tech |
| [Electronic Frontier Foundation: Privacy](https://www.eff.org/issues/privacy) | Resource | The digital-rights perspective |

### 🤔 Make You Think (Optional)

- How much is your personal data worth to advertisers?
- The difference between European (GDPR) and US privacy laws
- Look up your state: does it have a comprehensive privacy law yet?

---

## Privacy in Practice

### What's Being Collected?

| Type | Examples | Who Collects |
|------|----------|--------------|
| **Location Data** | GPS, WiFi, cell towers | Apps, phone companies, advertisers |
| **Browsing History** | Sites visited, searches | Browsers, search engines, ISPs |
| **Purchase History** | What you buy, when, where | Retailers, credit cards, banks |
| **Social Data** | Friends, interests, posts | Social media platforms |
| **Biometric Data** | Fingerprints, face, voice, DNA | Phones, security systems, testing companies |
| **AI Conversations** 🤖 | What you tell chatbots | AI companies (read those data policies!) |

### The Data Economy

Your data is valuable:
- **Targeted Advertising**: Companies pay to reach specific audiences
- **Product Development**: Data reveals what people want
- **Risk Assessment**: Insurance, loans, and employment decisions
- **Research**: Academic and market research
- **AI Training**: Your posts, photos, and conversations may train tomorrow's models

:::{warning} "If you're not paying for the product, you are the product."
Free services often monetize your data. Consider what you're really trading.
:::

### How to Read a Privacy Policy (Without Reading All of It)

The document that governs the trade above is the privacy policy, and almost nobody reads it; researchers have estimated it would take weeks per year to read the policies of every service an average person uses. You do not need to read every word. You need to interrogate the document with a few pointed questions, most of which can be answered with the browser's find-in-page function:

- **What do they collect?** Search for "collect." Distinguish data you provide (name, email) from data gathered automatically (location, contacts, device identifiers, browsing behavior). Automatic collection is where surprises live.
- **Who do they share it with?** Search for "share," "third parties," "partners," and "affiliates." "We do not sell your data" can coexist with extensive "sharing" with "partners"; the vocabulary is chosen carefully.
- **How long do they keep it?** Search for "retain." "As long as necessary" with no upper bound is a yellow flag.
- **What happens if the company is sold?** Search for "merger," "acquisition," or "bankruptcy." Most policies quietly state that data is a transferable business asset. After 23andMe, you know why this clause matters.
- **What are your controls?** Can you download your data, delete it, and opt out of targeted advertising or AI training? Is deletion actually deletion, or "deactivation"?
- **Watch for weasel words.** "May," "including but not limited to," and "such as" make lists open-ended; a policy that "may share data with partners including advertisers" has promised you almost nothing.

Reading policies this way turns a wall of legalese into a ten-minute audit, and it is exactly the transparency test you will apply in the Trustworthiness section below.

---

## Privacy Rights and Regulations

| Regulation | Region | Key Provisions |
|------------|--------|----------------|
| **GDPR** | European Union | Right to access, delete, and port your data |
| **CCPA / CPRA** | California | Right to know what's collected and opt out |
| **State privacy laws** | ~20 US states (and counting) | California started it; comprehensive laws now cover a growing share of Americans; check yours |
| **BIPA** | Illinois 📍 | The nation's strongest biometric privacy law, right here in Illinois; it's why some face-recognition features simply aren't offered in this state |
| **TAKE IT DOWN Act (2025)** | US Federal | Criminalizes publishing nonconsensual intimate images, including AI deepfakes, and requires platforms to remove them within 48 hours ([Congress.gov](https://www.congress.gov/bill/119th-congress/senate-bill/146)) |
| **HIPAA** | US Healthcare | Protects medical information |
| **FERPA** | US Education | Protects student records |

One thing is missing from this table: the US still has **no comprehensive federal privacy law**. Protection depends on what kind of data it is and which state you live in.

---

## Trustworthiness of Information Systems

When evaluating if a system is trustworthy, consider:

- **Transparency**: Do they explain what data they collect and why?
- **Security Practices**: How do they protect your data?
- **Data Minimization**: Do they only collect what's necessary?
- **User Control**: Can you access, correct, or delete your data?
- **Accountability**: What happens if something goes wrong?

These five criteria are the trust triangle from earlier in the module turned into a checklist, and they work in both directions: as a *user* deciding whether to adopt a service, and as a *builder* deciding how to design one. The exercise below puts you on the builder's side of the table.

:::{tip} 🛠️ Try It: Trust by Design
Pick a product concept: a health-tracking app, a payment system, a smart home device, or an educational platform. In a small group (or solo), work through the same process real product teams use:

1. **Map the data.** List every data point the product collects. Classify each by sensitivity (public, personal, sensitive) and decide how long each actually needs to be stored.
2. **Model the threats.** Brainstorm who might attack the product and how. Consider different adversaries: outside hackers, malicious insiders, competitors, even governments. Which vulnerabilities would matter most?
3. **Design for privacy.** Sketch the authentication and authorization scheme. What consent and control mechanisms do users get? What data could you simply *not collect*?
4. **Communicate trust.** Draft a plain-language summary of your data policy (apply the privacy-policy checklist above to your own draft!), and design one indicator in the interface that shows users their data status at a glance.

Then trade designs with another group and attack theirs: which threat did they miss? This is the whole module in miniature: security, privacy, and trust as *design decisions*, made before a single user signs up.
:::

### 🗝️ Key Terms This Week

*Security · Privacy · Phishing · Credential stuffing · Encryption · Two-factor authentication · Data breach · Biometric data · Deepfake*: see the [Glossary](../glossary.md).

---

## 📝 This Week's Assignments

| Assignment | Due | Notes |
|------------|-----|-------|
| Weekly Reflection | Friday by class | Connect to security/privacy concepts |
| Research Questions | Should be approved | Begin working on your report |

:::{tip} Reflection Prompt
Conduct a "privacy audit" of yourself. Check what apps have access to your location, review a privacy policy of a service you use, or check if your data has been in a breach at [Have I Been Pwned](https://haveibeenpwned.com/). What did you discover? What will you change?
:::

---

## Looking Ahead

Next week, we explore **Copyright & Law**: the legal frameworks that govern digital information.
