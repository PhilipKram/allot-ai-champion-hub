# AI Champion Enablement — Pre-Workshop Preparation

**Complete before attending the 2-day training**
**Estimated time:** 4 hours (self-paced, can be spread across several days)
**Deadline:** Start at least 1 week before the workshop (tool access requests may take several days)
**Submission:** Part 5 (the Readiness Exam) must be submitted to the AI Champions Teams channel at least **48 hours before Day 1**. Your facilitator reviews submissions to surface common gaps and schedule 30-min coaching calls where needed.

---

## Why Pre-Work?

The 2-day workshop is hands-on and fast-paced. This pre-work ensures everyone starts from a common baseline so we can skip the basics and dive straight into practical skills. Completing it will make the workshop significantly more valuable for you.

---

## Part 1: Tool Setup & Access (30 min)

Complete these before the workshop so you're ready to go on Day 1.

### Checklist

> **Start this part at least 1 week early.** IT ticket resolution can take 2–3 business days. Don't let tool access block your preparation.

- [ ] **Claude access** — Verify you can log in at the approved Allot instance. If you don't have access, submit a request via IT Service Desk **now** (reference: AI Tools License Request).
- [ ] **GitHub Copilot** (R&D participants) — Confirm Copilot is enabled in your IDE. Check: IDE Settings → Extensions → GitHub Copilot → Status: Active.
- [ ] **Bookmark key resources:**
  - Allot AI usage policy (Confluence) — **you will need this for Part 5**
  - AI Champions Teams channel
  - AI program Jira board (ALLOTAI)
- [ ] **Bring to the workshop:**
  - Your laptop with approved AI tools installed
  - 2–3 real work examples you'd like to try with AI (code snippets, documents, reports, tickets — sanitized per the Data Classification table below)

---

## Part 2: AI Foundations — Core Concepts (45 min)

Read through these concepts. You don't need to memorize them — the goal is familiarity so we can build on them during the workshop.

### What is a Large Language Model (LLM)?

An LLM is a machine learning model trained on vast amounts of text data. It predicts the most likely next word (token) given a sequence of input words. Key points:

- **It generates text, not truth.** Output is statistically probable, not guaranteed to be correct.
- **It has no memory between conversations.** Each new conversation starts fresh unless context is provided.
- **It works with a "context window."** There's a limit to how much text it can process at once (think of it as working memory).
- **It can follow instructions.** Modern LLMs are fine-tuned to respond helpfully to prompts.

### Key Terminology

| Term | What It Means | Why It Matters |
|---|---|---|
| **Prompt** | The text you send to the AI | Better prompts → better outputs |
| **Token** | A chunk of text (~4 characters or ~¾ of a word) | Determines cost and context limits |
| **Context window** | Maximum tokens the model can handle at once | Limits how much info you can provide |
| **Hallucination** | AI generating plausible but incorrect information | Always verify critical outputs |
| **Temperature** | Controls randomness (0 = deterministic, 1 = creative) | Lower for facts, higher for brainstorming |
| **System prompt** | Hidden instructions that shape AI behavior | Used to create consistent personas |
| **Few-shot learning** | Providing examples in your prompt to guide output | One of the most effective prompting techniques |
| **RAG (Retrieval-Augmented Generation)** | Feeding relevant documents to AI before asking a question | Grounds AI in your actual data |

### Data Classification & AI — Know Before You Paste

This table governs what you can and cannot share with AI tools. **Memorize it** — as a champion, your team will ask you about this constantly.

| Data Classification | AI Usage | Examples |
|---|---|---|
| **Public** | Any approved tool | Published docs, open-source code, public website content |
| **Internal** | Approved tools with enterprise agreement | Internal specs, meeting notes, non-sensitive code |
| **Confidential** | Only on-premise/approved private instances | Customer data, financial reports, unreleased product details |
| **Restricted** | **Never use with AI tools** | Credentials, API keys, PII, NDA-protected material, security configs |

**When in doubt, treat it as Confidential.** You can always ask in the Champions Teams channel.

