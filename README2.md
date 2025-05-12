# Repository Architecture & Team Alignment Policy

## Overview

This repository follows a **modular monorepo architecture** using [Nx](https://nx.dev/) and [Angular](https://angular.io/) to support a scalable, maintainable, and collaborative development environment across multiple domain teams.

This policy outlines the **expectations, responsibilities, and boundaries** for contributing teams, including guidance for Micro Frontend (MFE) development, library usage, CI/CD practices, and shared tooling.

---

## Why a Monorepo?

A monorepo enables:

- **Consistent tooling** across projects (builds, tests, linting)
- **Shared libraries** for design, authentication, and business logic
- **Decoupled MFEs** deployed independently via modern hosting strategies
- **Improved collaboration** and discoverability across domain teams
- **Centralized versioning and CI/CD pipelines**

---

## What Is Not Allowed

To ensure architectural alignment and system integrity, the following practices are **prohibited**:

- Creating **separate repositories** for MFEs that belong to this system
- Forking or duplicating shared libraries, configuration, or build tooling
- Creating parallel **Azure DevOps organizations** without prior architectural review
- Maintaining isolated CI/CD pipelines disconnected from core product delivery

---

## Team Responsibilities

| Team Role | Responsibility |
|-----------|----------------|
| **MFE Owners** | Integrate their remote apps into the monorepo; align with Nx structure; consume shared libraries |
| **DevOps** | Maintain shared pipelines, environments, release cadence |
| **Architects** | Review changes to deployment models, cross-cutting concerns, or infrastructure strategy |
| **All Teams** | Contribute to shared tooling, follow architectural patterns, escalate blockers early |

---

## Autonomy ≠ Isolation

This monorepo is intentionally designed to **enable autonomy** without sacrificing alignment:

- Each MFE remote is deployable on its own schedule
- Teams manage their own feature branches and release scope
- Domain boundaries are respected through shared interfaces and services

Autonomy thrives when it's built on shared foundations—not fractured ones.

---

## Enforcement

Architectural violations—such as creating rogue repos or duplicating core logic—will trigger:

1. **Review and rollback of non-compliant structures**
2. **Escalation to engineering and product leadership**
3. **Refactoring effort to reintegrate isolated code**

---

## Need Help?

We support you.

- Open a discussion in `#dev-architecture` Slack channel
- Request pairing or training on Nx, Angular, or monorepo conventions
- File an `@architects` tagged GitHub issue for architectural guidance

---

## Final Word

We don’t run a fiefdom of isolated castles. We build **systems**.

That means one product, one platform, and one shared mission to deliver high-quality solutions across all domains—**together**.

Let’s keep it that way.