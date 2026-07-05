# Angular Hello World + GitHub Learning Repo

This project is intentionally small so you can practice GitHub and GitHub Copilot.

## Included

- Minimal Angular Hello World app
- CI workflow for build and tests
- GitHub Pages deployment workflow

## Run locally

1. Install dependencies.
2. Start the app.

Commands:

npm install
npm start

Open http://localhost:4200.

## Push to GitHub

1. Create an empty repository in GitHub.
2. Run these commands in this folder.

Git commands:

git init
git add .
git commit -m "Initial Angular hello world"
git branch -M main
git remote add origin https://github.com/<your-user>/<your-repo>.git
git push -u origin main

## Branch policy setup

In GitHub, open Settings > Branches and add a rule for main.

Recommended options:

- Require pull request before merging
- Require at least 1 approval
- Require status checks to pass
- Require branches to be up to date
- Block force pushes
- Block branch deletion

Required check to select after first workflow run:

- CI / build-and-test

## Workflows

- .github/workflows/ci.yml
  - Runs on pull requests and pushes to main
  - Installs dependencies, runs tests, and builds the app

- .github/workflows/deploy-pages.yml
  - Runs on pushes to main
  - Builds Angular with correct base path
  - Deploys to GitHub Pages

## GitHub Pages setup

In GitHub, open Settings > Pages and set source to GitHub Actions.

Site URL pattern:

https://<your-user>.github.io/<your-repo>/

## Copilot practice ideas

1. Add a second component and route.
2. Add a service and inject it.
3. Improve app tests.
4. Add a lint workflow.
5. Add a pull request preview workflow.
