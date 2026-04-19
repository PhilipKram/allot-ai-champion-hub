# AI Champion Enablement Training — 2-Day Program

**Program:** ALLOT AI Champions
**Cohort:** 2026 Q2
**Dates:** Day 1 — Wed 29 Apr 2026 · Day 2 — Mon 4 May 2026
**Schedule:** 10:00–18:00 IL both days
**Duration:** 2 days (8 hours per day)

**Audience:** Newly selected AI Champions across R&D, Product, and Business teams  
**Objective:** Equip champions with the knowledge, skills, and confidence to drive AI adoption within their local teams

---

## Day 1 — Foundations & Personal Capability

**Schedule:** 10:00–18:00 Israel time (multi-region: IL / EU / India)
**Format:** Hybrid — in-person in Hod HaSharon + remote participants via Teams
**Outcome:** By 18:00, each champion can structure a prompt, pick the right model, verify the output, chain steps, and knows when to reach for a Skill or `MEMORY.md` instead of retyping context every time.

---

### Session 1: Welcome & the Champion Role (10:00–10:30)

**Objective:** Set audience, set expectations, frame the Champion ↔ Team relationship.

#### 1.1 Who's in this room
- Champions from R&D, Product, Security, and Support — *you are not the team, you are the bridge*
- Multi-region cohort: IL in-person + remote from EU and India

#### 1.2 The Champion ↔ Team relationship — the five hats

| Hat | What you do for your team |
|---|---|
| **Evangelist** | Promote real use cases they can copy |
| **First Responder** | First line for AI questions before they escalate |
| **Feedback Loop** | Channel their pain points back to the AI program |
| **Quality Gate** | Ensure responsible, secure usage in your domain |
| **Trainer** | Run the 60-minute local workshop and mentor 1:1 |

#### 1.3 The 3-phase outcome ladder
- **Pre-work (done):** baseline access, shared vocabulary, real problems in hand
- **Workshop (today + tomorrow):** personal capability → leadership capability
- **Post-training (60 days):** first local workshop delivered, prompt library seeded, eNPS pulse

#### 1.4 Pre-work pulse
Quick show of hands: tools working? Firehawk sanitization done? Policy scavenger hunt? Real examples in hand?

---

### Session 2: Foundations & Friction-Busters (10:30–11:30)

**Objective:** Refresh the mental model, pick the right model for the job, and kill the fear of "I'll have to retype everything every time."

#### 2.1 LLM behavior you must internalize (15 min)
From pre-work, now as a group:
- It generates *plausible*, not *true*
- No memory between conversations unless you provide it
- Context window = working memory
- Output quality compounds with input quality

#### 2.2 Picking the right model and context size (20 min)

| Model | Best for | Avoid when |
|---|---|---|
| **Opus** | Complex reasoning, architecture, deep analysis, novel problems | Routine summaries, short classifications |
| **Sonnet** | Day-to-day work — the sensible default | Only skip when you *know* the job needs more or less |
| **Haiku** | Fast, lightweight, repetitive, operational tasks | Anything requiring deep reasoning |

**Context-size tradeoff:**
- 200k context is usually better than 1M
- Bigger context = higher cost, slower responses, more anchoring on irrelevant earlier content, more signal dilution
- Rule of thumb: if you don't need the long context, don't pay for it

**Don't default to Opus with 1M context.** It feels safe, but it's expensive, slower, and often produces worse results than Sonnet at 200k.

#### 2.3 The relief message — Skills & MEMORY.md (20 min preview)
You do **not** need to rewrite your role, context, and constraints into every prompt.

- **Skills** encapsulate reusable logic, prompts, and workflows — invoke with a single line instead of re-explaining.
- **`MEMORY.md`** stores who you are, the project, assumptions, and constraints — Claude reads it automatically at the start of a session.

*Deep dive tomorrow. Today we just want you to know these exist, so no one leaves thinking "every prompt has to be a 500-word essay."*

#### 2.4 Live demo — same question, three models (5 min)
One realistic Allot task run against Opus, Sonnet, and Haiku side-by-side. See the difference in output quality, speed, and where each one earns its keep.

*Break 11:30–11:45*

---

### Session 3: Prompt Anatomy — The Inigo Frame (11:45–13:00)

