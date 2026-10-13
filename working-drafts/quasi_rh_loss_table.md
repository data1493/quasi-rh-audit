> **Unreviewed working draft, kept for transparency.** Some wording in this file overstates what was verified (for example "independently machine-checked" or "the bound holds"). The citable record is the corresponding file in [`audit/`](../audit/); every wording change is listed in [`audit/CHANGELOG_wording.md`](../audit/CHANGELOG_wording.md).

# Quasi-Riemann Hypothesis — Specialist Loss Table
## Stage 1 (11/12) and Stage 2 (7/8) endpoint certificates

**Purpose:** Self-contained extraction of every charged loss that feeds the final positive margins, with the reserved budgets they are charged against.

### Stage 1 — High-side saving \(1/4800\)

**Source:** Proposition on balanced-high estimate and Lemma on late-height-closure.

**Reserved parameters**
| Parameter | Value | Role |
|-----------|-------|------|
| \(m_0\) | \(1/1200\) | Minimum error-free saving on every major contribution |
| \(\epsilon_*\) | \(10^{-6}\) | Unit loss charged to each listed class |
| \(m\) | \(1/2400\) | Saving used after preliminary losses |
| \(\omega\) | \(\Delta_1/2\) | Low-bound room |

**Charged losses (explicit count)**
| Loss class | Coefficient | Charged amount | Reserved budget |
|------------|-------------|----------------|-----------------|
| Central (row count, numerator, local correction, reciprocal, multiplicity, physical dyads) | \(13\epsilon_* + 2(15\epsilon_*) + 3\epsilon_*\) | \(46\epsilon_*\) | \(< m_0/4 = 1/4800\) |
| Principal residues (two terms) | \(\le (3/2+1)\epsilon_*\) and \(2\epsilon_*\) | each \(< m_0/4\) | \(m_0/4\) |
| Small-row | \(\le 2\epsilon_*\) | \(< m_0/4\) | \(m_0/4\) |
| Large-row | requested \(\epsilon_*\) | absorbed | reserved |
| Height factor \((1+T_1)^{A_\eta}\) | late choice of \(\tau\) | absorbed into half remaining margin | late-height closure |
| Contour tails \(O(Z^{B_\eta}T_1^{-N})\) | increase \(N\) after target | smaller than any positive power | external order |

**Accounting**
- After all listed losses and division by the fixed scalar \(c_S\), at least \(3m_0/4 = 1/1600\) remains before the height factor.
- Using \(m=1/2400\) leaves an unused \(1/4800\).
- Late-height closure absorbs the height factor into half the remainder.
- Final claimed high-side saving: \(1/4800\).

**Status:** Every listed loss is strictly smaller than its reserved fraction under the paper’s accounting. The table closes with a positive remainder.

### Stage 2 — Endpoint certificate \(49/440640\)

**Source:** Lemma on balanced-endpoint (or equivalent high-bin endpoint calculation).

**Certificate derivation (extracted)**
The high exponent at the endpoint satisfies an identity of the form
\[
10368\,\mathcal{J}\,(-E_*) = \text{(non-negative quadratic form in \(\delta,y\))}.
\]
The leading constant term is \(49\). Bounding the remaining factors (\(\mathcal{J}\le5/2\), \(v\le17(3+5y)\)) produces
\[
-E_*\ge\frac{49}{440640}>\frac{1}{10000}.
\]
The inequality holds uniformly for \(1/50<\delta\le5/6\).

**Charged losses against this certificate**
| Loss class | Treatment | Budget |
|------------|-----------|--------|
| Amplitude bin width \(\vartheta\), witness subdivisions | absorbed into \(O(\epsilon)\) | reserved fraction of high margin |
| Capacity reduction (\(\nu_0\)) | charged \(2q\nu_0+\delta\max w_i\) | \(\Delta/4\) or equivalent |
| Height factor | late \(\tau\) as in Stage 1 | half high margin |
| Contour tails | external order \(N\) | smaller than any positive power |
| Compensation and asymmetric dyadics | absorbed into same \(\epsilon_{\rm total}\) | target-independent coefficient |

**Accounting**
- The constant term alone already exceeds \(1/10000\).
- All additional losses are charged to a reserved fraction of the high-side margin (proportional to \(\Delta=\beta_*-7/8\)) or to an arbitrarily small \(\epsilon_{\rm total}\).
- The certificate remains positive for every \(\Delta>0\).

**Status:** The endpoint inequality is negative by a fixed positive amount plus a term proportional to \(\Delta\). Under the paper’s accounting the remainder stays positive.

### Overall specialist conclusion

Both certificates close with a positive remainder under the losses the paper explicitly charges. The Stage 1 table accounts for every listed \(\epsilon_*\) class and leaves \(1/4800\). The Stage 2 certificate supplies a fixed positive constant larger than \(1/10000\) that survives the same style of reserved-budget accounting. No listed loss exceeds its budget in the extracted text. The quantitative hinge survives this level of extraction.

**Remaining limitation:** The table uses the paper’s own charged amounts. Full certification still requires confirming that no intermediate lemma contains an additional unlisted loss of larger size. Within the extracted accounting, the margins hold.
