# acme-04-platform - Orchestration

Central coordination repository for the acme-04-platform project.

## 📊 Project Tracking

| Resource | Value |
|----------|-------|
| **GitHub Project** | [acme-04-platform-project](https://github.com/users/mdizcalvinoaz400-01/projects/7) |
| **Current Sprint** | Sprint 1 |
| **Project ID** | `PVT_kwHOBTtpKc4BJm1e` |

## 🏢 Department Repositories

| Department | Repository | Tech Stack |
|------------|------------|------------|
| frontend | [test-acme-04-platform-frontend](https://github.com/mdizcalvinoaz400-01/test-acme-04-platform-frontend) | html |
| backend | [test-acme-04-platform-backend](https://github.com/mdizcalvinoaz400-01/test-acme-04-platform-backend) | python |
| infrastructure | [test-acme-04-platform-infrastructure](https://github.com/mdizcalvinoaz400-01/test-acme-04-platform-infrastructure) | aws |

## 🤖 Copilot Agents

### @orchestrator

Manages user stories and coordinates work across departments.

**Commands:**
- `@orchestrator user-story "As a customer, I want to..."` - Create user story with department issues
- `@orchestrator user-story "description" --milestone "Sprint 2"` - Use different milestone
- `@orchestrator status` - Show overall project status
- `@orchestrator status --milestone "Sprint 1"` - Show sprint status
- `@orchestrator sync` - Sync issue statuses with project board

### @tracker

Tracks progress and reports on project health.

**Commands:**
- `@tracker user-story #1` - Track specific user story
- `@tracker sprint "Sprint 1"` - Show sprint progress
- `@tracker project` - Show project overview
- `@tracker blockers` - List all blockers

## 📋 How Issues Flow

```
┌─────────────────────────────────────────────────────────────┐
│                    User Story Created                        │
│              (@orchestrator user-story "...")                │
└─────────────────────┬───────────────────────────────────────┘
                      │
                      ▼
┌─────────────────────────────────────────────────────────────┐
│              Department Issues Created                       │
│     (Infrastructure → Backend → Frontend dependencies)       │
└─────────────────────┬───────────────────────────────────────┘
                      │
                      ▼
┌─────────────────────────────────────────────────────────────┐
│            Issues Added to GitHub Project                    │
│       (Backlog → Ready → In Progress → Review → Done)        │
└─────────────────────┬───────────────────────────────────────┘
                      │
                      ▼
┌─────────────────────────────────────────────────────────────┐
│            Assigned to Current Milestone                     │
│                    (Sprint 1, etc.)                          │
└─────────────────────────────────────────────────────────────┘
```

### Workflow Steps

1. **Create User Story** with `@orchestrator user-story "..."`
2. **Orchestrator creates** linked department issues automatically
3. **Issues are added** to the GitHub Project board
4. **Departments work autonomously** using their own specialized agents
5. **Track progress** with `@tracker` or view the project board
6. **Sync statuses** with `@orchestrator sync`

## ⚙️ Configuration

### Project Configuration (`.github/project-config.json`)

Each repository contains a project configuration file that links it to the GitHub Project:

```json
{
  "projectId": "PVT_kwHOBTtpKc4BJm1e",
  "projectNumber": 7,
  "projectUrl": "https://github.com/users/mdizcalvinoaz400-01/projects/7",
  "owner": "mdizcalvinoaz400-01",
  "projectName": "acme-04-platform-project",
  "currentMilestone": {
    "number": 1,
    "title": "Sprint 1"
  }
}
```

This file is used by the Copilot agents to:
- Add new issues to the correct project
- Assign issues to the current milestone
- Update issue status on the project board

### Issue Linking

All issues include:
- **Project:** acme-04-platform-project
- **Milestone:** Current sprint
- **Parent:** Link to user story (for department issues)
- **Labels:** user-story:[name] for filtering

## 🚀 Getting Started

1. Clone this repository
2. Open in VS Code with GitHub Copilot enabled
3. Start creating user stories: `@orchestrator user-story "As a user, I want..."`
4. Monitor progress on the [project board](https://github.com/users/mdizcalvinoaz400-01/projects/7)
