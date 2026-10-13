# Zero-Detector Saturation

**Status:** The product-versus-individual comparison forces the plain-polynomial length into the regime \(m\le1/2+O(\epsilon)\). The length relation is elementary and feeds the envelope optimization correctly.

## Precise statement

For a residual row in a bin with parameter \(\delta=2a-1\ge1/50\), the zero detector produces an inverse polynomial \(M_r\) and a plain polynomial \(S_m\) such that the product lower bound and the individual upper bounds satisfy
\[
|M_r S_m|\gg U^{\delta(r+m)-\epsilon},
\qquad
|M_r|^2\ll U^{\delta r+\epsilon},
\qquad
|S_m|^2\ll U^{\delta\min(m,1-m)+\epsilon}.
\]

## Length relation

Comparing the product lower bound with the product of the individual upper bounds yields
\[
\delta(r+m)\le\frac\delta2 r+\frac\delta2\min(m,1-m)+O(\epsilon).
\]
Rearrangement gives
\[
\delta\bigl(m-\min(m,1-m)\bigr)\ll\epsilon.
\]
Since \(\delta\ge1/50>0\), this forces
\[
m\le\frac12+O(\epsilon).
\]
(The same relation holds with the complementary length.) Thus the shorter of the two lengths is at most \(1/2+O(\epsilon)\).

## How it feeds the envelope

Once the plain length is known to be \(\le1/2+O(\epsilon)\), the residual-row count is controlled by the specialized sextic sieve applied to a squarefree factor of length at most that of the inverse witness. The resulting envelope is exactly
\[
R(\delta)=\min\bigl\{1,\max(1-\delta/2,4/3-\delta)\bigr\},
\]
which is the optimization of the sieve bound against the detector spike. The \(O(\epsilon)\) is absorbed into the usual \(\epsilon\)-loss of the row-count proposition.

## Residual risk assessment

The comparison is elementary once the product lower bound and the individual upper bounds are granted. The length relation contains no hidden arithmetic and the \(O(\epsilon)\) is the standard one absorbed elsewhere. The only way this step fails is if the product lower bound itself is weaker than claimed (for example, if the simultaneous zero-free rectangles do not produce a full-strength product). Within the extracted argument, the saturation holds and correctly forces the rows into the regime where the sieve supplies a positive saving.

**ROI status:** Zero-detector saturation survives extraction. The length relation that feeds the envelope is correct under the stated bounds.
