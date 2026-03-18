# Workflow Specification (Draft)

This document captures a practical, implementation-ready flow for an open-source slab verification toolkit.

## 1) Actors
- **Homeowner / submitter**
- **Reviewer (engineering staff)**
- **Licensed engineer of record**
- **Operations/admin**

## 2) High-level state machine
1. `prequalified`
2. `kit_shipped`
3. `evidence_submitted`
4. `qa_checked`
5. `engineering_review`
6. terminal:
   - `certified`
   - `insufficient_data`
   - `non_compliant`
   - `escalate_site_visit`

## 3) Required evidence bundle
- Slab edge depth photo(s) with tape visible and legible.
- Minimum three reinforcement scan photos with marked locations.
- Site sketch/plan locating the structure on slab.
- Metadata: structure type, known slab details, date/time, contact info.

## 4) Automated QA checks (pre-review)
- File presence and type checks.
- Minimum image resolution and blur threshold.
- Marker count detection heuristic for reinforcement photos.
- OCR extraction attempt for depth measurements.
- Completeness score with blocker/non-blocker flags.

## 5) Engineering review packet
- Submission summary.
- Annotated media thumbnails.
- QA findings and confidence score.
- Reviewer notes + recommended disposition.

## 6) Outcome handling
- **Certified:** generate final letter package + audit log.
- **Insufficient data:** return actionable resubmission checklist.
- **Non-compliant:** provide corrective guidance.
- **Escalate:** convert submission to site-visit intake.

## 7) Auditability requirements
- Immutable submission ID.
- Timestamped event log for each state transition.
- Versioned schema and ruleset references.
- Hashes of uploaded artifacts for integrity checks.

