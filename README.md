# ParaliSetu (पराली सेतु) 🌾🚜

> **Transforming Paddy Stubble (Parali) from an Air Pollution Crisis into Farmer Wealth.**  
> Built for **Environmental Hacks (WeMakeDevs × AWS)**.

---

## 📌 Executive Summary

Every autumn, northern India faces hazardous air quality (AQI 500+) driven by paddy residue burning (*parali*). Farmers operate in a tight 10–15 day window between paddy harvest and wheat sowing; without accessible, affordable baling machinery and verified off-takers, burning remains the default choice.

**ParaliSetu** connects farmers directly to baling machine contractors, transport truckers, and industrial bio-energy/pellet buyers.
- **Multilingual Voice & Form Input**: Farmers specify land size and harvest dates via speech (Hindi, Punjabi, English) or guided touch UI.
- **Dynamic Yield Estimation**: Instant stubble tonnage prediction based on acreage and crop variety.
- **Algorithmic Aggregation**: Google OR-Tools matches farmer windows with nearby balers and trucks.
- **Weighbridge-Verified Fair Pay**: Settlement based on certified weighbridge weights with mocked escrow state machine protection.
- **Industrial Web Portal**: Real-time dispatch, booking intake, and weight ticket capture for buyers and machine operators.

---

## 🚦 Feature Status: BUILT vs. PLANNED

| Feature / Component | Description | Status |
| :--- | :--- | :--- |
| **Governance & Safety Standards** | Hackathon compliance, strict .gitignore, secret scanning, disclosure notice | **BUILT** |
| **Farmer Mobile App** | Flutter Android app (English default, Hindi, Punjabi) with voice & form booking | **PLANNED** |
| **Voice Query Pipeline** | AWS Transcribe + Bedrock intent extraction for dialectal farmer speech | **PLANNED** |
| **Stubble Yield Estimator** | Acreage-to-tonnage estimation model with verified regional bounds | **PLANNED** |
| **Matching Engine** | FastAPI + OR-Tools route and capacity scheduler for balers and trucks | **PLANNED** |
| **Weighbridge & Escrow Flow** | Weighbridge ticket processing + state-machine mock escrow payouts | **PLANNED** |
| **Industrial Buyer Portal** | Web console for off-takers, baler dispatchers, and weighbridge operators | **PLANNED** |
| **Satellite Hotspot Map** | MODIS / VIIRS stubble burn hotspot visualization & satellite validation | **IF-TIME** |

> *Note: All buyer accounts, machinery fleets, and price discovery rates in development are **SIMULATED**.*

---

## ☁️ Real AWS Cloud Architecture

In strict adherence to our project rules, AWS services are real, functional, and verifiable:
- **Amazon EC2**: Containerized FastAPI backend with PostgreSQL + PostGIS.
- **Amazon CloudFront**: SSL/TLS edge routing with global caching and CDN distribution.
- **Amazon S3**: Ephemeral audio storage configured with 24-hour lifecycle auto-deletion.
- **Amazon Transcribe**: Low-latency automated speech-to-text for Indian regional dialects.
- **Amazon Bedrock**: Conversational natural language parsing and intelligent intent recognition.
- **Amazon CloudWatch**: Centralized operational monitoring, metrics, and structured log streams.
- **AWS Systems Manager Parameter Store**: SecureString secret management without hardcoded credentials.

See full verification criteria and video demonstration requirements in [docs/AWS_EVIDENCE.md](file:///c:/Users/Rishabh%20Bansal/Documents/parali-setu-v2/docs/AWS_EVIDENCE.md).

---

## 🤖 AI Tools & Transparency

All AI usage during the design and development lifecycle is disclosed in [docs/AI_TOOLS.md](file:///c:/Users/Rishabh%20Bansal/Documents/parali-setu-v2/docs/AI_TOOLS.md).
- **Development Assistant**: Google DeepMind Antigravity IDE (Gemini 3.8 Flash).
- **Runtime Intent Parsing**: AWS Bedrock Foundation Models.

---

## 📜 Credits & Open Source Attribution

All third-party libraries, datasets, and open-source frameworks are cataloged with their respective licenses in [docs/CREDITS.md](file:///c:/Users/Rishabh%20Bansal/Documents/parali-setu-v2/docs/CREDITS.md).

---

## 🛡️ Hackathon Disclosure & Governance

- **Governance Rules**: [docs/HACKATHON_RULES.md](file:///c:/Users/Rishabh%20Bansal/Documents/parali-setu-v2/docs/HACKATHON_RULES.md)
- **Zero-Carryover Disclosure**: [docs/DISCLOSURE.md](file:///c:/Users/Rishabh%20Bansal/Documents/parali-setu-v2/docs/DISCLOSURE.md)
- **Engineering Journal & Viva Prep**: [docs/LEARNING_LOG.md](file:///c:/Users/Rishabh%20Bansal/Documents/parali-setu-v2/docs/LEARNING_LOG.md)
