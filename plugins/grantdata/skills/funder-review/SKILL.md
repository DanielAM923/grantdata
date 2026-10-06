---
name: funder-review
description: Verify a named funder or partner's current program fit, instrument, eligibility, amount basis and approach route. Use to qualify historical funding leads, refresh stale evidence or build a source-backed account plan.
---

# Funder review

Read [shared evidence rules](../azimuth-research/references/evidence-rules.md). Start with the applicant, concrete case and selected funder/partner rather than an undifferentiated web prospect list. Resolve identities using `search`/`fetch`; use selected-peer observations or purpose rows only when the relevant tools are available. An incoming funding card for a foundation does not list its outgoing grants.

Inspect current official guidelines, application/program pages, original award/filing records, reports and project announcements with native search. Keep warehouse age, source publication date and date checked distinct. Old warehouse visibility does not establish inactivity; an active website does not establish an open relevant cycle. Do not roll a past deadline into a new year.

Build an account row with program/instrument; applicant/geography/activity fit; amount and individual-award basis; current cycle and timezone if stated; invitation/application/sponsor route; official contact/channel; relationship provenance; materials/readiness; source/check date; and proposed pursue, validate, steward, hold or set-aside disposition. Leave uncertain amounts and contacts unknown. Do not turn a multi-year aggregate, cohort total or deal value into a typical grant check.

For public bridge, DAF/donor or housing-finance research read [public routes and capital](references/public-routes-and-capital.md). Those methods add source-backed leads, not warm relationships. Prioritize an application or outreach only when route and case fit are supported; otherwise prioritize the missing checks. Include the applicant's capacity and timing before proposing a solicitation plan.

For a roster, preserve unresolved entities and material blockers in a short queue. Follow [research review](../azimuth-research/references/research-review.md) for conflicts and explicitly requested enrichment. Native research supplies current checks; the MCP does not silently call another web-search provider.

## In Claude

In Claude Code the tools appear as `mcp__grantdata__<tool>`; in claude.ai they sit under the Grant Data connector. Every tool is read-only, so call them freely. There is no save tool on this connection; keep findings in the answer.

Use Claude's native web search and page fetch for currentness checks and original sources. Fetch the page you cite; a search snippet is a lead.

Grant Data returns structured data for a text answer. Render comparisons as Markdown tables yourself; do not wait for an app panel.

When the plugin is installed, the guides are already local skills. Call `get_research_workflow` only for a reference you do not have or to confirm the deployed version.

In Claude Code, when several candidates need the same verification, delegate one candidate per parallel subagent with the same rubric and question definition, then collect one disposition table. Keep the final judgment in the main thread.

Deliverables: in claude.ai use an Artifact or Doc for a packet; in Claude Code write a dated Markdown file into the project and say where it is. State that nothing was saved to Grant Data.

Keep a claim/source table in the answer. Mark each claim observed, user-stated, inferred, recommended or unknown.

Fetch each funder's current guidelines or program page and cite its URL and the date checked. Keep warehouse year, page publication date and check date distinct in the account row.
