# Metric semantics to preserve

Based on the Spiral tool contracts inspected on 2026-10-17. Current callable schemas remain authoritative if they change.

- Account totals and ranked-ad windows use completed UTC days and exclude today. `all_time` means all stored history.
- `latest_data_date` is the last observed row, not a completeness guarantee. Sync time is not a metrics snapshot guarantee.
- Ranked lists may sort on stored configured-event CPA while displayed `metrics.cpa` uses `account.conversion.metric`. Validate the metric basis before calling the sorted first row the lowest displayed-CPA ad.
- Per-ad detail dates are independent of the preceding ranked-list timeline. Details preserve internal configured-event reporting; their CPA can differ from account-list projections.
- A name-group representative UUID returns the single representative ad's data. With `group_by_name` and `only_active`, a group needs an active member, but its metrics include all members.
- Per-ad breakdowns have a fixed `last_90d` window, not the selected ranked-list window. Account breakdowns have their own snapshot controls. Do not compare them as if periods match.
- Daily data supports inclusive start/end dates; missing daily metrics are omitted. Missing raw counts and rates in detail responses can have zero defaults. Do not claim measured zero without corroboration when this distinction matters.
- Currency comes from the account. CTR is percent; ROAS is a ratio. Conversion score uses internal purchase actions and is not automatically a score for the account's selected trial/install event.
- Hook/watch/social and account-relative scores are not interchangeable with raw rates or externally comparable benchmarks. Use documented meanings only.
- Keep pagination filters stable. If a snapshot refresh invalidates a cursor, restart that retrieval without a cursor.

For compatible rows, aggregate from raw numerators and denominators: CPA = total spend / total conversions; CTR = total clicks / total impressions × 100; ROAS = total attributed value / total spend. Do not average ratios across ads. Undefined denominators remain undefined. Never combine currencies, events, overlapping aggregates, or incompatible attribution/reporting bases without reconciliation.

Concept families inferred from media may differ from name groups. Label inferred membership, avoid duplicate counting, and report coverage. A sampled comparison is not an exhaustive account-level result. Observational creative tags and performance correlations do not prove creative causation.
