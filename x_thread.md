# Draft X thread (DO NOT POST until approved; replace https://github.com/data1493/quasi-rh-audit)

1/
We ran an external, multi-agent audit of OpenAI's quasi-Riemann hypothesis manuscript (zero-free half-plane Re(s) > 7/8). It is an audit of the existing paper, not a re-proof. Loss table, residual-risk notes and review request: https://github.com/data1493/quasi-rh-audit

2/
What we did: layer-by-layer reconstruction of the argument, a specialist audit of the paper's own exponent accounting, computational confirmation of the critical constants, and an outline of how the Lean statements line up with the logical hinge.

3/
What we found: the structure holds at every layer we examined. The paper's own ledgers close with a positive remainder under the losses it charges: 1/4800 in Stage 1, 49/440640 > 1/10000 at the Stage 2 endpoint. Lean of the final theorems is machine-checked.

4/
The residual risk: those margins are small. Ruling out an unlisted loss in some intermediate lemma, bigger than the reserved budget, needs a specialist reading of the original. We did not verify every estimate.

5/
If you work on large sieves or zero-density, the 10-minute path is: loss table → residual-risk notes → 5 prioritized review items. Primary sources: OpenAI's preprint and Lean in github.com/openai/math. https://github.com/data1493/quasi-rh-audit
