# Options Greeks Showcase
Showcase for options Greeks (Delta, Gamma, Vega, Theta, Rho) with concise docs and examples.

Live site: https://greeksplayground.com/

## Quick View

- Purpose: learn options Greeks through interactive, real time visuals
- Sections: Greeks Playground, Greeks Learning, Value Proposition
- Stack: React + Vite, ESLint, Vitest, Playwright, GitHub Actions, Cloudflare Pages

## Highlights

- Instant feedback loop for payoff curves and Greeks
- Focused learning flow without distractions
- CI/CD with lint, tests, coverage, build, and smoke checks

## Screenshots

Place screenshots in `docs/assets/` and update the references below.

- `docs/assets/home.png`
- `docs/assets/playground.png`
- `docs/assets/learning.png`

## GitHub Actions

The CI pipeline runs linting, unit tests, coverage, build, and smoke tests before deploy.

## Overview

Options Greeks Playground is an interactive web app that helps traders and learners build intuition about options Greeks and payoff dynamics. The experience is intentionally fast, visual, and hands on: change inputs and see the consequences immediately.

## Product Scope

- Greeks Playground: interactive controls with real-time payoff and Greeks
- Greeks Learning: focused explanations and learning flow
- Value Proposition: project goals and context

## User Experience

- Fast iteration: every control change updates charts and Greeks instantly
- Minimal friction: clear layout, direct controls, no forced signup
- Guided clarity: learning section complements the playground

## Visual System

- Layout: clean, centered content with strong hierarchy
- Typography: bold headings + readable body text
- Color: high contrast for data visibility and quick scanning
- Components: dashboards, charts, strategy selectors, input controls

## Architecture

- Client rendered React app
- Vite for dev speed and production builds
- No server side rendering in the current stack

## Tech Stack

- React + Vite
- ESLint for linting
- Vitest for unit tests
- Playwright for smoke tests
- GitHub Actions for CI/CD
- Cloudflare Pages for hosting

## CI/CD and Quality

CI pipeline tasks:
- Linting
- Unit tests
- Coverage tests
- Build
- Smoke tests (basic load + title check)

## Hosting

- Static site deployed to Cloudflare Pages
- Preview deployments for each PR

## Roadmap

- Add more strategy presets
- Expand learning content with examples
- Performance budgets and monitoring
