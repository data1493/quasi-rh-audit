# Specialized Sextic Large Sieve

**Status:** The lemma is a precise adaptation of the Blomer–Goldmakher–Louvel norm recursion. The $(KD)^{2/3}$ term appears correctly derived under the stated conventions. No arithmetic defect is visible in the extracted argument.

## Precise statement

**Lemma (sextic large sieve).** For squarefree ideals outside a fixed finite set $S$, and every $\epsilon>0$,
$$
\sum_{\substack{k\,\mathrm{sf}\\q_k\le K}}\Bigl|\sum_{\substack{n\,\mathrm{sf}\\q_n\le D}}c_n\chi_n(k)^\varsigma\Bigr|^2
\ll_{S,\epsilon}(KD)^\epsilon\bigl\{K+D+(KD)^{2/3}\bigr\}\sum|c_n|^2,
$$
where $\varsigma\in\{\pm1\}$ and symbols are zero on nonunits. Fixed restrictions on rows or coefficients are allowed.

## Norm-recursion that produces the $2/3$

The proof follows the Blomer–Goldmakher–Louvel recursion, specialized to the sextic setting:

1. **Paired summation.** For coprime squarefree $b,c$ with matching type, form ray characters and Gauss sums via sextic reciprocity. Poisson summation on the pair produces a dual length.
2. **Recursion via gcd and shells.** Möbius inversion over the gcd and residue classes yields a recursive bound relating the energy at scale $(M,N)$ to smaller scales. The powers that appear are closed under $j\mapsto 2j\bmod 6$ (the set $\{1,2,4\}$).
3. **Power decomposition.** Write the evaluation ideal as $a=a_1a_2^2\cdots a_6^6$. The inductive hypothesis with exponent $\alpha>4/3$ produces a recurrence that decreases $\alpha$ until it stabilizes at $4/3$.
4. **Dyadic subdivision.** The bound is transferred to dyadic balls; symmetry and transposition give the final form.

The cross term $(KD)^{2/3}$ is the stable value of the recursion. Intermediate losses are absorbed into the $(KD)^\epsilon$ factor.

## Conditions that must hold

- Ideals primary and squarefree outside the fixed set $S$.
- Valuations of residual rows at most 5 (sixth-power-free).
- Zero extension on nonunits preserved throughout.
- Primary-generator convention used for the reciprocity phases.

These match the conventions used elsewhere in the paper for the reflected and Poisson rows.

## How it feeds the envelope

When the sieve is applied to the squarefree factor of residual rows in a bin with parameter $\delta=2a-1$, the resulting count is bounded by $U^{R(\delta)+\epsilon}$ where
$$
R(\delta)=\min\bigl\{1,\max(1-\delta/2,4/3-\delta)\bigr\}.
$$
The $2/3$ term is what forces $R(\delta)<1$ for $\delta>1/3$, supplying the high-side saving.

## Residual risk assessment

No arithmetic error or missing loss is visible in the extracted recursion. The exponent $2/3$ is the expected output of the BGL-style induction under the mod-6 closure. The only remaining way this lemma fails to deliver the margin is if an intermediate step in the full write-up introduces an extra factor that is not absorbed into $\epsilon$. Within the extracted argument, no defect in the claimed bound is visible.

**ROI status:** Highest-leverage novel step survives extraction. The source of the positive margins is intact under the stated conventions.

---

[← 13_late_height_closure.md](13_late_height_closure.md) · [Index](../README.md) · [15_detector_saturation.md →](15_detector_saturation.md)
