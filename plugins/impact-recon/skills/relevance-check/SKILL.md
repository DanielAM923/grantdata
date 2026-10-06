---
name: relevance-check
description: Check whether discovered organizations, programs, peers, or funders fit a specific nonprofit research question before presenting them as a shortlist. Use after graph or search discovery when names, taxonomy tags, shared funders, or broad geography may be misleading.
---

# Relevance check

Read the shared [evidence rules](../azimuth-research/references/evidence-rules.md). A search hit is a candidate, not a finding. The question defines relevance: record the population or issue, activity, geography, organization role, and (for funding questions) instrument and intended use. Recheck these if the user changes the ask.

For each candidate:

1. **Resolve identity and role.** Match the actual organization and EIN when available; keep a program, parent, affiliate, federation, and local chapter distinct. Classify the issue connection as `primary_organization`, `named_program_in_broad_org`, `adjacent`, `unresolved`, or `out_of_scope`. For peers, also state the comparison role and one material difference. A plausible but unresolved name stays provisional; exclude only a duplicate, clearly wrong entity, or contradicted candidate.
2. **Verify the work and place.** Follow the graph route to the organization's own program page, report, filing program description, or another direct source. Say what it actually does and who it serves. A name, NTEE code, broad tag, purpose-word match, recipient address, or funder-neighbor link alone cannot establish service delivery in the requested place. Record whether geography is a service area, program site, headquarters, mailing address, or unknown.
3. **Check the exact relationship being claimed.** Separate an issue-matching grant-purpose row, general support to an organization with relevant work, a shared funder, a capital/deal participant, and a current grant opportunity. Preserve the individual source, date, amount basis, recipient and stated purpose where available. General support to a broad parent is not proof of support for its named program. Mixed-purpose grant dollars are not issue-dedicated dollars. A shared funder generates another candidate to review, not an endorsement or warm introduction.
4. **Assess funder fit separately.** For a prospect, check current official priorities, eligible applicant and place, grant versus investment instrument, typical award basis, invitation/application route, and timing. A historical supporter may be a stewardship lead while an unverified peer funder remains a research lead. Use the [funder review](../funder-review/SKILL.md) when the user needs a qualified approach plan.
5. **Make a disposition with the missing check.** Return `include`, `include_as_program`, `context_only`, `provisional`, or `set_aside`, plus a short reason, source and check date, confidence, and the most important unresolved fact. Keep inclusion, relevance to this question, and evidence strength separate; a highly relevant organization may have sparse funding data. Missing graph edges or a zero-row search do not prove no funding or no work.

For a **landscape or published shortlist**, review a known-organization seed for omissions, inspect a sample across routes and ranks for false positives, and check whether federated chapters or broad parents dominate the result. Report the sample, misses, and limitations; a retrieval cap is not a complete universe. If the gate is weak, present a smaller reviewed set and a research queue. Reclassify recipients found through funder expansion with the same steps before adding them. The current MCP supplies bounded candidate routes and funding observations; source review and coverage testing still require the host's research capabilities and human judgment.

Explain the decision in ordinary language: “This group directly serves the requested population here,” “this larger organization runs a relevant program,” or “we found a possible connection but have not confirmed it.” Never turn a candidate list into a claim that all listed organizations are equivalent prospects.

## In Claude

In Claude Code the tools appear as `mcp__impact-recon__<tool>`; in claude.ai they sit under the Impact Recon Alpha connector. Every tool is read-only, so call them freely. There is no save tool on this connection; keep findings in the answer.

Use Claude's native web search and page fetch for currentness checks and original sources. Fetch the page you cite; a search snippet is a lead.

Impact Recon returns structured data for a text answer. Render comparisons as Markdown tables yourself; do not wait for an app panel.

When the plugin is installed, the guides are already local skills. Call `get_research_workflow` only for a reference you do not have or to confirm the deployed version.

In Claude Code, when several candidates need the same verification, delegate one candidate per parallel subagent with the same rubric and question definition, then collect one disposition table. Keep the final judgment in the main thread.

Deliverables: in claude.ai use an Artifact or Doc for a packet; in Claude Code write a dated Markdown file into the project and say where it is. State that nothing was saved to Impact Recon.

Keep a claim/source table in the answer. Mark each claim observed, user-stated, inferred, recommended or unknown.

Run per-candidate checks in parallel subagents, one candidate each. Return one table: candidate, role class, geography basis, disposition, source and check date, missing check.