**Objective:** One durable structure for any prompt, borrowed from Inigo Montoya.

#### 3.1 The 4-part frame (plus optional 5th)

A good prompt is basically how you introduce yourself properly in any meeting:

| Part | Purpose | Example phrasing |
|---|---|---|
| **1. Greeting / framing** | Why are we here | "I need help preparing for tomorrow's design review." |
| **2. Who am I** | Calibrate the response to you | "I'm a senior QA lead on the DPI module at Allot." |
| **3. Who are you / shared context** | Tell the AI who it should be and what we're looking at | "You are a senior QA architect with experience in high-throughput packet-inspection systems. We're reviewing a draft test plan for a throughput-optimization feature." |
| **4. Desired outcome** | What should exist at the end | "Produce a list of missing edge cases, grouped by risk tier, as a markdown table." |
| **5. Constraints (optional)** | What to avoid or assume | "Stay within functional/performance testing; ignore security (AppSec owns that). Limit to 10 items." |

#### 3.2 A worked example that satisfies all 4 parts

```
[1. Framing]      I need to prep feedback on a test plan before tomorrow's design review.
[2. Who am I]     I'm a QA lead at Allot, a network-security company; I own test strategy
                  for our DPI module.
[3. Who are you]  You are a senior QA architect with experience in high-throughput
                  packet-inspection systems. We are reviewing a draft test plan for a
                  new throughput-optimization feature; your goal is to find gaps before
                  it ships.
[4. Outcome]      Produce a list of edge cases missing from the plan, grouped by risk
                  tier (High / Medium / Low), with one sentence of rationale each.
                  Format as a markdown table.
[5. Constraints]  Stay within functional and performance testing; ignore security
                  scenarios (covered by AppSec). Max 10 items.
```

Every part is explicit. Compare to *"review this test plan"* — which gives the AI nothing to work with.

#### 3.3 Pair exercise — rewrite a pre-work prompt (30 min)
Take the prompt you brought from pre-work Exercise 3. In pairs, rewrite it to hit all 4 parts. Run the original and the rewrite against Claude. Compare.

**Hybrid logistics:** pair remote-with-remote and in-room-with-in-room; Teams breakout rooms for remote pairs. Cameras on.

#### 3.4 Share & critique (15 min)
Two pairs share their before/after. The group critiques against the 4-part checklist.

#### 3.5 Common failure modes (5 min)
- Skipping part 2 ("who am I") — AI can't tailor tone
- Skipping part 3 ("who are you") — AI defaults to generic
- Vague part 4 — vague output
- Burying constraints inside context

*Lunch 13:00–14:00*

---

### Session 4: V-C-A-F — The Trust Protocol (14:00–15:15)

**Objective:** Build the verification reflex that is the Quality-Gate hat in practice.

#### 4.1 Why verification is the #1 Champion skill (10 min)
As a Champion, you are the person your team trusts to say "this AI output is safe to ship" — or "this one isn't." If you skip verification, they will too.

#### 4.2 Live hallucination demo (15 min)
Facilitator asks Claude for something plausibly wrong in the Allot domain. The room spots what's off. Debrief the specific failure mode.

#### 4.3 Walk through V-C-A-F (20 min)

| Step | Action | Key Question |
|---|---|---|
| **Verify** | Check technical & factual integrity | Is this actually correct? Cross-reference claims, dates, specs against internal data. For code, ask the AI to explain its reasoning. |
| **Contextualize** | Check business / domain alignment | Does this fit Allot's specific context, architecture, and branding? |
| **Authorize** | Take human accountability | Are you willing to put your name on this? Security-critical or legal output requires a second set of eyes. |
| **Fairness Check** | Check for bias & ethical risk | Is this output treating all groups/scenarios fairly? Mandatory for anything people-related. |

Apply the full protocol to the prompt outputs produced in Session 3.

#### 4.4 Fairness deep-dive (15 min)
Why the Fairness Check matters even when no one says the word "bias":
- LLMs inherit historical patterns from training data
- Performance reviews, hiring rubrics, customer segmentation, support prioritization — all carry demographic signal
- **Decision support, not decision making** — AI helps you think; *you* decide

#### 4.5 Sanitization debrief (15 min)
Review the pre-work Firehawk transcript in groups. Common mistakes, what "sanitized enough" actually looks like, and the one-question test: *"Would I read this aloud to an auditor?"*

