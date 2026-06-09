---
description: Runs the sales pipeline end to end, pausing at human approval gates.
---
Run our outbound pipeline for the leads in ./data/leads_raw/.

Follow these steps and STOP for my approval at each [GATE]:

1. Use the lead-scorer subagent to normalise and score all raw leads. Show me
   the ranked table. [GATE] I will name the top N to pursue.

2. For each lead I approve, use the researcher subagent to produce a
   qualification brief. Show me the verdicts. [GATE] I will confirm who to
   contact and on which channel.

3. For each approved lead, use the outreach-writer subagent to draft the first
   touch + 5-step sequence + call script. [GATE] I review and send manually.

4. When I tell you a prospect has replied positively, use the proposal-builder
   subagent for that prospect.

5. Before any booked meeting, use the meeting-prep subagent for that prospect.

Never send anything yourself - you produce drafts only. Honour every hard rule
in CLAUDE.md, especially: human reviews every message, never invent facts,
cite sources, and keep prospect data inside ./data and ./output.
