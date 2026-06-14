# Astraform

**Customer outcome simulation for AI agents before launch.**

Most AI evals ask whether the agent behaved correctly. Astraform asks the
harder question: **what happens to customers and the business if this change
ships?**

Astraform helps teams test proposed customer-facing AI changes against
synthetic customer cohorts, business policies, tools, APIs, workflow rules, and
domain systems before production. The output is not a toy benchmark score. It
is replayable launch evidence: who was affected, what failed, which controls
held, and whether the release should continue, needs controls, or should stop.

## What We Help Teams Catch

- Customer harm hidden behind passing agent-level tests.
- Policy and compliance gaps in realistic multi-step journeys.
- Escalation failures when agents, tools, and human handoff rules interact.
- Risky tool/API permission changes before they touch real customers.
- Operational bottlenecks that only appear across cohorts and simulated time.

## How Astraform Works

1. Define the launch decision or policy change under review.
2. Run baseline and proposed paths through synthetic customer cohorts.
3. Exercise agents, APIs, tools, MCP/A2A workflows, policies, and domain
   providers over simulated time.
4. Compare business outcomes, failure reasons, controls, and customer impact.
5. Produce replayable evidence for product, risk, compliance, and engineering
   review.

## Current Wedge

The first proof is a banking customer outcome wind tunnel: hardship, disputes,
fraud escalation, support paths, policy changes, and tool-permission changes
tested before customer-facing AI reaches production.

Banking is the proof domain, not the platform identity. The platform is built
for any domain where AI decisions, business rules, and customer outcomes have
to be tested before launch.

## For Domain Engineers

Astraform is protocol-first. Domain teams connect their business world through
`remote-domain.v1` providers:

- you own business state, policies, actions, and evidence projections
- Astraform owns simulation time, replay, guardrails, and outcome evidence
- providers expose a manifest and lifecycle operations
- SDKs and conformance checks keep implementations honest

## Links

- Website: [astraform.ai](https://astraform.ai)
- Developer docs: [astraform.ai/developers.html](https://astraform.ai/developers.html)
- Partner preview: [astraform.ai/partner-preview](https://astraform.ai/partner-preview/)
- Contact: [admin@astraform.ai](mailto:admin@astraform.ai)
