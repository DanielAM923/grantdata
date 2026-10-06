---
name: azimuth-research
description: Search Azimuth nonprofit intelligence for a research topic or source and give a concise evidence-backed answer. Use for open-ended corpus lookup; use the focused entity or peer-funding skills for those workflows.
---

# Azimuth Research

Read [shared evidence rules](references/evidence-rules.md). Use Azimuth `search` and `fetch` for name/EIN and paper-title discovery. Inspect the chosen result before making claims; clarify plausible identity matches. Use the discovered catalog for actual tool availability.

Explain the evidence at the same level the tool supports:

- A warehouse aggregate is an observed funding signal. The organization profile URL identifies the entity but does not validate the aggregate amount. A linked IRS filing is an example for that funder-recipient pair, not proof of the whole aggregate.
- Grant history does not show an open application, a warm introduction, or current strategic fit. Say when those items need separate verification.
- A paper result identifies a source; inspect the linked paper before claiming a specific finding.

Give the user a concise answer, name the selected entities and years, link source-bearing records, and state the one or two material coverage limits. Do not use private files or infer private relationships from public graph paths.

This MCP search covers organization names and paper titles. If a longer phrase returns no match, retry the core entity name. Use the MCP result to identify the entity, known relationships, source links, and exact coverage gap. It is a starting point for research, not the only source the host assistant may use.

When the user asks about mission, programs, current status, or another claim that `fetch` cannot establish, use the host assistant's own web search if it is available. Search with the resolved legal name and EIN, then inspect an official organization or funder page, filing, or other primary source that speaks to the claim. A graph path, third-party discovery result, or website link can guide the query, but its summary is not confirmation. Cite the page actually checked, distinguish its date from historical MCP observations, and note any conflict. If web search is unavailable or no suitable source is found, give the useful MCP findings and mark the claim unverified.

For cohort or program-role questions, do not classify an organization from its name, NTEE, website URL, or grant rows alone. Check a program-specific source with native web search when possible; otherwise say the program evidence is missing.

Choose the focused workflow for the next job: `entity-evidence` for identity; `peer-funding-comparison` for selected peers/benchmarks; `issue-to-funding-map` for an issue landscape; `program-evidence` for studies and analogs; `funder-review` for current fit/access; `research-packet` for an artifact; `fundraising-strategy-process` for decisions across the whole process. The same guides are retrievable through `list_research_workflows` / `get_research_workflow` when exposed.

For conflicts, new discoveries and whole-org research use [research review](references/research-review.md). For any retain request follow [connection boundaries](references/connection-boundaries.md). Never assume a save or graph refresh happened from instructions alone.

## In Claude

In Claude Code the tools appear as `mcp__impact-recon__<tool>`; in claude.ai they sit under the Impact Recon Alpha connector. Every tool is read-only, so call them freely. There is no save tool on this connection; keep findings in the answer.

Use Claude's native web search and page fetch for currentness checks and original sources. Fetch the page you cite; a search snippet is a lead.

Impact Recon returns structured data for a text answer. Render comparisons as Markdown tables yourself; do not wait for an app panel.

When the plugin is installed, the guides are already local skills. Call `get_research_workflow` only for a reference you do not have or to confirm the deployed version.

In Claude Code, when several candidates need the same verification, delegate one candidate per parallel subagent with the same rubric and question definition, then collect one disposition table. Keep the final judgment in the main thread.

Deliverables: in claude.ai use an Artifact or Doc for a packet; in Claude Code write a dated Markdown file into the project and say where it is. State that nothing was saved to Impact Recon.

Keep a claim/source table in the answer. Mark each claim observed, user-stated, inferred, recommended or unknown.
