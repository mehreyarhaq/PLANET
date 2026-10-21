# Mathematics and computation: amateur-accessible discovery projects (status as of 2026-10-21)

*Method note for the report writer.* This note was built from ~45 web-search result sets. Direct page retrieval (WebFetch, curl via the proxy, Firecrawl, GitHub API) was blocked or out of credits in this sandbox, so every finding below rests on search-result excerpts of the cited page rather than a full read. Where a figure differs between sources I say so. Tool names flagged "(background knowledge)" were not verified in this session. The person is a U of T undergraduate with group theory (MAT301), elementary number theory (MAT315) and history of mathematics, driving Claude Code on a laptop with free software.

## Key question 0: Vetted shortlist — which 8–15 projects are doable, new, checkable and announceable?

### Takeaway
The best-evidenced route to a credited new result in 2026 is no longer "ask an LLM to prove an Erdős problem" (that lane is crowded by labs *and* hobbyists, and Tao estimates only 1–2% of open Erdős problems are AI-accessible), but a *computational-certificate* lane: pick a concrete record table or an open problem flagged tractable, run a search or verification that a laptop can finish, and ship a mechanically checkable artefact (a tile, a graph, a Lean certificate, a b-file). Fourteen candidates are carded below; the strongest fits for this student are P2 (Erdős computational certificate), P5 (cage graphs), P8 (finite-group tables, matching coursework), P1 (Heesch ≥ 7, high-risk/high-reward) and P10 (Life search).

### Cited Findings

