---
name: peer-funding-comparison
description: Compare observed funders across explicitly selected nonprofit peers and a focal organization in Azimuth. Use for peer-funder overlap or gap questions, not for unverified peer discovery or prospect recommendations.
---

# Peer Funding Comparison

Read [shared evidence rules](../azimuth-research/references/evidence-rules.md). For cohort choice or earned-revenue comparables read [peer design](references/peer-design.md); propose source-checked candidates, then obtain a selected set before running this comparison.

Resolve the focal organization and each chosen peer with `search` and `fetch`. Use `find_peer_funders` only when the user named the peers or they were clearly selected earlier in the conversation. If the user has only a strategy or a vague “organizations like us,” ask for the peer set or explain that this version cannot yet verify a comparable cohort. Keep close operating peers distinct from broader reference models when the user supplied both; do not imply they are equivalent.

Read the comparison as historical grant observations. Report the selected peers, observed years, overlapping funders, and whether a focal edge was observed. “Not observed here” means only that the selected warehouse path did not return that edge. The recorded funder role can include an operating partner or intermediary. Linked filings are examples for a pair and do not validate the aggregate total.

Treat a missing `funder_type` as an unresolved role. Warehouse year and example filing year are separate; a mismatch cannot verify aggregate amount/recency. Use native primary sources to check pass-through or donation roles. For retain requests follow [connection boundaries](../azimuth-research/references/connection-boundaries.md); an unavailable save becomes a conversation review note, not a claimed graph update.

Do not turn a peer-connected funder into a prospect recommendation without separate current fit, instrument, eligibility, application route, and access evidence. Keep grants separate from debt, equity equivalents, recoverable capital, and partnership routes. The current peer tool covers grant aggregates, not those other instruments. If the user asks for a shortlist, offer a clearly labeled research queue with the missing checks instead of a ranked recommendation.

If the user wants to investigate one of those funders further, use the host assistant's web search when available to inspect the funder's current official pages for program scope, eligibility, and application route. The peer table supplies names and historical leads; it does not confirm a current opportunity. Cite the pages actually checked and keep unresolved checks in the research queue.

The peer table helps inspect rows and sources. In prose, include the strongest observed patterns and the coverage limit even when the widget renders.

## In Claude

In Claude Code the tools appear as `mcp__impact-recon__<tool>`; in claude.ai they sit under the Impact Recon Alpha connector. Every tool is read-only, so call them freely. There is no save tool on this connection; keep findings in the answer.

Use Claude's native web search and page fetch for currentness checks and original sources. Fetch the page you cite; a search snippet is a lead.

Impact Recon returns structured data for a text answer. Render comparisons as Markdown tables yourself; do not wait for an app panel.

When the plugin is installed, the guides are already local skills. Call `get_research_workflow` only for a reference you do not have or to confirm the deployed version.

In Claude Code, when several candidates need the same verification, delegate one candidate per parallel subagent with the same rubric and question definition, then collect one disposition table. Keep the final judgment in the main thread.

Deliverables: in claude.ai use an Artifact or Doc for a packet; in Claude Code write a dated Markdown file into the project and say where it is. State that nothing was saved to Impact Recon.

Keep a claim/source table in the answer. Mark each claim observed, user-stated, inferred, recommended or unknown.

Render the peer-funder matrix as a Markdown table: funder, peers observed, focal status, latest year, example filing. Put the coverage limit directly under the table.