*Break 15:15–15:30*

---

### Session 5: Lab — Prompt Chaining on Real Work (15:30–17:00)

**Objective:** Ship a working 3-step chain on a real problem you brought from pre-work.

#### 5.1 Chaining pattern — extract → analyze → format (15 min)
- **Step 1** extracts structured data from raw input
- **Step 2** analyzes or classifies it
- **Step 3** formats for the target audience / system

Each step's output is the next step's input. Smaller, more testable, and more reliable than one mega-prompt.

#### 5.2 Build your chain (60 min)
Pair work (breakout rooms for remote pairs):
1. Pick one real problem from your pre-work examples
2. Design the 3 steps on paper first
3. Build it in Claude, one step at a time
4. Apply V-C-A-F at the final step
5. Document as a reusable template

#### 5.3 Red-team swap (15 min)
Swap chains with another pair. Each pair tries to:
- Break the chain with unexpected input
- Find a case where V-C-A-F fails silently
- Report back one finding to the group

*Break 17:00–17:15*

---

### Session 6: Feasibility vs. Impact + Capstone Problem ID (17:15–18:00)

**Objective:** Walk out with a chosen capstone target for Day 2.

#### 6.1 The Feasibility vs. Impact matrix (10 min)

```
                    HIGH IMPACT
                        │
        ┌───────────────┼───────────────┐
        │  QUICK WINS   │  STRATEGIC    │
        │  Do first     │  Plan & invest│
  EASY ─┼───────────────┼───────────────┼─ HARD
        │  LOW PRIORITY │  AVOID        │
        │  Automate if  │  (for now)    │
        │  trivial      │               │
        └───────────────┼───────────────┘
                        │
                    LOW IMPACT
```

#### 6.2 Map your pre-work use cases (15 min)
Place each use case on the matrix. Identify your personal Top Quick Win and Top Strategic Opportunity.

#### 6.3 Pick your capstone and write the problem statement (15 min)

**Capstone format: pairs within the same function / domain.**
- One problem per pair
- 2–3 sentence problem statement: *what goes in, what comes out, who benefits*
- Refined overnight, built and presented at the end of Day 2

#### 6.4 Day 1 close (5 min)
- One sentence each: *"What did you un-learn today?"*
- Day 2 preview: Skills & `MEMORY.md` deep-dive, domain tracks (Technical / Business), leadership playbook, capstone build & present

---

## Day 2 — Advanced Skills & Champion Leadership

### Session 5: Advanced Prompting & Domain Workflows (09:00–10:30)

**Objective:** Go beyond basics into production-grade AI usage with hands-on practice.

#### 5.1 System Prompts & Personas (20 min)
- Crafting reusable system prompts for consistent behavior
- Building personas for different use cases (code reviewer, tech writer, analyst)
- Template:
```
You are [ROLE] at Allot, a network security company.
Your expertise: [DOMAINS]
Your communication style: [STYLE]
When uncertain: [BEHAVIOR]
Output format: [FORMAT]
```

#### 5.2 Working with Long Documents (15 min)
- Chunking strategies for large inputs
- Summarize-then-analyze patterns
- Using AI to navigate and extract from lengthy specs, logs, or reports

#### 5.3 AI Agents & Reusable Custom Tools (15 min)
- Building custom AI agents for repeatable team tasks
- Sharing agents and prompt configurations across the team
- When to build an agent vs. use a one-off prompt
- Demo: create a simple agent for a common team workflow

#### 5.4 Domain Workflows — Parallel Tracks (40 min)

*Split into tracks. Each track includes a 10-min teaching block + 30-min hands-on lab.*

**Track A (Technical):** Code-Focused Workflows
*For R&D, Security, and Engineering champions*
- Code review prompts that catch real bugs
- Test generation with meaningful coverage
- Documentation generation from code
- Refactoring assistance with safety checks
- Log analysis and anomaly detection
- *Lab: Review a real code PR using AI, apply V-C-A-F to the output*

**Track B (Business):** Analysis & Communication Workflows
*For Product, Support, and Business champions*
- Market analysis and competitive intelligence prompts
- User story generation from feature briefs and customer feedback
- Customer sentiment mapping and ticket categorization
- Executive summary creation from technical reports
- *Lab: Transform raw customer feedback into a structured insights report using AI*

