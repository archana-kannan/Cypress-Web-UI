# Cypress Web UI

This repository contains an end-to-end testing project built with Cypress. The Cypress dependency is declared in `package.json`, and the E2E configuration is in `cypress.config.js`.

## Prerequisites

- Node.js and npm
- Git

Check that they are installed:

```powershell
node --version
npm --version
git --version
```

## Install the project

Clone the repository if you have not already, then open a terminal in the project directory and install its dependencies:

```powershell
git clone https://github.com/archana-kannan/Cypress-Web-UI.git
cd Cypress-Web-UI

npm install cypress -- will install the cypress in our local
```

`npm install` reads `package.json` and `package-lock.json` and installs Cypress and the project's other dependencies.

## Open Cypress

Launch Cypress in interactive mode:

```powershell
npx cypress open
```

Choose **E2E Testing**, select a browser, and run a spec. The example specs are in `cypress/e2e/`; shared support code is in `cypress/support/`, and test fixtures are in `cypress/fixtures/`.

To run the E2E specs from the command line:

```powershell
npx cypress run
```

## Configure Git identity

Set the name and email that Git records on your commits. These commands configure them globally for your Windows user:

```powershell
git config --global user.name "username"
git config --global user.email "email"
```

Verify the values:

```powershell
git config --global --get user.name
git config --global --get user.email
```

Git configuration uses `git config`, not `set git.username` or `set git.email`. The name and email identify the author of commits; they do not sign you in to GitHub or authorize a push.

## Push changes

After making and committing your changes, push the current branch:

```powershell
git add .
git commit -m "Describe your changes"
git push
```

If `git push` is rejected or asks you to authenticate, check the remote with `git remote -v` and sign in using your configured Git credential manager, a personal access token, or SSH key. GitHub does not accept your Git commit email as push authentication.
