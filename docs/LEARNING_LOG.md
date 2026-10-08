# Learning Log & Engineering Journal

This document tracks implementation decisions, rejected alternatives, step-by-step methodologies, and defense preparation for every completed task in accordance with Hackathon Rule 15.

---

## Log Template

```markdown
## [Task ID / Title] - [Date/Time]

### 1. What was done
- Brief summary of work completed.

### 2. Why & Rejected Alternatives
- **Why this approach**: Rationale for the technical or design choice.
- **Rejected alternative**: What other option was considered and why it was passed over.

### 3. Step-by-Step Implementation
1. Step 1...
2. Step 2...
3. Step 3...

### 4. Files Created / Modified
- `path/to/file1`
- `path/to/file2`

### 5. 30-Second Judge Pitch
- Concise explanation highlighting the environmental impact, technical robustness, and real-world viability.

### 6. Viva Questions & Answers
1. **Q1**: 
   - **A1**: 
2. **Q2**: 
   - **A2**: 
3. **Q3**: 
   - **A3**: 
```

---

## Entries

## Task 1: Governance, Compliance Documentation, and Hackathon Rule Setting - 2026-10-09

### 1. What was done
- Conducted mandatory safety check on workspace directory (`c:\Users\Rishabh Bansal\Documents\parali-setu-v2`), verifying it is completely empty with no legacy code, git history, or virtual environments.
- Authored canonical hackathon rules in `docs/HACKATHON_RULES.md`.
- Created open-source and dependency inventory in `docs/CREDITS.md`.
- Created AI tools and models tracking log in `docs/AI_TOOLS.md`.
- Established real AWS verification tracking in `docs/AWS_EVIDENCE.md`.
- Initialized structured engineering journal in `docs/LEARNING_LOG.md`.
- Drafted prior-prototype disclosure statement in `docs/DISCLOSURE.md`.

### 2. Why & Rejected Alternatives
- **Why this approach**: Establishing rigorous compliance and documentation foundations upfront ensures zero rule violations, enforces absolute isolation from any pre-hackathon prototypes, provides complete auditability of AI/AWS usage, and guarantees clean governance throughout the sprint.
- **Rejected alternative**: Consolidating all rules and logs into a single sprawling `README.md`. Rejected because separate, specialized documentation files allow clear modular tracking (e.g. dynamic credits, AWS call sites, secret safety) and clean automated checks.

### 3. Step-by-Step Implementation
1. Inspected the workspace directory using `list_dir` to confirm zero existing files or hidden histories.
2. Formatted and generated `docs/HACKATHON_RULES.md` matching all prompt event, git, AWS, privacy, and style directives.
3. Created `docs/CREDITS.md` with structured tables for frameworks, APIs, and datasets.
4. Created `docs/AI_TOOLS.md` recording current IDE/model usage and planned foundation models.
5. Structured `docs/AWS_EVIDENCE.md` detailing all planned AWS services, CLI safety rules, and demo video requirements.
6. Initialized `docs/LEARNING_LOG.md` with template and entry format.
7. Prepared `docs/DISCLOSURE.md` containing formal declaration text.

### 4. Files Created / Modified
- [docs/HACKATHON_RULES.md](file:///c:/Users/Rishabh%20Bansal/Documents/parali-setu-v2/docs/HACKATHON_RULES.md)
- [docs/CREDITS.md](file:///c:/Users/Rishabh%20Bansal/Documents/parali-setu-v2/docs/CREDITS.md)
- [docs/AI_TOOLS.md](file:///c:/Users/Rishabh%20Bansal/Documents/parali-setu-v2/docs/AI_TOOLS.md)
- [docs/AWS_EVIDENCE.md](file:///c:/Users/Rishabh%20Bansal/Documents/parali-setu-v2/docs/AWS_EVIDENCE.md)
- [docs/LEARNING_LOG.md](file:///c:/Users/Rishabh%20Bansal/Documents/parali-setu-v2/docs/LEARNING_LOG.md)
- [docs/DISCLOSURE.md](file:///c:/Users/Rishabh%20Bansal/Documents/parali-setu-v2/docs/DISCLOSURE.md)

### 5. 30-Second Judge Pitch
- ParaliSetu starts with total engineering integrity and zero inherited debt. From the very first file, we have instituted non-negotiable boundaries: zero code reuse from past prototypes, auditable logging of AI assistance and open-source licenses, and explicit verification requirements for every single AWS cloud service. We are building a clean, transparent, and high-impact solution to eliminate crop burning.

### 6. Viva Questions & Answers
1. **Q**: How do you guarantee no code from the previous prototype was brought into this submission?
   - **A**: The workspace was verified empty at inception, git history starts fresh within the hackathon window, and `docs/DISCLOSURE.md` formalizes our zero-carryover commitment along with independent auditing.
2. **Q**: Why is AWS usage explicitly documented in `AWS_EVIDENCE.md` before writing code?
   - **A**: To eliminate 'cloud-washing'. Every AWS service declared must have verifiable code call sites, live console/terminal visibility in the demo video, and cost-controlled teardown steps.
3. **Q**: How does this setup protect sensitive farmer data and credentials?
   - **A**: Hackathon Rules 8, 9, 11, and 13 enforce pre-commit secret scans, mandatory SSM Parameter Store usage instead of embedded keys, synthetic data for testing, and an S3 24-hour lifecycle deletion rule for audio recordings.

