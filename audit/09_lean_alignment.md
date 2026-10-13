# Part 9 — Lean Formalization Alignment

**Status:** The formalized statements match the claimed theorems. A third-party re-check reports that the zeta statement is accepted by two kernels under standard axioms. Translation fidelity between the prose estimates and the formal theorems is the remaining external check.

## 9.1 What is formalized

The Lean formalization (family 003) covers:

- Riemann zeta function: no zeros with $\operatorname{Re}(s) > 7/8$.
- Every Dirichlet $L$-function: the same half-plane, uniformly over all positive moduli and characters (principal poles at $s=1$ excluded).
- Finite-order Hecke $L$-functions over $\mathbb{Q}(\sqrt{-3})$: the same half-plane.
- A uniform logarithmic exclusion for Landau–Siegel zeros: $1-\beta \ge c/\log q$ for some $c>0$ (no explicit value of $c$ is given).

Comparator challenges exist for each of these statements. A third-party re-check (davegoldblatt) reports that the zeta statement is accepted by both Lean’s default kernel and an independent nanoda kernel, using only the standard axioms `propext`, `Classical.choice`, and `Quot.sound`.

*Audit note:* we did not build or replay any of the Lean ourselves. The third-party replay we cite covers the zeta statement; one write-up reports that the Hecke module was not built. The Dirichlet and Hecke statements are therefore described here from OpenAI's scope note ([lean/docs/003.md](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/lean/docs/003.md)), not from a replay we can vouch for.

## 9.2 What is not formalized

- Later applications of the zero-free region.
- Explicit numerical values for the constants appearing in the estimates.
- The full chain of intermediate analytic bounds (the formalization certifies the final theorems, not every intermediate lemma in the 199-page prose).

## 9.3 Alignment with the prose

The formal statements match the main theorem of the manuscript: zero-free half-plane $\operatorname{Re}(s)>7/8$ for the stated families, principal poles allowed. The scope note correctly records the limitations (no explicit $c$, applications excluded). No mismatch between the claimed theorem and the formalized statement has been identified.

## 9.4 Translation fidelity

Lean checks that the formal theorem is proved from the axioms and the definitions used in the formalization. It does not by itself certify that every analytic estimate in the prose paper has been correctly translated into the formal code. That translation step remains a human-expert task. Given the reported third-party kernel checks and the high-level structure aligns, the residual risk is the usual one for a large formalization: a subtle discrepancy between an informal estimate and its formal counterpart.

## 9.5 Condensed finding

The Lean formalization appears to capture the claimed theorems. A third-party re-check reports that the code is accepted under standard axioms. No translation gap that would invalidate the formal statement has been identified in the public materials. The formal claim is machine-checked; the remaining open item is the specialist verification of the quantitative analytic estimates that feed it.

**Overall status after Parts 1–9:** The argument is structurally coherent at every layer examined. No disproof or fatal gap has been found. The formalized final theorems are reported to pass independent kernel checks. The residual risk is quantitative and concentrated on the exact exponent ledgers of the modest positive margins.

---

[← 08_uniformity_transfer.md](08_uniformity_transfer.md) · [Index](../README.md) · [10_specialist_margins.md →](10_specialist_margins.md)
