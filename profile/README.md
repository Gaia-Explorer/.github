# GAIA Explorer

## Branching & Contribution Strategy

### Overview

All development happens on **feature branches**. The `main` branch is always stable and production-ready. Direct commits to `main` are **not allowed** — all changes must go through a pull request, which will be reviewed and approved by another team member.

---

### Branch Structure

- `main` — stable, always deployable
- `feature/<short-description>` — one branch per task or feature

---

### Workflow

### 1. Create a feature branch

Always branch off from `main`:

```bash
git checkout main
git pull origin main
git checkout -b feature/<your-task-name>
```

### 2. Develop on your feature branch

Do all your work here. Commit changes with short and descriptive commit messages.

### 3. Before opening a PR — sync with main

Before creating a pull request, merge the latest `main` into your feature branch and verify everything still works:

```bash
git checkout main
git pull origin main
git checkout feature/<your-task-name>
git merge main
```

Resolve any conflicts, test your changes, and only then proceed.

### 4. Open a Pull Request

Push your branch and open a PR against `main` on GitHub. Prefferably, write a clear description of what was done and why.

### 5. Do not merge your own PR

A pull request must be **reviewed and approved by at least one other team member** before merging. Never approve or merge your own PR.

### 6. CI must pass

A pull request will **not be approved if the build or tests fail**. Fix any issues before requesting a review.

### 7. Merge

Once approved and CI passes, the reviewer (or the author — but not both) merges the PR into `main`.

![Branching strategy](./branching-strategy.svg)
