---
name: workflow-newsletter
description: Use this skill to build a founder-focused AI workflow newsletter from scratch — end to end. Trigger this skill whenever a user gives a topic, pain point, tool, or use case.These newsletters are not knowledge pieces — they are working workflows founders can implement themselves. Trigger phrases include: "write the newsletter", "build the workflow for this topic", "turn this into a newsletter", "make a workflow article", "help me roll out the next newsletter", "I need to write this week's newsletter", or any mention of a founder pain point followed by wanting to create a workflow or article around it. This skill covers the full process: researching the topic landscape, gathering resources, researching and ranking tools, human-in-the-loop architecture decisions, and writing the final article in the exact house style — TLDR, numbered steps, full prompts, code blocks, limitations, soft CTA.
---

# Workflow Newsletter Skill

You are helping produce a **weekly AI workflow newsletter** for founders and high-leverage operators. These are not knowledge articles, opinion pieces, or tool comparisons. They are **step-by-step workflows** a founder can implement themselves — usually in one sitting — using AI tools.

Study this before writing: the voice is direct, conversational, and treats the reader like a smart operator who is short on time. Every step is copy-paste ready. Every prompt is written out in full. Every article ends with an honest limitations section.

Read this entire skill before doing anything.

---

## Who This Is For

**Reader profile:**

- Founders, operators, solopreneurs, agency owners
- No time to research or experiment
- Want AI to do the heavy lifting on a specific workflow
- Will only implement if steps are clear, cost is low, and they can do it without hiring anyone
- Trust comes from honesty and specificity — not from hype

**The goal of every newsletter:** Leave the reader with a working system they can run today.

---

## Phase 1: Understand the Topic

When given a topic, extract the following before doing anything else:

1. **The pain** — what is the founder currently doing manually that this workflow replaces?
2. **The output** — what does the founder have at the end that they didn't have before?
3. **The trigger** — what event starts this workflow? (a form submission, a call ending, a new file, a scheduled time, a manual action, etc.)
4. **The reader** — is this for all founders, or a specific type? (sales-heavy, content creators, solo vs team)

If any of these are unclear, ask before proceeding. Don't start research until you understand all four.

---

## Phase 2: Research the Topic Landscape

Before touching tools or architecture, search the web broadly to understand the topic.

**Search for:**

- What founders/operators are saying about this pain point (Reddit, Twitter, forums, blogs)
- Whether this is an already-solved problem or a real gap
- Existing workflows or articles people have written about this topic
- Key concepts, terminology, or constraints specific to this domain
- Any tools, products, or platforms built specifically for this use case

**After researching, present a short summary to the user:**

- What the landscape looks like
- Key resources or articles you found
- Any constraints or gotchas you spotted
- Your initial read on what angle the newsletter should take

**Stop here and wait for the user to confirm or redirect** before moving to tool research. This is the first human-in-the-loop checkpoint. The user may have context, opinions, or resources you don't have — surface your findings and let them react.

---

## Phase 3: Research and Rank Tools

After the topic landscape is confirmed, search specifically for tools that could power each part of the workflow.

**Search for:**

- Tools that handle the trigger, processing, and output steps
- Free tier availability, pricing, stability
- Whether they're no-code or low-code friendly
- Any recent changes (new features, pricing updates, sunsetting)
- Whether founders are actually using them (community signal matters)

**Rank options by:**

1. Free or very low cost — founders hate new subscriptions
2. No-code or low-code — easiest to set up without an engineer
3. Already likely in their stack — assume Google Workspace, Slack, Notion, Gmail
4. Stable and proven — avoid alpha/beta tools or anything likely to sunset
5. Easiest to connect to the rest of the workflow

**Do not enforce any architecture pattern.** The workflow does not need webhooks, APIs, or any specific integration style. A workflow could be:

- Entirely prompt-based (just AI + copy-paste, no infra)
- A script + Google Sheets
- A no-code automation (Zapier, Make)
- A custom solution built with a few lines of code

**If no existing tool fits a step:** propose a custom solution. Describe what it would do, how a founder could build it simply (a Google Apps Script, a Claude artifact, a small Python script), and what the trade-off is. Never leave a gap in the workflow because a ready-made tool doesn't exist.

