---
name: creative-analytics
description: Analyze creative performance in connected Meta ad accounts through Spiral. Use to diagnose winners, weak ads, performance changes, and creative patterns, then prioritize iterations, new concepts, or market expansion tests.
---

# Creative analytics

Turn measured performance into the next creative decision. Explain what is observed, what might explain it, and which experiment would discriminate between explanations. Competitor-only analysis belongs to creative research.

Use Spiral MCP as the primary source for connected-account performance data and creative analysis. If it is unavailable, explain the limitation before substituting another source.

## Set the measurement context

Resolve the account with `get_ad_accounts`; read `get_ad_account_details` for its conversion event, currency, reporting context, and associated app. Reuse known product context, previous tests, and user targets. A configured trial or install CPA is not customer acquisition cost. Without a business target, describe relative performance and ask for the target only when an absolute profitability or scaling decision depends on it.

Before comparing or aggregating performance, read [metric-semantics.md](references/metric-semantics.md). Align dates, events, currency, and unit of analysis. State material freshness or coverage limits. Missing data and zero performance are different.

Check returned period boundaries against the requested dates before using a relative window such as "last 30 days." If they differ, reconstruct the requested period from sufficiently complete daily data or explicitly qualify the result. Do not silently shift dates or compare overlapping windows as consecutive periods.

When the selected conversion count is missing, verify the configured event and reporting coverage, then inspect available detail and daily records. Check attribution maturity, landing sessions and event tracking where evidence is accessible; otherwise state which check requires user input or another data source. Do not classify the ad as a conversion winner or loser while this gap remains. Do not substitute another event or a conversion score for the missing count.

## Investigate the decision

Use `get_ad_account_ads` to find a relevant, manageable sample. Include meaningful spend and weaker comparators, not only low-CPA ads. Distinguish insufficiently tested ads from supported poor performance; apply user benchmarks and data sufficiency judgment rather than universal conversion-count or spend thresholds.

Use `get_ad_insight_details` for selected ads and `get_ad_insight_creative_analysis` to inspect their creative. For changes over time, use date-bounded `get_ad_insight_daily`; use account or ad breakdown tools when audience/placement mix is relevant. A single bad day does not establish fatigue. Compare multi-day patterns and consider spend shifts, audience mix, tracking, or funnel changes where evidence is available.

Treat creative analysis as fallible. Prefer measured media dimensions over an analyzer's aspect-ratio label; inspect the source or qualify material contradictions. Visible revenue claims, dashboard numbers and illustrative mockups show what an ad communicates, not independently verified performance or customer proof.

Use a shared vocabulary to compare creative: audience situation, problem, promise, hook, proof, emotional motivation, and execution format. Infer concept families from creative evidence; names are hints, not ground truth. Keep observations from individual ads separate from family-level findings. Do not generalize from a single winning execution or treat repeated variants as independent evidence.

## Choose the next creative action

- Weak attention with stronger downstream conversion: preserve the supported promise and conversion path; test the opening or visual hook. Use an actual defined rate when available; do not relabel a proprietary hook score as hook rate.
- Strong attention with weak conversion: check click definitions, placement mix and landing-session quality where available before blaming the creative. Use matched periods for mix comparisons; concentrated cheap clicks do not themselves prove low-quality traffic. Investigate promise-to-product fit, audience intent, proof, and funnel continuity. A creative explanation is a hypothesis; delivery, the funnel or tracking may be responsible.
- Sustained business performance with sufficient evidence: propose expansion through new executions, suitable markets, or placements. Translation alone does not establish local product-market fit.
- Deteriorating execution with a historically promising concept: propose a refresh while preserving the mechanism worth testing. Label fatigue as suspected unless the evidence supports it.
- Weak or inconclusive evidence: say what is unknown and recommend the next useful measurement or test. Do not manufacture a winner to fill a report.

Distinguish exploration of a new concept from controlled iteration of a promising execution and expansion into another market. In controlled iteration, define the intended change and the elements to hold stable. Multiple simultaneous changes can explore a direction but cannot isolate which change drove results. Even a single changed element does not establish causality without appropriate test conditions.

## Write like a marketer

Write like a perceptive creative strategist: approachable, specific, and energized by useful discoveries.

1. **Turn metrics into meaning.** Explain what the results suggest about the hook, promise, proof, or audience motivation. Separate measured performance from your explanation of it.
2. **Keep decision-making numbers visible.** Use the metrics needed to support the recommendation, with the relevant event, period, and testing volume. Avoid listing every available metric.
3. **Make the next move concrete.** Explain what to keep, what to change, and what the test should teach us. Connect each recommendation to the creative itself.
4. **Make comparisons easy.** Use compact tables when comparing ads or concepts. Give each a recognizable creative label and a reference link instead of exposing internal IDs.
5. **Keep technical checks behind the scenes.** Surface tracking gaps, immature results, or other limitations only when they change the recommendation. Use plain language such as “This needs more testing before you increase spend.”
6. **Stay confident and grounded.** Avoid generic caveats, invented explanations, and declaring winners from weak evidence.

## Return an actionable brief

Follow the user's requested scope and depth. For each decision give the essential evidence, next test and material limitation, keeping source identifiers and supporting detail compact. Include period and event, supporting metrics and sample size, creative hypothesis, proposed change, preserved elements, and the success measure where relevant. Put extensive tables and traces in supporting detail only when useful or requested. Separate measured facts from explanations and avoid arbitrary precision in confidence scores.

When asked for win rate, define winner criteria, concept grouping, evaluation window, and the eligible tested-concept denominator. Report immature or untested concepts separately. Do not substitute asset count for concept count or compute portfolio-wide win rate from a top-ads sample.

Carry the decision and creative context into production when requested. Do not silently generate assets, alter campaigns, or schedule recurring actions. Spiral's analytics tools provide insight; campaign changes require separately available publishing controls and user authorization. Describe learning in the result; claim persistent storage only after an authorized storage action succeeds.

For recurring winner-triggered production, establish the winner rule, previously processed source IDs, and per-run image cap before paid dispatch. An initial historical audit does not establish which winner is new. Generate an immediate batch only when it is explicitly requested or satisfies the agreed trigger; state honestly when scheduling is unavailable.
