# DIKWP-NOESIS 9.5

## Cosmic-Essence-Oriented Personal Cognitive Transparency, Reversible Correction and Enhancement System

**DIKWP-NOESIS 9.5** is a local-first, owner-governed open-source reference system for making consequential cognition inspectable without turning a person into a single score or allowing software to rewrite beliefs automatically.

It sits downstream of **DIKWP-EIDOS 9.5**:

- **EIDOS95** compiles accumulated content, knowledge, experience, revisions and rights into a source-grounded cognitive essence representation.
- **NOESIS95** records living cognition as an append-only worldline and closes the loop through evidence, competing world models, probability forecasts, reality outcomes, calibration, reversible correction proposals and burden-bounded enhancement experiments.

The system is inspired by the 2026 bilingual research-book programme on the ultimate essence/world model of the universe, native semantic continuity, semantic mathematics, physical history and artificial-consciousness physics. It does **not** claim that those works, this software or the bundled 24 cards establish final experimentally proven laws of physics or consciousness.

## Core contract

1. Every consequential cognitive record can declare an **E/H/F/P/N** claim class and a **D/I/K/W/P** semantic position. These are separate namespaces: claim-class `P` means an empirical hypothesis; DIKWP `P` means purpose or executable input-output orientation.
2. Evidence IDs must resolve to an attribution- and rights-aware evidence ledger.
3. High-impact judgments require at least two materially different world models and a distinguishing reality-contact step where feasible.
4. Predictions retain their original probabilities; outcomes are appended and scored with Brier/log-loss/calibration summaries.
5. Corrections never overwrite prior records. The system generates candidates only. A successor event requires a named owner and authorization reference.
6. Affected worlds, beneficiaries, burden bearers, power positions, refusal, exit, repair and successor freedom are visible.
7. The 24 working-law cards carry epistemic status, scope, falsifier entry points and retirement conditions.
8. Automatic external-action authority is fixed at **0**.


## Two namespaces that must not collapse

| Field | Namespace | Meanings |
|---|---|---|
| `claim_class` | `research_book_claim_status` | `E` established/source-bound result; `H` historical interpretation; `F` formal/relational construction; `P` empirical hypothesis; `N` normative/metaphysical proposal |
| `dikwp` | `semantic_position` | `D` same-semantics/data registration; `I` difference/information; `K` cognitively completed semantics; `W` value-configured semantics; `P` purpose/executable input-output orientation |

A fluent formalism, diagram, program or model does not upgrade an empirical hypothesis into an established result. Conversely, a purpose record is not an empirical-hypothesis label merely because both use the letter `P` in their respective source vocabularies.

## What it produces

A compilation directory includes:

- `noesis_bundle.json` — complete machine-readable compilation;
- `ledger_snapshot.jsonl` — verified append-only cognitive event worldline;
- `audit.json` — event-level transparency vectors and rule-grounded epistemic risk patterns;
- `calibration_report.json` — resolved/pending predictions, Brier scores and calibration bins;
- `world_model_competition.json` — structural diversity and discriminator audit;
- `cosmic_law_registry.json` and `law_alignment.json` — 24 versioned working-law cards and record alignment;
- `correction_register.json` — owner-approval-only reversible correction candidates;
- `enhancement_plan.json` / `.md` — evidence- and burden-bounded exercises;
- `cognitive_graph.json` — provenance, model, revision, forecast, impact and audit graph;
- `transparency_report.md` and `dashboard.html` — human review surfaces;
- `MANIFEST.json` and `VERIFY.txt` — output integrity receipts.

## Quick start

```bash
python run.py doctor

python run.py demo \
  --out outputs/yucongduan_cosmic_method \
  --eidos /path/to/DIKWP_EIDOS95/essence_bundle.json

python run.py verify outputs/yucongduan_cosmic_method
```

Create a private workspace:

```bash
python run.py init my_noesis --owner-id my-owner-id --display-name "My Name"
```

Append one event:

```bash
python run.py append \
  --ledger my_noesis/cognitive_ledger.jsonl \
  --event my_event.json \
  --owner-id my-owner-id
```

Compile:

```bash
python run.py compile \
  --owner my_noesis/owner.json \
  --ledger my_noesis/cognitive_ledger.jsonl \
  --evidence my_noesis/evidence.json \
  --config my_noesis/config.json \
  --out my_noesis/output
```

Review `correction_register.json`. Approval appends a successor; it does not mutate the original:

