# Astraform

**Customer outcome simulation for AI agents before launch.**

Most AI evals ask whether the agent behaved correctly. Astraform asks the
harder question: **what happens to customers and the business if this change
ships?**

Astraform helps teams investigate proposed customer-facing AI changes against
synthetic customer cohorts, business policies, tools, APIs, workflow rules, and
domain systems before production. Available run evidence helps reviewers trace
customer decisions, failures, tool use, and business consequences under the
simulation's stated assumptions.

Access is currently an **engineer-assisted Partner Preview**. Deployment,
integration, model access, test data, and evidence scope are agreed for each
engagement.

## What We Help Teams Investigate

- Customer harm hidden behind passing agent-level tests.
- Policy and compliance gaps in multi-step journeys.
- Escalation failures across agents, tools, and human handoff rules.
- Risky tool/API permission changes before they touch real customers.
- Business consequences that emerge over simulated time.

## From Customer Configuration to Evidence

1. Define the launch decision or policy change under review and the customer
   journeys to exercise.
2. Configure and publish customer personas and goals, then select a
   deployment-owned model binding, scoped tools, and any partner-agent target.
   Customer model adapters support Gemini, Ollama, and OpenAI.
3. Connect an existing A2A partner agent for conversation testing. Add a
   supported native domain profile and deployment binding when partner business
   data must progress over simulated time.
4. Launch an Agent Journey simulation (`nativeAgentJourney`) through the
   platform API. Customers make model-driven decisions; native logical events
   schedule work over simulated time.
5. Inspect available customer decisions, tool receipts, partner exchanges,
   domain evidence, and recorded failures. Use that evidence to review the
   configured scenarios and compare baseline and proposed behavior.

Completed execution does not mean customer goals succeeded. Retained evidence
is bounded by the integration and recorded source; it is not a complete raw
transcript of every system interaction.

## Platform and Domain Boundary

Astraform coordinates customer agents, scheduled logical events, run execution,
and evidence. There is no global simulation clock or tick broadcast.

Domain teams keep business state, rules, actions, and evidence projections
behind `remote-domain.v1` providers. MCP gives customers access to scoped tools;
A2A supports partner-agent exchanges. MCP or A2A connectivity alone does not
integrate a partner's time-dependent business work: that requires a supported
native domain profile and deployment binding.

Provider conformance checks the supported contract and lifecycle. It does not
certify full runtime integration, recovery, authorization, or business outcomes.

## Published SDKs and Contracts

Each existing author kit includes **domain-provider helpers and a generated
platform client**. Use the provider helpers to implement your domain boundary
and the platform client to configure customers, launch simulations, and retrieve
available evidence through the supported API surface.

- **Java 0.4.0:** [`ai.astraform:remote-domain-author-kit-java` on Maven Central](https://central.sonatype.com/artifact/ai.astraform/remote-domain-author-kit-java/0.4.0).
- **Python 0.3.0:** [`astraform-remote-domain-author-kit` on PyPI](https://pypi.org/project/astraform-remote-domain-author-kit/0.3.0/).
- **Shared contracts 1.2.0:** [release and contract bundle](https://github.com/astraform/remote-domain-contracts/releases/tag/v1.2.0).
- **Platform API:** [customer configuration, launch, and evidence schema](https://github.com/astraform/remote-domain-contracts/blob/v1.2.0/platform-api/v1/openapi/platform/experiment/experiments.yaml).
- **Provider API:** [`remote-domain.v1` contracts and profiles](https://github.com/astraform/remote-domain-contracts/tree/v1.2.0/remote-domain/v1).

These package and schema links are public. Access to private implementation
repositories is separate from access to the published packages.

## Preview Limits

Simulation findings are stress-test evidence, not production forecasts or
automatic launch approval. Your team remains responsible for release decisions.
Published packages and focused integration checks do not establish production
readiness, capacity at scale, or compliance certification. Partner Preview is
not a generally available hosted service.

## Links

- Website: [astraform.ai](https://astraform.ai)
- Developer docs: [astraform.ai/developers](https://astraform.ai/developers)
- Trust and evidence limits: [astraform.ai/trust](https://astraform.ai/trust/)
- Partner Preview: [astraform.ai/partner-preview](https://astraform.ai/partner-preview/)
- Contact: [admin@astraform.ai](mailto:admin@astraform.ai)
