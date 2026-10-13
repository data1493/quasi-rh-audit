> **Unreviewed working draft, kept for transparency.** Some wording in this file overstates what was verified (for example "independently machine-checked" or "the bound holds"). The citable record is the corresponding file in [`audit/`](../audit/); every wording change is listed in [`audit/CHANGELOG_wording.md`](../audit/CHANGELOG_wording.md).

# Quasi-Riemann Hypothesis Verification — Part 2
## Cubic-Theta Reflection Identities

**Status:** Structural analysis of the reflection step. Identity appears exact under stated conditions; quantitative bounds feed later large-sieve estimates.

### 2.1 Statement of the completed reflection

The core identity (Proposition on completed-reflection, with marked extension in a corollary) equates a smoothed Mellin transform of a completed cubic-theta sum \(T(s,\Psi)\) to a reflected sum over lattice points.

Direct side: sum over squarefree primary elements \(c, n \equiv 1 \pmod{3}\), character \(\Psi\) acting on the full index \(cn^3\), retaining zero extensions on nonunits. No coprimality between \(n\) and \(c\) is required; collisions are handled by masks.

Reflected side: sum over nonzero \(\mu \in \lambda^{-4}\mathcal{O}\) of cusp coefficients \(d(\mu)\), local factors \(B_p(\lambda^4\mu)\) depending on the valuation \(j_p \in \{0,\dots,5\}\) of active primes, a phase scalar \(\zeta\) with \(|\zeta| \le 1/81\), and the transformed test function \(V^\sharp(q_\mu X / q_c^2)\).

Local factors \(B_p\):
- For \(j_p \ne 0,4\): \(\chi_p(x)^{-j_p-2}\)
- For \(j_p = 4\): \(q_p^{-1/2}(-1 + q_p \mathbf{1}_{p\mid x})\)
- For \(j_p = 0\) and active: \(q_p^{-1/2}\chi_p(x)^{-2}\)

The scalar \(\zeta\) incorporates Gauss-sum phases \(\omega_{p,j_p}\), reciprocity, and the fixed ray character. Marked primes (for later compensation) are incorporated by expanding indicator factors \(1_{q\mid nb^3}\) and applying the base reflection to each term; inactive contributions recombine as \(q_q^{-1}\).

### 2.2 Exactness of the identity

The identity holds exactly for \(\operatorname{Re}(s) > 1\) by absolute convergence, with entire continuation of \(T(s,\Psi)\) and polynomial growth in vertical strips. Zero-on-nonunit restrictions are preserved by extending characters by zero rather than evaluating on nonunits. Shared primes between the squarefree and cube parts are removed by the last assertion of the proposition (no division by zero symbols). Fixed arithmetic data (moduli, ray groups, local prime sets) are independent of the smoothing parameter \(Z\) but may depend on the target character.

No hidden main term or incomplete cancellation is indicated in the construction. The reflection retains the full cubic factor in the index, which is necessary for the subsequent Poisson comparison.

### 2.3 Bounds on the transformed test function

The reflected test function \(V^\sharp\) satisfies
\[
|(x\partial_x)^j V^\sharp(x)| \ll_{A,j} \min\{x^{1/4},(1+x)^{-A}\} \mathfrak{M}_{A,\lceil 4A\rceil+j+2}(V)
\]
for seminorms \(\mathfrak{M}_{A,B}(V)\) controlled by integrals of \(V\) and its derivatives. Annular Fourier transforms of \(V^\sharp\) obey the same decay. These bounds are of the expected quality for applying large sieves and contour shifts later; they do not themselves produce the positive power margins.

### 2.4 Potential fragility points

1. **Dependence of fixed data on the target**. The sector modulus, local prime sets, and ray characters can depend on \(\eta\). This is permitted by the continuation criterion (only the power margins must be uniform). The risk is that the dependence introduces a factor that grows with the conductor and erodes the margin when the large sieve is applied. This must be tracked in the exponent ledgers of Parts 4–6.

2. **Marked-prime expansion**. Expanding the compensation indicators and reapplying the base reflection produces a finite sum of reflected series. Each term is of the same shape; the number of terms is controlled by the (fixed) number of slots. No uncontrolled proliferation is apparent.

3. **Local factor non-vanishing**. The factors \(B_p\) and the holomorphic corrections \(H_p\) must not introduce zeros that cancel the principal signal. The construction chooses the deleted set and the slot primes large enough to avoid this; the argument is standard but must be verified not to depend on height.

### 2.5 Condensed finding

The completed cubic-theta reflection identity is exact under the stated arithmetic conditions. It correctly retains zero-on-nonunit restrictions and produces a reflected series whose coefficients are of the form required for large-sieve bounds. The transformed test function has the expected decay. No structural defect in the reflection step has been identified. The identity supplies one side of the dual representation needed for the continuation criterion; the positive margins still originate in the quantitative large-sieve and moment estimates of later parts.

**Next:** Part 3 — Poisson summation and isolation of the principal \(1/L\) signal.
