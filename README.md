# AI Sales Engine (Claude Code)

A human-in-the-loop outbound sales workflow for an IT-services business, built
as Claude Code subagents. Five specialist agents + one orchestrator command.
Nothing is ever sent automatically — every agent produces drafts you review.

## What's in here

```
ai-sales-engine/
├─ CLAUDE.md                  <- project memory (EDIT THIS FIRST)
├─ README.md                  <- this file
├─ .gitignore
├─ .claude/
│  ├─ agents/                 <- the five specialist agents
│  │  ├─ lead-scorer.md
│  │  ├─ researcher.md
│  │  ├─ outreach-writer.md
│  │  ├─ proposal-builder.md
│  │  └─ meeting-prep.md
│  └─ commands/
│     └─ run-pipeline.md      <- /run-pipeline orchestrator
├─ data/
│  ├─ schema.md               <- lead field definitions
│  ├─ leads_raw/
│  │  └─ sample_leads.csv     <- fictional leads for a first test run
│  └─ leads_scored/
└─ output/
   ├─ research/ ├─ outreach/ ├─ proposals/ └─ meetings/
```

## Setup (Windows + Git Bash)

```bash
# 1. Confirm your tools are present
node --version        # any current LTS is fine
claude --version      # Claude Code

# 2. Go to where you unzipped this folder, e.g.:
cd ~/Documents/ai-sales-engine

# 3. (Optional but recommended) start version control
git init
git add .
git commit -m "Initial AI sales engine scaffold"
```

Then open the folder in VS Code (`code .`) and edit **CLAUDE.md** — fill in
every line marked `TODO` (company name, services, ICP, pricing, spelling).
The quality of every agent depends on this file.

## Run it

```bash
# From inside the project folder, launch Claude Code:
claude
```

Inside Claude Code:

```
/agents                 # confirm the 5 agents are listed
/run-pipeline           # runs the whole flow, pausing at each approval gate
```

Or call a single agent directly, e.g.:

```
Use the lead-scorer agent to score the leads in data/leads_raw/
```

Review outputs in the `output/` folders. Send messages yourself, manually.

## The golden rules (baked into every agent)

1. A human reviews and sends every outbound message.
2. Agents never invent facts, emails, or prices — unknowns are tagged [VERIFY].
3. Sources are cited; prospect data stays in ./data and ./output.
4. Respect platform terms and email law. When unsure, flag — don't send.

See the full strategy document for compliance, deliverability, roles, KPIs,
and the phased rollout plan.
