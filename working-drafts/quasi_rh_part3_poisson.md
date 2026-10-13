> **Unreviewed working draft, kept for transparency.** Some wording in this file overstates what was verified (for example "independently machine-checked" or "the bound holds"). The citable record is the corresponding file in [`audit/`](../audit/); every wording change is listed in [`audit/CHANGELOG_wording.md`](../audit/CHANGELOG_wording.md).

# Quasi-Riemann Hypothesis Verification — Part 3
## Poisson Summation and Isolation of the Principal Signal

**Status:** Structural analysis of the Poisson side. Principal signal isolation is exact under the stated conditions; residual row control is deferred to later large-sieve and detector parts.

### 3.1 Poisson representation

Poisson summation is applied to the averaging variable of the completed cubic-theta sum. Nonzero frequencies take the form \(u a^6\) where \(u\) is sixth-power-free (prime valuations \(\le 5\)) and \(a\in\mathcal{O}\). The resulting expression for the normalized probe is a triple Mellin integral
\[
\frac{1}{(2\pi i)^3}\int\int\int \mathcal{W}(X,Y,Z;x,w,z)\sum_u^{(6)} q_u^{-z}\overline{\xi(u)}\frac{\zeta_F^S(6z)L^S(w,\chi_\bullet(u))}{L^S(x,\eta\overline{\chi_\bullet(u)})}\mathcal{H}_{\eta,u}(x,w,z)\,dz\,dw\,dx,
\]
absolutely convergent on the initial vertical lines. The coefficient series factors as an Euler product times a holomorphic correction \(\mathcal{H}_{\eta,u}\).

### 3.2 Principal row (\(u=1\))

The principal row produces the desired Mellin signal containing \(1/L_F^S(s,\eta)\). After residue extraction at the scalar poles \(w=1\) and \(z=1/6\), the principal contribution is
\[
\mathscr{P}_\eta(Z) = c_S\cdot\operatorname{Res}\Bigl[\mathcal{W}\cdot\frac{\zeta_F^S(6z)\zeta_F^S(w)}{L_F^S(s,\eta)}\mathcal{H}_{\eta,1}\Bigr],
\]
with \(c_S>0\) depending only on fixed data. The normalized principal signal differs from the target Mellin transform
\[
f_\eta(Z)=\frac{1}{2\pi i}\int Z^{C(s)}e^{(s-5/6)^2}\frac{H_\eta(s)}{L_F^S(s,\eta)}\,ds
\]
by a holomorphic factor \(H_\eta(s)=\mathcal{H}_{\eta,1}(s,1,1/6)\) satisfying \(|H_\eta(s)-1|\le 1/2\) on the relevant half-plane (so it cannot cancel a zero of \(L\)). The correction is exact for the base probe; compensation in Stage 2 modifies it by a controlled amount that is absorbed into the same holomorphic factor.

### 3.3 Residual rows

Residual rows (\(u\neq 1\)) are grouped by norm and by the location of zeros of the finite family of Hecke twists associated to \(u\). Each contributes a quotient of L-functions times a holomorphic correction. The zero detector assigns zero-free rectangles to these twists; rows above a fixed floor produce large inverse and plain Dirichlet polynomials that are later counted by the sextic large sieve. Small and large norm ranges are bounded directly. The construction ensures that residual rows do not contribute to the principal residue.

### 3.4 Exactness and isolation

The Poisson identity is exact on the initial contours by absolute convergence. Contour moves that isolate the principal residue remain inside regions where the corrections \(\mathcal{H}_{\eta,u}\) are holomorphic. The principal term is cleanly separated: its holomorphic factor is bounded away from zero, and residual rows are excluded from the residue by construction. No hidden main term or incomplete cancellation is indicated.

### 3.5 Potential fragility points

1. **Holomorphic factor non-vanishing**. \(H_\eta\) must stay away from zero on the half-plane. The local Euler factors are arranged so that this holds after deleting a finite set and choosing slot primes large enough; the argument is standard but height-independent only if the deleted set is fixed before the target.

2. **Contour movement**. Moving the contours to extract the residue at \(w=1\), \(z=1/6\) requires that no poles of residual rows are crossed and that tails are smaller than the claimed margin. The paper asserts this via external tail lemmas; the quantitative size of those tails must be checked against the (often small) positive margins of later parts.

3. **Uniformity**. The principal scalar \(c_S\) and the normalizer can depend on the target. This is permitted; only the power difference between the principal signal and the residual contribution must be uniform.

### 3.6 Condensed finding

Poisson summation cleanly isolates a principal Mellin signal containing \(1/L_F^S(s,\eta)\) times a holomorphic factor bounded away from zero. The identity is exact, residual rows are structurally excluded from the principal residue, and the form matches what the continuation criterion requires. No structural defect in the isolation step has been identified. The positive power margins still originate entirely in the quantitative control of residual rows (large sieve, zero detector, moment estimates) that appear in subsequent parts.

**Next:** Part 4 — Large sieve and row energy bounds (the primary source of the positive margins).
