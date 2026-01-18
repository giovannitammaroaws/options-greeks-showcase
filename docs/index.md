# Options Greeks Playground — Documentation

## Table of Contents

- Overview
- Product Scope
- User Experience
- Visual System
- Architecture
- Tech Stack
- CI/CD and Quality
- Hosting
- Assets
- Roadmap

## Overview

Options Greeks Playground is an interactive web app that helps traders and learners build intuition about options Greeks and payoff dynamics. The experience is intentionally fast, visual, and hands-on: change inputs and see the consequences immediately.

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

- Client-rendered React app
- Vite for dev speed and production builds
- No server-side rendering in the current stack

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

## Assets

Store screenshots and diagrams in `docs/assets/`.

Suggested files:
- `home.png`
- `playground.png`
- `learning.png`
- `ci-pipeline.png`
- `architecture.png`

## Roadmap

- Add more strategy presets
- Expand learning content with examples
- Performance budgets and monitoring

