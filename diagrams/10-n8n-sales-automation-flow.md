# n8n Sales Automation Flow

```mermaid
flowchart LR
  DEALER[Dealer Send Comset] --> API[Backend API]

  API --> SAVE[Save Comset]
  SAVE --> DB[(PostgreSQL)]

  API --> WEBHOOK[n8n Webhook]

  WEBHOOK --> FORMAT[Format Comset Data]
  FORMAT --> NOTIFY[Notify Sales]

  NOTIFY --> EMAIL[Send Email]
  NOTIFY --> SHEET[Log to Sales Sheet]
