# Computational Check

*Critical constants feeding the margins (option 2)*

## Row envelope $R(\delta)$

The envelope used for residual row counts is
$$
R(\delta)=\min\bigl\{1,\ \max(1-\delta/2,\ 4/3-\delta)\bigr\}.
$$

Numerical evaluation confirms the claimed behavior:

- $R(\delta)=1$ for $\delta\le1/3$ (no saving)
- $R(\delta)<1$ strictly for $\delta>1/3$
- At the operating floor $\delta=1/50=0.02$, $R=1$ (handled by direct bounds)
- At intermediate values used in the paper ($\delta=0.4,0.5,0.7$): $R\approx0.933,0.833,0.65$

This matches the optimization that produces a positive high-side saving relative to the trivial count in the ranges required by both stages.

## Stage 2 endpoint certificate

The extracted algebraic identity yields the lower bound
$$
-E_*\ge\frac{49}{440640}\approx0.0001112>0.0001=\frac{1}{10000}.
$$

The inequality holds. The constant term alone already exceeds $1/10000$, so after the paper’s arbitrarily small $\epsilon_{\rm total}$ the remainder stays positive.

## Stage 1 budget arithmetic

With $\epsilon_*=10^{-6}$ and $m_0=1/1200$:

- $46\times10^{-6}=0.000046<1/4800\approx0.0002083$
- Retained after charged losses: $\ge3/4800=1/1600$
- Final claimed after late-height: $1/4800$

The arithmetic is consistent with the extracted ledger.

## Conclusion

Independent numerical checks of the two critical constants (the row envelope $R(\delta)$ and the Stage 2 endpoint lower bound $49/440640$) confirm the values that feed the positive margins. No discrepancy with the paper’s claimed numbers is found. The two critical constants match the paper under direct evaluation.

---

[← 16_stage2_compensation.md](16_stage2_compensation.md) · [Index](../README.md) · [18_expert_review_request.md →](18_expert_review_request.md)
