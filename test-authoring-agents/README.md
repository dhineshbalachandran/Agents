# Test Authoring Agents

A family of agents that consume the output of the
[App Code Scan Agent](../app-code-scan-agent.md) — the business
requirement document, flow diagrams, API inventory, and integration/data
dependency map — and turn it into tests.

Each agent covers one layer of testing, so they can be used independently
or chained together.

| Agent | Purpose | Status |
|---|---|---|
| [API Automation Agent](./api-automation-agent.md) | Reconstructs API contracts from code (no Swagger needed) and generates a runnable BDD or TDD automation framework with environment switching, reporting, and Azure DevOps publishing | Available |
| UI Automation Agent | Generates UI automation from business flows | Coming soon |
| Database Testing Agent | Generates data validation and database test cases from the data dependency map | Coming soon |
| Manual Test Case Agent | Generates manual test cases from the business requirement document and flows | Coming soon |

## Shared conventions

- **Input:** the structured output of the App Code Scan Agent
- **Confidence tags:** every extracted detail is marked Confirmed,
  Inferred, or Needs validation
- **No client detail:** no client names, real URLs, or credentials in any
  output
- **One file per agent:** each agent is a single instruction file with a
  changelog at the bottom
