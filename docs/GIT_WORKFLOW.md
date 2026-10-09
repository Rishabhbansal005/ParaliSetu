# Git Workflow & Integrity Standards

This document establishes the Git protocol for the ParaliSetu repository, ensuring complete auditability, honest history, and strict credential safety in compliance with Hackathon Rules 6–8.

---

## 1. Branching Strategy
- **`main` Branch**: The trunk branch. It must remain functional, tested, and green at all times. Direct pushes to `main` occur only for verified base setup or after explicit user authorization.
- **Task Branches**: Every subsequent feature or fix develops on its own isolated branch (e.g., `feat/stubble-estimator`, `infra/fastapi-docker`).
- **Merge Criteria**: Merges to `main` happen only when all unit tests pass, secrets scans are clean, and the human lead approves.

---

## 2. Commit Message Standards
Commit messages must accurately convey the nature of changes with conventional prefixes:
- `feat:` New capability or user-facing feature.
- `fix:` Bug fix or defect remediation.
- `docs:` Documentation and architecture updates.
- `test:` Unit tests, integration tests, or mock datasets.
- `chore:` Dependency management, config tweaks, and repo hygiene.

---

## 3. Mandatory Pre-Commit Secret Scan
Before any commit is created:
1. Stage desired files with `git add <files>`.
2. Run `git status` to verify no untracked secrets, build artifacts, or private files are present.
3. Perform a pattern scan across all staged changes for API keys, AWS credentials, secret tokens, private keys (`.pem`, `.key`), and password strings.
4. If any sensitive data is discovered, immediately unstage, sanitize, and verify before proceeding.

---

## 4. Remote Management & Integrity
- **Canonical Remote**: `https://github.com/Rishabhbansal005/ParaliSetu.git`
- **Strict Prohibition**: The legacy repository (`Rishabhbansal005/Parali-setu`) must never be added as a remote or referenced.
- **No History Manipulation**: `git push --force`, rebase rewrites of published commits, and commit backdating are strictly prohibited. The first commit (`c19fef7`) has a placeholder author email by mistake and history was intentionally not rewritten.
- **Push Reporting**: After every push, the agent must report the branch name, commit hash, and list of files modified.
