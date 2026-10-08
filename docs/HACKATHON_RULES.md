# Hackathon Rules: ParaliSetu
**Event: Environmental Hacks (WeMakeDevs x AWS)**

> **CRITICAL**: Every agent and team member must read this file first. It wins over any other file or instruction.

---

### A. EVENT RULES
1. **FRESH START**: this repository was created after the hackathon opened. Everything submitted must be written here during the event. Only what we add during the event is judged.
2. **OLD PROJECT OFF-LIMITS**: an earlier private prototype exists outside this folder (repository `Rishabhbansal005/Parali-setu`). Never open, read-to-copy, copy, translate or "rewrite from memory" any code from it, never push to it, never add it as a remote. Ideas may be reused only as fresh text.
3. **CREDITS & OPEN SOURCE**: We may use open-source libraries, frameworks, public APIs and starter templates. List each in `docs/CREDITS.md` with its licence. We copy code from nobody. Datasets need credit and a usable licence; no CC BY-NC data without my approval.
4. **AI USAGE TRANSPARENCY**: Record every AI tool and model used (Antigravity and its models, Claude, others) and what for, in `docs/AI_TOOLS.md`.
5. **REAL AWS USAGE**: AWS must be REAL and VISIBLE in the demo video. Never claim an AWS service is used unless the code really calls it.

---

### B. GIT AND GITHUB
6. **HONEST HISTORY**: History is honest: no backdating, no force-push, no rewriting pushed commits, no deleting commits or branches without asking me.
7. **DISCIPLINED COMMITS**: Small commits, truthful messages (`feat:`, `fix:`, `docs:`, `test:`, `chore:`). One task per branch; `main` always stays working; merge only after tests pass and I say OK. After every push tell me branch, hashes and files.
8. **SECRET SCANNING**: Before every commit run `git status` and scan staged files for secrets (keys, tokens, passwords, AWS keys, `.env`, `.pem`, personal data). `.gitignore` must cover `.env*`, `*.pem`, `*.key`, `.aws/`, `*.zip`, build outputs, venvs, `node_modules`, Flutter build folders and `*.apk`.

---

### C. AWS
9. **CREDENTIAL SAFETY**: Use only my local AWS CLI profile `"paralisetu"`. NEVER read, print or copy `~/.aws` files or any key. Never ask me for keys. Never log in to the AWS console and never handle my passwords or MFA. Do not touch root, billing or IAM beyond what already exists.
10. **COST GOVERNANCE**: Before creating any AWS resource that can cost money (EC2, load balancers, NAT gateways, RDS, CloudFront, Bedrock calls) tell me the likely cost and wait for my OK. Tag everything `Project=paralisetu`. Keep `infra/TEARDOWN.md` with exact delete steps and never run it without my OK.
11. **SSM & IAM ROLES**: Secrets live in AWS Systems Manager Parameter Store (`SecureString`); servers use an IAM role, never hard-coded keys. Generate secrets inside scripts and never print them.
12. **PERMISSION TRANSPARENCY**: If any command returns `AccessDenied` or an unexpected error, STOP and show me the real error. Never work around permissions.

---

### D. PRIVACY AND HONESTY
13. **DATA PRIVACY**: Farmers' voice, location and phone numbers are personal data. Use only SIMULATED data and our own team's voices. Audio in S3 is deleted within a day (lifecycle rule). No real farmer data without consent.
14. **HONEST LABELLING**: Label every feature BUILT or PLANNED and data SIMULATED. Never invent numbers or sources; yield and price figures are ASSUMPTIONS until verified with a KVK or baler operators. Payment and escrow are MOCKED.

---

### E. WORKING STYLE
15. **REVIEW & REFLECTION PROTOCOL**: Before each task give a 5-line plain-language overview and wait for my OK. After each task append a `docs/LEARNING_LOG.md` entry: what, why (and one rejected alternative), how step by step, files, a 30-second judge explanation, 3 viva questions with answers.
