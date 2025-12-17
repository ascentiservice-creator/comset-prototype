```mermaid
flowchart LR

  %% User & Frontend
  U[User Browser]
  FE[Frontend Web App<br/>Comset UI]

  %% Data Sources
  GS[Google Sheets<br/>Product / Price]
  IMG[Image Storage]

  %% Automation
  N8N[n8n Workflow<br/>Sync / Transform]

  %% Backend Core
  API[Backend API]
  RULE[Rule Engine<br/>Compatibility Check]
  AI[AI Recommender<br/>Budget / Usage]

  %% Database
  DB[(Central Database)]

  %% Flow
  U --> FE

  FE --> API
  FE --> IMG

  API --> RULE
  API --> AI
  RULE --> API
  AI --> API

  API --> DB
  DB --> API

  GS --> N8N
  N8N --> DB
  N8N --> IMG
