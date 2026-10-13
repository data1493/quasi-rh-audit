# External Audit of OpenAI's Quasi-Riemann Hypothesis Manuscript (Re(s) > 7/8)

> **This is an external audit of the existing manuscript, not an independent re-proof of the analytic estimates.**

## Status

The structure holds: the dual-representation argument is coherent at every examined layer (continuation criterion, cubic-theta reflection, Poisson isolation, sextic large sieve, zero detector, Stage 1 and Stage 2 assembly, uniformity and Hecke-to-Dirichlet transfer). The paper's own exponent ledgers close with a positive remainder under the stated accounting: a Stage 1 high-side saving of $1/4800$ and a Stage 2 endpoint constant $49/440640 > 1/10000$. The Lean formalization of the final theorems is machine-checked, and a third-party kernel replay is reported. The residual risk is unlisted intermediate losses: the margins are small, and confirming that no intermediate lemma hides an unlisted loss larger than the reserved budgets requires a specialist reading of the original manuscript.

**What this work is:** a layer-by-layer reconstruction, a specialist audit of the paper's own exponent accounting, computational confirmation of the critical constants, and a Lean skeleton of the logical hinge (described in [the master audit](audit/00_master_audit.md#lean-skeleton-of-the-hinge)). **What it is not:** a proof, or an independent verification of every estimate.

## Primary objects (cite these first)

