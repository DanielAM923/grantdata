---
name: program-evidence
description: Research an intervention or program idea through studies, implementation analogs, named delivery partners and payer evidence. Use for what works, who implements it, or what makes a pilot fundable.
---

# Program evidence

Read [shared evidence rules](../azimuth-research/references/evidence-rules.md). Normalize the question by population, setting, delivery model, geography, outcomes and decision. Use Azimuth `search`/`fetch` for paper pointers and entity identities, then inspect the original study or evaluation with native host research. Paper metadata alone cannot establish a finding. If title search misses a relevant intervention, use native discovery and clearly identify which source came from which path.

For each useful study report the model, study design/strength, population/setting, outcomes, costs when observed and transfer limits. Distinguish causal evaluation, descriptive implementation and toolkit guidance. Deduplicate identical source URLs. Do not extrapolate a result to a different program or population without explaining the inference.

Find direct and adjacent implementation analogs on official program pages, evaluations and partner announcements. Map named providers, intermediaries, government payers, lenders/investors, grantors and evaluators by their actual roles. Inspect program-specific payer/award evidence before saying who funded the intervention. A historical organization-level grant or a named study investor does not prove a program grant or current availability.

Use issue tools when present for candidate discovery, followed by source verification. Keep ambiguous EINs unresolved. If no paper/program graph traversal is exposed, say the named participants came from original-source reading, then resolve their identities separately.

Produce a concise evidence/analog table and a provisional pilot concept: learning question, actual model, partner requirements, implementation and staffing needs, budget basis, baseline/outcome measures, replication deliverable and gaps. Distinguish someone doing similar work from someone willing to pay for this applicant. For the broader case or proposal use `research-packet`; for current supporter qualification use `funder-review`.

## In Claude

In Claude Code the tools appear as `mcp__grantdata__<tool>`; in claude.ai they sit under the GrantData connector. Every tool is read-only, so call them freely. There is no save tool on this connection; keep findings in the answer.

Use Claude's native web search and page fetch for currentness checks and original sources. Fetch the page you cite; a search snippet is a lead.

GrantData returns structured data for a text answer. Render comparisons as Markdown tables yourself; do not wait for an app panel.

When the plugin is installed, the guides are already local skills. Call `get_research_workflow` only for a reference you do not have or to confirm the deployed version.

In Claude Code, when several candidates need the same verification, delegate one candidate per parallel subagent with the same rubric and question definition, then collect one disposition table. Keep the final judgment in the main thread.

Deliverables: in claude.ai use an Artifact or Doc for a packet; in Claude Code write a dated Markdown file into the project and say where it is. State that nothing was saved to GrantData.

Keep a claim/source table in the answer. Mark each claim observed, user-stated, inferred, recommended or unknown.

For warehouse queries through any other tool: `grant_edges` is a relationship rollup over the row lanes (Schedule I, spider), never a third lane; sum the row lanes, deduped by funder and recipient EIN. `kg_nodes` joins on `node_id`, not `ein`.

When a table cell shows a funder → recipient arrow, copy the direction from the tool payload's funder and recipient fields; do not infer it from the order names appear in the prompt.
