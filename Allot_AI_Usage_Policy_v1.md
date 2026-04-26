# Allot AI Usage Policy

**Version:** 1.0 (draft)
**Owner:** Philip Kramer · AI Enablement & Standards
**Audience:** All Allot employees and contractors using AI tools for work
**Last updated:** 2026-04-27

---

## 1. Purpose

This policy defines how Allot employees may use third-party and on-premise AI tools (Claude, ChatGPT, Copilot, etc.) for work tasks. It exists to:

1. **Unlock productivity** — make it easy to use AI safely for everyday work.
2. **Protect Allot, our customers, and our employees** — keep sensitive data out of tools that can't hold it.
3. **Set a clear bar** — so every employee knows what is allowed, what isn't, and how to escalate when in doubt.

This policy is short on purpose. The default answer to "can I use AI for X?" should be **yes, sensibly** — not a quarter-long approval cycle.

---

## 2. Approved AI tools

Use only AI tools that have been reviewed and approved by AI Enablement & Security.

| Tool | Status | Use cases |
|---|---|---|
| **Claude (Allot Team)** | ✅ Approved | Default for R&D, Product, Support, Business — code, docs, analysis, writing |
| **ChatGPT (Allot Team)** | ✅ Approved | Specific cases where Claude is unavailable; coordinate with AI Enablement |
| **GitHub Copilot (Allot Team)** | ✅ Approved | In-IDE code authoring, completion, and chat (VS Code / JetBrains) for repos approved for AI assistance. No Restricted material. |
| Personal/free AI accounts | ❌ Not approved | Never paste Allot work content into a personal tool |
| Models running on customer infrastructure | ⚠️ Case-by-case | Requires AI Enablement + Security review before use |

**License tier:** Allot uses the **Team** licensing tier for Claude, ChatGPT, and GitHub Copilot. Team gives us account-level data isolation (no training on our prompts) but does **not** give us the contractual enterprise-grade controls (e.g., custom DLP, SCIM provisioning, audit-log API). Treat Team as suitable for **Public** and **Internal** data only — never paste Confidential or Restricted material, even into a Team-licensed tool.

To request access to an approved tool, email **pkramer@allot.com** with the subject *"AI Tools License Request"* — do **not** route this through the IT Service Desk.

---

## 3. Data classification — know before you paste

This is the most important table in this policy. Memorize it.

| Classification | Examples | AI usage |
|---|---|---|
| **Public** | Published docs, public marketing copy, open-source code, anything already on allot.com | Any approved tool |
| **Internal** | Internal specs, meeting notes, non-sensitive code, normal day-to-day Allot information | Approved tools on Allot's Team licenses (Claude / ChatGPT / GitHub Copilot) |
| **Confidential** | Customer data, financial reports, unreleased product details, sensitive architecture | Only on-premise / approved private instances |
| **Restricted** | Credentials, API keys, tokens, PII, NDA-protected material, security configurations, raw customer logs | **Never use with AI tools** |

**When in doubt, treat it as Confidential** and ask in the *AI Champions - Training* Teams channel.

**The one-question test:** *"Would I read this aloud to an auditor?"* If no, sanitize before pasting.

---

## 4. Verification — V-C-A-F

Every AI output you intend to use, share, or ship must pass V-C-A-F:

| Step | Question to ask |
|---|---|
| **Verify** | Is this output factually correct? Cross-reference critical claims. |
| **Contextualize** | Does this fit Allot's specific situation, architecture, customers, and constraints? |
| **Authorize** | Am I willing to put my name on this? You own every AI output you act on. |
| **Fairness Check** | Is this treating all groups, regions, and scenarios fairly? Mandatory for anything people-related. |

For routine, low-stakes output, V-C-A may suffice. **Always include the Fairness Check** when the output involves people, decisions, or analysis that could affect groups differently.

AI is **decision support, not decision making**. AI helps you think — *you* decide.

---

## 5. Security & responsible use

- **Never** paste credentials, API keys, tokens, customer PII, or NDA-protected material into any AI tool.
- **Sanitize** logs, configs, and code snippets before sharing — replace customer identifiers with placeholders.
- **Verify AI-generated code** against OWASP Top 10 and your team's secure-coding standards before merging.
- **Disclose** when AI has been used to generate substantial portions of a report, deck, or decision-support document.
- **Document** your use of AI for any deliverable that an auditor or customer might review.
- **Do not** use AI to make final decisions on security-critical configurations, legal/compliance determinations, or anything requiring real-time accurate data the model can't access.

---

## 6. Intellectual property & compliance

- Treat AI-generated code/text as a draft authored by a junior engineer — review, adapt, and own it before committing.
- Do not paste customer-supplied confidential code or specs into any AI tool unless explicitly permitted by the customer agreement.
- Export-control rules still apply to AI outputs the same way they apply to anything else you produce at Allot.
- For AI-generated content used in customer deliverables, follow the existing Allot legal review process.

---

## 7. Incident response

If sensitive data is accidentally shared with an AI tool:

1. **Stop.** Do not continue the conversation; do not generate further outputs from the leaked context.
2. **Report immediately.** Email pkramer@allot.com and your line manager within the same business day. Include: what was pasted, which tool, when, and whether the conversation was retained.
3. **Document.** Record the incident in the AI program's incident log (Confluence page, link TBD). Include the redaction or remediation taken.
4. **Review.** AI Enablement will lead a brief post-incident review and propose a process or training change if needed.

The goal is honest reporting, not punishment. Silent incidents are the only failure mode that matters.

---

## 8. Roles

- **AI Enablement & Standards (Philip Kramer)** — owns this policy, manages tool access, runs the AI Champion program, runs incident response.
- **AI Champions** — first-line support for their team, evangelists, quality gate, feedback loop, and trainers. See the AI Champion program for details.
- **Line Managers** — make sure their teams have access to approved tools and follow this policy.
- **Every employee** — knows the data classification table, applies V-C-A-F, escalates when in doubt.

---

## 9. Where to ask questions

- **AI Champions - Training** Teams channel — for prompt help, policy questions, and general discussion.
- **pkramer@allot.com** — for tool access requests and incidents.
- **AI program Jira board (ALLOTAI)** — for feature requests and program backlog.
- **Your local AI Champion** — for first-line help in your team.

---

## 10. Changes to this policy

This is version 1.0. The policy will be reviewed at least quarterly and updated as tooling, regulation, and our experience evolves. The current version always lives at this Confluence page; older versions are kept in the page history.
