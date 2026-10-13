# Part 4 — Large Sieve and Row Energy Bounds

**Status:** Quantitative analysis of the primary source of positive power margins. The specialized sextic sieve and row envelope produce savings in the operating ranges; residual risk is in the exact accounting of ε-losses against small margins.

## 4.1 Key large-sieve statements

**Quadratic large sieve** (Goldmakher–Louvel style, applied to completed indices):  
$$
\sum_{q_k\le K}\Bigl|\sum_{q_n\le N} c_n\chi_k(n)^3\Bigr|^2\ll_\epsilon(KN)^\epsilon(K+N)\sum|c_n|^2.
$$

**Planar additive large sieve**: mean-square over reduced fractions in $\mathbb{C}/\mathcal{O}$ controlled by separation and mass, yielding an additive factor $\ll(Q+\delta^{-2})$ times coefficient mass.

**Specialized sextic large sieve** (Lemma on sextic specialization): for squarefree ideals outside a fixed set $S$,
$$
\sum_{\substack{k\,\mathrm{sf}\\q_k\le K}}\Bigl|\sum_{\substack{n\,\mathrm{sf}\\q_n\le D}}c_n\chi_n(k)^\varsigma\Bigr|^2\ll_{S,\epsilon}(KD)^\epsilon\bigl\{K+D+(KD)^{2/3}\bigr\}\sum|c_n|^2,
$$
with $\varsigma\in\{\pm1\}$. The $2/3$ cross term arises from a norm-recursion on valuations modulo 6 (powers closed under $j\mapsto 2j\bmod 6$, paired residue characters, primary-generator convention). This is the technical heart of the residual-row control.

## 4.2 Row-counting envelope

For intermediate rows in a bin with parameter $\delta=2a-1$ ($1/50<\delta\le1$), the number of physical rows satisfies
$$
\#\mathcal{B}\ll U^{R(\delta)+\epsilon}(1+T_1)^A,
$$
where
$$
R(\delta)=\min\bigl\{1,\max(1-\delta/2,\,4/3-\delta)\bigr\}
=
\begin{cases}
1 & 0\le\delta\le1/3,\\
4/3-\delta & 1/3\le\delta\le2/3,\\
1-\delta/2 & 2/3\le\delta\le1.
\end{cases}
$$
The envelope is strictly less than the trivial count precisely when $\delta>1/3$. Combined with the zero-detector witnesses (saturated inverse and plain polynomials), this produces the high-side saving relative to the target exponent $C(\beta_*)$.

## 4.3 How the margins arise (Stage 1 parameters)

For the balanced Stage 1 scales $\asymp Z^{1/2}$ and $C_{\mathrm{I}}(s)=s-2/3$:

- Direct (reflected) side: Cauchy–Schwarz + quadratic + planar additive large sieve yields $|J|\ll Z^{1+\epsilon}$, which is $Z^{C(11/12)+\omega}$ with room ($C(11/12)=1/4$).
- Poisson side: the sextic sieve + envelope $R(\delta)$ on intermediate rows, plus direct bounds on small/large ranges, produces a remainder smaller than the principal signal by a positive power. Extracted calculations show a raw saving on the order of $1/4800$ after intermediate losses; the paper asserts this remains positive after all contour tails and height factors.

The operating range $\delta\ge1/50$ keeps $R(\delta)$ and the hybrid exponents strictly below the threshold required by the continuation criterion. The saving collapses only outside the paper’s declared ranges.

## 4.4 Potential fragility points

1. **Sextic recursion**. The norm-recursion (valuations cycling modulo 6, paired characters) is a precise adaptation of existing large-sieve technology. An error in the recursion or in the primary-generator convention would be the most likely place for a quantitative failure. No such error is visible in the stated lemma, but the ledger must be checked.

2. **Size of the margin**. The final positive powers are small (order $10^{-3}$–$10^{-4}$ in the extracted Stage 1 calculations). This is workable if every $\epsilon$-loss, contour tail, and height factor is strictly smaller than the margin, but it leaves little room for an under-accounted logarithmic factor or incomplete uniformity.

3. **Uniformity**. Fixed arithmetic data ($S$, ray characters, frozen sets) and the sixth-power-free condition keep the bounds independent of the target character’s conductor. No conductor-dependent growth appears in the sieve statements. The risk remains that an intermediate step introduces a factor depending on the conductor that is absorbed into an $\epsilon$ but actually grows slowly enough to eat the small margin.

## 4.5 Condensed finding

The specialized sextic large sieve and the row envelope $R(\delta)$ supply the positive power margins required by the continuation criterion in the operating ranges used for both stages. No structural gap or vanishing of the saving is identified. The argument survives this layer. Residual risk is a computational error in the sextic recursion or an under-accounted loss that exceeds the (modest) claimed margin. Quantitative verification of the exact exponent ledgers remains the open specialist task.

**Next:** [Part 5](05_zero_detector_moments.md) — Zero detector and moment estimates (how the witnesses and inductions feed the envelope).

---

[← 03_poisson_principal_signal.md](03_poisson_principal_signal.md) · [Index](../README.md) · [05_zero_detector_moments.md →](05_zero_detector_moments.md)
