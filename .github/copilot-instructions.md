# Copilot Instructions for acme-04-platform Orchestration

This is the orchestration repository for the acme-04-platform project. It coordinates work across all department repositories.

## Repository Purpose

- Cross-repository feature coordination
- Issue tracking and synchronization
- Project-wide status reporting
- Dependency management

## Related Repositories

- [test-acme-04-platform-frontend](https://github.com/mdizcalvinoaz400-01/test-acme-04-platform-frontend) - Frontend (html)
- [test-acme-04-platform-backend](https://github.com/mdizcalvinoaz400-01/test-acme-04-platform-backend) - Backend (python)
- [test-acme-04-platform-infrastructure](https://github.com/mdizcalvinoaz400-01/test-acme-04-platform-infrastructure) - Infrastructure (aws)

## Available Agents

### @orchestrator
Use for coordinating work across repositories:
- Creating multi-department features
- Managing dependencies
- Cross-repo issue creation

### @tracker
Use for monitoring progress:
- Status reports
- Blocker detection
- Velocity metrics

## Workflows

### coordinate-feature.yml
Creates issues in department repos when a parent feature issue is created.

### sync-issues.yml
Synchronizes issue status between repos.

## Labels

| Label | Purpose |
|-------|--------|
| `feature` | Parent feature issues |
| `cross-repo` | Involves multiple repos |
| `blocked` | Blocked by dependency |
| `priority-high` | High priority items |

## Creating a New Feature

1. Create an issue with the `feature` label
2. Tag the orchestrator agent: `@orchestrator`
3. Describe the feature and which departments are involved
4. The orchestrator will create linked issues in department repos
