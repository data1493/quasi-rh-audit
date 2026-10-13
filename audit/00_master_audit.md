# External Multi-Agent Audit of the OpenAI Quasi-Riemann Hypothesis Manuscript

**Date:** 2026-10-13  
**Method:** Layer-by-layer reconstruction and stress-test using an AI-assisted multi-agent workflow (SuperGrok Heavy), led by data1493, reading the public TeX source and Lean formalization (openai/math commit `adc7f12`). No human specialist has yet reviewed these findings.

## Claims (precise scope)

1. The logical architecture of the proof is coherent at every examined layer.
2. The paper’s own exponent ledgers for the modest positive margins (Stage 1 $1/4800$, Stage 2 endpoint $49/440640$) close with a positive remainder under the losses they explicitly charge.
3. The Lean formalization of the final theorems aligns with the claimed statements; the final theorems are machine-checked, and an independent third-party kernel replay has been reported (see Part 9).
4. No structural gap or disproof has been identified.

**What this is not:** A complete independent proof of the analytic estimates. The residual risk is quantitative and localized to the possibility of an unlisted loss in an intermediate lemma.

## Architecture (Parts 1–9)

| Part | Layer | Finding |
|------|-------|---------|
| 1 | Continuation criterion | Dual representations produce contradiction if zero lies too far right. No structural gap found at this layer. |
| 2 | Cubic-theta reflection | Exact under stated conditions; retains zero-on-nonunit restrictions. |
| 3 | Poisson & principal signal | Principal $1/L$ Mellin signal cleanly isolated. |
| 4 | Large sieve & row energy | Specialized sextic sieve + envelope $R(\delta)$ supply the positive margins. |
| 5 | Zero detector & moments | Saturation forces inverse witness dominant; feeds the envelope. |
| 6 | Stage 1 assembly (11/12) | Balanced scales, $C(s)=s-2/3$, margin $1/4800$ under stated accounting. |
| 7 | Stage 2 refinement (7/8) | Compensation + asymmetric scales, endpoint positive. |
| 8 | Uniformity & transfer | Margins independent of target; quadratic factorization transfers to Dirichlet $L$-functions. |
| 9 | Lean alignment | Final theorems formalized and kernel-checked; third-party replay reported. |

## Specialist quantitative audit

**Stage 1 high-side saving**

- Reserved: $m_0=1/1200$, $\epsilon_*=10^{-6}$, $m=1/2400$.
- Central losses: $46\epsilon_*<1/4800$.
- Principal and small-row losses each $<m_0/4$.
- After fixed scalar and late-height closure: claimed remainder $1/4800$.
- Status: table closes with positive remainder under charged losses.

**Stage 2 endpoint certificate**

- Algebraic identity yields $-E_*\ge49/440640>1/10000$.
- Additional losses charged to reserved fraction of high-side margin or arbitrarily small $\epsilon_{\rm total}$.
- Status: remainder positive for every $\Delta=\beta_*-7/8>0$.

**Computational confirmation**

- Row envelope $R(\delta)=\min\{1,\max(1-\delta/2,4/3-\delta)\}$ evaluated; strict saving for $\delta>1/3$.
- Endpoint constant $49/440640\approx0.0001112>1/10000$ checked arithmetically (the algebraic identity behind it was not re-derived).

## Logical hinge (prose outline)

*No Lean skeleton was built for this audit; this is a prose outline of how the formal statements line up with the hinge.* The continuation criterion has been isolated as a pure logical implication: dual bounds with uniform positive powers imply holomorphic continuation of $1/L$ past the supposed rightmost zero. The concrete margins appear as explicit constants. The analytic estimates that discharge the implication remain in the prose.

## Residual risk

The margins are small. Within the extracted text, they survive every loss the paper explicitly charges and that the computational constants match. The residual risk is the existence of an unlisted intermediate loss larger than the reserved budget. Full certification requires specialist verification of every lemma that feeds the ledger, or formalization of those steps.

## Conclusion

The manuscript survives structural scrutiny, Lean alignment, and specialist audit of its own exponent accounting. No disproof has been found. The quantitative hinge is localized and, under the stated accounting, closes with a positive remainder. The paper’s own accounting is internally consistent under its methods; the result has not been independently re-proved from first principles.

## Artifacts

- [01_continuation_criterion.md](01_continuation_criterion.md) – [09_lean_alignment.md](09_lean_alignment.md)
- [10_specialist_margins.md](10_specialist_margins.md)
- [11_loss_table.md](11_loss_table.md)
- [17_computational_check.md](17_computational_check.md)
- This document

---

[Index](../README.md) · [01_continuation_criterion.md →](01_continuation_criterion.md)
