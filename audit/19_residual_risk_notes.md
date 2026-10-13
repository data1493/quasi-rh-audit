# Residual-Risk Notes

*Editorial index compiled for this repository. Every statement below is taken from the audit files linked; nothing here adds a new finding.*

## Where the risk sits

The margins are small: a Stage 1 high-side saving of $1/4800$ and a Stage 2 endpoint constant $49/440640\approx0.0001112>1/10000$. Within the extracted text, these survive every loss the paper **explicitly** charges and that the computational constants match ([00](00_master_audit.md), [11](11_loss_table.md), [17](17_computational_check.md)). The residual risk is the existence of an **unlisted** intermediate loss larger than the reserved budget. Confirming that none exists requires a specialist reading of every lemma that feeds the ledger, or formalization of those steps.

## Item-by-item

| Item | What could fail | Audit file |
|------|-----------------|------------|
| Stage 1 central loss $46\epsilon_*<m_0/4$ | Additional loss classes in the full central-contribution equation not included in the 13 or the two 15s | [12](12_stage1_central_loss.md) |
| Late-height closure | An estimate producing $A_\eta$ that itself depends on a height not yet closed | [13](13_late_height_closure.md) |
| Specialized sextic large sieve $(KD)^{2/3}$ | An extra factor in the full write-up not absorbed into $\epsilon$; an error in the mod-6 recursion would degrade $R(\delta)$ | [14](14_sextic_large_sieve.md), [04](04_large_sieve_row_energy.md) |
| Zero-detector saturation | Product lower bound weaker than claimed | [15](15_detector_saturation.md), [05](05_zero_detector_moments.md) |
| Stage 2 compensation identities | An uncancelled, target-dependent main term in an intermediate expansion | [16](16_stage2_compensation.md), [07](07_stage2_refinement_7_8.md) |
| Uniformity in the conductor | A slowly growing conductor factor hidden inside an $\epsilon$ | [08](08_uniformity_transfer.md), [01](01_continuation_criterion.md) |
| Lean translation fidelity | Lean certifies the final theorems, not every intermediate prose estimate | [09](09_lean_alignment.md) |

## What would settle it

A short specialist note either confirming that the listed losses are fully accounted for under the paper's methods, or naming a specific lemma and loss that exceeds the reserved budget. See [18](18_expert_review_request.md).
