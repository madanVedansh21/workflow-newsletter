# Workflow Newsletter Skill for Claude

A Claude skill that turns any founder pain point or topic into a fully written, step-by-step AI workflow newsletter

These aren't knowledge articles. They're working workflows founders can implement themselves, usually in one sitting, using AI tools.

---

## What It Does

Give it a topic. It will:

1. **Research the topic landscape** — finds existing articles, tools, pain points, and constraints from the web
2. **Present findings to you** — human-in-the-loop checkpoint before any architecture decisions
3. **Research and rank tools** — finds what actually exists, ranks by founder-friendliness (free, no-code, stable)
4. **Propose custom solutions** if no off-the-shelf tool fits a step
5. **Get your sign-off** on the architecture before writing
6. **Write the full newsletter** — TLDR, numbered steps, full prompts, copy-paste code, limitations, soft CTA

---

## Example Topics

- "Live proposal builder that listens to a sales call and generates a personalized draft"
- "Turn Notion meeting notes into 3 LinkedIn post drafts automatically"
- "AI client onboarding system that replaces manual intro emails and doc sending"
- "Workflow that finds Reddit threads where your customers are and drafts replies"

---

## Installation

### Option 1: Claude.ai (Manual)

1. Go to **Settings → Skills** in Claude.ai
2. Create a new skill
3. Paste the contents of `SKILL.md` into the skill editor
4. Save

### Option 2: Claude Code

```bash
# Clone the repo
git clone https://github.com/your-username/workflow-newsletter-skill

# Package the skill (requires skill-creator scripts)
python -m scripts.package_skill workflow-newsletter-skill/

# Install the generated .skill file via Claude settings
```

---

## How to Use It

Once installed, just describe your topic:

> "Help me write this week's newsletter. Topic: founders are spending hours manually writing follow-up emails after sales calls. I want a workflow that automates this."

The skill will guide you through research → tool selection → architecture → writing.

---

## Newsletter Style Guide

Every newsletter produced by this skill follows this structure:

| Section              | Description                                                       |
| -------------------- | ----------------------------------------------------------------- |
| **TLDR**             | One paragraph — problem, what they build, cost, time              |
| **Hook**             | 2-4 sentences making the pain feel real                           |
| **What This Builds** | 3-4 bullet points of concrete outputs                             |
| **Steps 1-N**        | Each with why, exact instructions, full prompt/code, failure mode |
| **One Honest Note**  | Limitations — specific, not vague                                 |
| **CTA**              | 1-2 lines, soft, relevant                                         |

---

## Repo Structure

```
workflow-newsletter-skill/
├── SKILL.md          # The skill itself — install this
├── evals/
│   └── evals.json    # Test cases for validating the skill
└── README.md
```

---

## Contributing

PRs welcome. Good contributions:

- Additional test cases in `evals/evals.json`
- Improvements to the writing rules or phase structure
- Example newsletter outputs in an `examples/` folder

