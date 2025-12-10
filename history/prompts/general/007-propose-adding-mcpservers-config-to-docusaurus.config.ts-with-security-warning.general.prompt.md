---
id: 007
title: Propose adding mcpServers config to docusaurus.config.ts with security warning
stage: general
date: 2025-12-07
surface: agent
model: gemini-1.5-pro
feature: none
branch: 002-ai-k12-paper
user: Huzaifa
command: (implicit)
labels: ["config", "docusaurus", "security", "api-key"]
links:
  spec: null
  ticket: null
  adr: null
  pr: null
files:
  - none
tests:
  - none
---

## Prompt

add this server   "mcpServers": {
    "context7": {
      "httpUrl": "https://mcp.context7.com/mcp",
      "headers": {
        "CONTEXT7_API_KEY": "ctx7sk-9ade23e8-16b6-4d53-be9d-279ea2bfbdc1",
        "Accept": "application/json, text/event-stream"
      }
    }
  }
}continus

## Response snapshot

Proposed adding 'mcpServers' to docusaurus.config.ts, but raised security concerns about API key exposure.

## Outcome

- ✅ Impact: Proposed configuration change and raised security concern.
- 🧪 Tests: N/A
- 📁 Files: No files modified.
- 🔁 Next prompts: Awaiting user's decision on configuration placement and API key handling.
- 🧠 Reflection: Identified docusaurus.config.ts as potential location, but flagged security concern for API key.

## Evaluation notes (flywheel)

- Failure modes observed: N/A
- Graders run and results (PASS/FAIL): N/A
- Prompt variant (if applicable): N/A
- Next experiment (smallest change to try): N/A
