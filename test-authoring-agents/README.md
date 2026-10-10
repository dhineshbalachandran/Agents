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
| [UI Automation Agent](./ui-automation-agent.md) | Generates UI automation from business flows and user stories; updates existing tests first and creates new ones only when none exist; BDD or TDD with an object repository, Playwright or Selenium, environment switching, and check-in-based test selection | Available |
| [Database Testing Agent](./database-testing-agent.md) | Generates database tests across Oracle, PostgreSQL, Azure SQL, Snowflake, Cosmos DB, and MarkLogic; handles multiple authentication methods, validates schema, data types, and sizes, and verifies that UI/API inputs land correctly in the database | Available |
| Manual Test Case Agent | Generates manual test cases from the business requirement document and flows | Coming soon |

## Shared conventions

- **Input:** the structured output of the App Code Scan Agent
- **Confidence tags:** every extracted detail is marked Confirmed,
  Inferred, or Needs validation
- **No client detail:** no client names, real URLs, or credentials in any
  output
- **One file per agent:** each agent is a single instruction file with a
  changelog at the bottom