**P1. A polyform with Heesch number ≥ 7 (planar), or the first systematic Heesch records in 3D.**
- (1) *Discovery:* a shape whose Heesch number beats the standing record of 6. The record "a shape with Heesch number exactly 6, is due to Bašić from 2021", and Epoch AI lists "a polyform with Heesch number at least 7" with "a size limit of 200 cells" as a FrontierMath open problem — [Epoch AI open problem](https://epoch.ai/frontiermath/open-problems/heesch-number). An Oct-2026 3D paper says the planar record holders "all obtaining Heesch number 6, are a family of tiles first discovered by Dave Smith, with later confirmation by Bašić and Bakker" — [arXiv 2610.02579](https://arxiv.org/html/2610.02579).
- (2) *Tools:* Epoch's problem page (above); Kaplan's SAT-based polyform tiling code, "Detecting Isohedral Polyforms with a SAT Solver" — [arXiv 2406.16407](https://arxiv.org/pdf/2406.16407); survey "The Path to Aperiodic Monotiles" — [arXiv 2509.12216](https://arxiv.org/pdf/2509.12216); free polyomino enumerators (counts to n=59 exist) — [arXiv 2510.22446](https://arxiv.org/html/2510.22446v1).
- (3) *Method:* enumerate polyforms (polyominoes/polyhexes/polyiamonds) in a target size band; filter out tilers with Kaplan's isohedral SAT test; compute coronas with a SAT/backtracking corona solver; prioritise shapes near Dave Smith's Heesch-6 family. Variant: the 3D paper above is a *density method for bounding* Heesch numbers in E^3, which suggests the 3D polycube record table is largely unexplored — [arXiv 2610.02579](https://arxiv.org/html/2610.02579).
- (4) *Verification/recognition:* a Heesch-7 shape is checkable by anyone who recomputes the coronas; Epoch's FM:OP verifies submissions by program; coverage precedent: Scientific American on the hat/einstein hunt — [SciAm](https://www.scientificamerican.com/article/inside-mathematicians-search-for-the-mysterious-einstein-tile/).
- (5) *Effort:* months; CPU-heavy corona search.
- (6) *Saturation:* **some competition** — the problem is on Epoch's AI benchmark (so labs are trying), yet "I found no sign of a new planar Heesch number record in 2025–2026" (search summary across [Epoch](https://epoch.ai/frontiermath/open-problems/heesch-number), [arXiv 2610.02579](https://arxiv.org/html/2610.02579)); the only 2026 Heesch results are hyperbolic ("resolves the Heesch problem in the hyperbolic plane") — [arXiv 2603.27827](https://arxiv.org/abs/2603.27827).
- (7) *Risk:* search space explodes; the record-6 shapes were found by a hobbyist's insight rather than exhaustive search, so a laptop sweep may find nothing. Fallback deliverable: an OEIS-style table "max Heesch number among n-cell polyforms" extended by one size (see Gaps).

**P2. A kernel-checked computational certificate or small-case extension on an Erdős problem flagged "tractable".**
- (1) *Discovery:* a verified negative/positive resolution of a finite case, a counterexample, or a verification bound (e.g. "holds up to 10^12") on a still-open Erdős problem.
- (2) *Tools:* [erdosproblems.com](https://www.erdosproblems.com/faq) (each forum page has markers "This problem looks difficult"/"This problem looks tractable" and whether someone is working on it — [forum thread 710](https://www.erdosproblems.com/forum/thread/710)); a community Claude Code skill already queries "Problems marked tractable by community" — [sharedcontext.ai erdos-solver](https://sharedcontext.ai/skills/external/0bserver07/erdos-solver); Lean 4 for certificates; PARI/GP, SageMath (background knowledge).
- (3) *Method:* literature-check first (the Oct-2025 fiasco was literature search, see KQ1); choose a problem whose statement has a finite checkable instance; write a fast search; wrap the result in a Lean-kernel-checked certificate as in [arXiv 2608.17880](https://arxiv.org/pdf/2608.17880).
- (4) *Verification/recognition:* exactly this pipeline has already produced credited, individual results: the Problem 647 certificate paper cites "Jamal Agbanwa's AI-assisted possible solution, bentrd's frontier extension, and Patrik Idén's computational verification up to 10^12", and "Ibrahim Mian and Shayaan Siddique also published a kernel-checked verification of a negative resolution of Problem 486 (Pilus)" — [arXiv 2608.17880](https://arxiv.org/pdf/2608.17880). Maintainer Thomas Bloom records contributions on the site; Quanta covered hobbyist/undergrad solvers — [Quanta](https://www.quantamagazine.org/why-the-legendary-erdos-problems-are-falling-to-ai-20260803/).
- (5) *Effort:* 2–8 weeks per problem.
- (6) *Saturation:* **crowded** for proof-style "easy" problems (labs: 9 solved by AlphaProof Nexus, 4 by a Feb-2026 DeepMind survey of ~700; hobbyists with GPT-5.2 Pro) — [the-decoder](https://the-decoder.com/google-deepminds-alphaproof-nexus-solves-decades-old-math-problems-for-a-few-hundred-dollars/), [Wikipedia list](https://en.wikipedia.org/wiki/List_of_mathematical_discoveries_by_artificial_intelligence); **some competition** for computational certificates (only a handful of named individuals so far per [arXiv 2608.17880](https://arxiv.org/pdf/2608.17880)).
- (7) *Risk:* problem already solved in literature — "it can be very challenging to determine for sure whether a particular problem is actually open" — [arXiv 2511.16072](https://arxiv.org/pdf/2511.16072); a finite verification is not a solution and may be judged trivial.

**P3. New OEIS sequences tied to Erdős problems (the crowdsourced erdosproblems→OEIS linking project) or to group-theory objects.**
- (1) *Discovery:* a genuinely new, well-defined integer sequence (with b-file and code) attached to an Erdős problem or to a group-theoretic count.
- (2) *Tools:* [OEIS submit](https://oeis.org/Submit.html), [pre-submit checklist](https://oeis.org/wiki/Suggested_pre-submit_checklist), a "crowdsourced project to link up erdosproblems.com to the OEIS" (title only in results) — [feed item](https://tagteam.harvard.edu/hub_feeds/3899/feed_items/15618117); GAP for group counts (background knowledge).
- (3) *Method:* for a chosen Erdős problem, define the extremal function f(n) it asks about, compute it exactly for small n, submit with program and reference to the problem page.
- (4) *Verification/recognition:* OEIS editorial review ("a group of about 130 editors reviews submissions", "all submissions are refereed") — [OEIS Foundation](https://oeisf.org/); students' OEIS entries get institutional press (a dean and MSc student at UACS — [UACS](https://uacs.edu.mk/home/?p=7513); a Grade-12 student with two hexagonal-tiling sequences — [DAIS](https://www.dais.edu.in/aarnav-gogri-of-ibdp-publishes-math-research-in-OEIS.html)).
- (5) *Effort:* days to two weeks per sequence.
- (6) *Saturation:* **crowded** generically (over 378,000 sequences; default cap of 3 pending submissions because "the editors were (and still are) drowning in submissions" — [OEIS wiki](https://oeis.org/wiki/Why_am_I_limited_to_3_submissions)); **open niche** for Erdős-linked sequences (DeepMind had to formalise 492 open OEIS conjectures, showing OEIS is being mined as a conjecture source — [seqfan](https://groups.google.com/g/seqfan/c/gbb7MKvandc)).
- (7) *Risk:* "submissions that seem arbitrary will be silently deleted" — [OEIS FAQ](https://oeis.org/FAQ.html); not newsworthy on its own.

**P4. Extend an OEIS sequence tagged `hard`/`more` by new terms.**
- (1) *Discovery:* new verified terms of a sequence whose extension needs ideas or heavy compute.
- (2) *Tools:* OEIS keyword semantics ("hard" = "cannot reasonably be extended at all (but which is not known to be complete)") — [Greathouse keyword page](https://www.oeis.org/wiki/User:Charles_R_Greathouse_IV/Keywords/difficulty); example entries [A032502](https://oeis.org/A032502) (nonn,hard,more; extended Dec 2024 by Jeppe Stig Nielsen) and [A214655](https://oeis.org/A214655); PARI/GP, primality tools (background knowledge).
- (3) *Method:* pick a `more` sequence whose last extension is years old and whose next term is a few CPU-days away; write optimised code; submit with program.
- (4) *Verification/recognition:* editors check terms; credit line "a(n) from <name>" in EXTENSIONS, as for Nielsen 2024 — [A032502](https://oeis.org/A032502).
- (5) *Effort:* 1–4 weeks.
- (6) *Saturation:* **some competition** — roughly 7,500 sequences carry `hard` (figure reported in one arXiv paper in results, exact source not confirmed: [arXiv 2105.05111](https://arxiv.org/pdf/2105.05111)); many extensions are done by hobbyists.
- (7) *Risk:* low newsworthiness; some "hard" entries are hard by nature and no compute helps.

**P5. New cage-graph records (smallest k-regular graphs of girth g) for open (k,g) cases.**
- (1) *Discovery:* a smaller (k,g)-graph than the current best, lowering the upper bound on n(k,g).
- (2) *Tools:* House of Graphs cages directory (linked from the paper) — [arXiv 2511.07247](https://arxiv.org/pdf/2511.07247v1); nauty/geng, SAT (background knowledge); the 2025–26 paper's methods — [EJC v33i3p48](https://www.combinatorics.org/ojs/index.php/eljc/article/view/v33i3p48).
- (3) *Method:* voltage-graph lifts / Cayley-graph and hypergraph constructions (Erskine–Tuite set records for cubic girths 23–32 that way — [EJC v30i1p57](https://www.combinatorics.org/ojs/index.php/eljc/article/view/v30i1p57)) plus local search and SAT for girth constraints; the student's group theory is directly relevant (Cayley graphs, lifts).
- (4) *Verification/recognition:* a graph file is verified in seconds (degree, girth, order); upload to House of Graphs; short arXiv note; EJC publishes such records — [arXiv 2511.07247](https://arxiv.org/abs/2511.07247v1).
- (5) *Effort:* 1–3 months.
- (6) *Saturation:* **some competition** — Exoo, Goedgebeur, Jooken, Stubbe, Van den Eede improved "eleven classical cage cases, including n(3,16) ≤ 936 and n(3,17) ≤ 2048, and n(4,10) ≤ 320, down from a long-standing 384", noting some bounds "had stood for 22 years" — [arXiv 2511.07247](https://arxiv.org/abs/2511.07247v1); still-open structural cases (3,13), (3,14), (3,15) are listed in [arXiv 2503.07400](https://arxiv.org/pdf/2503.07400).
- (7) *Risk:* that group has more compute and experience; remaining cases may need new constructions, not search.

**P6. Lower bounds for small multicolour / book / ordered Ramsey numbers with SAT solvers (not classical two-colour R(s,t)).**
- (1) *Discovery:* a colouring certifying a new lower bound, e.g. of the type R(K4,K4−e,K4−e) ≥ 35 and R(K3,K4,C4,C4) ≥ 49 (Wesley, Sept 2025) — [arXiv 2509.03784](https://www.arxiv.org/abs/2509.03784).
- (2) *Tools:* Kissat/CaDiCaL (used for ordered Ramsey numbers in a 2026 paper — [EmergentMind 2604.16188](https://www.emergentmind.com/papers/2604.16188)); template/cyclic colourings — [arXiv 2203.13476](https://arxiv.org/pdf/2203.13476); Gasarch's SAT-and-Ramsey notes — [arXiv 2312.01159](https://arxiv.org/pdf/2312.01159).
- (3) *Method:* encode "n-vertex colouring with no forbidden monochromatic subgraph" as SAT with symmetry-breaking (circulant/template structure), run incremental n.
- (4) *Verification/recognition:* the colouring is a mechanical certificate; Radziszowski's dynamic survey records bounds (background knowledge); arXiv note.
- (5) *Effort:* 2–6 weeks per family.
- (6) *Saturation:* **crowded** for classical numbers — AlphaEvolve improved lower bounds for several (Wikipedia says nine, a Medium explainer says five, e.g. R(3,13) 60→61; sources conflict) — [Wikipedia list](https://en.wikipedia.org/wiki/List_of_mathematical_discoveries_by_artificial_intelligence), [Medium](https://medium.com/@AdithyaGiridharan/alphaevolve-just-moved-the-needle-on-ramsey-theory-and-that-is-a-very-big-deal-3750cf96b3ff); R(5,5) is pinned at 43–46 after Angeltveit–McKay — [arXiv 2409.15709](https://www.arxiv.org/pdf/2409.15709), with a CMU SAT project on 45-vertex SRGs ("141 of which we certify as unsatisfiable across 313 SAT subproblems") — [FAU abstract](https://www.math.fau.edu/combinatorics/abstracts/braginsky-57.pdf). **Some competition** for multicolour/book/ordered variants.
- (7) *Risk:* increments of +1 are modest news; DeepMind-scale search may sweep variants next.

**P7. Hadwiger–Nelson certificates: a finite unit-distance graph with fractional chromatic number ≥ 4, or a 5-chromatic unit-distance graph smaller than 510 vertices.**
- (1) *Discovery:* an explicit finite graph certifying a bound that is currently only known non-constructively.
- (2) *Tools:* SAT (Heule), LP for fractional colourings; Polymath16 pages (background knowledge).
- (3) *Method:* Matolcsi, Ruzsa, Varga and Zsámboki proved the fractional chromatic number of the plane is ≥ 4 but "could not produce a finite planar subgraph that certifies this bound" and "No finite unit distance graph has yet been found with fractional chromatic number at least 4" — [arXiv 2311.10069](https://arxiv.org/html/2311.10069v4). Heule's 510-vertex graph is "the smallest certificate for the current lower bound" and "raising the bound to 6 is still a challenge for automated reasoning" — [Heule, FoCM 2023](https://focm2023.pages.math.cnrs.fr/files/confirmed/I3-05171-Heule.pdf).
- (4) *Verification/recognition:* graph + LP/SAT certificate is mechanical; Polymath16/MathOverflow; precedent of amateur Aubrey de Grey (2018) — [Aaronson blog](https://scottaaronson.blog/?p=3697).
- (5) *Effort:* 1–3 months.
- (6) *Saturation:* **some competition** (Heule, Parts and the Polymath16 group active, but no 2025–26 change to the 5 ≤ χ ≤ 7 bounds found in searches).
- (7) *Risk:* likely needs thousands of vertices; may be infeasible on a laptop.

**P8. Finite-group data: extend or audit tables of perfect groups, (2,3)-generated groups, or group counts (OEIS-type sequences) with GAP.** *(Best coursework match.)*
- (1) *Discovery:* new verified entries (or corrections) in group census tables; new OEIS terms.
- (2) *Tools:* GAP (free); Hulpke's perfect-group enumeration — [arXiv 2104.10828](https://arxiv.org/pdf/2104.10828); Dietrich–Eick–Pan algorithms for orders with ≤ 4 prime factors "implemented in GAP" — [arXiv 2012.02933](https://arxiv.org/pdf/2012.02933); the (2,3)-group census to order 6,000,000 — [arXiv 1505.00888](https://ar5iv.arxiv.org/html/1505.00888); OEIS [A392130](https://oeis.org/A392130/internal) (revised Jan 2026; terms "up to 5·10^14 listed for the first 13 values").
- (3) *Method:* re-derive a table range independently (different method), compare, extend by a step; publish as OEIS b-file and a note. Hulpke "found five groups (in addition to two groups found already in 2005 by Jack Schmidt) that had been overlooked" in the classical Holt–Plesken tables — [arXiv 2104.10828](https://arxiv.org/pdf/2104.10828), so audits do find errors.
- (4) *Verification/recognition:* OEIS editors; GAP package maintainers; an ICMS 2026 plenary frames enumeration vs construction of "423 164 062 groups" for orders ≤ 2000 — [ICMS 2026](https://icms-conference.org/2026/papers/pleanary1/main.pdf).
- (5) *Effort:* 1–3 months; CPU-days.
- (6) *Saturation:* **open niche** — these tables are produced by a few specialists (Hulpke; Dietrich–Eick–Pan; Potočnik–Spiga–Verret) and "no closed formula is known for general n"; "The number of groups of order n is known for all n ≤ 2000, and for most n at most 20000" — [ICMS 2026](https://icms-conference.org/2026/papers/pleanary1/main.pdf).
- (7) *Risk:* correctness depends on deep GAP expertise; newspaper appeal is low unless an error in a standard table is found.

**P9. God's number (Cayley-graph diameter) for an unsolved permutation puzzle, or tightening the 4×4×4 bounds.**
- (1) *Discovery:* an exact diameter or an improved bound for a puzzle group.
- (2) *Tools:* open-problem list — [cuberoot.me open problems](https://cuberoot.me/math/group/open-problems), [other puzzles](https://www.cuberoot.me/math/group/other-puzzles), [rubiks.fandom God's Number](https://rubiks.fandom.com/wiki/God%27s_Number); coset/pruning-table solvers (background knowledge).
- (3) *Method:* coset enumeration with symmetry reduction; for 4×4×4 the diameter "is bounded only to [22, 36] HTM" and "[35, 53]" in QTM; 5×5×5 "[20, 32]"; Megaminx "≈ 45?" with "upper bound unproved" and a conjectured upper bound of 114 reported by HKHLR (Feb 2026) — sources conflict — [cuberoot](https://cuberoot.me/math/group/open-problems), [HKHLR](https://www.hkhlr.de/node-export/pdf/4006).
- (4) *Verification/recognition:* cubing community (speedsolving.com), OEIS sequences for move-count distributions, arXiv.
- (5) *Effort:* weeks for a small puzzle; exact 4×4×4 is far beyond a laptop.
- (6) *Saturation:* **some competition** (active hobbyist community); searches found "no 2025 result computing the 4x4x4 or Megaminx diameter".
- (7) *Risk:* the small puzzles with laptop-sized state spaces may already be solved in forum posts that are hard to cite; need to check speedsolving.com archives first.

**P10. Conway's Game of Life: a new small spaceship/oscillator or a smaller ship for a known velocity, via SAT-based search.**
- (1) *Discovery:* a new pattern (new velocity, or record-small for its velocity/period).
- (2) *Tools:* LifeWiki/ConwayLife forums — [Spaceship](https://conwaylife.com/wiki/Spaceship); Golly, LLS/ikpx2 search programs (background knowledge).
- (3) *Method:* precedent: Copperhead (first c/10 ship) was "found in 2016 by a forum newcomer, was found by a search whose key insight was that a microscopic ship can be found in reasonable time despite its high period" — [Wikipedia Spaceship](https://en.wikipedia.org/wiki/Spaceship_(cellular_automaton)); 2026 shows the community still constructing (Annelid, "(28,3)c/84 spaceship which was constructed by Brithos and finalised on 22 June 2026", 168,807,151 cells) — [LifeWiki Annelid](https://conwaylife.com/wiki/Annelid), [forum thread](https://conwaylife.njohnston.ca/forums/viewtopic.php?p=230298).
- (4) *Verification/recognition:* immediate on the forums/LifeWiki (RLE file is mechanically checkable); Quanta/press covered Life milestones historically (knightship on HN — [HN](https://news.ycombinator.com/item?id=16546152)).
- (5) *Effort:* weeks to months of search time.
- (6) *Saturation:* **crowded but productive** hobbyist niche; "many 2020s developments produced results orders of magnitude smaller than the largest engineered ships" — [LifeWiki Spaceship](https://conwaylife.com/wiki/Spaceship).
- (7) *Risk:* being scooped by veterans running the same tools; news value depends on the target (a new elementary velocity is news, a marginal size reduction is not).

**P11. Busy Beaver: decide individual BB(6) holdout machines with a provable decider (contribution to bbchallenge).**
- (1) *Discovery:* proofs that specific holdout Turing machines never halt (or halt), shrinking the holdout list.
- (2) *Tools:* [bbchallenge.org](https://bbchallenge.org/), [BB(6) wiki](https://wiki.bbchallenge.org/wiki/BB(6)), [holdouts lists](https://wiki.bbchallenge.org/wiki/Holdouts_lists), monthly roundups — [TMBR Feb 2026](https://wiki.bbchallenge.org/wiki/TMBR:_February_2026).
- (3) *Method:* write/extend deciders (cyclers, bouncers, closed tape language) and prove them, or hand-analyse a single holdout's dynamics.
- (4) *Verification/recognition:* community reproduces deciders; holdout counts updated on the wiki; contributions named in TMBR roundups.
- (5) *Effort:* weeks per decider class.
- (6) *Saturation:* **some competition** — "The latest list, from September 16, 2026, has 855 holdouts ... down from 1,104 on April 29, 2026"; Feb 2026 roundup: "All machines simulated to 1e13, 100 solved machines" — [holdouts](https://wiki.bbchallenge.org/wiki/Holdouts_lists), [TMBR](https://wiki.bbchallenge.org/wiki/TMBR:_February_2026).
- (7) *Risk:* BB(6) itself is out of reach ("solving a Collatz-like problem is required to solve BB(6)" because of Antihydra; champion by mxdys June 2025 gives Σ(6) > 10↑↑10↑↑10↑↑8) — [BB(6) wiki](https://wiki.bbchallenge.org/wiki/BB(6)), [Brubaker](https://benbrubaker.com/why-busy-beaver-hunters-fear-the-antihydra/); remaining holdouts are the hardest; low press value.

**P12. Lean: formalise a solved-but-unformalised Erdős result or an OEIS conjecture, contributing to Formal Conjectures / mathlib.**
- (1) *Discovery:* not a new theorem, but a machine-checked proof or statement accepted into a recognised repository.
- (2) *Tools:* DeepMind's Formal Conjectures repo (Lean statements of Erdős problems, "drawn from an online catalog of over 1,200 open problems") — [arXiv 2605.13171](https://arxiv.org/pdf/2605.13171), e.g. [258.lean](https://github.com/google-deepmind/formal-conjectures/blob/main/FormalConjectures/ErdosProblems/258.lean) credits "the proof by Chojecki and GPT-5.4 Pro, formalised in Lean by ster-oc"; Harmonic's Aristotle (used by Barreto to check #728) — [Quanta](https://www.quantamagazine.org/why-the-legendary-erdos-problems-are-falling-to-ai-20260803/); mathlib (>210,000 theorems as of May 2025) — [Wikipedia Lean](https://en.wikipedia.org/wiki/Lean_(proof_assistant)).
- (3) *Method:* choose a recently solved Erdős problem without a formal proof; formalise with Claude Code + Lean; PR to Formal Conjectures or mathlib (review "favors lots of small contributions over one giant contribution") — [arXiv 2110.03551](https://arxiv.org/pdf/2110.03551).
- (4) *Verification/recognition:* Lean kernel; repo maintainers; the #728 Lean writeup is an arXiv paper — [arXiv 2601.07421](https://arxiv.org/abs/2601.07421).
- (5) *Effort:* 2–8 weeks.
- (6) *Saturation:* **some competition** (DeepMind formalised 492 OEIS conjectures and 68 Erdős problems are in Epoch's Lean benchmark — [seqfan](https://groups.google.com/g/seqfan/c/gbb7MKvandc), [arXiv 2609.25050](https://arxiv.org/abs/2609.25050)); undergraduates do contribute to mathlib ("valuable contributions come from undergraduates and professors alike") — [arXiv 2110.03551](https://arxiv.org/pdf/2110.03551).
- (7) *Risk:* newsworthy only when attached to a *solve*; mathlib review latency.

**P13. Improve a construction in the AlphaEvolve "67 problems" list where AlphaEvolve only matched (not beat) the record.**
- (1) *Discovery:* a better packing/kissing/sum-free/overlap construction.
- (2) *Tools:* Georgiev–Gómez-Serrano–Tao–Wagner, "Mathematical exploration and discovery at scale" (67 problems; roughly 20 improved per a co-author's summary) — [arXiv 2511.02864](https://alphaxiv.org/overview/2511.02864v2); AlphaEvolve paper (kissing number 593 in 11D; minimum overlap) — [arXiv 2506.13131](https://arxiv.org/html/2506.13131v1); benchmark with automatic verification — [arXiv 2603.15617](https://arxiv.org/pdf/2603.15617); survey of computer-assisted graph theory — [arXiv 2508.20825](https://arxiv.org/pdf/2508.20825).
- (3) *Method:* local search / evolutionary search with an exact verifier; exploit problem-specific symmetry a generic agent missed; "results were strongest when subject experts guided the prompts" — [alphaXiv](https://alphaxiv.org/overview/2511.02864v2).
- (4) *Verification/recognition:* construction + exact-arithmetic check; arXiv; the FunSearch cap-set lineage (size-512 cap set in dim 8; asymptotic bound to 2.2202) shows how such records are recorded — [Wikipedia FunSearch](https://en.wikipedia.org/wiki/FunSearch).
- (5) *Effort:* 1–3 months.
- (6) *Saturation:* **crowded** — DeepMind, FunSearch replications and a dedicated benchmark all target the same tables; no 2025–26 cap-set change was found in searches.
- (7) *Risk:* improvements are tiny and need exact verification; compute asymmetry.

**P14. Polyform enumeration: add one term to a polyiamond/polyhex/polycube OEIS sequence.**
- (1) *Discovery:* a new verified count.
- (2) *Tools:* Shirakawa's Oct-2025 free-polyomino count to n=59 (Burnside + multithreading) — [arXiv 2510.22446](https://arxiv.org/html/2510.22446v1); Jensen's transfer-matrix method (background knowledge).
- (3) *Method:* transfer-matrix or Redelmeier-style enumeration with symmetry classes; parallelise.
- (4) *Verification/recognition:* OEIS editors; counts are cross-checked against fixed-count identities.
- (5) *Effort:* weeks; memory-bound.
- (6) *Saturation:* **some competition**; the n=59 extension itself was a single-author computation.
- (7) *Risk:* next terms may need cluster memory; low news value.

**Not recommended (time sinks or infeasible on a laptop).**
- Collatz: verification reached 2^71 (Jan 2025) using "thousands of parallel workers across several European supercomputers" — [Springer](https://link.springer.com/article/10.1007/s11227-025-07337-0), [HLF blog](https://scilogs.spektrum.de/hlf/a-collatz-conundrum/).
- Mersenne primes: M136279841 (Oct 2024) was found by Luke Durant with cloud GPUs; it "ends the 28-year run of ordinary personal computers finding these huge primes"; PopSci headline says he spent ~$2 million — [GIMPS](https://www.mersenne.org/primes/press/M136279841.html), [PopSci](https://www.popsci.com/science/largest-prime-number/).
- Wall–Sun–Sun / Wieferich primes: PrimeGrid's joint search ran Nov 2020–Dec 2022 with no find; earlier bound 9.7×10^14 (Dorais–Klyve) — [Wikipedia](https://en.wikipedia.org/wiki/Wall%E2%80%93Sun%E2%80%93Sun_prime).
- Exact R(5,5), BB(6) exact value, Goldbach/Riemann: see P6/P11 and KQ5/KQ8.

### Inferences
- Ranking by (feasibility × novelty × recognisability) for this student: P2 > P8 > P5 > P10 > P1 > P3/P4 > P6 > P12 > P7 > P9 > P11 > P14 > P13. P8 is the only "open niche" with a direct coursework match; P1 has the highest press ceiling ("student finds record tile") but the lowest success probability.
- Newsworthiness evidence: Quanta profiled an undergraduate (Barreto) and hobbyists solving Erdős problems with public LLMs; GIMPS finds reach CNN/Smithsonian; student OEIS entries reach institutional news pages; Life and Busy Beaver results stay on forums/wikis. So an Erdős-site credit or a record-table entry is the most "paper-covers-it" outcome.
- A reproducible pipeline (literature check → search → mechanical certificate → public record table) is what distinguished the credited individuals (Idén, Mian/Siddique, Barreto) from the discredited Oct-2025 claim.

### Gaps
- I could not read erdosproblems.com's own AI-contributions wiki or its tag list, so I cannot confirm an official "computational" tag or give per-category counts; the "tractable" marker is community-voted.
- Kaplan's tables of Heesch numbers for all polyforms up to a given size (which would define the fallback deliverable in P1) were not retrievable; current size frontier unknown.
- No source gives the current list of unsolved small permutation puzzles (P9) or the exact state of the Megaminx bound (sources conflict).
- Prize money: none found for Epoch FM:OP or for Erdős problems; GIMPS pays $3,000 per prime — [Heise](https://heise.de/en/news/M136279841-New-largest-known-Mersenne-prime-number-confirmed-with-GPU-9989146.html).

## Key question 1: Erdős problems — which have been solved by AI or amateurs since 2025, what was the "literature search" controversy, and what remains tractable?

### Takeaway
After a false start in Oct 2025 (GPT-5 "solved" ten problems that were already in the literature), 2026 brought genuine AI and hobbyist solves (#397, #728, #729 in Jan 2026; nine by AlphaProof Nexus in May; the unit-distance conjecture disproved by OpenAI in May), but Tao calls them "lowest hanging fruit" and puts the AI-accessible fraction of open problems at 1–2%; the remaining credited-individual lane is computational certificates on problems flagged "tractable".

### Cited Findings
- Oct 2025 controversy: an OpenAI VP posted that GPT-5 had found solutions to ten unsolved Erdős problems; Bloom refuted it, explaining the "open" status "simply meant he was unaware of published solutions" and the model had found existing papers; the post was deleted — [Hacker News](https://news.ycombinator.com/item?id=45633482), [Ilke News](https://ilkha.com/english/science-technology/openai-faces-backlash-over-false-claims-that-gpt-5-solved-erd%C5%91s-math-problems-486794), [36kr](https://eu.36kr.com/en/p/3517395760716937). A later item is titled "GPT-5.2 Erdős 281 already solved" (title only; suggests a second already-in-literature episode) — [aihola](https://aihola.com/article/gpt-5-2-erdos-281-already-solved).
- Jan 2026: GPT-5.2 Pro produced proofs for #397, #728 and #729, formalised in Lean and accepted by Tao; Neel Somani (software engineer, former quant) drove #397; Kevin Barreto (Cambridge undergraduate) with Liam Price drove #728 on Jan 4 2026 and checked it with Aristotle — [delante](https://delante.co/gpt-5-2-solves-erdos-problems/), [Medium](https://medium.com/@cognidownunder/three-erd%C5%91s-problems-fell-in-seven-days-and-terence-tao-verified-every-proof-himself-1a1ff4399bc6), [Quanta](https://www.quantamagazine.org/why-the-legendary-erdos-problems-are-falling-to-ai-20260803/). The #728 Lean writeup calls it "the first recognized Erdős problem solved autonomously by an AI system" and its author "received substantial assistance from ChatGPT in writing this manuscript" — [arXiv 2601.07421](https://arxiv.org/abs/2601.07421).
- Tao: early GPT-5.2 solves were "lowest hanging fruit"; some problems Erdős "clearly did not put much effort/thought into"; he "estimates 1-2% of open Erdős problems are currently accessible to AI methods with minimal human help"; "the more AI is involved in a solution, the simpler that solution tends to be" — [the-decoder](https://the-decoder.com/terence-tao-says-gpt-5-2-pro-cracked-an-erdos-problem-but-warns-the-win-says-more-about-speed-than-difficulty/), [besthub](https://www.besthub.dev/articles/why-ai-companies-are-racing-to-solve-erd-s-problems-3c15c05b2b48).
- Bloom (Quanta, Aug 2026): "most of the new results had come from hobbyists and undergraduates using publicly available LLMs" — [Quanta](https://www.quantamagazine.org/why-the-legendary-erdos-problems-are-falling-to-ai-20260803/); companion piece "How AI tore through a mathematical community" — [Quanta](https://www.quantamagazine.org/how-ai-tore-through-a-mathematical-community-20260803/).
- Labs: Feb 2026 DeepMind survey of ~700 open Erdős problems proved four; May 2026 an AlphaEvolve-like prover proved nine Erdős problems and 44 OEIS conjectures — [Wikipedia list](https://en.wikipedia.org/wiki/List_of_mathematical_discoveries_by_artificial_intelligence). AlphaProof Nexus: "9 out of 353 open Erdős problems and proved 44 out of 492 open conjectures from the OEIS", "a few hundred dollars per problem", arXiv May 21 2026, reported in Science Oct 8 2026 (secondary) — [the-decoder](https://the-decoder.com/google-deepminds-alphaproof-nexus-solves-decades-old-math-problems-for-a-few-hundred-dollars/), [cryptobriefing](https://cryptobriefing.com/deepmind-alphaproof-nexus-erdos-problems/), [arXiv 2605.22763](https://arxiv.org/pdf/2605.22763).
- May 20 2026: OpenAI announced an internal model's counterexample to Erdős's planar unit-distance conjecture (#90) — [TechCrunch](https://techcrunch.com/2026/05/20/openai-claims-it-solved-an-80-year-old-math-problem-for-real-this-time/), [phys.org](https://phys.org/news/2026-05-ai-major-breakthrough-math-problem.html), [The Conversation](https://theconversation.com/an-ai-solution-to-an-80-year-old-problem-has-shocked-mathematicians-283686), follow-up [arXiv 2605.20695](https://arxiv.org/html/2605.20695v1). Anthropic then ran "isolated Claude Code instances with Mythos access" on it; Sholto Douglas called the result a "cute, simple proof", Daniel Litt "a bit worse" than OpenAI's — [the-decoder](https://the-decoder.com/claude-mythos-reportedly-solves-openais-landmark-erdos-problem-with-a-cute-simple-proof/), [36kr](https://eu.36kr.com/en/p/3827354186847105).
- #119 "was resolved with GPT-5.6 and a mathematician, and Bloom verified it" — [besthub](https://www.besthub.dev/articles/why-ai-companies-are-racing-to-solve-erd-s-problems-3c15c05b2b48). #767 has a 2026 arXiv note "On Erdős Problem 767: Cycles with Chords" — [arXiv 2609.15330](https://arxiv.org/pdf/2609.15330). #647 has a "Kernel-Checked Exclusion Certificate" crediting individual computational contributors — [arXiv 2608.17880](https://arxiv.org/pdf/2608.17880).
- Counts: "1217 problems, of which 652 remain unsolved" (one snapshot) vs "1,135 problems total. About 680 remain open" (another) — [sharedcontext](https://sharedcontext.ai/skills/external/0bserver07/erdos-solver), [besthub](https://www.besthub.dev/articles/why-ai-companies-are-racing-to-solve-erd-s-problems-3c15c05b2b48).
- Tractability signals on the site: forum pages carry "This problem looks difficult" / "This problem looks tractable" and "currently working on it" fields — [forum 710](https://www.erdosproblems.com/forum/thread/710); a Claude Code skill already exists to query "Problems marked tractable by community" — [erdos-solver](https://sharedcontext.ai/skills/external/0bserver07/erdos-solver).
- Benchmarks: FrontierMath Erdős = 68 open Erdős problems "curated by Thomas Bloom and formalized in Lean"; "GPT-6 Astra scored 3%, and all others scored 0%" — [arXiv 2609.25050](https://arxiv.org/abs/2609.25050), [Epoch](https://epoch.ai/latest/announcing-frontiermath-erdos).

### Inferences
- The "easy" proof-style Erdős problems are being harvested quickly by labs and hobbyists alike; an undergraduate's edge is a careful computational certificate or a finite-case resolution, where the credit model (#647, #486) already exists.
- Given the Oct-2025 episode, the first deliverable of any Erdős project must be a documented literature search (Bloom's site + the problem's references), ideally posted on the forum before work starts.

### Gaps
- Could not read erdosproblems.com's AI-contributions wiki, so there is no verified per-category count (autonomous vs assisted) or a verified list of "computational" problems.
- Science publication of AlphaProof Nexus (Oct 8 2026) is from secondary coverage only.

## Key question 2: OEIS — amateur contributions, acceptance bar, and newsworthiness

### Takeaway
OEIS accepts refereed contributions from anyone, but the bar is "well-defined, of general interest, ideally infinite" with a 3-pending-submission cap because editors are overwhelmed; a new sequence is institution-newsletter news, not newspaper news, unless tied to a bigger story (an Erdős problem, a record).

### Cited Findings
- "a group of about 130 editors reviews submissions"; "all submissions are refereed" — [OEIS Foundation](https://oeisf.org/).
- A sequence "should be well-defined, of general interest and ideally infinite"; "submissions that seem arbitrary will be silently deleted" — [OEIS Welcome](https://oeis.org/wiki/Welcome), [FAQ](https://oeis.org/FAQ.html).
- Default cap of 3 pending submissions; "The limit was 7 from 2010 to 2019" and was lowered because "the editors were (and still are) drowning in submissions" — [OEIS wiki](https://oeis.org/wiki/Why_am_I_limited_to_3_submissions).
- Near-duplicates are usually rejected but may be accepted "when a non-matching term lies beyond term visibility" — [pre-submit checklist](https://oeis.org/wiki/Suggested_pre-submit_checklist); editors check "the logic and arithmetic" and style — [Instructions for Associate Editors](https://oeis.org/wiki/Instructions_For_Associate_Editors).
- Scale: "over 378,000 sequences", "11,000 citations" — [OEIS Welcome](https://oeis.org/wiki/Welcome).
- Keyword `hard`: "cannot reasonably be extended at all (but which is not known to be complete)"; extension "can only be done by new ideas, rather than more computation" — [Greathouse keyword page](https://www.oeis.org/wiki/User:Charles_R_Greathouse_IV/Keywords/difficulty). Example amateur extension: A032502 "a(27)-a(28) from Jeppe Stig Nielsen, Dec 21 2024" — [A032502](https://oeis.org/A032502).
- Student press examples: UACS dean + MSc student sequence on binary tree rolls — [UACS](https://uacs.edu.mk/home/?p=7513); Grade-12 student with two hexagonal-tiling sequences — [DAIS](https://www.dais.edu.in/aarnav-gogri-of-ibdp-publishes-math-research-in-OEIS.html).
- OEIS as a conjecture source for AI: DeepMind "formalized 492 open conjectures from the OEIS in the Lean proof assistant", resolved 44; a separate benchmark model "settled 147 of the 492" — [seqfan](https://groups.google.com/g/seqfan/c/gbb7MKvandc).

### Inferences
- The most defensible OEIS projects for this student are (a) sequences that encode an Erdős extremal function (links to the crowdsourced linking project) and (b) extensions of `more` sequences with a documented program — both are evaluated mechanically by editors.
- Because 448 of 492 formalised OEIS conjectures remain open after DeepMind's run, OEIS comments/conjectures are themselves a target list for small computational attacks.

### Gaps
- No quantitative data on how many new sequences per year come from amateurs, nor any 2025–26 policy change; the `hard` count (~7,500) comes from a paper excerpt whose exact source I could not confirm — [arXiv 2105.05111](https://arxiv.org/pdf/2105.05111).

## Key question 3: Tilings and discrete geometry after the hat and spectre

### Takeaway
The planar Heesch record (6) has not moved since 2021 and is now an Epoch open-problem target; 3D aperiodic monotiles (Sept 2026 preprint) and 3D Heesch bounds (Oct 2026) are the active frontier, with SAT-based polyform tools from Kaplan making computational attacks feasible.

### Cited Findings
- Heesch record 6 (Bašić 2021; Dave Smith family confirmed by Bašić and Bakker) — [Epoch](https://epoch.ai/frontiermath/open-problems/heesch-number), [arXiv 2610.02579](https://arxiv.org/html/2610.02579); Epoch asks for Heesch ≥ 7 with ≤ 200 cells — [Epoch](https://epoch.ai/frontiermath/open-problems/heesch-number).
- March 2026: Heesch number unbounded for hyperbolic convex monotiles — [arXiv 2603.27827](https://arxiv.org/abs/2603.27827).
- Sept 2026: "A Strongly Aperiodic Monotile in Three Dimensions" — polyhedral prototile whose tilings "always have finite symmetry groups", answering a request by Kaplan — [arXiv 2609.19214](https://arxiv.org/pdf/2609.19214).
- Oct 2026: "A Density Method for Bounding Heesch Numbers in E^3" — [arXiv 2610.02579](https://arxiv.org/html/2610.02579).
- Tools/surveys: SAT isohedral detection — [arXiv 2406.16407](https://arxiv.org/pdf/2406.16407); "The Path to Aperiodic Monotiles" — [arXiv 2509.12216](https://arxiv.org/pdf/2509.12216); hat paper with computer-assisted proof — [arXiv 2303.10798](https://arxiv.org/abs/2303.10798v3).
- Polyomino counts to n=59 (Oct 2025, single author, multithreaded) — [arXiv 2510.22446](https://arxiv.org/html/2510.22446v1).

### Inferences
- A Heesch-7 search is the one tiling project with real press potential; 3D polycube Heesch tables are a plausible open niche since the only 2026 3D work is a bounding method, not records.

### Gaps
- Could not retrieve Kaplan's Heesch-number tables or the Epoch problem's verifier details; no source states whether any AI system has attempted the Heesch problem.

## Key question 4: Graph theory and combinatorics — what AI has swept, what remains

### Takeaway
AlphaEvolve has taken the easy wins on classical Ramsey lower bounds, kissing numbers and packings, but cage graphs (eleven records improved by a human team in Nov 2025), multicolour/book/ordered Ramsey variants, and Hadwiger–Nelson certificates remain SAT-and-laptop territory.

### Cited Findings
- R(5,5) ≤ 46 (Angeltveit–McKay 2024, "linear programming and computer case-checking", replicated) with lower bound 43 (Exoo 1989) — [arXiv 2409.15709](https://www.arxiv.org/pdf/2409.15709); CMU SAT project on 45-vertex strongly regular graphs — [FAU abstract](https://www.math.fau.edu/combinatorics/abstracts/braginsky-57.pdf). "Improving R(3,k) in just two bites" — [arXiv 2510.19718](https://arxiv.org/pdf/2510.19718).
- AlphaEvolve Ramsey improvements (March 2026): nine per Wikipedia, five per a Medium explainer citing Nagda, Raghavan and Thakurta (e.g. R(3,13) 60→61) — conflict noted — [Wikipedia](https://en.wikipedia.org/wiki/List_of_mathematical_discoveries_by_artificial_intelligence), [Medium](https://medium.com/@AdithyaGiridharan/alphaevolve-just-moved-the-needle-on-ramsey-theory-and-that-is-a-very-big-deal-3750cf96b3ff), [DeepMind blog](https://deepmind.google/blog/alphaevolve-impact/).
- SAT-found multicolour bounds (Wesley, Sept 2025): R(K4,K4−e,K4−e) ≥ 35, R(K3,K4,C4,C4) ≥ 49, plus book Ramsey bounds — [arXiv 2509.03784](https://www.arxiv.org/abs/2509.03784); template graphs — [arXiv 2203.13476](https://arxiv.org/pdf/2203.13476); Gasarch's R3(L) ≥ 21 — [arXiv 2312.01159](https://arxiv.org/pdf/2312.01159); Kissat on ordered Ramsey numbers (2026) — [EmergentMind](https://www.emergentmind.com/papers/2604.16188).
- Cages: eleven improved upper bounds, n(4,10) ≤ 320 from 384; "some of the improved bounds had stood for 22 years"; House of Graphs cages directory — [arXiv 2511.07247](https://arxiv.org/abs/2511.07247v1), [EJC](https://www.combinatorics.org/ojs/index.php/eljc/article/view/v33i3p48); cubic girth-23–32 records via Cayley graphs — [EJC](https://www.combinatorics.org/ojs/index.php/eljc/article/view/v30i1p57).
- Hadwiger–Nelson: 5 ≤ χ ≤ 7; Heule's 510-vertex certificate; fractional ≥ 4 with no finite certificate — [Heule](https://focm2023.pages.math.cnrs.fr/files/confirmed/I3-05171-Heule.pdf), [arXiv 2311.10069](https://arxiv.org/html/2311.10069v4), [Aaronson](https://scottaaronson.blog/?p=3697).
- Graceful trees verified to 35 vertices (Fang 2010) — [arXiv 1003.3045](https://arxiv.org/pdf/1003.3045); Nov 2025 asymptotic "almost graceful" result — [arXiv 2511.11331](https://arxiv.org/abs/2511.11331v1).
- Cap sets: FunSearch's size-512 cap set in dimension 8 and asymptotic 2.2202 — [Wikipedia FunSearch](https://en.wikipedia.org/wiki/FunSearch); best upper bound improvement 2021 — [arXiv 2103.06481](https://arxiv.org/pdf/2103.06481). AlphaEvolve: kissing number 593 in 11D, minimum overlap — [arXiv 2506.13131](https://arxiv.org/html/2506.13131v1), [IEEE Spectrum](https://spectrum.ieee.org/deepmind-alphaevolve); 67-problem study (~20 improved) — [alphaXiv 2511.02864](https://alphaxiv.org/overview/2511.02864v2); ω < 2.371177 — [arXiv 2608.16884](https://arxiv.org/abs/2608.16884).
- Survey of computer-assisted graph theory (2025) — [arXiv 2508.20825](https://arxiv.org/pdf/2508.20825).

### Inferences
- Graceful-tree verification beyond 35 vertices is a natural "extend the record" project (last extension 2010), though news value is low; cages and Ramsey variants have the clearest publication path (EJC accepts such records).

### Gaps
- Exact list of which Ramsey numbers AlphaEvolve improved is unresolved (five vs nine); no 2025–26 kissing-number or sum-free amateur results were found.

## Key question 5: Number theory records — open, newsworthy, laptop-feasible?

### Takeaway
The headline number-theory records (Collatz range, Mersenne primes, Wall–Sun–Sun/Wieferich searches) are now supercomputer/GPU-farm territory and should be treated as time sinks; smaller OEIS-style prime/aliquot sequences remain extendable but are rarely newsworthy.

### Cited Findings
- Collatz verified to 2^71 (Jan 15 2025), "thousands of parallel workers across several European supercomputers", GPU algorithm "1 335× faster" — [Springer J. Supercomputing 81(1)](https://link.springer.com/article/10.1007/s11227-025-07337-0), [VUT](https://www.fit.vut.cz/research/publication/c197809), [HLF](https://scilogs.spektrum.de/hlf/a-collatz-conundrum/).
- GIMPS M136279841 (41,024,320 digits), Luke Durant, Oct 2024, GPUs; "$3000 award"; "ends the 28-year run of ordinary personal computers" — [GIMPS](https://www.mersenne.org/primes/press/M136279841.html), [Heise](https://heise.de/en/news/M136279841-New-largest-known-Mersenne-prime-number-confirmed-with-GPU-9989146.html), [Smithsonian](https://www.smithsonianmag.com/smart-news/amateur-mathematician-discovers-the-largest-known-prime-number-with-more-than-41-million-digits-180985321/), [PopSci](https://www.popsci.com/science/largest-prime-number/).
- Wall–Sun–Sun: none known; Dorais–Klyve to 9.7×10^14; PrimeGrid joint Wieferich/WSS search Nov 2020–Dec 2022 — [Wikipedia](https://en.wikipedia.org/wiki/Wall%E2%80%93Sun%E2%80%93Sun_prime), [t5k](https://t5k.org/glossary/xpage/WallSunSunPrime.html).
- Sociable numbers: Catalan–Dickson conjecture "still open, but generally thought to be false"; aliquot 3630 terminated after reaching 100 digits — [Wikipedia](https://en.wikipedia.org/wiki/Sociable_number), [Moews](https://www.djm.cc/amicable.html), [core.ac.uk](https://core.ac.uk/works/16969909).

### Inferences
- An individual cannot plausibly win a Mersenne prime on a laptop in 2026; number-theory effort is better spent on OEIS `more` prime-form sequences (P4) or Erdős number-theory problems with finite checks (P2).

### Gaps
- No 2025–26 sources found on amicable/sociable records, aliquot 276, perfect cuboid bounds, Lehmer's totient bound, or PrimeGrid 2026 status; search budget was exhausted before these could be retried.

## Key question 6: Group theory and permutation puzzles (coursework match)

### Takeaway
Finite-group census tables are maintained by a handful of specialists and have been found to contain errors, making audits/extensions with GAP an open niche; puzzle diameters (4×4×4, Megaminx) are open but exact values are beyond laptops.

### Cited Findings
- Perfect groups to 2·10^6: 15,768; five previously overlooked groups found — [arXiv 2104.10828](https://arxiv.org/pdf/2104.10828); groups whose orders have ≤ 4 prime factors, GAP implementation — [arXiv 2012.02933](https://arxiv.org/pdf/2012.02933); (2,3)-groups to order 6,000,000 — [arXiv 1505.00888](https://ar5iv.arxiv.org/html/1505.00888); group numbers known for n ≤ 2000 and most n ≤ 20000; 423,164,062 groups for orders ≤ 2000 excl. 1024 — [ICMS 2026](https://icms-conference.org/2026/papers/pleanary1/main.pdf); OEIS A392130 revised Jan 2026 — [A392130](https://oeis.org/A392130/internal).
- Puzzle diameters: 4×4×4 "[22, 36] HTM", "[35, 53]" QTM; 5×5×5 "[20, 32]"; Megaminx open — [cuberoot](https://cuberoot.me/math/group/open-problems), [rubiks.fandom](https://rubiks.fandom.com/wiki/God%27s_Number), [HKHLR](https://www.hkhlr.de/node-export/pdf/4006).

### Inferences
- Cayley-graph constructions for cages (P5) and group census audits (P8) use exactly MAT301 material; both have mechanical verification.

### Gaps
- No sources on Hurwitz groups, Latin-square records, symmetric Latin squares or small-cancellation examples were found before the search budget ran out.

## Key question 7: Formalization — is a Lean contribution recognised/newsworthy for an undergrad?

### Takeaway
Lean work is recognised (repo credits, arXiv writeups) and undergraduates routinely contribute to mathlib, but it becomes newsworthy only when it certifies a new solve, as with #728.

### Cited Findings
- Formal Conjectures benchmark paper — [arXiv 2605.13171](https://arxiv.org/pdf/2605.13171); third-party credit example (#258: "proof by Chojecki and GPT-5.4 Pro, formalised in Lean by ster-oc") — [GitHub](https://github.com/google-deepmind/formal-conjectures/blob/main/FormalConjectures/ErdosProblems/258.lean).
- "Advancing Mathematics Research with AI-Driven Formal Proof Search" (9 of 353 Erdős problems; statements checked by human experts) — [arXiv 2605.22763](https://arxiv.org/pdf/2605.22763).
- mathlib: >210,000 theorems (May 2025) — [Wikipedia Lean](https://en.wikipedia.org/wiki/Lean_(proof_assistant)); undergraduate contributions and small-PR review culture — [arXiv 2110.03551](https://arxiv.org/pdf/2110.03551); remaining gaps "differential geometry, partial differential equations, numerical analysis" and graph theory concepts — [UW Math AI Lab Spring 2026](https://sites.math.washington.edu/ai/spring2026.html), [DIMACS REU 2026](https://archive.reu.dimacs.rutgers.edu/2026/js4426/public_html).
- Lean Atlas (human–AI formalisation environment) — [arXiv 2604.16347](https://arxiv.org/pdf/2604.16347); #728 Lean proof writeup — [arXiv 2601.07421](https://arxiv.org/abs/2601.07421).

### Inferences
- Pairing P2 (a computational result) with a Lean kernel certificate is the strongest combination: it is exactly the format that got individuals cited in [arXiv 2608.17880](https://arxiv.org/pdf/2608.17880).

### Gaps
- The Xena Project's Dec-2025 post on formalising Erdős problems was referenced but not readable; could not access the Formal Conjectures README for contribution rules.

## Key question 8: Recreational and computational records (Busy Beaver, Life, Langton's ant, sandpiles)

### Takeaway
BB(6) is effectively out of reach (Antihydra), but holdout-decider work is ongoing and credited; Life remains a productive hobbyist niche (Annelid 2026); Langton's ant highway and sandpile limit-shape conjectures are open but proof-level, not search-level.

### Cited Findings
- BB(6) unsolved; Antihydra makes it Collatz-like; champion mxdys June 2025, Σ(6) > 10↑↑10↑↑10↑↑8 (table figures inconsistent); holdouts 855 (Sept 16 2026) from 1,104 (Apr 29 2026) — [BB(6) wiki](https://wiki.bbchallenge.org/wiki/BB(6)), [holdouts](https://wiki.bbchallenge.org/wiki/Holdouts_lists), [TMBR Feb 2026](https://wiki.bbchallenge.org/wiki/TMBR:_February_2026), [Aaronson](https://scottaaronson.blog/?p=8972).
- Life: Annelid (28,3)c/84, Brithos, 22 June 2026, ~168.8M cells — [LifeWiki](https://conwaylife.com/wiki/Annelid), [forum](https://conwaylife.njohnston.ca/forums/viewtopic.php?p=230298); Copperhead found by a forum newcomer (2016) — [Wikipedia](https://en.wikipedia.org/wiki/Spaceship_(cellular_automaton)).
- Langton's ant: highway conjecture unproven — [101computing](https://www.101computing.net/?p=6873); LLLR note June 2025 — [arXiv 2506.10482](https://arxiv.org/abs/2506.10482v1). Sandpile limiting shape open — [Verbitskiy](https://pub.math.leidenuniv.nl/~gaansowvan/BASB2013/BASB-verbitskiy-sandpile.pdf); "simply stated conjectures ... remain open" — [TCS 2020](https://halshs.archives-ouvertes.fr/halshs-02884875v1/file/S0304397520303601.pdf).

### Inferences
- Among recreational targets only Life (P10) offers a realistic weeks-scale new object with instant community verification.

### Gaps
- Omniperiodicity of Life (p19/p41, Dec 2023) and BB(3,3)/BB(2,5) status were not retrievable in this session (background knowledge only, unverified).

## Key question 9: 2025–2026 examples of individuals using AI agents to get credited results, and coverage

### Takeaway
There are now several named, credited individuals — an undergraduate (Barreto), a software engineer (Somani), and computational contributors (Idén; Mian & Siddique) — whose LLM-assisted Erdős results were covered by Quanta, TechCrunch, phys.org and The Conversation; no documented case of a student using *Claude Code specifically* was found, though Anthropic itself ran Claude Code swarms on the unit-distance problem.

### Cited Findings
- Barreto (Cambridge undergraduate) + Price, GPT-5.2 Pro, #728, Jan 4 2026, Aristotle check — [Quanta](https://www.quantamagazine.org/why-the-legendary-erdos-problems-are-falling-to-ai-20260803/); Somani on #397 — [delante](https://delante.co/gpt-5-2-solves-erdos-problems/).
- Individually credited computational work on #647 and #486 — [arXiv 2608.17880](https://arxiv.org/pdf/2608.17880).
- Anthropic's Claude Code + Mythos multi-instance run on the unit-distance conjecture — [the-decoder](https://the-decoder.com/claude-mythos-reportedly-solves-openais-landmark-erdos-problem-with-a-cute-simple-proof/).
- Coverage venues: [Quanta](https://www.quantamagazine.org/why-the-legendary-erdos-problems-are-falling-to-ai-20260803/), [TechCrunch](https://techcrunch.com/2026/05/20/openai-claims-it-solved-an-80-year-old-math-problem-for-real-this-time/), [phys.org](https://phys.org/news/2026-05-ai-major-breakthrough-math-problem.html), [The Conversation](https://theconversation.com/an-ai-solution-to-an-80-year-old-problem-has-shocked-mathematicians-283686); surveys of the field — [arXiv 2607.07779](https://arxiv.org/pdf/2607.07779), [arXiv 2608.24961](https://arxiv.org/pdf/2608.24961).

### Inferences
- The press pattern is "student/hobbyist + public model + maintainer verification (Bloom/Tao) + Lean"; replicating that pattern with Claude Code on a computational certificate is the most credible route to a "U of T student finds..." story.

### Gaps
- No source found describing an undergraduate using Claude Code for a credited result; the search budget was exhausted before targeted queries on Idén/Mian/Siddique could run.