---

### Session 6: Responsible AI, Security & Ethics (10:45–12:00)

**Objective:** Ensure champions can guide their teams on safe AI usage.

#### 6.1 Data Classification & AI
| Data Classification | AI Usage |
|---|---|
| **Public** | Any approved tool |
| **Internal** | Approved tools with enterprise agreement |
| **Confidential** | Only on-premise/approved private instances |
| **Restricted** | Never use with AI tools |

#### 6.2 Security Best Practices
- Never paste credentials, tokens, or PII into prompts
- Sanitize code before sharing (remove connection strings, API keys)
- Verify AI-generated code for security vulnerabilities
- Review AI suggestions against OWASP Top 10

#### 6.3 Intellectual Property & Compliance
- AI-generated code ownership and licensing considerations
- Export control considerations for AI outputs
- Documentation requirements for AI-assisted work

#### 6.4 When NOT to Use AI
- Final decisions on security-critical configurations
- Legal or compliance determinations
- Situations requiring real-time accurate data
- When you can't verify the output

#### 6.5 AI Ethics: Bias, Fairness & Decision-Making — Deep Dive

You learned the **Fairness Check** as the fourth step of V-C-A-F on Day 1. Now let's go deeper into *why* it matters and *how* to apply it rigorously.

**Understanding Algorithmic Bias:**
- LLMs are trained on vast public datasets that contain historical and societal biases
- Risk: AI may generate suggestions that favor certain demographics or exclude others — especially in hiring, performance reviews, or customer segmentation

**Ethical Decision-Making Rules:**
- **Decision support, not decision making** — AI is for brainstorming and analysis, not final calls on people or high-stakes strategy
- **Transparency** — Always disclose when AI has been used to generate substantial portions of a report or decision-support document
- **Accountability** — If you use it, you own it. AI output with your name on it is your responsibility

#### 6.6 Incident Response & Live Drill (20 min)

**Process:**
1. What to do if sensitive data is accidentally shared with AI
2. Reporting process and escalation path
3. Post-incident review template

**Live Fire Drill:**
> *Scenario: A team member sends you a Teams message: "Hey, I accidentally pasted a customer's full API credentials and account details into Claude while debugging an integration issue. What do I do?"*

In pairs, walk through the full response:
1. **Immediate action** — What do you tell them to do right now?
2. **Escalation** — Who do you contact and how?
3. **Documentation** — What do you record?
4. **Prevention** — What process change do you recommend?

*Debrief: Compare responses. Did everyone follow the same escalation path?*

---

### Session 7: Leading Your Team — The Champion Playbook (13:00–14:30)

**Objective:** Prepare champions to drive adoption in their local teams.

#### 7.1 Running a Local Workshop
**Workshop Template (60 min):**
| Time | Activity |
|---|---|
| 0–10 min | Intro: Why AI matters for our team |
| 10–20 min | Live demo: AI solving a real team problem |
| 20–40 min | Hands-on: Team members try with their own tasks |
| 40–50 min | Share results and discuss |
| 50–60 min | Next steps and ongoing support |

**Tips for effective workshops:**
- Use real examples from your team's domain, not generic demos
- Start with quick wins to build confidence
- Pair skeptics with enthusiasts
- Follow up individually within a week

#### 7.2 Building & Maintaining a Team Prompt Library
- Create a shared space for team-specific prompts
- Categories: code review, testing, documentation, analysis, communication
- Template for documenting prompts:
```
Name:        [Descriptive name]
Version:     [v1.0, v1.1, etc.]
Last tested: [Date and model version]
Purpose:     [What it does]
When to use: [Situation]
Prompt:      [The actual prompt with placeholders]
Example:     [Real example with sample output]
Tips:        [What to watch out for]
```

**Prompt Versioning & Maintenance:**
- AI models update regularly — a prompt that works today may behave differently next month
- Version your prompts (v1.0, v1.1) and record which model they were tested on
- **Monthly check:** Re-test your top 5 team prompts after any model update
- If a prompt degrades, document the change and adjust — don't just delete it

#### 7.3 Handling Resistance — Roleplay Exercise (30 min)

