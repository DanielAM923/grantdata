---
name: issue-to-funding-map
description: Map an issue and U.S. state to organizations doing the work, then inspect their observed funders. Use for questions like who funds Chicago veteran services; do not use for an open-grants-only search.
---

# Issue to funding map

Read the shared [evidence rules](../azimuth-research/references/evidence-rules.md) and [connection boundaries](../azimuth-research/references/connection-boundaries.md). Check the selected connection’s actual tool catalog first. If the three issue tools are absent, follow the same discovery and source-review method using native primary-source research and report the missing graph route; do not invent tool results.

Start with the work, then follow support. Azimuth's full landscape method is broader than this MCP currently supports: graph-route probes, multiple independent organization discovery methods, EIN deduplication, sampled precision and seed-recall review, whole-org versus named-program classification, funding-neighbor expansion, reclassification of neighbors, and graph writeback. This guide contains the portable method. Landscapes built earlier for specific organizations are not MCP data and must not be presented as a fresh or public result; do not describe the present MCP as reproducing that full process end to end.

1. Identify the issue and state. Call `search_interventions` and select the specific returned taxonomy ID. If the phrase is ambiguous, narrow it with the user rather than guessing. Call `map_issue_funding` with that ID and state, plus city when relevant. Its first call is **candidate discovery only**; no funders are returned.
2. Read the returned `basis` for every organization. Apply the [relevance check](../relevance-check/SKILL.md) before presenting a candidate as a verified organization, named program, peer, or prospect. `organization_route` is an active organization-level graph path; `named_program_route` means the issue is attached to a program inside a broader parent; `taxonomy_candidate` is a broad fallback. Use `route_basis_filter=organization` and `route_basis_filter=named_program` when the two kinds need separate review. Routes can be noisy. Inspect the organization's own program page or another primary source before stating that it serves the population or geography. Do not call a broad parent a veteran nonprofit because it has a veteran program. Use `candidate_offset` to inspect later bounded pages when the first page is full, then search beyond those pages with native research when needed; no page is a complete landscape. For a claimed landscape or shortlist, deduplicate identities and check a curated known-organization seed plus a sample of candidates; if those gates are absent, label the output a preliminary set of leads.
3. Call `map_issue_funding` again with the source-checked `selected_eins` and a small set of specific `purpose_terms` including relevant word forms such as `veteran`, `veterans`, and `military`. A selected organization with no issue route is labeled `selected_unrouted`; investigate the graph gap separately. Read its two funding lanes separately. `purpose_rows` are **individual filing rows whose purpose text mentions a requested term**; a mixed-purpose row's full amount is not issue-dedicated spending. `incoming_funding_signals` are historical funders of the selected organization regardless of purpose; they show who to investigate but do **not** establish support for the selected issue or named program. A linked filing there is only an example for the funder-recipient pair and does not verify the aggregate. Schedule I purpose rows currently lack a direct filing URL in this tool; foundation rows may have one. Inspect the original award or filing before claiming what it funded. A zero-row result in either lane means this warehouse path found nothing, not that the organization has no supporters.
4. When another recipient would help test a support pattern, call `expand_issue_funder` for a selected funder, state and the same purpose terms; pass the starting organization as `exclude_eins` when looking for other recipients. This returns other purpose-mention rows, not verified peers; recipient state is an address, not a service area. Check each organization's work before treating it as a peer.
5. For the most relevant supporters, inspect the funder's own current pages for role, geography, eligibility and approach rules. Separate incumbent supporters, relationship leads, open application routes, partners and unresolved names. A grant history alone never becomes an application recommendation. If the requested current check cannot be made, report a research lead with the missing check.
6. If the map is thin, say where the route broke: issue taxonomy, organization/program evidence, missing funding edge, grant-purpose evidence or current approach information. Use native primary-source research when available to repair the answer. A missing MCP edge does not prove no relationship. If the user explicitly asks to save a public-source-backed correction, use `save_enrichment_candidate` when available; otherwise keep it as a review note in the conversation.

Explain the path in plain language: “We found groups doing the work, checked who supported them, and then checked what that support actually covered.” Show the organization, named program when relevant, supporter, date/source, and remaining uncertainty. The current MCP provides candidate routes and purpose-text filing rows; it does not automatically reproduce the full classification and source-review process.

## In Claude

In Claude Code the tools appear as `mcp__impact-recon__<tool>`; in claude.ai they sit under the Impact Recon Alpha connector. Every tool is read-only, so call them freely. There is no save tool on this connection; keep findings in the answer.

Use Claude's native web search and page fetch for currentness checks and original sources. Fetch the page you cite; a search snippet is a lead.

Impact Recon returns structured data for a text answer. Render comparisons as Markdown tables yourself; do not wait for an app panel.

When the plugin is installed, the guides are already local skills. Call `get_research_workflow` only for a reference you do not have or to confirm the deployed version.

In Claude Code, when several candidates need the same verification, delegate one candidate per parallel subagent with the same rubric and question definition, then collect one disposition table. Keep the final judgment in the main thread.

Deliverables: in claude.ai use an Artifact or Doc for a packet; in Claude Code write a dated Markdown file into the project and say where it is. State that nothing was saved to Impact Recon.

Keep a claim/source table in the answer. Mark each claim observed, user-stated, inferred, recommended or unknown.
