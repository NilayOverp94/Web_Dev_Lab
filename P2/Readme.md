# Practical 02: Portfolio Repository with an Initial Commit

## Aim
To initialize a local Git version control repository for a developer portfolio project, track changes through the staging area, record an initial commit with a descriptive message, connect the local repository to GitHub, and push the commit to the `main` branch.

---

## Prerequisites
- Git CLI installed and verified (`git --version`)
- A remote repository created on GitHub (e.g., `https://github.com/NilayOverp94/Web_Dev_Lab.git`)

---

## Step-by-Step Git Workflow

### 1. Configure Global Git Identity
Ensure user identity is registered for authorship tracking:
```bash
git config --global user.name "Nilay Raj"
git config --global user.email "nilayraj713@gmail.com"
```

### 2. Initialize Local Repository
Navigate to the project root and initialize Git with the primary branch designated as `main`:
```bash
cd dev-portfolio
git init -b main
```
*Output:*
```text
Initialized empty Git repository in /Users/nilayraj/Web_Dev_Lab/dev-portfolio/.git/
```

### 3. Configure `.gitignore`
Prevent system and editor temporary files from entering tracking:
```bash
cat << 'EOF' > .gitignore
# System artifacts
.DS_Store
Thumbs.db

# IDE and editor settings
.vscode/
.idea/
*.swp
*.swo

# Dependency and log directories
node_modules/
*.log
EOF
```

### 4. Inspect Untracked Files
Verify which files are recognized by Git:
```bash
git status
```
*Output confirms untracked files: `.gitignore`, `index.html`, `css/`, `js/`, `docs/`.*

### 5. Stage Files to the Index
Stage all newly created files into the Git index:
```bash
git add .
```

Re-check status to verify files are staged:
```bash
git status -s
```

### 6. Create the Initial Commit
Record the staged snapshot into the repository history:
```bash
git commit -m "feat: initialize developer portfolio structure and base assets"
```

### 7. Associate Remote Origin and Push
Link the local repository with the remote GitHub repository:
```bash
# Add origin remote link
git remote add origin https://github.com/NilayOverp94/Web_Dev_Lab.git

# Verify remote configuration
git remote -v

# Push commits to remote origin and configure upstream tracking
git push -u origin main
```

### 8. Verify Commit History
Confirm that the commit is saved in the local tree:
```bash
git log --oneline --stat
```

---

## Git Architecture Concepts

```text
+-----------------------+     git add      +----------------------+   git commit   +------------------------+
|   Working Directory   | ---------------> |     Staging Area     | -------------> |    Local Repository    |
| (Files in filesystem) |                  |       (Index)        |                |     (.git database)    |
+-----------------------+                  +----------------------+                +------------------------+
                                                                                               |
                                                                                         git push -u origin main
                                                                                               |
                                                                                               v
                                                                                   +------------------------+
                                                                                   |   Remote Repository    |
                                                                                   |       (GitHub)         |
                                                                                   +------------------------+
```

| Git Concept | Role in Version Control |
|---|---|
| **Working Tree** | The local files and folders visible on disk where edits are performed. |
| **Staging Area (`Index`)** | The preparation layer where specific modifications are curated before committing. |
| **Commit Object** | An immutable cryptographic snapshot of the staged files with author metadata and a timestamp. |
| **Remote (`origin`)** | A remote copy of the repository hosted on a cloud platform like GitHub for backup and collaboration. |
| **Upstream (`-u`)** | Sets the default remote branch tracking so future syncs require only `git pull` or `git push`. |

---

## Learning Outcomes
1. Initialized a Git repository and properly managed ignored files via `.gitignore`.
2. Mastered the distinction between untracked, staged, and committed states.
3. Connected local source code to GitHub and published the initial release commit on the `main` branch.