**Quick Reference:**
| Objection | Response Strategy |
|---|---|
| "AI will replace my job" | Focus on augmentation and higher-value work |
| "I don't trust AI output" | Validate the concern, pivot to V-C-A-F verification |
| "It's too slow/complicated" | Demonstrate a 2-minute quick win |
| "Security risk" | Walk through approved tools and policies |

**Exercise: The Champion's Response**
*Work in pairs. One person plays the Skeptic, the other the Champion. Switch roles after each scenario.*

**Scenario 1: The Accuracy Skeptic** (Senior Dev)
> *"I tried using Copilot for a complex refactor, and it hallucinated a library that doesn't even exist. It's a waste of time if I have to fix its mistakes."*

Champion's goal: Validate the frustration, then pivot to the "Verify, don't trust" mindset. Suggest Few-Shot prompting to constrain output to the actual tech stack.

**Scenario 2: The Anxious Junior** (Junior Analyst)
> *"If the AI can summarize these 50-page reports in two minutes, why does the company need me to do it? I feel like I'm training my own replacement."*

Champion's goal: Focus on augmentation. The AI handles the initial summary; their value is the analysis and the "so what?" — the parts AI can't do because it doesn't know Allot's strategy.

**Scenario 3: The Overwhelmed Manager** (Project Manager)
> *"I don't have time to learn 'prompt engineering.' I have a backlog of 200 tickets. It's faster if I just write the user stories myself."*

Champion's goal: Don't argue about time. Show a 30-second demo — turn rough notes into a structured user story on the spot.

*Debrief: What responses worked? What felt forced? How would you adapt for your real team?*

#### 7.4 Measuring Team Adoption & Your Analytics Dashboard

**Your metrics toolkit:** As a champion, you have access to the following dashboards:

| Metric | Where to Find It | Target |
|---|---|---|
| Monthly active users | AI Platform Admin → Team Usage | 60%+ of team within 3 months |
| Queries per user | AI Platform Admin → User Activity | 10+ per week per active user |
| Tool utilization by type | AI Platform Admin → Tool Breakdown | Balanced across available tools |

**Qualitative tracking (you own this):**
- Collect time-saved estimates from team members monthly
- Document use cases and wins for sharing across the organization
- Track quality improvements (fewer review cycles, fewer bugs, faster onboarding)
- Report insights back through the champion community

**Monthly reporting template:**
```
Champion Monthly Update — [Team Name] — [Month]
- Active users: X/Y (Z%)
- Top use cases this month: [list]
- Time saved estimate: [hours]
- Wins: [specific examples]
- Blockers: [what's preventing adoption]
- Requests: [tools, features, training needed]
```

---

### Session 8: Capstone Exercise (14:45–16:30)

**Objective:** Apply everything learned in a realistic end-to-end scenario.

#### The Challenge
Each champion team will (problem was identified in Day 1 wrap-up):

1. **Refine** the problem statement and align on scope (10 min)
2. **Design** an AI-assisted workflow to address it (30 min)
   - Define the prompt chain or template
   - Identify inputs, outputs, and V-C-A-F verification steps
   - Consider security and data classification
3. **Build & Test** the workflow using AI tools (45 min)
   - Build the prompt chain or agent
   - Test with real (sanitized) data
   - Debug and iterate
   - Document the workflow
4. **Present** the workflow to the group (5 min per team, 20 min total)
   - Problem statement
   - Solution design
   - Live demo
   - Lessons learned

#### Evaluation Criteria
- Practical value to the team
- Prompt quality and effectiveness
- V-C-A-F applied: verification steps, context awareness, accountability, and fairness check
- Security and data classification compliance
- Reusability, documentation, and versioning

---

### Session 9: Wrap-Up & Next Steps (16:30–17:30)

#### 9.1 Certification & Commitments

**Certification Exam (post-training).** Within 7 days of Day 2 (by **Mon 11 May 2026, 10:00 IL**), each champion completes the AI Champion Certification Exam in the training hub. Five sections: Case Studies, Your Capstone, Your First Local Workshop, Prompt Library Starter, and Commitments.