> **Note:** Different AI tools have different security boundaries. For example, Claude (enterprise) may accept Internal data, while Copilot operates only on code context. The workshop will cover tool-specific rules in detail — for pre-work, use the table above as your baseline.

### The V-C-A-F Verification Framework — Preview

During the workshop, you'll learn and practice the **V-C-A-F framework** — the core habit every champion teaches their team. Here's a preview:

| Step | Question to Ask |
|---|---|
| **Verify** | Is this output factually correct? (Cross-reference against known data) |
| **Contextualize** | Does this fit Allot's specific situation? (AI doesn't know our business) |
| **Authorize** | Am I willing to put my name on this? (You own every AI output you use) |
| **Fairness Check** | Is this treating all groups/scenarios fairly? (AI can reflect biases from training data — critical for people-related analysis) |

For routine tasks, V-C-A may suffice. **Always include the Fairness Check** when the output involves people, decisions, or analysis that could impact groups differently.

**Apply this during Exercise 4 below** — when you spot mistakes, you're already doing V-C-A-F.

### How AI Fits at Allot

Allot is a network security and intelligence company. AI tools help us:
- **Accelerate development** — code generation, test writing, code review
- **Improve documentation** — technical writing, summarization, translation
- **Enhance analysis** — log analysis, pattern detection, report generation
- **Streamline operations** — ticket management, knowledge base creation, process automation

As a champion, you'll help your team find the right use cases and use AI tools effectively and safely.

---

## Part 3: First Steps with AI (30 min)

Two short exercises to warm up before the exam. The goal is to get comfortable with the interaction, not to produce perfect results.

### Exercise 3.1: Draft an Inigo-Format Prompt (20 min)

Think about a repetitive task in your daily work. Turn it into a prompt using the **Inigo Montoya 4-part frame** — the same structure you'll be drilled on during Day 1.

A good prompt is basically how you introduce yourself properly in any meeting:

```
[1. Greeting / framing]    Why are we here — the task framing.
[2. Who am I]               Your role, team, and relevant context about you.
[3. Who are you / context]  Who the AI should be + what we're looking at together.
[4. Desired outcome]        What should exist at the end (format + structure).
[5. Constraints]            Optional — what to avoid or assume.
```

Write your prompt, label each part explicitly, and run it against Claude. Save it — you'll use it in Part 5 (the Readiness Exam) and again on Day 1 Session 3.

### Exercise 3.2: Spot the Mistakes — Apply V-C-A-F (10 min)

Ask Claude a factual question about something you know deeply (your team's tech stack, a protocol you work with daily, or a tool you use). Then apply V-C-A-F:

- **Verify:** Did it get the facts right? Where did it hallucinate?
- **Contextualize:** Does the answer account for Allot's specific setup, or is it generic?
- **Authorize:** Would you send this output to your manager as-is? What would you change?
- **Fairness Check:** If the question touched on people or groups, did it stereotype or exclude?

**This is the most important Champion skill:** knowing when to trust AI output and when to verify.

---

## Part 4: Security Sandbox — The Sanitization Challenge (15 min)

As a champion, you'll be the "Quality Gate" for AI usage on your team. Practice identifying and removing sensitive data before it reaches an AI tool.

**Instructions:** Below is a raw transcript from an internal Allot meeting. It contains **Restricted** and **Confidential** data that must never be shared with AI tools. Rewrite or redact the transcript so it is safe to send to an AI for summarization.

**Raw Transcript:**
> "Okay, let's start. For Project Firehawk, we're integrating the new deep-packet inspection module for our client, Verizon. To test the uplink, use the temporary staging API Key: AKIA-8821-ALLOT-TR-99. If you run into auth issues, contact our lead dev, Sarah Jenkins (s.jenkins@allot.com). Also, remember that the internal architecture specs for Firehawk are currently under an NDA and should not be discussed outside this group."

**Your sanitized version:**
*(Write it out — what did you remove or replace? Why?)*

---

## Part 5: Champion Readiness Exam (90 min) — **REQUIRED SUBMISSION**

This exam replaces the old reflection/policy questions. It's designed to show — through actual artifacts, not multiple-choice trivia — that you understand the AI tools, when to use them, and how to verify their output.

**Submit one document to the AI Champions Teams channel at least 48 hours before Day 1.** Your facilitator reviews submissions and schedules a 30-min coaching call only for anyone flagged as "Needs work" in two or more sections.

---

### Section A — Knowledge Check (15 min)

Pick the best answer. For each, be prepared to explain your reasoning on Day 1.

**A1.** You're debugging a function that handles customer IP addresses in production logs. Before pasting the code into Claude, you should:
- a) Paste it as-is — Allot has an enterprise agreement with Claude
- b) Remove only the IP addresses
- c) Remove IPs and any customer identifiers; note in the prompt that IPs were masked
- d) Never paste customer-related code into Claude — only Copilot in the IDE

