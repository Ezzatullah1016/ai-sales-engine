# Project Memory — Sales Engine
# Auto-loaded by Claude Code at the start of every session in this folder.
# >>> Edit every line marked TODO before your first real run. <<<

## About us
- Company: TODO: [Your Company name], an IT-services provider based in Karachi, Pakistan.
- We sell to: TODO: [e.g. SMBs & startups in US / UK / EU / AU / GCC].
- Services we offer (our catalogue):
  1. Custom web application development
  2. Mobile app development (iOS / Android)
  3. TODO: [e.g. MVP builds, staff augmentation, QA, DevOps, AI integration]
- What makes us different: TODO: [e.g. fast delivery, fixed-bid option,
  time-zone overlap with clients, named portfolio pieces].
- Typical engagement: TODO: [e.g. $5k–$50k fixed-bid, or $2k–$8k/month retainer].

## Ideal Customer Profile (ICP)
- Good fit: TODO: [industry, size, signals — e.g. "hiring developers",
  "recently funded", "outdated or slow website", "posted a relevant Upwork job",
  "expanding product team"].
- Poor fit / disqualify: TODO: [e.g. budget < $3k, our direct competitors,
  regions we don't serve, one-off micro tasks, no working website].

## Voice & tone
- Plain English, concise, specific. No hype, no buzzwords.
- Lead with the prospect's problem, not our company.
- Spelling: TODO: [British or American — pick one].

## Hard rules for EVERY agent (do not break these)
1. A human reviews and sends every outbound message. Agents draft only.
2. Never invent facts, names, emails, prices, or case studies. If something
   is unknown, write [VERIFY] and explain what to check.
3. Cite a source URL for any researched claim.
4. Respect platform terms and email law. If unsure, flag it — do not send.
5. Keep prospect data inside ./data and ./output only. Never paste personal
   data into a public web search.

## Where things live
- Raw leads:    ./data/leads_raw/        (drop CSVs or pasted text here)
- Scored leads: ./data/leads_scored/
- Field guide:  ./data/schema.md
- Research:     ./output/research/
- Outreach:     ./output/outreach/
- Proposals:    ./output/proposals/
- Meeting prep: ./output/meetings/

## The agents (in .claude/agents/) and what each does
- lead-scorer      → normalises + scores raw leads against the ICP above
- researcher       → researches one prospect, writes a fit brief
- outreach-writer  → drafts first touch + 5-step follow-up + call script
- proposal-builder → drafts a tailored proposal / SOW
- meeting-prep     → objection handling, negotiation guardrails, closing scripts

## The pipeline command (in .claude/commands/)
- /run-pipeline → runs the agents in order, pausing for your approval at each gate.
