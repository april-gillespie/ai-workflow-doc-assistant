# AI-Assisted Home Network Diagnostic Case Study

## Summary

This case study documents a practical, AI-assisted troubleshooting workflow used to diagnose inconsistent home Wi-Fi performance. The objective was to determine whether poor perceived internet performance was caused by the internet service provider, the router, the client device, or localized Wi-Fi coverage limitations within the home.

The workflow converted an ambiguous household complaint into a structured diagnostic process using location-based speed testing, screenshot-based data extraction, and human review of the resulting recommendation.

## Problem Statement

A household experienced inconsistent internet performance in common living areas despite having a gigabit internet plan. The initial symptom was broad and non-specific: the internet felt slow in areas where the family regularly used streaming devices, mobile devices, and general home internet services.

The primary question was whether the household needed a faster internet plan, different equipment, a Wi-Fi extender, or a different placement strategy.

## Constraints

- No new tools or paid diagnostic software were used.
- Testing was performed with consumer-facing ISP app speed-test results.
- Results were interpreted from screenshots and manually validated against observed household locations.
- Public documentation excludes personal identifiers, precise home layout, account details, network names, and family-specific room names.

## Inputs

The workflow used screenshots from the ISP speed-test interface showing two distinct measurements:

1. Router-side throughput from the ISP network to the home router.
2. Client-device throughput from the router to the mobile device at specific household locations.

Location labels were generalized for documentation purposes.

## Method

1. Establish a baseline for the internet service entering the home by reviewing router-side speed-test results.
2. Test the same personal device from multiple household locations.
3. Compare device-side results against the router-side baseline.
4. Separate service-level performance from Wi-Fi coverage performance.
5. Identify transition zones where Wi-Fi signal remained strong enough to support a possible extender or mesh-node placement.
6. Develop a recommendation based on measured results rather than plan speed assumptions.

## Sanitized Test Results

| Test Location | Device Download | Device Upload | Interpretation |
|---|---:|---:|---|
| Router area | 819 Mbps | 580 Mbps | Excellent device-side Wi-Fi performance near the router |
| Upstairs room | 193 Mbps | 98 Mbps | Adequate performance for normal household use |
| Downstairs living area | 81 Mbps | 29 Mbps | Localized weak zone |
| Aquarium / adjacent downstairs area | 86 Mbps | 37 Mbps | Similar weak-zone result, suggesting a local coverage issue |
| Bottom of stairs / transition outlet | 291 Mbps | 116 Mbps | Viable candidate location for extender placement |

Router-side throughput remained consistently above the subscribed gigabit plan level during testing, with results around 1.13-1.15 Gbps. This indicated that the service entering the home was performing well and that the limiting factor was not the ISP connection.

## Findings

The test pattern showed a clear distinction between internet service performance and Wi-Fi coverage performance. The router was receiving better-than-plan throughput, and the personal device achieved high speeds when tested near the router. However, device-side performance dropped substantially in downstairs living areas.

The most likely cause was localized Wi-Fi signal degradation between floors, potentially influenced by distance, building materials, furniture, water mass from an aquarium, and general signal-path obstruction.

The bottom-of-stairs outlet provided substantially better performance than the living area while still being positioned between the router and the weak zone. This made it a reasonable candidate for extender placement, because an extender should be placed where it can still receive a strong upstream signal rather than directly inside the weakest coverage area.

## Recommendation

Do not upgrade the internet plan based on the observed data. The incoming service was not the bottleneck.

Prioritize Wi-Fi coverage improvement instead:

1. Adjust router placement where possible, keeping it elevated, open, and away from large obstructions.
2. If using an extender, place it in the transition zone rather than the weakest room.
3. Re-test the downstairs living area after extender installation to confirm measurable improvement.
4. Treat success as improved stability and a practical increase in downstairs device speed, not full gigabit performance at every location.

## AI-Assisted Workflow Contribution

AI assistance was used to accelerate the diagnostic process by interpreting screenshots, extracting relevant speed-test values, explaining unfamiliar networking concepts, and structuring the troubleshooting sequence. This reduced manual transcription effort and helped convert a vague household symptom into a testable diagnostic workflow.

AI was not used as the final authority. Final conclusions were based on observed speed-test results, repeated location-based measurements, and human validation of the household context.

## Value Demonstrated

This workflow demonstrates:

- Practical troubleshooting from incomplete real-world symptoms.
- Evidence-based separation of ISP performance from local Wi-Fi performance.
- Screenshot-based data extraction and documentation.
- Use of AI to reduce analysis and documentation effort while retaining human judgment.
- Clear communication of technical findings for a non-specialist household decision.
- Cost-aware recommendation development based on measured need rather than default upgrades.

## Public Sharing Notes

This case study is intentionally sanitized. It does not include the real network name, account information, precise home layout, personal room names, addresses, or raw screenshots. The documented values are sufficient to show the diagnostic method without exposing private household information.
