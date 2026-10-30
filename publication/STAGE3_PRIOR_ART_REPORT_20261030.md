# No.192 — Stage 3 bibliographic and novelty audit (2026-10-30)

**Author**: Ryutaro Yonezu — Independent Researcher  
**Proof under consideration**: n≤12 entails L(f)=Σ_i |f̂({i})| ≤ √deg(f) for sign-valued nonconstant Boolean f.  
**Earlier audits**: v1.2 Stage 1 FAIL; repaired v1.3 Stage 1 logic PASS (one separate AI reviewer, **not** a human expert); Stage 2 computation PASS, including a separate reproduction by the reviewer.  
**This Stage 3 determination**: **REFERENCES—PASS for identity and topical attribution (original five); PRIOR-ART SEARCH—PARTIAL; NOVELTY—INCONCLUSIVE; RELEASE—HOLD.**

## Result-specific source comparisons

| Source | Verified publication or identifier | Mathematical result actually relevant | Does it directly establish n≤12? |
|---|---|---|---|
| OpenAI (2026), original No.192 | GitHub OpenAI Math preprint, 26 Sep 2026 | Arbitrarily large violations; explicitly says no useful growth bounds for n | **No**, not stated; finite lower-bound question distinct |
| Jha (2016) | arXiv:1611.01029v2 | Discrete-derivative/equivalent formulations of the stronger majority-type conjecture | **No direct n≤12 result identified** |
| Wang (2020) | IACR ePrint 2020/002 | Theorem 2.2: cryptographic equivalence; Theorem 3.2 d=1; Theorem 3.6 d=n−1 | **No**, n=12,d=5 is neither case |
| Kudin–Pašalić (2021) | DAM 289, 345–353; DOI 10.1016/j.dam.2020.11.005 | Majority inequality true all n for d=2,3; counterexample to **stronger** inequality at d=4 | **No**, d4 counterexample does not disprove sqrt bound |
| Maitra et al. (2025) | DAM 365, 138–159; DOI 10.1016/j.dam.2025.01.003 | Parity transform and resiliency vs polynomial degree; higher-order sensitivity, some small-variable tests | **No direct universal correlation bound found**, but related classification caveat |
| O'Donnell (2012) | arXiv:1204.6447 | Original open-problem framing | **No** |
| Filmus–Hatami–Keller–Lifshitz (2016) | Israel J. Math. 214; arXiv:1404.3396 | Influence bounds and conjecture context, not the stated finite n obstruction | **No directly equivalent theorem located** |
| Rasoolzadeh (2023) | ToSC 2023(3):213–226; DOI 10.46586/tosc.v2023.i3.213-226 | All (n−4)-resilient Boolean functions (up to given equivalence) | **No**; n=12,d=5 maps to (n−6)-resilient |
| Rasoolzadeh (2024) | ToSC 2024(3):298–301; DOI 10.46586/tosc.v2024.i3.298-301 | Quadratic/cubic (n−5)-resilient functions, not general (n−6) | **No**, advertised scope distinct |

## Exact cryptographic equivalence relevant to a stronger prior-art search

Let g(x)=f(x) χ_[12](x). Then ĝ(S)=f̂([12]\S) for any S⊆[12], so deg(f)≤5 iff g is 6-resilient. Moreover, with unnormalized Walsh W_g(S)=2^12 ĝ(S),

  Σ_i |f̂({i})| = 2^(−12) Σ_(|S|=11) |W_g(S)|.

Thus a duplicate might be published under **extremal sums of twelve Walsh coefficients of order 11 for 12-variable 6-resilient Boolean functions**, not under the original conjecture's name. The parity transform is **not new** (Wang 2020; Maitra et al. 2025).

## Bibliographic verification specifics

1. **OpenAI preprint**: actual original source on openai/math; abstract, September 26 date, indefinite n quantifier and no-useful-n-bound disclosure verified in full-text web mirror. A GitHub preprint URL is appropriate; no DOI asserted.
2. **Kudin–Pašalić**: publisher's Discrete Applied Mathematics record and author's university page match full journal/volume/page/DOI and d2/d3/d4 claims.
3. **Jha**: arXiv title/author, arXiv:1611.01029 and v2 verified. The arXiv identifier is sufficient; journal publication/DOI not invented.
4. **Wang**: original IACR ePrint title/author, 2020/002 verified; original PDF text of theorems accessible in indexed material, though automated rendered-page screenshot request was denied by host. No DOI invented.
5. **Maitra et al.**: publisher and open author-hosted paper confirm complete title, four authors, journal vol.365 pp138–159 and DOI. Old manuscript's abbreviated title was corrected.
6. **Rasoolzadeh two papers**: bibliographic metadata verified via IACR ePrint / DBLP and ToSC summaries; direct DOI landing pages were inaccessible in the browsing tool, so mark **publisher direct-page verification partial** rather than implying complete access.
7. **O'Donnell/Filmus et al.**: original arXiv pages verified; additional recommended contextual references.

## Novelty search boundary

- Search performed against original OpenAI release, arXiv/Jha, Wang/IACR ePrint, Kudin–Pašalić, Maitra et al., related Rasoolzadeh classification, O'Donnell/Filmus and targeted phrase/numeric searches for minimal dimensions and 12 variables.
- **Direct duplicate found: NONE in this checked set.** This does **not** establish global novelty or that no older paper entails the result.
- **Main remaining risk:** papers phrased as (n−6)-resiliency, Walsh-weight-11 optimization, orthogonal-array OA(2048,12,2,6) extremality, or coding/design-theoretic linear programming bounds; this deserves deeper specialist bibliography search prior to any strong novelty claim.
- Existing low-degree facts, parity transform and representation-theoretic rank argument are background tools, not individually novel.
- Reproducibility is separable: verifier PASS does not certify logical correctness, and a single AI-review PASS is not peer review.

**Recommended publication phrasing:** "We prove a finite-dimensional nonviolation bound through n=12 and provide reproducible exact certificates. In the literature checked, we did not locate this precise bound; we do not assert a comprehensive priority search." Use only after author accepts the scope and decides to publish. No public posting or submission was performed.

## Exact source URLs

- https://github.com/openai/math/tree/main/preprints/Unbounded-Violations-of-the-Square-Root-Degree-Bound-September-26-2026
- https://arxiv.org/abs/1611.01029
- https://eprint.iacr.org/2020/002
- https://kripto.famnit.upr.si/publication/kudinpasalic2021
- https://www.sciencedirect.com/science/article/pii/S0166218X20304960
- https://www.sciencedirect.com/science/article/pii/S0166218X25000034
- https://faculty.nps.edu/pstanica/research/2025DAM_InterplayResiliencyDegree.pdf
- https://arxiv.org/abs/1204.6447
- https://arxiv.org/abs/1404.3396
- https://eprint.iacr.org/2023/638
- https://doi.org/10.46586/tosc.v2024.i3.298-301

**Status:** Stage 3 literature audit completed to stated finite source scope. REFERENCES PASS for original five metadata; duplicate evidence NOT FOUND in checked scope; NOVELTY INCONCLUSIVE; RELEASE HOLD. Stage 4 (publication formatting) not undertaken in this audit.
