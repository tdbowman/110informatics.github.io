# Common Security Threats and Defenses

> "Phishing succeeds not because victims are foolish but because the attack is engineered around how busy people read email."

---

## 🎯 In This Section

- Survey the most common attack types, from phishing to AI-enabled scams
- Walk through the five steps of a phishing attack, and the one habit that defeats it
- Learn the psychological levers social engineers pull, and the procedural countermeasure
- Understand the three industrial-scale password attacks and why unique passwords beat everything
- Layer your personal defenses with defense in depth

---

## Common Security Threats

### Types of Attacks

| Threat | Description | Protection |
|--------|-------------|------------|
| **Phishing** | Fake emails/websites tricking you into sharing info | Verify sender, don't click suspicious links |
| **Malware** | Software that damages or gains access to systems | Use antivirus, keep software updated |
| **Social Engineering** | Manipulating people to reveal information | Be skeptical, verify requests |
| **Password Attacks** | Guessing, stealing, or reusing passwords (see the [23andMe case study](security-privacy-and-trust.md)!) | Use strong, unique passwords |
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

```{figure} images/phishing-anatomy.svg
:alt: Flow diagram of the five steps of a phishing attack. Step one, the lure: a message that looks like it comes from an organization you trust. Step two, the hook: an urgent reason to act right now. Step three, the fake page: a near-perfect login page at an almost-right address. Step four, the harvest: you type your password, and kits can capture two-factor codes too. Step five, the exploitation: the attacker logs in as you and your inbox becomes the master key. A green banner below states the defense: never log in from a link in a message; type the address yourself or use the app.
:width: 100%
:name: fig-phishing-anatomy

Every step depends on the one before it, which is why the single habit of never logging in from an emailed link breaks the entire chain.
```

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
- **Credential stuffing**: the attack that hit [23andMe](security-privacy-and-trust.md). Attackers take username-password pairs leaked from one breach and automatically try them on hundreds of other sites. It works because people reuse passwords. If your streaming-service password is also your email password, then a breach at the weakest site you ever signed up for becomes a breach of everything.

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

```{figure} images/defense-in-depth.svg
:alt: Diagram of defense in depth as five layered shields standing between an attacker and your data. From the outside in: skepticism, which verifies requests through a second channel; software updates, which patch known holes; unique passwords, which keep one breach from cascading; multi-factor authentication, which makes a stolen password insufficient on its own; and tested backups, the last resort that turns ransomware into an inconvenience. A dashed arrow from the attacker is stopped as it crosses the layers before reaching the data.
:width: 100%
:name: fig-defense-in-depth

No single layer is heroic: each one exists to catch what the layer before it missed.
```

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

## Up Next

Attacks are only half the story. The other half is what happens to your data when nothing goes "wrong" at all: [Privacy in Practice](privacy-in-practice.md).
