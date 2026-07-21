# Module 9: Security & Privacy 🔐

**Week 9 | Protecting Information**

---

## The Big Picture

Every day, you share personal information—sometimes knowingly, sometimes not. Your location, browsing history, purchases, and social connections create a detailed digital portrait. Who has access to this information? How is it protected? What are your rights?

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

## Security vs. Privacy

These terms are related but different:

| Concept | Definition | Focus |
|---------|------------|-------|
| **Security** | Protecting information from unauthorized access | Keeping data safe from attackers |
| **Privacy** | Controlling who has access to your information | Deciding what to share and with whom |

You can have security without privacy (your data is safe but shared widely), and privacy concerns even when security is strong (companies legally collecting your data).

:::{important} 📌 Case Study: 23andMe — When the Company Holding Your DNA Goes Bankrupt
In 2023, attackers used **credential stuffing** (trying passwords stolen from *other* breaches) to access millions of 23andMe accounts and scrape genetic-ancestry data. Then in 2025, 23andMe filed for bankruptcy — and its most valuable asset was the DNA data of some 15 million customers, which came up for sale as part of the proceedings. State attorneys general publicly urged customers to delete their data.

This one story contains the whole module: a security failure (weak authentication + reused passwords), a privacy question (who should be able to buy genetic data?), and a trust question nobody had thought to ask (what does "we protect your data" mean when the company itself can be sold?). Your DNA doesn't just identify you — it partially identifies your relatives, who never signed up at all.
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

:::{warning} The AI Twist
Generative AI has industrialized old scams. Phishing emails no longer have telltale typos; a scammer needs only seconds of audio to clone a loved one's voice; and deepfake video calls have been used to authorize multimillion-dollar corporate transfers. The defenses are old-fashioned: verify identity through a *different channel*, and be suspicious of urgency.
:::

### Protecting Yourself

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

---

## Privacy Rights and Regulations

| Regulation | Region | Key Provisions |
|------------|--------|----------------|
| **GDPR** | European Union | Right to access, delete, and port your data |
| **CCPA / CPRA** | California | Right to know what's collected and opt out |
| **State privacy laws** | ~20 US states (and counting) | California started it; comprehensive laws now cover a growing share of Americans — check yours |
| **BIPA** | Illinois 📍 | The nation's strongest biometric privacy law — right here in Illinois; it's why some face-recognition features simply aren't offered in this state |
| **TAKE IT DOWN Act (2025)** | US Federal | Criminalizes publishing nonconsensual intimate images — including AI deepfakes — and requires platforms to remove them within 48 hours ([Congress.gov](https://www.congress.gov/bill/119th-congress/senate-bill/146)) |
| **HIPAA** | US Healthcare | Protects medical information |
| **FERPA** | US Education | Protects student records |

Notice what's missing: the US still has **no comprehensive federal privacy law** — protection depends on what kind of data it is and which state you live in.

---

## Trustworthiness of Information Systems

When evaluating if a system is trustworthy, consider:

- **Transparency**: Do they explain what data they collect and why?
- **Security Practices**: How do they protect your data?
- **Data Minimization**: Do they only collect what's necessary?
- **User Control**: Can you access, correct, or delete your data?
- **Accountability**: What happens if something goes wrong?

### 🗝️ Key Terms This Week

*Security · Privacy · Phishing · Credential stuffing · Encryption · Two-factor authentication · Data breach · Biometric data · Deepfake* — see the [Glossary](../glossary.md).

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

Next week, we explore **Copyright & Law**—the legal frameworks that govern digital information.
