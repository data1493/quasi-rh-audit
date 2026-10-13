# External Audit of OpenAI's Quasi-Riemann Hypothesis Manuscript (Re(s) > 7/8)

**What this is:** an external, AI-assisted audit of OpenAI's preprint *The Quasi-Riemann Hypothesis: A Zero-Free Half-Plane Re(s) > 7/8* (September 30, 2026) and its Lean formalization in [openai/math](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a).

> **This is an external audit of the existing manuscript, not an independent re-proof of the analytic estimates.** We did not prove anything, did not verify every estimate, and did not build the Lean ourselves.

**Verdict (scope-limited):** the dual-representation structure is coherent at every layer we examined, and the paper's own exponent ledgers close with a positive remainder under the losses the paper explicitly charges: a Stage 1 high-side saving of $1/4800$ and a Stage 2 endpoint constant $49/440640 \approx 0.0001112 > 1/10000$. The Lean statements of the final theorems match the paper; OpenAI reports them machine-checked, and a third-party kernel replay (davegoldblatt) is reported for the zeta statement.

**Residual risk:** the margins are small. An intermediate lemma could carry an unlisted loss larger than the reserved budgets. Ruling that out needs a specialist reading of the original manuscript.

**Ten-minute path for a number theorist:**

1. [Loss table](audit/11_loss_table.md): every charged loss against its reserved budget.
2. [Residual-risk notes](audit/19_residual_risk_notes.md): where an unlisted loss could hide.
3. [Expert review request](audit/18_expert_review_request.md): five prioritized items and precise questions. Findings welcome as [issues](https://github.com/data1493/quasi-rh-audit/issues/new/choose).

Audited version: openai/math commit [`adc7f12`](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a) (the audited files are byte-identical at the current `main`, see [Version audited](#version-audited)).

---

## Primary objects (cite these first)

- OpenAI, *The Quasi-Riemann Hypothesis: A Zero-Free Half-Plane Re(s) > 7/8*, preprint dated September 30, 2026 (199 pages):
  - TeX source: [paper.tex](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/The-Quasi-Riemann-Hypothesis-September-30-2026/build/paper.tex)
  - PDF: [paper.pdf](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/The-Quasi-Riemann-Hypothesis-September-30-2026/paper.pdf)
- Lean formalization (result family 003):
  - Scope note: [lean/docs/003.md](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/lean/docs/003.md)
  - Proof module: [OAI/NumberTheory/DirichletL/Nonvanishing.lean](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/lean/OAI/NumberTheory/DirichletL/Nonvanishing.lean)
  - Comparator statements: [QuasiRiemannHypothesis.lean](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/lean/ComparatorChallenges/QuasiRiemannHypothesis.lean), [DirichletSevenEighths.lean](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/lean/ComparatorChallenges/DirichletSevenEighths.lean), [HeckeSevenEighths.lean](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/lean/ComparatorChallenges/HeckeSevenEighths.lean)

## Version audited

The audit read openai/math at commit [`adc7f12`](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a) (2026-10-06 14:58 PT, the repository's initial public commit). Later commits up to [`1581d4c`](https://github.com/openai/math/commit/1581d4cbdd69a0faf34b2089614fe2a814316a6a) (2026-10-12 14:55 PT) did **not** change any audited file: `paper.tex`, `paper.pdf`, `lean/docs/003.md`, `Nonvanishing.lean` and the three comparator files have identical git blob hashes at `adc7f12`, `3014888` and `1581d4c` (checked 2026-10-13 via the GitHub API). Those later commits added other preprints, other Lean families and repository housekeeping.

## Scope and what's not covered

- **OpenAI's October 5, 2026 preprint** ([The-Quasi-Riemann-Hypothesis-October-5-2026](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/The-Quasi-Riemann-Hypothesis-October-5-2026)) is not covered. It is a separate manuscript that claims a weaker zero-free half-plane, Re(s) > 11/12, for Dirichlet and $\mathbb{Q}(\sqrt{-3})$ Hecke L-functions by its own argument. Nothing here should be read as a statement about it.
- **Lean:** we did not build or replay any Lean. The third-party replay we cite covers the zeta statement; one write-up reports the Hecke module was not built. The Dirichlet and Hecke formal statements are unverified by us.
- **Analytic estimates:** we checked the paper's own exponent accounting, not every intermediate inequality. The Stage 2 algebraic identity behind $49/440640$ was extracted, not re-derived; only the final comparison was checked numerically.
- **Not covered at all:** the Landau–Siegel application and the paper's later applications; the companion preprint *Uniform exclusion of Landau–Siegel zeros* (October 1, 2026); explicit constants.

## About this audit / method

This is a multi-agent, AI-assisted reconstruction led by data1493. AI agents (SuperGrok Heavy) read the public TeX source and Lean files, reconstructed the argument layer by layer, extracted the paper's loss ledgers, and evaluated the two critical constants numerically. Where these files say "specialist audit", that describes the depth of the reading of the exponent accounting, not the credentials of a human reviewer: **no professional number theorist has reviewed this work yet.** Every finding is limited to what can be read off the public sources, and every number quoted here was cross-checked against `paper.tex` at `adc7f12` (for example $46\epsilon_* < m_0/4 = 1/4800$, $3m_0/4 = 1/1600$, $m/2 = 1/4800$, $1021/25000$, $-E_* \ge 49/440640$, $-\tfrac{51}{64}\Delta$).

We invite specialist review, especially from people who work on large sieves, zero detection and zero-density estimates. If you find a lemma whose loss exceeds its budget, please open a [Specialist review finding](https://github.com/data1493/quasi-rh-audit/issues/new/choose) issue. A confirmed defect will be recorded at the top of this README.

## Notation

| Symbol | Meaning (as used in the paper) |
|---|---|
| $\beta_*$ | real part of the rightmost hypothetical zero (contradiction hypothesis) |
| $\Delta = \beta_* - 7/8$ | Stage 2 excess over the target abscissa ($\Delta_1$ is the Stage 1 analogue relative to $11/12$) |
| $\eta$ | target Hecke character |
| $C_{\mathrm{I}}(s)=s-2/3$, $C_{\mathrm{II}}(s)=s-11/16$ | affine exponents compared in Stage 1 and Stage 2 |
| $m_0=1/1200$ | minimum error-free saving on every major contribution (Stage 1) |
| $\epsilon_*=10^{-6}$ | unit loss requested for each listed loss class |
| $m=1/2400$ | saving actually used after losses; final Stage 1 saving is $m/2=1/4800$ |
| $\omega,\sigma$ | the low-side and high-side positive powers in the continuation criterion |
| $\delta$ | row-size exponent; $R(\delta)=\min\{1,\max(1-\delta/2,4/3-\delta)\}$ is the row-count envelope |
| $E_*$ | Stage 2 high-side exponent at the compensated endpoint; $-E_*\ge 49/440640$ |
| $T_1$, $A_\eta$, $\tau$ | height, height order and late-chosen height exponent in late-height closure |
| $\epsilon_{\rm total}$ | aggregate small loss in Stage 2, claimed arbitrarily small with target-independent coefficient |

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
| — | [CHANGELOG_wording.md](audit/CHANGELOG_wording.md) | Every wording change from the working drafts |
| — | [ABSTRACT.md](ABSTRACT.md) | 150–200 word abstract |
| — | [pdf/quasi-rh-audit.pdf](pdf/quasi-rh-audit.pdf) | Static PDF: master audit, loss table, residual-risk notes |
| — | [working-drafts/](working-drafts/) | Unreviewed raw drafts, kept for transparency (do not cite) |
| — | [x_thread.md](x_thread.md) | Draft announcement thread |

## How to cite

Cite the OpenAI preprint and Lean formalization above as the primary objects. To cite this audit, use [CITATION.cff](CITATION.cff) (GitHub's "Cite this repository" button) or:

> data1493. *External Audit of OpenAI's Quasi-Riemann Hypothesis Manuscript (Re(s) > 7/8): layer reconstruction, loss table and residual-risk notes.* October 2026. https://github.com/data1493/quasi-rh-audit

```bibtex
@misc{quasi_rh_external_audit_2026,
  author       = {data1493},
  title        = {External Audit of OpenAI's Quasi-Riemann Hypothesis Manuscript (Re(s) > 7/8)},
  year         = {2026},
  month        = oct,
  howpublished = {https://github.com/data1493/quasi-rh-audit},
  note         = {External audit of the existing manuscript (openai/math commit adc7f12); not an independent re-proof of the analytic estimates}
}
```

## License

All text in this repository is licensed under [CC BY 4.0](LICENSE). This repository contains no code or Lean of its own. The OpenAI preprint and Lean formalization are separate works under their own license (openai/math is Apache-2.0) and are not redistributed here.

## Working drafts

[`working-drafts/`](working-drafts/) holds the 19 raw markdown files as the workflow produced them, each with a banner. They are unreviewed and some wording overstates what was verified; the `audit/` versions are the citable record, and [CHANGELOG_wording.md](audit/CHANGELOG_wording.md) lists every change.
