# No.192 Stage 2 — Independent computation audit (2026-10-30)

**Verdict: COMPUTATION PASS for the explicitly scoped checks.**

Prior status: v1.2 failed a logical review. v1.3 replaced the flawed bridge; a separate hand review reported Stage-1 **logic PASS**. This report is *not* another comprehensive logical peer review; it independently verifies the numerical and finite-algebraic items the reviewer had not checked.

## Independent checks performed

1. **Swap rank 154:** generated all 13,860 distinct 3-pair matchings on 12 coordinates; for each, built its eight-term signed triple vector (over GF(2) signs reduce to 1), using a separate bit-mask implementation and incremental XOR Gaussian elimination. Result: **154**.
2. **Degree-2 incidence rank 66:** constructed a 220-row × 66-column matrix whose rows represent 3-subsets and columns 2-subsets; entry is 1 iff the pair is contained in the triple. Independent elimination over GF(101) gives **66**. Since swap vectors annihilate those 66 pair-incidence functions over Q, their rational rank is at most 220−66=154. Rank GF(2)=154 gives a rational-rank lower bound of 154. Therefore the rational harmonic complement has dimension exactly 154.
3. **Dual residual table:** computed elementary symmetric polynomials over **every one of the 2^11 and 2^12 sign inputs**, not by the Krawtchouk formula used in prior code. Independent exact Fraction sums: n=11,d=4: 67/32; n=11,d=5:17/8; n=11,d=7:5/2; n=12,d=4:37/18; n=12,d=5:331/144; n=12,d=7:39/16. All match the paper. The three previously unchecked rows specifically pass.
4. **Equation (7) enumeration:** generated all 13 values of C(k) by a second elementary-symmetric computation; derived the two aggregate integer equations and enumerated all nonnegative solutions; re-evaluated the weighted high-degree orthogonality condition for each split, rather than calling the manuscript's linear equation. Results: (2,18,6)→(1,9,3); (5,10,7)→none; (8,2,8)→(4,1,4). All pass.
5. **Existing v1.3 repair verifier:** run separately after checking its saved SHA256 from the original package. Its role is supporting arithmetic; it is **not** an independent external logical audit.

## Editorial corrections (v1.3.1)

- Made explicit why at most one endpoint disagreement can occur on each face: global errors at levels 0 and 12 are impossible.
- Renamed only the final spherical average difference polynomial Q(k) to D(k), leaving the triple Q unchanged.
- Kept the invalid v1.2 claim removed; updated the status paragraph to record the Stage-1 logic PASS and Stage-2 arithmetic PASS.

## Boundaries

- **MODEL / LOGIC:** Stage-1 hand auditor reports PASS for v1.3 (separate evidence; not reproduced by computation here).
- **COMPUTATION:** PASS for items 1–4 above, using independent Python standard-library implementation; packaged SHA256 and clean-room reexecution PASS.
- **REFERENCES:** NOT CHECKED in Stage 2.
- **NOVELTY:** INCONCLUSIVE.
- **RELEASE:** HOLD; publication/new research number requires novelty and citation review and explicit approval.

No claim of exhaustive computer proof of all Boolean functions is made; the verified computations support the written symbolic proof.
