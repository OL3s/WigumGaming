# Git — Quick Guide (DEV FLOW, switch-based)

## Setup

```bash
git config --global user.name "Name"
git config --global user.email "email@example.com"
```

---

## Core Concepts (read once)

### origin/dev vs origin dev

| Syntax        | Type        | Meaning                          | Use case                      |
|---------------|------------|----------------------------------|-------------------------------|
| `origin/dev`  | Reference  | Remote branch pointer            | branching, logs, merge/rebase |
| `origin dev`  | Arguments  | remote + branch                  | pull, push                    |

---

### Merge vs Rebase

| Method  | Command                  | History        | When to use                     | Risk   |
|--------|--------------------------|---------------|--------------------------------|--------|
| Merge  | `git merge origin/dev`   | Branching     | Safe, team work                | Low    |
| Rebase | `git rebase origin/dev`  | Linear        | Personal branches, clean logs  | Medium |

## Basic Flow

### Create branch from latest dev (recommended)
```bash
git fetch origin && git switch -c feature/name origin/dev
```

## Chain Examples

### Add + commit + push + pr
```bash
git add -A && git commit -m "feat: message" && git push && gh pr create --fill --base dev
```

## Sync with dev

### Merge (safe)
```bash
git fetch origin
git merge origin/dev
```

### Rebase (clean)
```bash
git fetch origin
git rebase origin/dev
```

### After rebase
```bash
git push --force-with-lease
```

---

## Visual

### Merge
```text
A---B---C (dev)
     \     
      D---E (feature)
           \
            M (merge commit)
```

### Rebase
```text
A---B---C (dev)
             \
              D'---E' (feature rebased)
```

---

## Fix conflicts

```bash
# edit files
git add -A
git rebase --continue   # if using rebase
git commit              # if using merge
```

---

## Branching

```bash
git branch
git switch dev
git branch -d feature/name
git push origin --delete feature/name
```

---

## Logs

```bash
git log --oneline
```

---

## Undo

```bash
git restore --staged .
git restore .
```

---

## Rules

- Always branch from `origin/dev`
- Use `git switch`, not checkout
- Rebase > merge (cleaner history)
- Small commits, clear messages
- Sync with dev often
- NEVER rebase shared branches