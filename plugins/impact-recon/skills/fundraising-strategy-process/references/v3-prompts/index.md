Generated from the maintained v3 source; regenerate with scripts/mcp/build_research_library.py.

## Host/MCP adaptation

Use the research method below with this connection's actual catalog and the user's available conversation/artifact context. App placeholders, closed schemas, Neon state, job planes, UI actions, provider policies and revision receipts are source-app contracts, not capabilities or instructions to execute them here. Do not invent their presence or require their setup. Use the host assistant's native research for current primary sources. Return useful prose unless the user requests a schema. Separate copy-ready strategy from supporting analysis, evidence gaps and provisional candidates, keeping both visible to the user; no private metadata store is implied. Preserve accepted decisions and propose bounded changes for user review. Inactive/deferred source prompts supply drafting methods only, not active v3 features. Connection boundaries and evidence rules remain authoritative, including no saving on a read-only connection.

# v3 prompt library

Read [stage profiles](stage-profiles.md) for the relevant stage and linked modules. For a first six-chapter draft, use shared context and Fast Intake; for improving an existing artifact, use the section-helper methods. Consultant View remains inactive in the source app; its review method can guide conversational analysis without implying that app feature is active.

- [strategy_app/v3/agent/strategy-framework/angle-decision.v1.md](strategy-framework--angle-decision.v1.md)
- [strategy_app/v3/agent/strategy-framework/constitution.v1.md](strategy-framework--constitution.v1.md)
- [strategy_app/v3/agent/strategy-framework/entry-mode.v1.md](strategy-framework--entry-mode.v1.md)
- [strategy_app/v3/agent/strategy-framework/evidence-update.v1.md](strategy-framework--evidence-update.v1.md)
- [strategy_app/v3/agent/strategy-framework/final-review.v1.md](strategy-framework--final-review.v1.md)
- [strategy_app/v3/agent/strategy-framework/funding-route-update.v1.md](strategy-framework--funding-route-update.v1.md)
- [strategy_app/v3/agent/strategy-framework/initial-draft.v1.md](strategy-framework--initial-draft.v1.md)
- [strategy_app/v3/agent/strategy-framework/peer-update.v1.md](strategy-framework--peer-update.v1.md)
- [strategy_app/v3/agent/strategy-framework/roadmap-update.v1.md](strategy-framework--roadmap-update.v1.md)
- [strategy_app/v3/agent/strategy-prompt-family/consultant-view.v1.md](strategy-prompt-family--consultant-view.v1.md)
- [strategy_app/v3/agent/strategy-prompt-family/fast-intake-case-and-opportunities.v1.md](strategy-prompt-family--fast-intake-case-and-opportunities.v1.md)
- [strategy_app/v3/agent/strategy-prompt-family/fast-intake-first-value.v1.md](strategy-prompt-family--fast-intake-first-value.v1.md)
- [strategy_app/v3/agent/strategy-prompt-family/fast-intake-position-and-peers.v1.md](strategy-prompt-family--fast-intake-position-and-peers.v1.md)
- [strategy_app/v3/agent/strategy-prompt-family/shared-strategy-context.v1.md](strategy-prompt-family--shared-strategy-context.v1.md)
- [strategy_app/v3/agent/artifact-section-prompts.v1.md](agent--artifact-section-prompts.v1.md)

## Source binding

