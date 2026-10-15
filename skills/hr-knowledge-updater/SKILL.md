---
name: hr-knowledge-updater
description: Safely ingest new HR reference materials into the GitHub knowledge base with grounded claims, provenance, conflict handling and change review.
---

# HR Knowledge Updater

## Goal
Expand an evidence-traceable HR/OB/labour-law knowledge base without hallucinating facts, fake citations, or silently overwriting existing material.

## Non-negotiable steps
1. Inspect the current repo, including manifest, trusted/review notes and existing conventions.
2. Inspect the **actual uploaded source**, including relevant pages/figures; never infer unseen passages. Record document title, edition/date, exact page/section, and whether the text was legible.
3. Confirm redistribution rights before uploading any full documents. Public repository: do not push copyrighted books, restricted course notes or personal data. Store bibliographic metadata and original synthesis instead.
4. Extract atomic claims; for each claim, cite source file + precise page/section. Retain dates, thresholds, qualifiers, examples and original terminology.
5. Check each paraphrase against the source. If passage unavailable or visual-only and unreadable, put in `knowledge/review/` with `unverified`, not `verified`.
6. Identify duplicates, contradictions, outdated material and source-specific interpretations. Do not silently resolve contradictions. For Indian law distinguish enacted, commenced, notified rules, and jurisdiction; consult current official sources for live legal answers.
7. Update only impacted notes. Preserve existing verified entries unless stronger evidence supports change; keep an audit trail.
8. Create changes in a review branch/PR when supported. Check diff, source paths and citation validity before merge. Never claim tests passed unless they actually ran.
9. Report added/modified files, unresolved conflicts and verification status; no invented page references.

## Source card format
Use one concept per section or file:
```yaml
id: unique-kebab-case
topic: "Exact topic"
claim: "Precisely stated claim"
sources:
  - title: "Exact document title"
    file: "Local/upload identifier or repository reference"
    location: "Exact page or section"
    quote_checked: true
status: verified  # otherwise unverified, conflicting or outdated
verified_on: YYYY-MM-DD
notes: "Scope, exceptions, disputed interpretations"
```
Never set `quote_checked: true` without inspecting the indicated source span. If page cannot be established, use `location: unknown`, `status: unverified`.

## Update safety
- Source provenance is mandatory; a model-generated answer is not itself a source.
- Keep fact statements separate from inference, tips and mnemonic devices.
- Do not trust an older training document as authoritative on current labour law.
- Validate YAML/Markdown syntax where possible and run the regression tests.
- Do not rewrite an entire directory merely to accommodate a small update.
- A clean commit does not prove factual correctness; note manual verification needed.
