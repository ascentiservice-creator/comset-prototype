# Rule Based Compatibility Engine

```mermaid
flowchart LR
  INPUT[Selected Components] --> RULES[Compatibility Rules]

  RULES --> R1[Case vs VGA]
  RULES --> R2[PSU vs GPU]
  RULES --> R3[CPU vs Mainboard]
  RULES --> R4[RAM vs Mainboard]

  R1 --> O1[PASS<br/>WARN<br/>BLOCK]
  R2 --> O2[PASS<br/>WARN<br/>BLOCK]
  R3 --> O3[PASS<br/>WARN<br/>BLOCK]
  R4 --> O4[PASS<br/>WARN<br/>BLOCK]

  O1 --> RESULT[Compatibility Result]
  O2 --> RESULT
  O3 --> RESULT
  O4 --> RESULT
