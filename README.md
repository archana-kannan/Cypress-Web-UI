# 🌲 Cypress Web UI Automation

[![Cypress Tests](https://github.com/archana-kannan/Cypress-Web-UI/actions/workflows/cypress.yml/badge.svg)](https://github.com/archana-kannan/Cypress-Web-UI/actions/workflows/cypress.yml)
![Cypress](https://img.shields.io/badge/Cypress%2016-17202C?logo=cypress&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Tests](https://img.shields.io/badge/tests-122%20passing-brightgreen)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?logo=githubactions&logoColor=white)

End-to-end web UI test automation with **Cypress 16**. The suite has **122 tests across 20 specs** covering the main Cypress capabilities: UI actions, querying, assertions, network stubbing, cookies and storage, spies/stubs/clocks, viewports and more. It runs headless in Chrome on GitHub Actions.

## ✨ Coverage

| Area | Specs |
|------|-------|
| **User journeys** | `todo.cy.js`: add, complete, filter and clear todos |
| **Interacting with the UI** | `actions`, `querying`, `traversal`, `connectors`, `aliasing` |
| **Assertions** | `assertions`: implicit (`should`) and explicit (`expect`) |
| **Network** | `network_requests`: `cy.intercept` stubbing and waiting on requests |
| **Browser state** | `cookies`, `storage`, `location`, `navigation`, `window`, `viewport` |
| **Test doubles** | `spies_stubs_clocks`: `cy.spy`, `cy.stub`, `cy.clock` |
| **Data and utilities** | `files` (fixtures), `utilities`, `cypress_api`, `misc`, `waiting` |

## 📁 Project Structure

```
Cypress-Web-UI/
├── .github/workflows/cypress.yml     # CI: headless Chrome, screenshots on failure
├── cypress/
│   ├── e2e/
│   │   ├── 1-getting-started/        # todo app user journey
│   │   └── 2-advanced-examples/      # 19 capability-focused specs
│   ├── fixtures/                     # test data (JSON)
│   └── support/
│       ├── commands.js               # custom commands
│       └── e2e.js                    # global hooks
└── cypress.config.js
```

## 🚀 Getting Started

**Prerequisites:** Node.js 18+ and npm

```bash
git clone https://github.com/archana-kannan/Cypress-Web-UI.git
cd Cypress-Web-UI
npm ci
```

## ▶️ Running Tests

| Command | What it does |
|---------|--------------|
| `npm run cy:open` | Open the Cypress app, choose **E2E Testing**, pick a browser and spec |
| `npm test` | Run all specs headless (Electron) |
| `npm run test:chrome` | Run all specs headless in Chrome |

Run one spec: `npx cypress run --spec cypress/e2e/1-getting-started/todo.cy.js`

> **Running from the VS Code terminal?** If Cypress fails with `bad option: --smoke-test`, VS Code has set `ELECTRON_RUN_AS_NODE`. Clear it first: `Remove-Item Env:ELECTRON_RUN_AS_NODE` (PowerShell) or `unset ELECTRON_RUN_AS_NODE` (bash).

## 🔄 Continuous Integration

[`.github/workflows/cypress.yml`](.github/workflows/cypress.yml) uses the official [`cypress-io/github-action`](https://github.com/cypress-io/github-action) to install, cache and run the suite in headless Chrome. It runs on push and pull request to `main`, weekly, and on demand. If a test fails, its screenshots are uploaded as an artifact.

## 🗺️ Roadmap

- [ ] Page Object / app-action pattern for a real application under test
- [ ] Custom commands for login and API seeding
- [ ] Cross-browser matrix (Chrome, Firefox, Edge)
- [ ] Mochawesome HTML reporting

## 👩‍💻 Author

**Archana Kannan**, AI-Powered Software Quality Engineer
[GitHub](https://github.com/archana-kannan) · [LinkedIn](https://www.linkedin.com/in/archana-kannan-2021)
