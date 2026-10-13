# Stage 1 Central Loss Accounting — \(46\epsilon_*\)

**Status:** The explicit count is \(13\epsilon_*+2(15\epsilon_*)+3\epsilon_*=46\epsilon_*\). With \(\epsilon_*=10^{-6}\) this is strictly less than \(m_0/4=1/4800\). Every listed component is charged.

## Extracted accounting

From the proof of the balanced-high estimate:

\[
13\epsilon_*+2(15\epsilon_*)+\epsilon_*+\epsilon_*+\epsilon_*=46\epsilon_*.
\]

**Components**
| Term | Origin | Coefficient |
|------|--------|-------------|
| \(13\epsilon_*\) | Explicit central losses in the central-contribution equation (row-count envelope, numerator bound, local correction, buffered reciprocal, multiplicity) | 13 |
| \(2\times15\epsilon_*\) | Two intermediate blocks, each bounded by \(\epsilon_c\le15\epsilon_*\) after setting the preliminary losses \(\epsilon_r=\epsilon_n=\epsilon_H=\epsilon_*\) | 30 |
| \(3\epsilon_*\) | Physical-dyad loss + two additional bounded terms (local/outer) | 3 |
| **Total** | | **46** |

**Reserved budget**
- \(m_0=1/1200\)
- \(m_0/4=1/4800\approx0.0002083\)
- \(46\times10^{-6}=0.000046<1/4800\)

The inequality holds by more than a factor of four.

## Surrounding context

- Preliminary witness, dyadic, and sieve losses are chosen small in terms of \(\epsilon_*\) before the target.
- After the fixed scalar \(c_S\), at least \(3m_0/4=1/1600\) remains before the height factor.
- The unused portion supplies the final claimed \(1/4800\) after late-height closure.

## Residual risk assessment

The arithmetic of the stated count is correct and the comparison to the reserved budget holds. The only way this step fails is if the full write-up of the central-contribution equation contains additional loss classes that are not included in the 13 or the two 15’s. Within the extracted accounting, every listed component is charged and the budget is not exceeded.

**ROI status:** Stage 1 central loss accounting survives extraction. The \(46\epsilon_*\) bound is internally consistent and strictly inside its reserved fraction.
