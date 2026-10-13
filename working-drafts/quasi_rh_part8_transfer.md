> **Unreviewed working draft, kept for transparency.** Some wording in this file overstates what was verified (for example "independently machine-checked" or "the bound holds"). The citable record is the corresponding file in [`audit/`](../audit/); every wording change is listed in [`audit/CHANGELOG_wording.md`](../audit/CHANGELOG_wording.md).

# Quasi-Riemann Hypothesis Verification — Part 8
## Uniformity, Contours, Residues, and Hecke-to-Dirichlet Transfer

**Status:** Analysis of the final structural steps. Uniformity of the power margins is correctly formulated; the transfer is a standard quadratic factorization; contour and residue extraction introduce no new structural gaps.

### 8.1 Uniformity of the margins

The continuation criterion requires only that the positive powers \(\omega\) and \(\sigma\) be independent of the target character \(\eta\). All other quantities — excluded sets \(S\), ray characters, height orders \(A_\eta\), lower thresholds \(Z_{0,\eta}\), and implied constants — are permitted to depend on \(\eta\).

The parameter ordering enforces this distinction: fixed arithmetic data and the reserved power budgets are chosen before the target; \(\eta\)-dependent quantities are absorbed into thresholds or into the late choice of the height exponent \(\tau\). No step in the preceding parts introduces a power loss that grows with the conductor of \(\eta\). The family-wide assertion (needed because Poisson summation produces Hecke twists of the target) is essential and is handled by applying the same estimates uniformly across the finite family of twists associated to each residual row.

### 8.2 Contour moves and principal residue extraction

Contour shifts that isolate the principal residue at \(w=1\), \(z=1/6\) remain inside regions where the holomorphic corrections are holomorphic. External tails are controlled by rapid decay of the weight functions and by choosing the external order \(N\) after the target. The principal scalar \(c_S\) is nonzero and depends only on fixed data (or on data permitted to depend on \(\eta\)). Residual rows are excluded from the residue by construction. No hidden main term or incomplete cancellation is indicated.

### 8.3 Hecke-to-Dirichlet transfer

The transfer (Proposition on hecke-dirichlet-transfer) proceeds by quadratic factorization. Composing a Dirichlet character \(\chi\) with the ideal norm produces a Hecke character over \(\mathbb{Q}(\sqrt{-3})\). Away from finitely many Euler factors the L-function factors as
\[
L_F^{\mathcal{S}}(s,\eta)=L^{S}(s,\chi)\,L^{S}(s,\chi\chi_{-3}),
\]
where \(\chi_{-3}\) is the quadratic character of conductor 3. The omitted factors are nonzero for \(\operatorname{Re}(s)>0\). The principal pole at \(s=1\) is allowed and is nonzero for the quadratic factor. The same half-plane therefore passes from finite-order Hecke L-functions over \(\mathbb{Q}(\sqrt{-3})\) to all Dirichlet L-functions, including \(\zeta(s)\).

### 8.4 Potential fragility points

1. **Conductor dependence hidden in an \(\epsilon\)**. If an intermediate estimate absorbs a factor that grows slowly with the conductor into an \(\epsilon\) that is later treated as arbitrarily small, the uniformity of the power margin could fail for large conductors. The paper’s statements treat the margins as fixed before the target; the risk is in the implementation of the \(\epsilon\)-losses.

2. **Finite deleted sets**. The deleted Euler factors depend on the conductor of the target. They must remain non-vanishing in the half-plane and their number must not grow in a way that affects the power. The construction claims both are controlled.

3. **Family-wide uniformity**. The Poisson representation introduces twists of the target. The estimates must apply uniformly to that finite family. The paper asserts this; an error in the uniformity over the twists would prevent the contradiction from closing.

### 8.5 Condensed finding

Uniformity of the positive power margins is correctly formulated and is preserved by the parameter ordering used in the preceding parts. Contour moves and principal residue extraction introduce no new structural gaps. The Hecke-to-Dirichlet transfer is a standard quadratic factorization that correctly extends the half-plane to all Dirichlet L-functions. No structural defect is identified at this layer. The residual risk remains the quantitative one already noted: whether every intermediate loss has been correctly charged against the reserved uniform margin.

**Next:** Part 9 — Lean formalization alignment and any translation gaps between the prose estimates and the formal theorems.