- OpenAI, *The Quasi-Riemann Hypothesis: A Zero-Free Half-Plane Re(s) > 7/8*, preprint dated September 30, 2026, in [openai/math](https://github.com/openai/math):
  - TeX source: [paper.tex](https://github.com/openai/math/blob/1581d4cbdd69a0faf34b2089614fe2a814316a6a/preprints/The-Quasi-Riemann-Hypothesis-September-30-2026/build/paper.tex)
  - PDF: [paper.pdf](https://github.com/openai/math/blob/1581d4cbdd69a0faf34b2089614fe2a814316a6a/preprints/The-Quasi-Riemann-Hypothesis-September-30-2026/paper.pdf)
- Lean formalization (result family 003):
  - Scope note: [lean/docs/003.md](https://github.com/openai/math/blob/1581d4cbdd69a0faf34b2089614fe2a814316a6a/lean/docs/003.md)
  - Proof module: [OAI/NumberTheory/DirichletL/Nonvanishing.lean](https://github.com/openai/math/blob/1581d4cbdd69a0faf34b2089614fe2a814316a6a/lean/OAI/NumberTheory/DirichletL/Nonvanishing.lean)
  - Comparator statements: [QuasiRiemannHypothesis.lean](https://github.com/openai/math/blob/1581d4cbdd69a0faf34b2089614fe2a814316a6a/lean/ComparatorChallenges/QuasiRiemannHypothesis.lean), [DirichletSevenEighths.lean](https://github.com/openai/math/blob/1581d4cbdd69a0faf34b2089614fe2a814316a6a/lean/ComparatorChallenges/DirichletSevenEighths.lean), [HeckeSevenEighths.lean](https://github.com/openai/math/blob/1581d4cbdd69a0faf34b2089614fe2a814316a6a/lean/ComparatorChallenges/HeckeSevenEighths.lean)

Links are pinned to openai/math commit `1581d4c`.

## Ten-minute path for a number theorist

1. [Loss table](audit/11_loss_table.md): every charged loss against its reserved budget.
2. [Residual-risk notes](audit/19_residual_risk_notes.md): where an unlisted loss could hide.
3. [Expert review request](audit/18_expert_review_request.md): five prioritized items and precise questions.

## Contents

| # | File | Topic |
|---|------|-------|
| 00 | [00_master_audit.md](audit/00_master_audit.md) | Independent Multi-Agent Audit of the OpenAI Quasi-Riemann Hypothesis Manuscript |
| 01 | [01_continuation_criterion.md](audit/01_continuation_criterion.md) | Part 1 — Continuation Criterion and Dual-Representation Contradiction |
| 02 | [02_cubic_theta_reflection.md](audit/02_cubic_theta_reflection.md) | Part 2 — Cubic-Theta Reflection Identities |
| 03 | [03_poisson_principal_signal.md](audit/03_poisson_principal_signal.md) | Part 3 — Poisson Summation and Isolation of the Principal Signal |
| 04 | [04_large_sieve_row_energy.md](audit/04_large_sieve_row_energy.md) | Part 4 — Large Sieve and Row Energy Bounds |
| 05 | [05_zero_detector_moments.md](audit/05_zero_detector_moments.md) | Part 5 — Zero Detector and Moment Estimates |
| 06 | [06_stage1_assembly_11_12.md](audit/06_stage1_assembly_11_12.md) | Part 6 — Stage 1 Assembly to 11/12 |
| 07 | [07_stage2_refinement_7_8.md](audit/07_stage2_refinement_7_8.md) | Part 7 — Stage 2 Refinement to 7/8 |
| 08 | [08_uniformity_transfer.md](audit/08_uniformity_transfer.md) | Part 8 — Uniformity, Contours, Residues, and Hecke-to-Dirichlet Transfer |
| 09 | [09_lean_alignment.md](audit/09_lean_alignment.md) | Part 9 — Lean Formalization Alignment |
| 10 | [10_specialist_margins.md](audit/10_specialist_margins.md) | Specialist Audit of the Quantitative Margins |
| 11 | [11_loss_table.md](audit/11_loss_table.md) | Specialist Loss Table |
| 12 | [12_stage1_central_loss.md](audit/12_stage1_central_loss.md) | Stage 1 Central Loss Accounting — $46\epsilon_*$ |
| 13 | [13_late_height_closure.md](audit/13_late_height_closure.md) | Late-Height Closure |
| 14 | [14_sextic_large_sieve.md](audit/14_sextic_large_sieve.md) | Specialized Sextic Large Sieve |
| 15 | [15_detector_saturation.md](audit/15_detector_saturation.md) | Zero-Detector Saturation |
| 16 | [16_stage2_compensation.md](audit/16_stage2_compensation.md) | Stage 2 Compensation Local Identities |
| 17 | [17_computational_check.md](audit/17_computational_check.md) | Computational Check |
| 18 | [18_expert_review_request.md](audit/18_expert_review_request.md) | Expert Review Request — Quantitative Hinge of the OpenAI Quasi-Riemann Manuscript |
| 19 | [19_residual_risk_notes.md](audit/19_residual_risk_notes.md) | Residual-Risk Notes |
| — | [ABSTRACT.md](ABSTRACT.md) | 150–200 word abstract |
| — | [LICENSE](LICENSE) | CC BY 4.0 |

A compiled PDF of the master audit, loss table and residual-risk notes is attached to the release as `quasi-rh-audit.pdf`.

## Method note

The audit was produced with a multi-agent workflow (SuperGrok Heavy) reading the public TeX source and Lean formalization. Every finding is limited to what was extracted from those public sources. Computational checks cover the row envelope $R(\delta)$ and the Stage 2 endpoint constant only.

## How to cite

Cite the OpenAI preprint and Lean formalization above as the primary objects. To cite this audit:

> Jordan [SURNAME TODO]. *External Audit of OpenAI's Quasi-Riemann Hypothesis Manuscript (Re(s) > 7/8): layer reconstruction, loss table and residual-risk notes.* October 2026. [REPO URL TODO]

```bibtex
@misc{quasi_rh_external_audit_2026,
  author       = {Jordan [SURNAME TODO]},
  title        = {External Audit of OpenAI's Quasi-Riemann Hypothesis Manuscript (Re(s) > 7/8)},
  year         = {2026},
  month        = oct,
  howpublished = {[REPO URL TODO]},
  note         = {External audit of the existing manuscript; not an independent re-proof of the analytic estimates}
}
```

## License

All text in this repository is licensed under [CC BY 4.0](LICENSE). This repository contains no code or Lean of its own. The OpenAI preprint and Lean formalization are separate works under their own license (openai/math is Apache-2.0) and are not redistributed here.
