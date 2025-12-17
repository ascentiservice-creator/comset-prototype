# AI Recommendation Layer

```mermaid
flowchart LR
  VALID[Compatible Comset] --> AIIN[AI Optimization Engine]

  AIIN --> SCORE[Performance<br/>Price Score]
  AIIN --> MODE[Usage Mode<br/>Gaming or Work]
  AIIN --> BUDGET[Budget Efficiency]

  SCORE --> INSIGHT[AI Insight]
  MODE --> INSIGHT
  BUDGET --> INSIGHT

  INSIGHT --> UI[Display in UI]
