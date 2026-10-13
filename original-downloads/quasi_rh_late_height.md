# Late-Height Closure

**Status:** The parameter ordering is free of circularity. Choosing \(\tau\) and \(N\) after the target absorbs the height factor into half the reserved margin.

## Precise statement

**Lemma (late-height closure).** Suppose all real parameters and finite structural choices are fixed independently of the target \(\eta\), and there exist \(m>0\) and \(0<\omega<\Delta_0\) such that
\[
|J_\eta(Z)|\ll_\eta Z^{C(\sigma_0)+\omega}.
\]
After a finite sum of estimates one has, for every integer \(N\ge0\),
\[
|J_\eta(Z)-f_\eta(Z)|\ll_{\eta,N}Z^{C(\beta_*)-m}(1+T_1)^{A_\eta}+Z^{B_\eta}T_1^{-N},
\]
where \(A_\eta\ge0\) and \(B_\eta\) are finite and independent of \(N\). Suppose further that there exists \(\tau_{0,\eta}>0\), fixed after the real choices and the finite profile orders but before \(N\) and \(Z\), such that the estimate holds whenever \(T_1=Z^\tau\) and \(0<\tau\le\min\{d_{\min}/100,\tau_{0,\eta}\}\).

Then \(\tau\) and \(N\) may be chosen after \(\eta\) so that
\[
|J_\eta(Z)-f_\eta(Z)|\ll_\eta Z^{C(\beta_*)-m/2}.
\]
The resulting saving is \(\sigma=m/2\).

## Parameter ordering

1. All real losses, geometry, and finite structural choices are fixed before the target.
2. The height order \(A_\eta\) and the ceiling \(\tau_{0,\eta}\) are fixed after the target’s profile orders but before the external order \(N\) and the final \(Z\).
3. \(\tau\) is then chosen small enough that \((1+T_1)^{A_\eta}\) is absorbed into half the reserved margin \(m\).
4. \(N\) is chosen large enough that the external tail \(Z^{B_\eta}T_1^{-N}\) is smaller than the same half-margin.
5. Increasing \(N\) changes only external test seminorms; it does not alter \(A_\eta\) or any pre-fixed real power.

## Circularity check

- \(m\) and \(\omega\) are fixed before the target.
- \(A_\eta\) is determined by the (finite) profile orders of the target and does not depend on \(\tau\) or \(N\).
- \(\tau\) and \(N\) are chosen after both, so the absorption is a pure numerical comparison once \(A_\eta\) is known.
- The functions \(J_\eta\) and \(f_\eta\) themselves do not contain \(T_1\), so the exponent assertion is unaffected by the late choice.

No circular dependence is present.

## Residual risk assessment

The lemma does exactly what is claimed: it converts a height-dependent bound into a pure power saving after the target is fixed. The ordering prevents circularity. The only way this step fails is if an intermediate estimate that produces \(A_\eta\) itself depends on a height that has not yet been closed; within the extracted statement, the ordering is respected.

**ROI status:** Late-height closure survives extraction. The absorption of the height factor is correctly ordered and free of circularity.
