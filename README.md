```yaml
title: Jungian Shadow Hunting - Growth Detected in Uncomfortable Areas
id: 8f3c2a9b-7d4e-4b1a-9f2d-5e6f7a8b9c0d
status: experimental
description: |
  Detects instances where critical insights, fixes, or value ("that which you most need")
  are located in the least desirable areas. This rule identifies avoidance patterns in self-analysis.
  
  Core philosophy: "That which you most need is to be found where you least want to look." 
  - Carl Jung
  
  Real-world applications:
  - Personal/organizational growth: Confronting blind spots.
logsource:
  category: audit
  product: universal
  service: introspection
detection:
  selection_avoidance:
    location:
      - "comfort_zone"
      - "thinking_inside_the_box"
      - "group_consensus"
    behavior:
      - "avoidance_detected"
      - "rationalization_active"
      - "postponement_pattern"
  selection_uncomfortable:
    location:
      - "repressed_feedback"
      - "personal_blind_spots"
      - "emotional_resistance_areas"
    indicators:
      - "high_potential_value"
      - "insight_density_high"
      - "root_cause_likely"
  condition: selection_avoidance and selection_uncomfortable
falsepositives:
  - Jack of all trades, master of none
level: medium
tags:
  - philosophy
  - carl-jung
author: Now me (Inspired by Carl Jung)
date: 2026-06-15
references:
  - https://en.wikipedia.org/wiki/Carl_Jung
  - https://sigmahq.io (Sigma rule format)
```

&nbsp;

&nbsp;