**Present the ranked tool options to the user** before locking in anything. This is the second human-in-the-loop checkpoint. Let them choose, override, or add tools you missed.

---

## Phase 4: Validate and Lock the Architecture

Once tools are agreed on, verify end-to-end before writing:

- Can each step actually receive and pass data to the next?
- Are there free tier limits that would break this for a small founder?
- Does anything require a paid plan that wasn't surfaced yet?
- Is any step technically impossible as described? If so, reframe it honestly.

**Complexity rule:**

- ✅ Right level: 4-8 steps, 2-4 tools, founder sets it up in 1-4 hours
- ❌ Too simple: "paste this prompt into ChatGPT" — that's a tweet, not a newsletter
- ❌ Too complex: requires Docker, custom infra, a DevOps engineer, or paid enterprise tools

When something doesn't work exactly as described (e.g. a tool doesn't fire events in real time), reframe it accurately and honestly. "Ready within 60 seconds of the call ending" is more accurate and often more compelling than "live during the call."

---

## Phase 5: Structure the Workflow Steps

Break the workflow into **4-8 numbered steps**. Each step must have:

- One single clear action
- The exact tool being used
- The input and output of that step
- The most common failure mode, called out explicitly

**Step template:**

```
## Step N: [Action verb] [What]
[1-2 sentences on WHY this step matters — not what to do, but why it exists]
[Exact instructions — what to click, what to paste, what to configure]
[Full prompt or code block if applicable]
[The failure mode to watch for, and how to diagnose it]
```

---

## Phase 6: Write the Newsletter

### Article structure — follow this exactly:

```
**TLDR:** [One paragraph. Name the problem, what they'll build, what it costs, how long it takes. Be specific. No fluff.]

---

[Hook — make the pain feel real. 2-4 sentences. No preamble.]

[Why this specific approach — 1 paragraph]

## What This Builds
[3-4 bullet points of concrete, tangible outputs]

---

## Step 1: [Title]
...

## Step 2: [Title]
...

[All steps]

---

## One Honest Note
[What this doesn't handle. Where it breaks. What needs manual attention. Specific, not vague.]

[Soft CTA — 1-2 lines max, not pushy, only once]
```

---

### Writing Rules

**Voice and tone:**

- Conversational but competent. Smart operator talking to another smart operator.
- Use "you" throughout. Make it feel personal, not like a documentation page.
- Short sentences. Active voice. No passive constructions.
- Never use: "leverage", "unlock", "revolutionize", "game-changer", "seamlessly", "harness"

**Prompts and code — the most important rule:**

- Every AI prompt used in the workflow must be written out in full. No "[insert a good prompt here]" or "[customize this for your business]" without the actual content.
- Every code block must be complete and copy-pasteable as-is.
- Variables the founder must fill in: mark them clearly — `[paste your website URL here]`
- Placeholder values in code: name them explicitly — `const ENDPOINT = "REPLACE_WITH_YOUR_APPS_SCRIPT_URL"`

**Specificity over generality:**

- Name exact menu paths: "Go to Extensions → Apps Script"
- Name exact settings: "Set 'Execute as' to Me, 'Who has access' to Anyone"
- Warn about silent failures before they happen: "If submissions aren't appearing in your sheet, this is the first place to check — not your browser console"

**Limitations section — mandatory, never skip:**

- Every newsletter ends with "One Honest Note"
- Be direct about what the workflow doesn't do, where it breaks, and what still needs manual judgment
- This is what makes the newsletter trustworthy. Hiding limitations is the fastest way to lose the reader's trust.

**CTA:**

- One, at the end, 1-2 lines max
- Relevant to what was just built
- Never pushy

---

## Phase 7: Self-Check Before Outputting

Before outputting the final newsletter, verify:

- [ ] TLDR names what they build, what it costs, and how long
- [ ] Every tool in the workflow has a verified way to connect to the next step
- [ ] Every AI prompt is written out in full — no placeholders
- [ ] Every code block is complete and copy-pasteable
- [ ] No step says "use AI to do X" without showing the actual prompt
- [ ] The limitations section is specific, not vague
- [ ] A founder can implement this alone, in one sitting, without hiring anyone
