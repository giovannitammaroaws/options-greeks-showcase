<h1><img src="pages/icons/favicon.svg" alt="Options Greeks Playground favicon" width="40" height="40" align="absmiddle" style="margin-right: 12px;" />Options Greeks Playground</h1>
Showcase for options Greeks (Delta, Gamma, Vega, Theta) with concise docs and examples.

Live site: https://greeksplayground.com/

## Quick View

- Purpose: interactive playground to build intuition on payoff and Greeks
- Stack: React + Vite, ESLint, Vitest, Playwright, GitHub Actions, Cloudflare Pages

### Greeks Playground

Study strategies safely and explore payoffs in a sandbox. Use Search to find a strategy fast, or click Select (top right) and open the dropdown to browse all available strategies. More strategies will be added over time.

<p align="left">
  <a href="pages/screenshot/home2.png">
    <img src="pages/screenshot/home2.png" alt="Greeks Playground home" width="720" />
  </a>
</p>

### Greeks Learning

Interactive visuals for Delta, Gamma, Vega, and Theta so you can see how each Greek behaves and changes with inputs.

<p align="left">
  <a href="pages/screenshot/greeks_learning2.png">
    <img src="pages/screenshot/greeks_learning2.png" alt="Greeks learning view" width="720" />
  </a>
</p>

## Tech Stack

<table>
  <thead>
    <tr>
      <th align="left">Layer</th>
      <th align="left">Technology</th>
      <th align="left">Purpose</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>UI</td>
      <td><img src="pages/icons/react-logo.svg" alt="React" width="20" height="20" align="absmiddle" /> React</td>
      <td>Interactive single page interface</td>
    </tr>
    <tr>
      <td>Build</td>
      <td><img src="pages/icons/vite-logo.svg" alt="Vite" width="20" height="20" align="absmiddle" /> Vite</td>
      <td>Fast dev server and production builds</td>
    </tr>
    <tr>
      <td>Lint</td>
      <td><img src="pages/icons/eslint.svg" alt="ESLint" width="20" height="20" align="absmiddle" /> ESLint</td>
      <td>Code quality checks</td>
    </tr>
    <tr>
      <td>Unit Tests</td>
      <td><img src="pages/icons/vitest.svg" alt="Vitest" width="20" height="20" align="absmiddle" /> Vitest</td>
      <td>Fast unit testing</td>
    </tr>
    <tr>
      <td>E2E Tests</td>
      <td><img src="pages/icons/playwright.svg" alt="Playwright" width="20" height="20" align="absmiddle" /> Playwright</td>
      <td>Browser smoke coverage</td>
    </tr>
    <tr>
      <td>CI/CD</td>
      <td><img src="pages/icons/github-actions.svg" alt="GitHub Actions" width="20" height="20" align="absmiddle" /> GitHub Actions</td>
      <td>Automated pipeline</td>
    </tr>
    <tr>
      <td>Hosting</td>
      <td><img src="pages/icons/cloudflare-pages.svg" alt="Cloudflare Pages" width="20" height="20" align="absmiddle" /> Cloudflare Pages</td>
      <td>Static site hosting</td>
    </tr>
  </tbody>
</table>

## Highlights

- Instant feedback loop for payoff curves and Greeks
- Focused learning flow without distractions
- CI/CD with lint, tests, coverage, build, and smoke checks

## CI/CD and Quality

GitHub Actions runs linting, unit tests, coverage, build, and smoke tests before deploy.

Workflow runs (recent commits):
<p align="left">
  <a href="pages/screenshot/github_actions.png">
    <img src="pages/screenshot/github_actions.png" alt="GitHub Actions workflow runs" width="720" />
  </a>
</p>
Build and deploy pipeline steps:
<p align="left">
  <a href="pages/screenshot/build.png">
    <img src="pages/screenshot/build.png" alt="Build workflow summary" width="720" />
  </a>
</p>

Unit tests running now:
<p align="left">
  <a href="pages/screenshot/tests.png">
    <img src="pages/screenshot/tests.png" alt="Tests status" width="720" />
  </a>
</p>
Test coverage summary:
<p align="left">
  <a href="pages/screenshot/tests_coverage.png">
    <img src="pages/screenshot/tests_coverage.png" alt="Tests coverage status" width="720" />
  </a>
</p>

## Architecture

Architecture diagram below: everything is rendered via React in the browser. Below are the key pieces and how the quality gates work in practice.

- Client rendered React app
- Vite for dev speed and production builds
- GitHub Actions for CI/CD pipeline
- No server side rendering in the current stack

<p align="left">
  <a href="pages/screenshot/architecture.png">
    <img src="pages/screenshot/architecture.png" alt="Architecture flow" width="720" />
  </a>
</p>

Quality gates details (sequence):
1) Pre-commit checks (Husky): local Git hooks run before commit to block obvious issues. Husky can trigger linting and/or tests so broken code does not even reach the repo.
2) Push / PR to GitHub: every change goes through CI.
3) Lint (ESLint): runs in CI on each push/PR to enforce code style and catch common bugs early. The pipeline fails if lint errors exist.
4) Unit tests: fast test suite to validate core logic.
5) Coverage: ensures test coverage stays at an acceptable level.
6) Build: production build must succeed to proceed.
7) Smoke tests (Playwright): after build, a quick Playwright script launches a browser, loads the app, and checks a basic signal like page load and title to confirm the build is deployable.

## Roadmap

- Add more strategy presets
- Expand learning content with examples
- Performance budgets and monitoring

---

Built by Giovanni Tammaro | [LinkedIn](https://www.linkedin.com/in/pubtammarogiovanni/)
