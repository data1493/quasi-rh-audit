# Part 6 — Stage 1 Assembly to 11/12

**Status:** Assembly of the dual representations under balanced scales. The exponent matching is correct and the claimed margins are positive but extremely small; residual risk is whether every intermediate loss is strictly inside the reserved budget.

## 6.1 Geometry and the choice of $C(s)$

Stage 1 uses balanced scales $X=Y=Z^{1/2}$. The affine power is
$$
C_{\mathrm{I}}(s)=s-\frac23.
$$
At the boundary this gives
$$
C_{\mathrm{I}}\Bigl(\frac{11}{12}\Bigr)=\frac14.
$$
The geometry is chosen so that the natural output of the reflected large-sieve bound sits exactly at this threshold.

## 6.2 Low bound (reflected side)

Cauchy–Schwarz combined with the quadratic large sieve and the planar additive large sieve on the reflected rows produces
$$

|J_{\mathrm{I},\eta}(Z)|\ll_\eta Z^{1+\epsilon}.
$$
Relative to $C_{\mathrm{I}}(11/12)=1/4$ this leaves room for a positive $\omega$ independent of the target. The bound holds uniformly once the fixed arithmetic data are chosen.

## 6.3 High-side remainder (Poisson side)

After the zero detector and the specialized sextic sieve have controlled the residual rows, the difference between the normalized sum and the principal Mellin signal satisfies
$$

|J_{\mathrm{I},\eta}(Z)-f_{\mathrm{I},\eta}(Z)|\ll_\eta Z^{C_{\mathrm{I}}(\beta_*)-\sigma}
$$
for a positive $\sigma$. Extracted ledger items include:

- intermediate-row envelope saving on the order of $1021/25000\approx0.041$,
- principal $w$-residue remainder $\sim1/40$,
- principal $z$-residue remainder $\sim1/1200$,
- small-row and large-row contributions that save more.

The smallest of these is of size $1/1200$. After a common budget for $\epsilon$-losses, dyadic partitions, and contour tails, a residual high-side saving on the order of $1/4800$ remains. Late-height closure (Lemma) chooses the height exponent $\tau$ and the external order $N$ after the target so that the factor $(1+T_1)^{A_\eta}$ is absorbed into half the margin.

## 6.4 Uniformity

All reserved positive powers are fixed before the target character. Constants, excluded sets, and height thresholds may depend on $\eta$; the power margins themselves do not. The assembly therefore satisfies the hypotheses of the continuation criterion at $\sigma_0=11/12$.

## 6.5 Potential fragility points

1. **Size of the margin**. The final claimed saving is extremely small ($\sim1/4800$). Every intermediate $\epsilon$-loss, contour tail, and height factor must be strictly smaller than this number. An under-accounted logarithmic factor or a slightly larger height order can erase it.

2. **Late-height closure**. The ordering that chooses $\tau$ after $A_\eta$ is essential. If any height-dependent quantity is fixed before $\tau$ is chosen, the absorption fails.

3. **Ledger completeness**. The paper asserts that after all listed losses the remainder is still positive. Full verification requires checking that every loss appearing in the intermediate lemmas has been charged against the budget.

## 6.6 Condensed finding

Stage 1 correctly assembles the dual representations into the continuation criterion at $\sigma_0=11/12$. The exponent matching $C(11/12)=1/4$ is exact, and the claimed margins are positive under the stated parameter ordering. No structural gap is identified. The residual risk is quantitative and concentrated on whether the precise numerical ledger of all losses remains strictly inside the tiny reserved margin of order $1/4800$. The argument survives this layer pending that verification.

**Next:** [Part 7](07_stage2_refinement_7_8.md) — Stage 2 refinement to $7/8$ (compensation, asymmetric scales, and the tighter margin).

---

[← 05_zero_detector_moments.md](05_zero_detector_moments.md) · [Index](../README.md) · [07_stage2_refinement_7_8.md →](07_stage2_refinement_7_8.md)
