# README

## Project Structure
```
full-stack-fastapi-template/
├── backend/                    # FastAPI backend application
│   ├── app/
│   │   ├── main.py            # FastAPI app entry point
│   │   ├── models.py          # SQLModel data models
│   │   ├── api/               # API routes
│   │   ├── core/              # Core utilities (config, security, db)
│   │   └── crud.py            # CRUD operations
│   ├── alembic/               # Database migrations
│   ├── tests/                 # Pytest test suite
│   └── pyproject.toml         # Python dependencies (uv)
├── frontend/                   # React frontend application
│   ├── src/
│   │   ├── main.tsx           # React app entry point
│   │   ├── routes/            # TanStack Router routes
│   │   ├── components/        # React components
│   │   ├── client/            # Generated API client
│   │   └── hooks/             # Custom React hooks
│   ├── tests/                 # Playwright E2E tests
│   └── package.json           # Node dependencies (Bun)
├── scripts/                    # Utility scripts
│   └── generate-client.sh     # API client generation
├── .github/workflows/         # GitHub Actions CI/CD
├── compose.yml                # Production Docker Compose
├── compose.override.yml       # Development overrides
├── compose.traefik.yml        # Traefik configuration
├── .env                       # Environment variables
└── pyproject.toml             # Workspace configuration (uv)
├── .github/                    # Utility scripts
│   ├── dependabot.yml         # Auto-raise PRs to update GitHub Actions, uv, bun, Docker, and Docker Compose dependencies on a schedule dependabot.
│   └── workflows/
│       ├── deploy-staging.yml      # Deploy to staging on every push to master using a self-hosted runner labeled staging
│       ├── deploy-production.yml   # Deploy to production when a release is published using a self-hosted runner labeled production 
│       ├── test-backend.yml        # Run backend tests, migrations, and coverage; upload coverage artifact; enforce 90% coverage
│       ├── playwright.yml          # Run end-to-end Playwright tests on changes to backend/frontend/compose files; sharded; merge reports
│       ├── smokeshow.yml           # After Test Backend completes, download coverage HTML and publish via Smokeshow with a status check
│       ├── latest-changes.yml      # On PR close (merged), generate release notes into release-notes.md using tiangolo/latest-changes
│       ├── pre-commit.yml          # Run pre-commit on PRs; auto-commit formatting fixes if secrets available; otherwise use pre-commit-ci lite
│       └── labeler.yml             # Auto-label PRs based on files; then enforce that PR has at least one allowed label
```
