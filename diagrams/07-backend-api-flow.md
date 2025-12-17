# Backend and API Flow

```mermaid
flowchart LR
  FE[Comset Web UI] --> API[Backend API]

  API --> AUTH[Auth Service]
  AUTH --> API

  API --> USER[User Service]
  API --> COMSET[Comset Service]
  API --> RULE[Rule Engine]
  API --> AI[AI Engine]

  USER --> DB[(PostgreSQL)]
  COMSET --> DB
  RULE --> DB
  AI --> DB

  API --> FE
