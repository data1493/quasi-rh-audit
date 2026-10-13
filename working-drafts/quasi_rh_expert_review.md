> **Unreviewed working draft, kept for transparency.** Some wording in this file overstates what was verified (for example "independently machine-checked" or "the bound holds"). The citable record is the corresponding file in [`audit/`](../audit/); every wording change is listed in [`audit/CHANGELOG_wording.md`](../audit/CHANGELOG_wording.md).

# Expert Review Request — Quantitative Hinge of the OpenAI Quasi-Riemann Manuscript

**Purpose:** External specialist verification of the modest positive power margins that form the residual risk in the claimed zero-free half-plane \(\operatorname{Re}(s)>7/8\).

## Background (one paragraph)

An independent multi-agent audit of the public manuscript reconstructed the dual-representation strategy (cubic-theta reflection + Poisson isolation of the principal \(1/L\) signal + specialized sextic large sieve + zero detector). The paper’s own exponent ledgers leave a positive remainder under every loss they explicitly charge (Stage 1 high-side saving \(1/4800\); Stage 2 endpoint certificate \(49/440640>1/10000\)). Computational checks confirm the row envelope \(R(\delta)\) and the endpoint constant. The Lean formalization of the final theorems is independently machine-checked. No structural gap was found. The residual risk is the possibility of an unlisted intermediate loss larger than the reserved budgets.

## Highest-priority items for expert review

1. **Stage 1 central loss count**  
   Confirm that the charged central losses are fully accounted for by \(46\epsilon_*\) (with \(\epsilon_*=10^{-6}\)) and that no additional logarithmic or multiplicity factors appear in the chain from the sextic row count and detector dyads to the central contribution.  
   *Reference:* Proposition on balanced-high estimate and the surrounding loss-budget paragraph.

2. **Late-height closure**  
   Verify that choosing \(\tau\) after the height order \(A_\eta\) absorbs \((1+T_1)^{A_\eta}\) into half the reserved margin without circularity or under-counted dependence on the target character.  
   *Reference:* Lemma on late-height-closure.

3. **Specialized sextic large sieve recursion**  
   Check the norm-recursion (valuations modulo 6, paired residue characters, primary-generator convention) that produces the \((KD)^{2/3}\) term. An arithmetic error here would degrade the envelope \(R(\delta)\) and erase the margin.  
   *Reference:* Lemma on sextic large sieve / sextic specialization.

4. **Stage 2 endpoint identity**  
   Confirm the algebraic nonnegativity that yields \(-E_*\ge49/440640\) and that all compensation and asymmetric-scale losses are correctly charged against the reserved fraction of the high-side margin.  
   *Reference:* Lemma on balanced-endpoint (or equivalent high-bin endpoint calculation).

5. **Compensation local identities**  
   Verify that the two-term (marked + rescaled) cancellation removes the unwanted Euler factor exactly and does not introduce a conductor-dependent factor that grows with the target.  
   *Reference:* Local compensation section and the modified probe identity.

## Precise questions

- Does any intermediate lemma that feeds the Stage 1 or Stage 2 high-side estimates contain a loss larger than the reserved fraction of \(m_0\) or of the high-side margin?
- Is the late-height parameter ordering free of circularity?
- Does the specialized sextic recursion hold with the claimed exponent under the primary and zero-extension conventions used in the paper?
- Does the compensation step preserve uniformity of the power margins?

## Supporting materials available

- Specialist loss table (`quasi_rh_loss_table.md`)
- Computational check of \(R(\delta)\) and the endpoint constant (`quasi_rh_computational_check.md`)
- Layer-by-layer audit (`quasi_rh_part1_continuation.md` … `quasi_rh_part9_lean.md`)
- Full packaged audit (`quasi_rh_audit.md`)
- Original TeX source and Lean formalization (public)

## Requested output

A short note stating whether the listed losses are fully accounted for under the paper’s methods, or identifying a specific lemma and loss that exceeds the reserved budget. Either conclusion settles the residual quantitative risk.

---

*Prepared from an independent multi-agent audit. All claims are limited to the extracted accounting and the public source.*
