# n8n Product Data Sync Flow

```mermaid
flowchart LR
  TRIGGER[Schedule Trigger] --> GS[Google Sheets]

  GS --> FETCH[Fetch Product Data]
  FETCH --> CLEAN[Normalize and Validate]

  CLEAN --> CHECK[Brand and Spec Check]
  CHECK --> UPSERT[Upsert Product Data]

  UPSERT --> DB[(PostgreSQL)]
