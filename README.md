# Workflows

Reusable GitHub Actions and automation templates.

This repository stores GitHub workflows, Dependabot configurations, and related automation that can be reused across multiple projects (Laravel apps, Laravel packages, Next.js apps, etc).

---

## Structure

```text
.github/
  workflows/          # reusable workflows (workflow_call)
  dependabot.yml      # dependency updates for this repo

templates/            # optional extra templates (non-active)
```

---

## Usage

```yaml
jobs:
  ci:
    uses: MimisK13/workflows/.github/workflows/laravel-app.yml@main
```

---

## Notes

- Workflows use `workflow_call`, so they **do not run in this repository**
- Dependabot is enabled to keep GitHub Actions versions up to date
- Auto-merge is enabled for dependency updates

---

## Purpose

- Avoid copy-paste across repositories
- Keep CI/CD logic centralized
- Maintain updated GitHub Actions automatically