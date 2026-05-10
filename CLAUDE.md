# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

**Twines and Straps SA** — E-commerce platform for South Africa's industrial twines, ropes, and packaging supplies manufacturer. Features product catalog and WhatsApp quote integration.

## Tech Stack

- **Frontend**: Next.js 14, React, TypeScript 5.9, Tailwind CSS 3.4
- **Database**: Prisma 6.19 (ORM)
- **Backend**: Azure Functions
- **Testing**: Jest
- **CI/CD**: GitHub Actions (CI + Azure deploy + health check)
- **Deployment**: Azure

## Key Commands

```bash
npm install               # Install dependencies
npm run dev               # Start dev server
npm run build             # Production build
npm run lint              # ESLint
npm test                  # Jest tests
npx prisma generate       # Generate Prisma client
npx prisma migrate dev    # Run DB migrations
```

## Architecture

- `app/` — Next.js App Router pages
- `components/` — React components
- `lib/` — Shared utilities
- `hooks/` — Custom React hooks
- `prisma/` — Database schema and migrations
- `azure-functions/` — Serverless backend functions
- `infra/` — Infrastructure configuration
- `styles/` — Global styles

## Ecosystem

cognitive-mesh integration tracked in Issue #303.

## AgentKit Forge

This project has not yet been onboarded to [AgentKit Forge](https://github.com/phoenixvc/agentkit-forge). To request onboarding, [create a ticket](https://github.com/phoenixvc/agentkit-forge/issues/new?title=Onboard+twinesandstraps&labels=onboarding).

## Baton Integration

Baton is the shared task graph for cross-repo work. When the `baton` MCP server is available, agents should check for existing work with `task_check` at the start of meaningful tasks, create or claim visible work with `task_notify`/`log_agent_message`, update the task when significant new information becomes available, and log completion or blockers before handing off.
