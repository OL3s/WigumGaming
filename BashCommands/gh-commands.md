# GitHub CLI (gh) — Quick Guide (DEV FLOW)

## Setup
```bash
gh auth login
```

---

## Pull Requests (PR)

### Create PR (auto from commits → dev)
```bash
gh pr create --fill --base dev
```

### Create PR (manual → dev)
```bash
gh pr create --base dev
```

### Full control
```bash
gh pr create \
  --base dev \
  --title "Title" \
  --body "Description"
```

### View PR
```bash
gh pr view
```

### List PRs
```bash
gh pr list
```

### Checkout PR
```bash
gh pr checkout 12
```

### Merge PR
```bash
gh pr merge
```

---

## Issues

### List issues
```bash
gh issue list
```

### View issue
```bash
gh issue view 12
```

### View with comments
```bash
gh issue view 12 --comments
```

### Create issue
```bash
gh issue create \
  --title "Title" \
  --body "Description"
```

### Close issue
```bash
gh issue close 12
```

---

## Repo

### Clone repo
```bash
gh repo clone owner/repo
```

### Fork repo
```bash
gh repo fork
```

---

## Useful

### Open in browser
```bash
gh pr view --web
gh issue view 12 --web
```

### Check status
```bash
gh status
```

---

## Rules

- Always push before PR:
```bash
git push -u origin branch-name
```

- ALWAYS target dev:
```bash
gh pr create --base dev
```

- One feature per branch
- Small PRs = easier review
