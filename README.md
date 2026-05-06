```YAML
title: Jungian Shadow Hunting - Growth Detected in Uncomfortable Areas
id: 8f3c2a9b-7d4e-4b1a-9f2d-5e6f7a8b9c0d
status: experimental
description: |
  Detects instances where critical insights, fixes, or value ("that which you most need")
  are located in the least desirable inspection areas. This rule identifies avoidance
  patterns in threat hunting, incident response, code review, and self-analysis.
  
  Core philosophy: "That which you most need is to be found where you least want to look." 
  - Carl Jung
  
  Real-world applications:
  - Threat hunting: Deep dive into noisy/legacy logs, obscure endpoints, or dark web indicators.
  - Forensics: Checking suppressed alerts, unusual process trees, or user behavior anomalies.
  - Personal/organizational growth: Confronting blind spots, uncomfortable data, shadow processes.
logsource:
  category: audit
  product: universal
  service: introspection
detection:
  selection_avoidance:
    location:
      - "comfort_zone"
      - "familiar_logs"
      - "easy_metrics"
      - "popular_dashboards"
      - "group_consensus"
    behavior:
      - "avoidance_detected"
      - "rationalization_active"
      - "postponement_pattern"
  selection_uncomfortable:
    location:
      - "shadow_repositories"
      - "noisy_legacy_systems"
      - "repressed_feedback"
      - "dark_data_sources"
      - "personal_blind_spots"
      - "unmonitored_endpoints"
      - "emotional_resistance_areas"
    indicators:
      - "high_potential_value"
      - "insight_density_high"
      - "root_cause_likely"
  condition: selection_avoidance and selection_uncomfortable
falsepositives:
  - Routine maintenance in well-known areas
  - High-volume noise without context
  - Automated scans missing nuance
level: medium
tags:
  - philosophy
  - threat-hunting
  - shadow-work
  - detection-engineering
  - carl-jung
author: Unknown
date: 2026-05-07
references:
  - https://en.wikipedia.org/wiki/Carl_Jung
  - https://sigmahq.io (Sigma rule format)
```
