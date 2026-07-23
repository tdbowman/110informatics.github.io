# Privacy in Practice

> "Most policies quietly state that data is a transferable business asset."

---

## 🎯 In This Section

- Inventory what data is collected about you, and who collects it
- Follow the money: how the data economy turns your information into value
- Learn to audit a privacy policy in ten minutes with find-in-page
- Map the patchwork of privacy law, from GDPR to Illinois's BIPA
- Turn the trust triangle into a checklist, and try trust-by-design yourself

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
- **What happens if the company is sold?** Search for "merger," "acquisition," or "bankruptcy." Most policies quietly state that data is a transferable business asset. After [23andMe](security-privacy-and-trust.md), you know why this clause matters.
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

These five criteria are the [trust triangle](security-privacy-and-trust.md) from earlier in the module turned into a checklist, and they work in both directions: as a *user* deciding whether to adopt a service, and as a *builder* deciding how to design one. The exercise below puts you on the builder's side of the table.

:::{tip} 🛠️ Try It: Trust by Design
Pick a product concept: a health-tracking app, a payment system, a smart home device, or an educational platform. In a small group (or solo), work through the same process real product teams use:

1. **Map the data.** List every data point the product collects. Classify each by sensitivity (public, personal, sensitive) and decide how long each actually needs to be stored.
2. **Model the threats.** Brainstorm who might attack the product and how. Consider different adversaries: outside hackers, malicious insiders, competitors, even governments. Which vulnerabilities would matter most?
3. **Design for privacy.** Sketch the authentication and authorization scheme. What consent and control mechanisms do users get? What data could you simply *not collect*?
4. **Communicate trust.** Draft a plain-language summary of your data policy (apply the privacy-policy checklist above to your own draft!), and design one indicator in the interface that shows users their data status at a glance.

Then trade designs with another group and attack theirs: which threat did they miss? This is the whole module in miniature: security, privacy, and trust as *design decisions*, made before a single user signs up.
:::

---

## Up Next

That wraps the module's content pages. Head back to the [module overview](security-privacy.md) for this week's readings, reflection prompt, and assignments.
