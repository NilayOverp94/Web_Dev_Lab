# Practical 03: Feature-Branch Git Workflow

## Aim
To demonstrate an isolated feature-branch development workflow in Git by creating a dedicated branch, implementing code modifications, committing changes with conventional syntax, pushing the branch to a remote GitHub repository, merging changes into `main`, and pruning completed branches.

---

## Why Feature Branches?
Working directly on the `main` branch can destabilize production code and complicates multi-developer collaboration. A **Feature-Branch Workflow** isolates experimental changes, bug fixes, or new features in independent workspaces until code review and verification are complete.

---

## Step-by-Step Workflow Execution

### 1. Ensure `main` is Synchronized and Clean
Before creating a new branch, make sure the local `main` branch is up-to-date:
```bash
git checkout main
git pull origin main
git status
```

### 2. Create and Switch to a Feature Branch
Create a descriptive branch using standard naming conventions (`feature/<feature-name>`):
```bash
git switch -c feature/portfolio-cards
# Or using the classic syntax: git checkout -b feature/portfolio-cards
```
*Output:*
```text
Switched to a new branch 'feature/portfolio-cards'
```

### 3. Make Project Modifications
Edit the project files (for example, introducing a new portfolio cards section in `index.html` and styling rules in `css/style.css`).

### 4. Review Changes with `git diff`
Verify modified lines before staging:
```bash
git status -s
git diff
```

### 5. Stage and Commit Changes
Stage the modified files and record a granular, descriptive commit:
```bash
git add index.html css/style.css
git commit -m "feat(cards): add responsive project preview cards component"
```

### 6. Push the Feature Branch to GitHub
Publish the local branch to the remote repository so it can be reviewed:
```bash
git push -u origin feature/portfolio-cards
```

### 7. Merge Feature Branch into `main`
Once the feature is validated, switch back to `main` and merge:
```bash
# Switch back to the integration branch
git switch main

# Perform a merge (preserving history with --no-ff)
git merge --no-ff feature/portfolio-cards -m "merge: integrate feature/portfolio-cards into main"

# Push the updated main branch to remote
git push origin main
```

### 8. Clean Up Merged Branches
Delete the local and remote branch after successful integration:
```bash
# Delete local feature branch
git branch -d feature/portfolio-cards

# Delete remote feature branch on GitHub
git push origin --delete feature/portfolio-cards
```

---

## Visualizing the Feature-Branch Workflow

```text
main:            (c1) -------- (c2) ------------------------ (c4: merge commit) --->
                                 \                          /
feature/cards:                    \-- (c3: add cards) -----/
```

---

## Best Practices for Git Branching

1. **Branch Naming Standard:**
   - Features: `feature/short-description`
   - Bugfixes: `bugfix/issue-description`
   - Documentation: `docs/readme-update`
2. **Keep Branches Short-Lived:** Minimize merge conflicts by integrating branches frequently.
3. **Atomic Commits:** Each commit should represent a single logical unit of work.
4. **Always Verify Branch Context:** Run `git branch` or `git status` before staging and committing.

---

## Learning Outcomes
1. Isolated development work from the primary release branch using Git branching.
2. Tracked and compared active changes between commits and branches.
3. Executed standard merge procedures and remote branch synchronization on GitHub.
