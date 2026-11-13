# Practical 04: GitHub README and Version Tags

## Aim
To design and author professional repository documentation using GitHub Flavored Markdown (GFM), and execute software release management through annotated Git version tags following Semantic Versioning (SemVer).

---

## Part 1: Writing a Production-Grade GitHub README

A repository's root `README.md` is the primary entry point for instructors, collaborators, and recruiters. An effective README includes:

1. **Header & Badges:** Title, status badges (build, version, license).
2. **Overview:** Concise summary of the project purpose and scope.
3. **Module Index / Roadmap:** Tabular list of practicals or features with status.
4. **Technology Stack:** Languages, frameworks, tools utilized.
5. **Setup & Execution Instructions:** Step-by-step guidance for running the project locally.
6. **Author & Attribution:** Maintainer identity and contact links.

---

## Part 2: Semantic Version Tagging Workflow

### 1. Understanding Git Tags: Lightweight vs. Annotated
- **Lightweight Tags:** Simple bookmarks pointing directly to a specific commit hash (no author or message).
- **Annotated Tags (`-a`):** Complete objects stored in the Git database containing author, date, GPG signature (optional), and an explicit release description. **Best practice for version releases.**

### 2. Semantic Versioning Specification (SemVer)
Versions adhere to the `vMAJOR.MINOR.PATCH` format:
- `MAJOR` (`v1.0.0`): Breaking changes or foundational curriculum milestones.
- `MINOR` (`v1.1.0`): Backward-compatible feature additions (e.g., adding a new module).
- `PATCH` (`v1.0.1`): Backward-compatible bug fixes or styling corrections.

---

## Step-by-Step Tagging Commands

### 1. Verify Clean Working State and Commit Log
```bash
git status
git log --oneline -n 5
```

### 2. Create an Annotated Release Tag
Create the initial milestone release tag `v1.0.0`:
```bash
git tag -a v1.0.0 -m "Release v1.0.0: Completion of Module 1 Git & Terminal navigation practicals"
```

### 3. List and Inspect Tags
List all created tags with their annotations:
```bash
git tag -l -n
```

Inspect the full cryptographic signature and commit snapshot of the tag:
```bash
git show v1.0.0
```

### 4. Push Tags to GitHub
By default, `git push` does not transfer tags to remote servers. Push explicitly:
```bash
# Push a specific tag
git push origin v1.0.0

# Or push all local tags simultaneously
git push origin --tags
```

### 5. Managing Tags (Correction & Deletion)
In case a tag needs revision:
```bash
# Delete local tag
git tag -d v1.0.0

# Delete remote tag on GitHub
git push origin --delete v1.0.0
```

---

## Verification & Outcomes
1. Authored an organized, readable, and comprehensive root `README.md` for the entire repository.
2. Tagged a milestone commit with an annotated version tag (`v1.0.0`).
3. Published the version tag to GitHub, creating an official release checkpoint in the project history.
