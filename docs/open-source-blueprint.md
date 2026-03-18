# Open-Source Blueprint

## Goal
Create an OSS toolkit that standardizes slab verification evidence collection and review preparation, while allowing licensed professionals to make final determinations.

## Guiding principles
- **Safety first:** no autonomous certification.
- **Jurisdiction-aware:** configurable rule packs.
- **Human-in-the-loop:** engineer decision always explicit.
- **Auditable by default:** all decisions traceable.

## Architecture

### A. Web Intake (frontend)
- Guided form wizard.
- Upload assist prompts (photo examples, validation hints).
- Mobile-first upload reliability.

### B. Ingestion Service
- Secure media upload + metadata storage.
- Submission lifecycle orchestration.
- Notification hooks.

### C. QA Engine
- Computer vision checks for measurement/marker quality.
- Completeness scoring.
- Rule-based blockers for missing evidence.

### D. Review Workspace
- Structured evidence viewer.
- Disposition templates.
- Escalation and resubmission flows.

### E. Report Generator
- Deterministic report templates.
- JSON + PDF outputs.
- Signature integration points (external service).

## Data model (minimal)
- `submission`
- `artifact`
- `qa_result`
- `review_decision`
- `ruleset_version`
- `audit_event`

## Security baseline
- Short-lived upload URLs.
- PII minimization + retention policy.
- Encryption at rest + transport.
- Role-based access controls.

## 90-day execution plan

### Weeks 1-2
- Finalize schema + workflow states.
- Build submission API skeleton.

### Weeks 3-6
- Build upload portal MVP.
- Implement basic QA checks and reviewer queue.

### Weeks 7-10
- Add report generator and downloadable packet.
- Introduce ruleset versioning and audit log.

### Weeks 11-13
- Pilot with mocked cases and edge-case corpus.
- Harden security controls and observability.

## Definition of done for MVP
- End-to-end submission -> QA -> review packet pipeline works.
- Incomplete submissions auto-flagged with clear remediation prompts.
- Every decision and artifact traceable in an audit record.