```json
{
  "library_id": "azimuth.strategy_prompt_structure",
  "framework_version": "1.0.0",
  "structure_sha256": "5ba03a78f919be0bbefca761399fecd6efd56f30608e0145242698ca05e2321c",
  "family_version": "v4_first_value_v1",
  "stages": 11,
  "sources": [
    {
      "source": "strategy_app/v3/agent/strategy-framework/angle-decision.v1.md",
      "sha256": "7d21b7c13e6578ae48899da3bb5941015eba4a89f0e4517cf6dbb825a640fbc7",
      "reference": "strategy-framework--angle-decision.v1.md"
    },
    {
      "source": "strategy_app/v3/agent/strategy-framework/constitution.v1.md",
      "sha256": "ac3a552e5c4ad08d6c52995e427240bac73498f0950efd73b9e87e4113eed8a4",
      "reference": "strategy-framework--constitution.v1.md"
    },
    {
      "source": "strategy_app/v3/agent/strategy-framework/entry-mode.v1.md",
      "sha256": "3bb87abe79dca2fc2b2577eeb5660cb868e6e5e4ff189a9b1fe8aa968c8c3ea8",
      "reference": "strategy-framework--entry-mode.v1.md"
    },
    {
      "source": "strategy_app/v3/agent/strategy-framework/evidence-update.v1.md",
      "sha256": "75f2b312a38bc39698ef78f54f44fe1e35cfffac32b2524593798c92b6b69fd2",
      "reference": "strategy-framework--evidence-update.v1.md"
    },
    {
      "source": "strategy_app/v3/agent/strategy-framework/final-review.v1.md",
      "sha256": "08d5c69ada772bdd9593fbe09ba6831fb63a44424646d773393063f7b073431b",
      "reference": "strategy-framework--final-review.v1.md"
    },
    {
      "source": "strategy_app/v3/agent/strategy-framework/funding-route-update.v1.md",
      "sha256": "c332acf60d254ba8ac7b4f2deb5353f9424d121973358ac3117b87459a53c1ac",
      "reference": "strategy-framework--funding-route-update.v1.md"
    },
    {
      "source": "strategy_app/v3/agent/strategy-framework/initial-draft.v1.md",
      "sha256": "8612c752d5ff19864fe36982d2937b50f97b70b242151ed242c82e59eb8b1e79",
      "reference": "strategy-framework--initial-draft.v1.md"
    },
    {
      "source": "strategy_app/v3/agent/strategy-framework/peer-update.v1.md",
      "sha256": "72a58675f3826cf1305d24c6253632e2850dc0a62164d12b15856f6c874e888f",
      "reference": "strategy-framework--peer-update.v1.md"
    },
    {
      "source": "strategy_app/v3/agent/strategy-framework/roadmap-update.v1.md",
      "sha256": "1dcbf6990ca2e07b0bbab923ba37bedc57a8bf0ee2821bb2ae2fe72d745797b5",
      "reference": "strategy-framework--roadmap-update.v1.md"
    },
    {
      "source": "strategy_app/v3/agent/strategy-prompt-family/consultant-view.v1.md",
      "sha256": "6fb5c2ed9ec2458375baf812ee3be9fa54c49ba4f765bd4d5ce50ee3dc5bbdc4",
      "reference": "strategy-prompt-family--consultant-view.v1.md"
    },
    {
      "source": "strategy_app/v3/agent/strategy-prompt-family/fast-intake-case-and-opportunities.v1.md",
      "sha256": "2b6fff7bc9252d6ee7b3c06ce3a8776e422579ce6464fbb7aff46f180da54632",
      "reference": "strategy-prompt-family--fast-intake-case-and-opportunities.v1.md"
    },
    {
      "source": "strategy_app/v3/agent/strategy-prompt-family/fast-intake-first-value.v1.md",
      "sha256": "aae8915cea6566affc30f079d71d878344ab6d5dbb0b016dadd63ec62cc682d2",
      "reference": "strategy-prompt-family--fast-intake-first-value.v1.md"
    },
    {
      "source": "strategy_app/v3/agent/strategy-prompt-family/fast-intake-position-and-peers.v1.md",
      "sha256": "fb550223ebbc14dad26002b4d3fa10eae4a60a6d94d7d7049584565206ae1122",
      "reference": "strategy-prompt-family--fast-intake-position-and-peers.v1.md"
    },
    {
      "source": "strategy_app/v3/agent/strategy-prompt-family/shared-strategy-context.v1.md",
      "sha256": "b007ecd56dea3be80c9598080181f069437a88c3c5f7913c664ccf42dd10e649",
      "reference": "strategy-prompt-family--shared-strategy-context.v1.md"
    },
    {
      "source": "strategy_app/v3/agent/artifact-section-prompts.v1.md",
      "sha256": "51eaec10d29e9516874ad66ab289fdcecaafd6242f54b4f881e1d925263de8c4",
      "reference": "agent--artifact-section-prompts.v1.md"
    }
  ]
}
```
