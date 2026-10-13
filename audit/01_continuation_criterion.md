# Part 1 — Continuation Criterion and Dual-Representation Contradiction

**Status:** Structural analysis of the logical engine. No public disproof found; margins require quantitative verification in later parts.

## 1.1 What the criterion actually says

The paper reduces zero-freeness to a single comparison principle (Proposition / Lemma on continuation criterion). Assume for contradiction that the rightmost real part $\beta_*$ of zeros of the relevant L-functions (finite-order Hecke over $\mathbb{Q}(\sqrt{-3})$, then transferred) satisfies $\beta_* > \sigma_0$ for a fixed $\sigma_0 < 1$ (first $\sigma_0 = 11/12$, later $7/8$).

For each target character $\eta$, construct a normalized character sum $J_\eta(Z)$ that admits two representations:

- **Direct / reflected bound:** $|J_\eta(Z)| \ll_\eta Z^{C(\sigma_0) + \omega}$ for some $\omega > 0$.
- **Poisson / Mellin representation:** $J_\eta(Z) = f_\eta(Z) +$ error, where $f_\eta(Z)$ is essentially a Mellin transform of a holomorphic factor times $1/L_F^{\mathcal{S}}(s,\eta)$ (finitely many Euler factors deleted), and the error satisfies $|J_\eta(Z) - f_\eta(Z)| \ll_\eta Z^{C(\beta_*) - \sigma}$ for some $\sigma > 0$.

If both $\omega$ and $\sigma$ can be chosen **uniformly in $\eta$**, then $\epsilon_* = \min(\beta_* - \sigma_0 - \omega, \sigma) > 0$ is also uniform. This forces $1/L_F^{\mathcal{S}}(s,\eta)$ to continue holomorphically to $\operatorname{Re}(s) > \beta_* - \epsilon_*$, contradicting the existence of a zero at real part $\beta_*$.

The affine power is $C_{\mathrm{I}}(s) = s - 2/3$ for the first stage and $C_{\mathrm{II}}(s) = s - 11/16$ for the second. Deleted factors are nonzero for $\operatorname{Re}(s) > 0$; the principal pole at $s=1$ is excluded by construction.

## 1.2 Why this is the right engine

This is the classical “sum it two ways” strategy for zero-free regions, specialized to a fixed (non-shrinking) half-plane. The cubic-theta / Gauss-sum structure supplies the reflection representation that is controllable by large sieves; Poisson supplies the reciprocal. The positive uniform margins are what convert a classical shrinking zero-free region into a half-plane.

## 1.3 Potential fragility points specific to this criterion

1. **Uniformity of $\omega$ and $\sigma$**. The paper explicitly allows many constants, excluded sets $S$, and height thresholds to depend on $\eta$. Only the power margins themselves must be independent of $\eta$. If the large-sieve or moment bounds lose a factor that depends on the conductor of $\eta$ in a way that eats the margin, the half-plane collapses back to a shrinking region. This is the single most important quantitative claim and is not discharged by the Lean formalization alone.

2. **Holomorphic factor $H_\eta(s)$**. Must satisfy $|H_\eta(s) - 1| \le 1/2$ on the relevant half-plane so that it cannot cancel a zero of $L$. The construction of $H_\eta$ from local Euler factors and the compensation in Stage 2 must be checked not to introduce new zeros or poles inside the region.

3. **Deleted Euler factors $\mathcal{S}$**. Finite and independent of height, but can depend on $\eta$. Must remain non-vanishing for $\operatorname{Re}(s) > 0$. Standard, but the precise set arising from the cubic completion needs to be tracked.

4. **Identity theorem application**. Once the Mellin transform of $1/L$ is shown to have better than expected decay, analytic continuation follows. This step is standard once the power savings are in hand; the risk is upstream.

## 1.4 What must be verified for Part 1 to hold

- The existence of a character sum with the two exact representations (completed cubic-theta reflection vs. Poisson) is established in the arithmetic sections; this is structural and appears correctly set up.
- The continuation criterion itself is a standard implication. It holds *if* the two power-saving bounds are true with uniform margins.
- Therefore Part 1 reduces to: **do the estimates of Parts 2–3 actually produce $\omega, \sigma > 0$ independent of the target character?**

No logical gap in the criterion itself has been identified. The criterion is correctly formulated for producing a fixed half-plane. The burden of proof sits entirely in the quantitative estimates that feed it.

## 1.5 Condensed finding

The continuation criterion is the correct logical reduction for a fixed zero-free half-plane. It fires precisely when the dual representations of the completed cubic-theta sum produce uniform positive power savings. The criterion itself contains no identified flaw. Verification of the claim now depends on whether the large-sieve, reflected-energy, and moment estimates in the subsequent parts deliver those uniform margins.

**Next:** [Part 2](02_cubic_theta_reflection.md) — Stage 1 reflected bounds and principal signal extraction (the source of the first positive margin).

---

[← 00_master_audit.md](00_master_audit.md) · [Index](../README.md) · [02_cubic_theta_reflection.md →](02_cubic_theta_reflection.md)
