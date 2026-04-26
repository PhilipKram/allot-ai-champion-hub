# AI Champion Enablement — Pre-Workshop Preparation

**Complete before attending the 2-day training**
**Estimated time:** 2.5 hours (self-paced, can be spread across several days)
**Deadline:** Start at least 1 week before the workshop (tool access requests may take several days)
**Certification:** The **Champion Certification Exam** is post-training — complete it within 7 days of Day 2 (by **Mon 11 May 2026 at 10:00 IL**). Details in the training hub.

---

## Why Pre-Work?

The 2-day workshop is hands-on and fast-paced. This pre-work ensures everyone starts from a common baseline so we can skip the basics and dive straight into practical skills. Completing it will make the workshop significantly more valuable for you.

---

## Part 1: Tool Setup & Access (30 min)

Complete these before the workshop so you're ready to go on Day 1.

### Checklist

> **Start this part at least 1 week early.** IT ticket resolution can take 2–3 business days. Don't let tool access block your preparation.

- [ ] **Claude access** — Verify you can log in at the approved Allot instance. If you don't have access, email Philip Kramer (pkramer@allot.com), the AI Enablement lead, **now** with subject line "AI Tools License Request".
- [ ] **Bookmark key resources:**
  - [Allot AI Usage Policy](https://allot.atlassian.net/wiki/spaces/RD/pages/1472692298/Allot+AI+Usage+Policy) (Confluence)
  - **AI Champions - Training** Teams channel
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

**When in doubt, treat it as Confidential.** You can always ask in the **AI Champions - Training** Teams channel.

> **Note:** Different AI tools have different security boundaries. Claude (enterprise) may accept Internal data under Allot's enterprise agreement; other approved tools may differ. The workshop covers tool-specific rules in detail — for pre-work, use the table above as your baseline.

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

Write your prompt, label each part explicitly, and run it against Claude. Save it — you'll use it again on Day 1 Session 3.

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

## Part 5: Domain-Specific Deep Dive (30 min)

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
- [ ] I've completed one domain-specific deep dive task (Part 5)
- [ ] I'm bringing 2–3 real work examples (sanitized per the Data Classification table) to Day 1

**Time budget:** ~2.5 hours total (30 min tools + 45 min foundations + 30 min practice + 15 min sanitization + 30 min domain deep-dive).

> **Certification is post-training.** After Day 2, complete the **AI Champion Certification Exam** in the training hub within 7 days (by **Mon 11 May 2026 at 10:00 IL**).

---

## Questions?

If you get stuck during pre-work or have questions:
- Post in the **AI Champions - Training** Teams channel
- Contact your AI Champion program lead
- Questions are welcome — that's what the workshop is for

**See you at the training!**