Each champion commits to:
- [ ] Submit the Certification Exam by Mon 11 May 2026
- [ ] Run their first local team workshop within 2 weeks (by Mon 18 May 2026)
- [ ] Contribute at least 3 prompts to the shared prompt library within 1 month
- [ ] Identify and document 5 AI use cases for their team within 1 month
- [ ] Attend bi-weekly champion community syncs

#### 9.2 Your Champion Roadmap
| Timeframe | Focus |
|---|---|
| **Weeks 1–2** | Run first local workshop, set up team prompt library |
| **Month 1** | Document 5 use cases, contribute prompts to shared library |
| **Months 2–3** | Identify automation opportunities, mentor team members |
| **Months 4–6** | Propose AI-assisted workflow improvements, present wins to leadership |
| **Ongoing** | Stay current on AI developments, scout new tools, share via **AI Champions - Training** Teams channel |

**AI Scouting:** Use the **AI Champions - Training** Teams channel to report new AI tools, features, or techniques you discover. Champions are the organization's scouts — not just implementers of current tools.

#### 9.3 Your Champion Toolkit
You leave with:
- This training guide
- Prompt cookbook (companion document)
- Workshop facilitation template
- Quick-start reference card
- Access to the **AI Champions - Training** Teams channel and knowledge base

#### 9.4 Support & Escalation
| Need | Where to Go |
|---|---|
| Prompt help | **AI Champions - Training** Teams channel |
| AI tool access (Claude / Copilot licenses) | Email Philip Kramer (pkramer@allot.com) |
| General IT issues (laptop, VPN, login) | IT Service Desk |
| Security questions | AppSec team / AI program lead |
| Feature requests | AI program backlog (Jira) |
| Training materials | Confluence AI Champions space |

#### 9.5 Feedback
- Training evaluation survey (sent after the session)
- Ongoing feedback through the champion community
- Suggestions for improving the program are always welcome

---

## Appendix A: Quick Reference — Prompt Patterns

| Pattern | Template | Use Case |
|---|---|---|
| **Summarize** | "Summarize [X] in [N] points for [audience]" | Reports, docs, meeting notes |
| **Analyze** | "Analyze [X] for [criteria]. Think step by step." | Code review, security audit |
| **Generate** | "Generate [output type] based on [input]. Format as [format]." | Tests, docs, stories |
| **Transform** | "Convert [input format] to [output format]. Preserve [requirements]." | Data conversion, reformatting |
| **Compare** | "Compare [A] and [B] across [dimensions]. Present as a table." | Architecture decisions, tool eval |
| **Debug** | "This [code/config] produces [error]. Expected: [X]. Actual: [Y]. Diagnose." | Troubleshooting |

## Appendix B: Agenda at a Glance

### Day 1 — Foundations & Personal Capability (10:00–18:00 IL, hybrid)
| Time (IL) | Session | Duration |
|---|---|---|
| 10:00–10:30 | Welcome & the Champion Role | 30 min |
| 10:30–11:30 | Foundations & Friction-Busters (model selection + Skills/`MEMORY.md` preview) | 60 min |
| 11:30–11:45 | *Break* | 15 min |
| 11:45–13:00 | Prompt Anatomy — The Inigo Frame | 75 min |
| 13:00–14:00 | *Lunch* | 60 min |
| 14:00–15:15 | V-C-A-F — The Trust Protocol | 75 min |
| 15:15–15:30 | *Break* | 15 min |
| 15:30–17:00 | Lab — Prompt Chaining on Real Work | 90 min |
| 17:00–17:15 | *Break* | 15 min |
| 17:15–18:00 | Feasibility vs. Impact + Capstone Problem ID + Day 1 Close | 45 min |

### Day 2 — Advanced Skills & Champion Leadership
| Time | Session | Duration |
|---|---|---|
| 09:00–10:30 | Advanced Prompting & Domain Workflows (Track A/B) | 90 min |
| 10:30–10:45 | *Break* | 15 min |
| 10:45–12:00 | Responsible AI, Security, Ethics & Incident Drill | 75 min |
| 12:00–13:00 | *Lunch* | 60 min |
| 13:00–14:30 | Champion Playbook (Workshops, Resistance, Metrics) | 90 min |
| 14:30–14:45 | *Break* | 15 min |
| 14:45–16:30 | Capstone Exercise | 105 min |
| 16:30–17:30 | Wrap-Up, Roadmap & Next Steps | 60 min |
