Generated from the maintained v3 source; regenerate with scripts/mcp/build_research_library.py.

## Host/MCP adaptation

Use the research method below with this connection's actual catalog and the user's available conversation/artifact context. App placeholders, closed schemas, Neon state, job planes, UI actions, provider policies and revision receipts are source-app contracts, not capabilities or instructions to execute them here. Do not invent their presence or require their setup. Use the host assistant's native research for current primary sources. Return useful prose unless the user requests a schema. Separate copy-ready strategy from supporting analysis, evidence gaps and provisional candidates, keeping both visible to the user; no private metadata store is implied. Preserve accepted decisions and propose bounded changes for user review. Inactive/deferred source prompts supply drafting methods only, not active v3 features. Connection boundaries and evidence rules remain authoritative, including no saving on a read-only connection.

Source: `strategy_app/v3/agent/strategy-framework/evidence-update.v1.md`
SHA-256: `75f2b312a38bc39698ef78f54f44fe1e35cfffac32b2524593798c92b6b69fd2`

# Evidence-delta synthesis

Apply a bounded, material evidence delta to the current strategy. This module
does not authorize a new search, a whole-document rewrite, or a stage gate;
the current stage contract controls those decisions.

For every supplied evidence receipt:

1. confirm it belongs to the focal organization and current framework run;
2. confirm status, terminality, authority, scope, freshness, access boundary,
   and source pointer;
3. de-duplicate it against prior receipts and identify the prior claim,
   assumption, decision, or gap it bears on;
4. classify the resulting statement as `fact`, `user_stated`, `inference`,
   `recommendation`, or `gap`; and
5. map the material impact to authorized section IDs and dependent stage
   receipts.

Promote an assumption or user statement to `fact` only when the receipt has
the required authority. Treat old, conflicting, partial, failed, or differently
scoped evidence as a dated caveat or gap, not as a replacement fact. A receipt
that merely repeats current support is not a change.

Build the smallest patch that makes the strategy honest:

- preserve unaffected sections byte-for-byte where the effect contract allows;
- preserve user-authored and protected content;
- preserve accepted decisions unless the evidence creates an explicit,
  material contradiction;
- add, update, or resolve deterministic gaps with reasons;
- identify invalidated downstream receipts and the allowed loopback; and
- explain the evidence-to-change link for every proposed patch.

If new evidence conflicts with an accepted decision or protected wording,
propose the conflict and options for review. Do not silently choose. If a
remaining input is private or judgmental, ask only after the ordered retrieval
lanes are terminal and only when the answer can change the stage result. If the
evidence is insufficient but the stage permits continuation, mark the gap and
limit the conclusion.

Return bounded typed section patches, a focused question, a blocked-stage
result, or `no_change`. Return `no_change` when the delta is duplicate,
immaterial, out of scope, unsupported, or already reflected in the accepted
revision. Never regenerate the whole strategy.
