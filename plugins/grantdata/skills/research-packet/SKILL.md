---
name: research-packet
description: Turn reviewed nonprofit research into a proposal case, strategy brief, board memo or source packet with clear claims, partner roles and next decisions. Use when the user wants a reusable deliverable rather than another search answer.
---

# Research packet

Read [shared evidence rules](../azimuth-research/references/evidence-rules.md). Identify the audience, decision and requested artifact. Reuse the work and accepted choices already present. For a local issue/program case, assemble the need diagnosis, direct/adjacent analogs, claim-to-evidence table, delivery roles, applicant assets, cost basis and funder-specific requirements. Use `program-evidence` and `funder-review` for missing research; do not call a draft reviewed merely because it has every heading.

For a fundraising strategy, use `fundraising-strategy-process` and its relevant references. For a source brief or presentation, read [packet and citation cleanup](references/packet-and-citation-cleanup.md). Produce the requested usable artifact, with one recommendation/decision and material gaps visible. Capacity, relationship access, commitments and private budgets must come from user context or appropriate verified evidence.

Use native host document abilities to create files when available and requested. Otherwise deliver reusable text/tables in the conversation. Document generators, stored workspaces, hosted packets and monitoring from other Azimuth tools are not available on this connection. State the actual artifact location; drafting a message or application does not send or submit it.

## In Claude

In Claude Code the tools appear as `mcp__grantdata__<tool>`; in claude.ai they sit under the Grant Data connector. Every tool is read-only, so call them freely. There is no save tool on this connection; keep findings in the answer.

Use Claude's native web search and page fetch for currentness checks and original sources. Fetch the page you cite; a search snippet is a lead.

Grant Data returns structured data for a text answer. Render comparisons as Markdown tables yourself; do not wait for an app panel.

When the plugin is installed, the guides are already local skills. Call `get_research_workflow` only for a reference you do not have or to confirm the deployed version.

In Claude Code, when several candidates need the same verification, delegate one candidate per parallel subagent with the same rubric and question definition, then collect one disposition table. Keep the final judgment in the main thread.

Deliverables: in claude.ai use an Artifact or Doc for a packet; in Claude Code write a dated Markdown file into the project and say where it is. State that nothing was saved to Grant Data.

Keep a claim/source table in the answer. Mark each claim observed, user-stated, inferred, recommended or unknown.

claude.ai: produce an Artifact or Doc. Claude Code: write a dated Markdown file. Either way, say that nothing was saved to Grant Data.
