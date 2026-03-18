# DIY Concrete Slab Verification Kit (Open Source Starter)

This repository is an open-source starter for a **DIY concrete slab verification workflow** inspired by the Oasis Engineering service offering.

## Product review (based on public pages)

### What appears strong
- **Clear homeowner value proposition:** quick path to after-the-fact permit support for accessory structures (pergolas, patios, sheds, etc.).
- **Low-friction workflow:** ship a small kit, let the customer collect evidence, upload data, engineer reviews remotely.
- **Cost transparency:** public pricing structure with refund/credit logic and equipment return policy.
- **Scope controls:** explicit limits to accessory structures and non-destructive verification only.

### Key constraints / risks
- **Data quality variance:** photos and scanner readings from non-expert users can be inconsistent.
- **Inconclusive NDT edge cases:** hidden slab conditions can block confident certification.
- **Jurisdiction differences:** code requirements and AHJ expectations vary by city/county/state.
- **Chain-of-custody concerns:** evidence authenticity and timing may be questioned by strict reviewers.

### Open-source opportunity
The core workflow can be productized as software + documentation while keeping professional engineering sign-off as a licensed service layer:
- Open: intake UX, evidence schema, QA checks, report generation pipeline.
- Closed/professional: licensed engineer decision, stamping/signing, local code interpretation liability.

---

## Observed workflow summary
1. Customer receives a kit (scanner, tape, markers, return label, guide).
2. Customer documents slab edge depth and reinforcement indicators.
3. Customer uploads photos + structured answers in a form.
4. Engineering team reviews submission.
5. Outcome: certification letter (if requirements met) or corrective guidance / escalate to site visit.
6. Customer returns kit within defined window.

---

## Open-source blueprint
See detailed implementation plan in [`docs/open-source-blueprint.md`](docs/open-source-blueprint.md).

Suggested phases:
1. **MVP Evidence Portal**
2. **QA + Scoring Engine**
3. **Report Generator + API**
4. **Jurisdiction Rule Packs + Integrations**

---

## Suggested repository structure

```text
/docs
  open-source-blueprint.md
  workflow-spec.md
/schemas
  submission.schema.json
/services
  ingestion/
  qa-engine/
  report-generator/
/web
  portal/
```

---

## Initial OSS licensing note
Current repository license is MIT (`LICENSE`). For real-world deployment, consider adding:
- professional-use disclaimer,
- no-engineering-advice disclaimer,
- jurisdiction/legal compliance notice,
- explicit separation between software outputs and licensed engineering decisions.

---

## Next steps
- Create machine-readable submission schema.
- Build a simple web intake form + object storage upload.
- Add image quality gates (resolution, ruler visibility, marker count).
- Define report data contract for engineer review queue.
- Pilot with synthetic sample submissions.

