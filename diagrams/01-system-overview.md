# System Overview – Ascenti Comset

```mermaid
flowchart LR
  U[User or Dealer] --> FE[Comset Web UI<br/>GitHub Pages]

  FE -->|View Products| GS[Google Sheets<br/>Product Master]
  GS -->|Sync Data| N8N[n8n Automation]

  N8N --> DB[(PostgreSQL)]
  DB --> FE

  FE --> RULE[Compatibility Rule Engine]
  FE --> AI[AI Recommendation Layer]

  FE -->|Send Comset| SALES[Sales Team]
