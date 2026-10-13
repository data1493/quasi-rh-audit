# Draft X thread (not posted)

1/
We ran an external, AI-assisted audit of OpenAI's quasi-Riemann hypothesis manuscript (zero-free half-plane Re(s) > 7/8). It audits the existing paper; it is not a re-proof. Loss table, residual-risk notes and review request: https://github.com/data1493/quasi-rh-audit

2/
What we did: layer-by-layer reconstruction of the argument, an audit of the paper's own exponent accounting, numerical checks of the critical constants, and an outline of how the Lean statements line up with the logical hinge.

3/
What we found: the structure holds at every layer we examined. The paper's own ledgers close with a positive remainder under the losses it charges: 1/4800 in Stage 1, 49/440640 > 1/10000 at the Stage 2 endpoint. A third-party Lean kernel replay is reported for the zeta statement; we built no Lean ourselves.

4/
The residual risk: those margins are small. Ruling out an unlisted loss in some intermediate lemma, bigger than the reserved budget, needs a specialist reading of the original. We did not verify every estimate, and no human specialist has reviewed this yet.

5/
If you work on large sieves or zero-density, the 10-minute path is: loss table → residual-risk notes → 5 prioritized review items. Findings welcome as issues. Primary sources: OpenAI's preprint and Lean in github.com/openai/math (commit adc7f12). https://github.com/data1493/quasi-rh-audit