**A2.** You need to classify 500 support tickets by severity. Which model is most appropriate?
- a) Opus with 1M context — for maximum quality
- b) Sonnet with 200k context — the day-to-day default
- c) Haiku — fast and cheap for repetitive classification
- d) Any model works equally well

**A3.** You default to Opus with 1M context for "quality." What's the main risk?
- a) Opus doesn't support 1M context
- b) Higher cost, slower responses, and signal dilution from irrelevant earlier content
- c) 1M context is less accurate than 200k
- d) Allot's license doesn't cover 1M

**A4.** A teammate wants to paste a customer's production API key into Claude to debug why it's being rejected. You say:
- a) OK if it's the test environment
- b) OK if other parts of the request are sanitized
- c) Never — credentials are Restricted. Use a dummy key and describe the error symptoms.
- d) OK if they delete the conversation afterward

**A5.** You find a new AI Chrome extension that summarizes web pages. It's not on the approved tools list. Can you use it for Allot work?
- a) Yes — it only sees public web pages
- b) Yes — personal browsing is outside policy scope
- c) No — unapproved tools bypass Allot's data governance. Request it via IT.
- d) Yes, if you don't paste internal content

**A6.** You ask Claude *"What version of our DPI module shipped in 2024?"* It confidently answers "v7.2." You should:
- a) Trust and use — Claude has broad general knowledge
- b) Verify against internal release notes before using
- c) Trust — confidence correlates with accuracy
- d) Ask again with more detail to confirm

**A7.** You're drafting performance review feedback for a team member using AI. Which V-C-A-F step is *most* critical?
- a) Verify — facts must be right
- b) Contextualize — must match Allot's review format
- c) Authorize — you own the output
- d) Fairness Check — people-related output, bias risk is highest here

**A8.** A teammate asks *"can I upload this 400-page PDF into the chat?"* Your answer should touch on:
- a) Model choice (Opus for deep reasoning) and context size (200k likely enough)
- b) Whether the PDF contains Confidential/Restricted data
- c) Whether summarize-then-analyze chunking would work better
- d) All of the above

---

### Section B — Sanitization Task (10 min)

Take the Firehawk transcript from Part 4. Submit:
- Your sanitized version
- A 3–5 line rationale: **what did you remove, why, and what did you replace it with?**

---

### Section C — Inigo Prompt Construction (20 min)

**Scenario:** You need Claude to turn a 2-page customer feature request into a structured user story with acceptance criteria, ready for your Product team to triage.

Write a prompt using the 4-part Inigo frame. Label each part explicitly:

```
[1. Greeting / framing]
[2. Who am I]
[3. Who are you / shared context]
[4. Desired outcome]
[5. Constraints] (optional)
```

Run your prompt against a realistic, sanitized example. Submit:
- The labeled prompt
- The first-run output
- A 2-line self-critique: *what would you change for v2?*

---

### Section D — V-C-A-F on Seeded Output (15 min)

Below is a Claude-generated response to the prompt *"Analyze this customer support team's ticket resolution metrics and identify patterns."* The input data said: *avg resolution time 6.1 hours, 200 tickets, mixed enterprise and SMB customers, Allot is a global company headquartered in Israel with its own defined SLAs.*

**Seeded response (contains deliberate errors — your job is to find them):**

