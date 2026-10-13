# Stage 2 Compensation Local Identities

**Status:** The two-term cancellation is an exact local identity under the stated conventions. No residual main term that depends on the target conductor is introduced.

## Precise local identity

The compensation is realized by the holomorphic correction
$$
G_p=\frac{(\overline{\eta(p)}Q^x-Q^{-w})(1-V)(1-W)P_p^*-Q^{-w}(1-VW)}{1-D},
$$
which satisfies the exact identity
$$
\overline{\eta(p)}Q^{x+z-1}P_p^*-Q^{z-w-1}P_p=\frac{1-D}{(1-V)(1-W)}Q^{z-1}G_p
$$
on the raw-quotient locus in the Euler regions (where the denominators are nonzero).

Equivalently, after normalization one has the two-term form
$$
G_p+v^{-1}H_p=\frac{(1-V)(1-W)}{1-D}\Bigl[(v^{-1}-Q^{-w})\Bigl\{\frac{V}{1-V}-D\Bigr\}+(\overline{\eta(p)}Q^x+v^{-1}-Q^{-w})\mathcal{E}_p\Bigr],
$$
where the constants are arranged so that the unwanted Euler contribution cancels identically when $p\nmid u$.

## Conditions for exactness

- Denominators $1-R$, $1-V$, and $1-D$ nonzero in the Euler regions (ensured by the region parameters and a finite enlargement of the deleted set).
- Slot supports disjoint.
- Zero extension on nonunits preserved.
- Primary-generator convention used for the reciprocity phases.

Under these conditions the scalar prime contribution is removed and the sextic-character factor needed for the moments is retained.

## Residual factors

The only residual factor after cancellation is the holomorphic correction $\mathcal{H}_{\eta,u}$, which satisfies
$$
\mathcal{H}_{\eta,u}\ll_\epsilon q_u^\epsilon
$$
uniformly, and for the principal row $u=1$
$$
\mathcal{H}_{\eta,1}=1+O(P_0^{-c_H})
$$
with $c_H>0$ fixed. No additional factor that grows with the conductor of the target appears in the local identity itself.

## Residual risk assessment

The cancellation is an algebraic identity of local Euler factors, exact on the stated locus. The only way this step fails is if an intermediate expansion in the full write-up leaves an uncancelled main term that depends on the target. Within the extracted identities, the cancellation is clean and the residual is the standard holomorphic correction already accounted for in the earlier parts.

**ROI status:** Stage 2 compensation local identities survive extraction. The two-term cancellation is exact under the stated conventions and introduces no conductor-dependent main term.

## Final residual-risk status

All items on the short residual-risk list have now been extracted:

- Specialized sextic large sieve: extracted, no defect visible
- Stage 1 central loss accounting: extracted, no defect visible
- Late-height closure: extracted, no defect visible
- Zero-detector saturation: extracted, no defect visible
- Stage 2 compensation local identities: extracted, no defect visible
- Stage 2 endpoint certificate: constant computationally confirmed

No unlisted loss that exceeds the reserved budgets is visible in any of the extracted arguments. The quantitative hinge survives this extraction-level residual-risk review under the paper’s stated accounting; it does not replace a specialist reading of every intermediate lemma.

---

[← 15_detector_saturation.md](15_detector_saturation.md) · [Index](../README.md) · [17_computational_check.md →](17_computational_check.md)