```bash
python run.py approve \
  --ledger my_noesis/cognitive_ledger.jsonl \
  --proposals my_noesis/output/correction_register.json \
  --proposal-id corr-... \
  --approver "Named owner" \
  --authorization-ref "owner-review-2026-001"
```

## Event model

A cognitive event can include:

```json
{
  "owner_id": "my-owner-id",
  "kind": "decision",
  "content": "Use a small reversible pilot before scaling.",
  "claim_class": "P",
  "dikwp": "W",
  "confidence": 0.72,
  "scope": {
    "subjects": ["one pilot group"],
    "contexts": ["non-clinical voluntary research"],
    "time_horizon": "four weeks",
    "scale": "small pilot",
    "observer_position": "owner and named reviewer",
    "exclusions": ["coercive deployment"]
  },
  "evidence_refs": ["ev-001"],
  "counterevidence_refs": ["ev-002"],
  "world_models": [
    {
      "model_type": "causal",
      "claim": "The protocol improves decisions by exposing missing evidence.",
      "predictions": ["Fewer unresolved provenance gaps"],
      "discriminators": ["Compare with an equal-attention lightweight review"]
    },
    {
      "model_type": "selection",
      "claim": "Any apparent gain is mostly participant selection and extra attention.",
      "predictions": ["Benefit shrinks after attention and selection controls"],
      "discriminators": ["Compare with an equal-attention lightweight review"]
    }
  ],
  "values": [
    {
      "name": "agency",
      "beneficiaries": ["participant"],
      "burden_bearers": ["participant", "reviewer"],
      "measurement": "refusal, exit and rollback availability"
    }
  ],
  "purpose": {
    "input_state": "uncertain decision",
    "desired_state": "better-calibrated decision",
    "output": "small pilot",
    "success_metrics": ["resolved forecasts", "no material rights failure"],
    "stop_conditions": ["burden exceeds learning value"],
    "rollback": "return to prior safe process"
  },
  "affected_worlds": [
    {
      "stakeholder": "participant",
      "possible_burden": "time and disclosure",
      "consent_status": "explicit",
      "appeal_or_exit": "withdraw without penalty",
      "power_position": "lower leverage than operator"
    }
  ],
  "falsifiers": ["No prospective improvement after controls"],
  "predictions": [
    {
      "statement": "The pilot reduces unresolved provenance gaps.",
      "probability": 0.65,
      "due_at": "2026-10-01T00:00:00Z",
      "outcome_definition": "1 when the predeclared threshold is met; otherwise 0"
    }
  ],
  "action": {
    "description": "Run the minimum reversible pilot",
    "reversible": true,
    "rollback": "restore previous workflow",
    "external": false,
    "result_metric": "predeclared outcome record"
  }
}
```

## Transparency vector, not a total score

NOESIS95 reports sixteen dimensions:

- provenance traceability;
- scope explicitness;
- uncertainty explicitness;
- claim-class discipline;
- D/I/K/W/P separation;
- model plurality;
- distinguishing evidence;
- value visibility;
- purpose executability;
- affected-world visibility;
- falsifiability;
- action reversibility;
- reality contact;
- revision continuity;
- residual preservation;
- capacity/context recording.

A navigation mean is displayed only to locate incomplete records. It is not a measure of intelligence, truth, consciousness, sanity, personality, virtue, employability, insurability or legal responsibility.

## Safety and use boundaries

NOESIS95 is epistemic and decision-record support. It does not diagnose, treat or prevent a mental-health condition; provide crisis care; certify consciousness or personhood; determine culpability; or replace qualified medical, psychological, legal, financial, scientific or safety professionals.

It must not be used for involuntary profiling, employment screening, insurance pricing, political/religious conformity assessment, coercive education, secret monitoring or automatic belief modification.

See `docs/CLAIM_BOUNDARIES_CN_EN.md` and `docs/THREAT_MODEL_CN_EN.md`.

## Runtime

- Python 3.10+
- standard-library-only core
- no database required
- no model/API/network required for compilation
- dashboard is static and offline
- Apache-2.0 software license; source materials retain their own rights

## Verification

```bash
python -m unittest discover -s tests -v
python scripts/validate_release.py
```

## Attribution

The DIKWP and Mesh95 research programme is attributed to Yucong Duan. The bundled conceptual registry cites the six August 2026 author-prepared research-book/technical-report records listed in `docs/RESEARCH_PROVENANCE.md`. Inclusion in a source registry does not imply publisher-issued book status, external validation, endorsement of this implementation or transfer of identity/representation rights.

## Formal specification

See `docs/FORMAL_SPEC_CN.md` for the state model, dual typing, model competition, calibration, append-only correction and authority invariants.