> Based on the data, the team's average resolution time is 4.2 hours, which is strong. Enterprise customers are served faster than SMB customers, which makes sense since they pay more. Looking at the engineer breakdown, male engineers on the team resolve tickets 15% faster than female engineers, suggesting a training gap for the female staff. I recommend adopting the industry-standard SLAs used at large US tech companies like Salesforce and Google, where first-response time is under 1 hour.

Apply V-C-A-F and submit your findings as a table:

| Step | Finding |
|---|---|
| Verify | |
| Contextualize | |
| Authorize | |
| Fairness Check | |

*(There are at least 3 distinct issues across the layers. Find them all.)*

---

### Section E — Hands-On Chain & Reflection (20 min)

Build a 3-step prompt chain in Claude using one of the real work examples you prepared in Part 1:

1. **Extract:** pull structured data from your raw input (meeting note, bug report, email, etc.)
2. **Analyze:** classify, prioritize, or score the extracted data
3. **Format:** produce the final deliverable (ticket, table, summary)

Each prompt should follow the Inigo 4-part frame.

Submit:
- All 3 prompts (labeled)
- The final output
- A 3-line reflection: *where did V-C-A-F catch something? What surprised you?*

---

### Self-Assessment Rubric

Score yourself honestly. If you land in "Needs work" on two or more sections, your facilitator will reach out to schedule a 30-min coaching call.

| Section | Mastery (A) | Proficient (B) | Needs work (C) |
|---|---|---|---|
| A. Knowledge | 7–8 correct | 5–6 correct | <5 correct |
| B. Sanitization | All sensitive data removed; rationale clear | Most removed; rationale thin | Gaps in identification |
| C. Inigo prompt | All 4 parts explicit and distinct; output on-target | Parts present but blurred | Missing parts or vague |
| D. V-C-A-F | Caught all 3 issues across layers | Caught 2 | Caught 1 or 0 |
| E. Chain | Works end-to-end; V-C-A-F applied | Works but no verification | Chain doesn't hold together |

**Answer key for Section A:** submitted with your facilitator, not self-graded. You'll review it together on Day 1.

---

## Part 6: Domain-Specific Deep Dive (30 min)

Pick **one** task from your track and complete it. The goal is to have a real domain touchpoint with AI before Day 2's parallel tracks — not to cover everything.

### For R&D / Engineering
Use Claude to write a unit test for a function you maintain. Apply V-C-A-F to the output. Note one thing the AI got right and one thing it got wrong.

### For Product / Business
Use Claude to draft a user story (with acceptance criteria) from a feature description you have. Apply V-C-A-F. Note what you had to fix.

### For Security
Use Claude to explain a recent CVE relevant to your work in plain language for a non-security audience. Apply V-C-A-F. Note where it oversimplified or got a detail wrong.

**Bring the output and your V-C-A-F notes to Day 2.** Your track lead will call on 2–3 volunteers to share.

---

## Pre-Work Completion Checklist

Before Day 1, confirm:

- [ ] I have access to approved AI tools and they work (Part 1 — start 1 week early!)
- [ ] I've read the core concepts, data classification table, and V-C-A-F preview (Part 2)
- [ ] I've completed Exercises 3.1 (Inigo draft prompt) and 3.2 (V-C-A-F on a factual question) (Part 3)
- [ ] I've completed the Sanitization Challenge (Part 4)
- [ ] **I've submitted the Readiness Exam to the AI Champions Teams channel at least 48 hours before Day 1** (Part 5)
- [ ] I've completed one domain-specific deep dive task (Part 6)
- [ ] I'm bringing 2–3 real work examples (sanitized per the Data Classification table) to Day 1

**Time budget:** ~4 hours total (30 min tools + 45 min foundations + 30 min practice + 15 min sanitization + 90 min exam + 30 min domain deep-dive + 20 min buffer).

---

## Questions?

If you get stuck during pre-work or have questions:
- Post in the AI Champions Teams channel
- Contact your AI Champion program lead
- Questions are welcome — that's what the workshop is for

**See you at the training!**
