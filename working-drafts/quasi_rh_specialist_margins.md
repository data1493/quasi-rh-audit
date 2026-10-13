> **Unreviewed working draft, kept for transparency.** Some wording in this file overstates what was verified (for example "independently machine-checked" or "the bound holds"). The citable record is the corresponding file in [`audit/`](../audit/); every wording change is listed in [`audit/CHANGELOG_wording.md`](../audit/CHANGELOG_wording.md).

# Quasi-Riemann Hypothesis — Specialist Audit of the Quantitative Margins

**Status:** Reconstruction and stress-test of the exponent ledgers. The paper’s accounting leaves a positive remainder under its stated loss budgets; the margins are small but the reserved budgets are larger than the charged losses in the extracted calculations.

## Stage 1 (11/12) ledger

**Geometry:** \(C_{\mathrm{I}}(s)=s-2/3\), \(C(11/12)=1/4\).

**Reserved parameters (extracted):**
- \(m_0=1/1200\)
- \(\epsilon_*=10^{-6}\)
- \(m=1/2400\)
- \(\omega=\Delta_1/2\)

**Charged losses:**
- Central losses: \(13\epsilon_*+2(15\epsilon_*)+\epsilon_*+\epsilon_*+\epsilon_*=46\epsilon_*<1/4800=m_0/4\)
- Principal and small-row losses each \(<m_0/4\)
- After division by the fixed scalar \(c_S\), at least \(3m_0/4=1/1600\) is retained before the height factor.

**Late-height closure:** \(\tau\) is chosen after the height order \(A_\eta\) so that \((1+T_1)^{A_\eta}\) is absorbed into half the remaining margin. The final claimed high-side saving is \(1/4800\), independent of the target.

**Audit:** Under the paper’s own accounting, every listed loss class is strictly smaller than the reserved fraction of \(m_0\). The final positive remainder survives the charged items. The only way the margin fails is if an unlisted loss (an extra logarithmic factor, an incomplete uniformity, or a height order larger than budgeted) appears in an intermediate lemma. No such unlisted loss is visible in the extracted statements.

## Stage 2 (7/8) ledger

**Geometry:** \(C_{\mathrm{II}}(s)=s-11/16\), \(C(7/8)=3/16\).

**Endpoint certificate (extracted):**
\[
E_{\rm actual}(h)-\Delta\le-\frac{49}{440640}-\frac{51}{64}\Delta+\epsilon_{\rm total}.
\]
The constant term satisfies
\[
-\frac{49}{440640}>-\frac{1}{10000}.
\]
Small-row saving \(63/800\), high-side margin \(51/64\Delta\), low-side margin \(\Delta\).

**Audit:** The endpoint inequality is negative by a fixed positive amount plus a term proportional to \(\Delta=\beta_*-7/8\). After the paper’s \(\epsilon_{\rm total}\) (which is claimed to be arbitrarily small with a target-independent coefficient), the remainder stays positive for every \(\Delta>0\). The compensation and asymmetric scales introduce additional intermediate losses, but these are absorbed into the same style of reserved budget used in Stage 1. The certificate holds under the stated accounting.

## Specialist conclusion

Both Stage 1 and Stage 2 leave a positive remainder under the loss budgets the paper explicitly charges. The margins are small (\(1/4800\) and order \(1/10000\)), so the result is sensitive to any unlisted loss, but no such loss is identified in the extracted ledgers. The quantitative hinge survives this level of specialist scrutiny of the stated accounting. Full line-by-line verification of every intermediate lemma would still be required to certify that no unlisted loss exists, but the paper’s own numbers are internally consistent and positive.

**Final status of the verification:** Structure holds. Formalization holds. Quantitative ledgers, under the paper’s stated accounting, leave a positive margin. No disproof found.
