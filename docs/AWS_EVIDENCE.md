# AWS Evidence & Verification Log

In compliance with Hackathon Rule 5:
> *"AWS must be REAL and VISIBLE in the demo video. Never claim an AWS service is used unless the code really calls it."*

---

## 1. AWS CLI Profile Configuration
- **Profile Name**: `paralisetu`
- **Safety Standard**: No credentials, access keys, or secret files (`~/.aws`) are ever printed, copied, or stored in code.

---

## 2. Tracked AWS Services

| Service | Architecture Role | Real Call Site / Code Evidence | Visibility in Demo Video | Verification Status |
| :--- | :--- | :--- | :--- | :--- |
| **Amazon EC2** | Hosts FastAPI backend + PostgreSQL/PostGIS container | `infra/` deployment scripts / live public IP / DNS | Terminal / SSH / Service curl / Web portal | Planned |
| **Amazon CloudFront** | HTTPS termination & edge caching for API & portal | CloudFront distribution ID & domain URL | Browser devtools & SSL certificate | Planned |
| **Amazon S3** | Voice audio file staging (24h lifecycle expiry rule) | `boto3` S3 upload/download client | AWS S3 Console bucket view & upload logs | Planned |
| **Amazon Transcribe** | Speech-to-text for farmer voice input (Hindi/Punjabi/English) | `boto3` Transcribe client job dispatch | AWS Transcribe job list & transcription JSON | Planned |
| **Amazon Bedrock** | Intent recognition & conversational farmer extraction | `boto3` Bedrock runtime invocation | Bedrock request/response logs & output in app | Planned |
| **Amazon CloudWatch** | Structured logging, request metrics, and alerting | Application logger handler / CloudWatch log group | CloudWatch log stream viewer in video | Planned |
| **AWS Systems Manager Parameter Store** | SecureString runtime retrieval of database credentials and tokens | `boto3` SSM `get_parameter` | SSM Parameter Store console / CLI query | Planned |

---

## 3. Video Demonstration Checklist
- [ ] AWS CLI `aws sts get-caller-identity --profile paralisetu` shown on screen.
- [ ] CloudFront HTTPS URL serving live web requests.
- [ ] Live S3 audio upload shown triggering an AWS Transcribe job.
- [ ] Bedrock intent parsing logs shown in real time.
- [ ] Parameter Store SecureString retrieval demonstrated without hardcoded keys.
- [ ] CloudWatch live log stream showing backend events.
