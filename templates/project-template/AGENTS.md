# Project AGENTS.md

## Project overview
This repository contains [describe the project in 2-4 lines].

## Product goal
The main goal of this project is:
- [goal 1]
- [goal 2]

## Users / stakeholders
Primary users:
- [user type 1]
- [user type 2]

Important stakeholders:
- [stakeholder 1]
- [stakeholder 2]

## Stack
- Frontend: [e.g. Next.js 15, React, TypeScript]
- Backend: [e.g. FastAPI, Node.js, NestJS]
- Database: [e.g. Supabase/Postgres, MongoDB]
- Infra: [e.g. Docker Compose, Traefik, Vercel]
- Mobile: [if applicable]
- Other services: [Redis, email provider, queues, etc.]

## Important directories
- `apps/web`: [what it contains]
- `apps/mobile`: [if applicable]
- `services/api`: [what it contains]
- `services/auth`: [what it contains]
- `packages/ui`: [if applicable]
- `infra/`: deployment and infrastructure files
- `docs/`: requirements, plans, QA notes, and release notes

## Commands
Install:
- `[real command]`

Development:
- `[real command]`

Lint:
- `[real command]`

Typecheck:
- `[real command]`

Unit tests:
- `[real command]`

E2E tests:
- `[real command]`

Build:
- `[real command]`

## Local engineering rules
- Keep changes scoped and reviewable.
- Do not rename shared modules without strong justification.
- Do not change unrelated files.
- If auth changes, review session, cookies, middleware, roles, and permissions.
- If database changes, document migration impact and rollback considerations.
- If frontend changes, review loading, empty, and error states.
- If infra changes, explain deployment and rollback implications.
- Do not introduce new dependencies unless justified.

## Project-specific constraints
- [constraint 1]
- [constraint 2]
- [constraint 3]

## Preferred agent flow
1. `project_manager` clarifies scope and writes or updates planning artifacts.
2. `backend_developer` implements APIs, services, auth, and integrations.
3. `frontend_developer` implements UI and frontend behavior.
4. `infra_devops` handles deployment/runtime/infrastructure changes.
5. `seo_performance_reviewer` reviews public-facing pages when relevant.
6. `qa_engineer` validates critical flows and regressions.
7. `documenter` updates final documentation.
8. `designer` and `marketer` participate only if product/design/marketing scope requires them.

## Definition of done
A task is done when:
- the scoped goal is implemented or resolved
- relevant validation has been run
- risks or known gaps are explicitly stated
- docs are updated if behavior or architecture changed
- the output includes summary, files touched, validations, and next steps

## Planning artifacts
When work is ambiguous or substantial, the project_manager should create or update:
- `docs/REQUIREMENTS.md`
- `docs/ARCHITECTURE.md`
- `docs/TEST_PLAN.md`

## Output contract for all agents
Return:
1. Summary
2. Files changed or reviewed
3. Validation performed
4. Risks / open questions
5. Recommended next step