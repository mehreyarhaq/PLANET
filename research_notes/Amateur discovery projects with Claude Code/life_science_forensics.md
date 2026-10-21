# Amateur discovery projects in life sciences, public-health data, bioacoustics and scientific data forensics (laptop + Claude Code + open data; Toronto/Ontario angle)

Research date: 2026-10-21. Scope: what a Toronto undergraduate mathematics student with a laptop, Claude Code, free open data, no lab, no clinical access and no supervisor could plausibly discover in weeks to months, have confirmed by an expert, and get covered by a local or campus paper. Each key question below is followed by a vetted shortlist (final section) with 15 candidate projects, each rated for saturation with the evidence behind the rating.

Method note: ~35 web searches plus one failed page fetch and one failed Firecrawl scrape. Primary pages at heise.de, chemistryworld.com and secondthoughts.ai could not be fetched (DNS failure / no Firecrawl credits), so those items rely on search-result excerpts. Where I could not find prior work I say so rather than claiming novelty.

## Key Question 1: Data-forensics precedents (Bik, Data Colada, GRIM/SPRITE, statcheck, Sholto David, Black Spatula, YesNoError, AI-reviewer studies), public tools, remaining niches, ethical rules

### Takeaway
Research-integrity sleuthing by individuals has a strong track record (Dana-Farber retractions and a US$15M settlement from one blogger's post; Data Colada's exposure of Gino; GRIM/statcheck mass screens), and since 2025 LLM-based projects (Black Spatula, YesNoError, academic "AI checkers") have industrialised calculation-error hunting. The open niche for an amateur is not "scan everything" but a bounded, verifiable corpus (a specific journal, country or field nobody has screened) with human verification and author contact first; the ethical floor is PubPeer's rule of checkable facts without intent claims.

### Cited Findings
- Sholto David, a British molecular biologist and blogger, posted on 2 January 2024 about image irregularities in 30 papers from Dana-Farber scientists (including the CEO and COO); Dana-Farber retracted seven papers and corrected 31; in December 2025 Dana-Farber agreed to pay US$15 million to settle fraud allegations and David received 17.5% as whistleblower (~US$2.6M) — [Wikipedia: Sholto David](https://en.wikipedia.org/wiki/Sholto_David); figures on the number of affected studies differ (one article says >58) — [Wikipedia: Dana-Farber](https://en.wikipedia.org/wiki/Dana%E2%80%93Farber_Cancer_Institute)
- Data Colada: on 11 Sept 2024 a federal judge dismissed all of Francesca Gino's claims (defamation and others) against the Data Colada bloggers; Gino was ruled a public figure requiring proof of "actual malice by clear and convincing evidence"; her breach-of-contract claim against Harvard survived — [Poets&Quants](https://poetsandquants.com/2024/09/12/judge-dismisses-francesca-ginos-defamation-claims-against-harvard-data-colada/); Harvard revoked Gino's tenure in May 2025 — [NBC](https://www.nbcnewyork.com/news/national-international/harvard-revokes-tenure-from-professor-ethics-studies/6278474/); [Wikipedia: Data Colada](https://en.wikipedia.org/wiki/Data_Colada)
- GRIM tests whether a reported mean is possible given N and data granularity; SPRITE reconstructs possible datasets from mean, SD, N and bounds and works at larger N; statcheck recomputes p-values from APA-style test statistics and flags mismatches; a flag "is a signal worth investigating, not proof of misconduct" — [CASRAI guide](https://casrai.org/guides/statistical-fraud-detection-grim-sprite-statcheck); Dorothy Bishop recommends GRIM and SPRITE; Jack Wilkinson: "Question whether the p-value they've reported is even compatible with the summary data" — [Chemistry World, How to be a science sleuth](https://www.chemistryworld.com/careers/how-to-be-a-science-sleuth/4023176.article)
- statcheck is an R package (v1.5.0, Feb 2024) that scans a PDF/HTML file or a folder of them, but reads only APA-style reporting; a web version exists at statcheck.io — [CRAN refman](https://ftp.fau.de/cran/web/packages/statcheck/refman/statcheck.html); [statcheck.io](https://statcheck.io/); Nuijten et al. screened ~30,000 psychology articles (1985–2013) and about half of papers with NHST results had at least one inconsistency; a 2024 Nuijten & Wicherts paper links statcheck use in peer review at Psychological Science to a sustained drop in inconsistencies — [PMC7540394](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7540394/)
- Black Spatula Project: open-source, volunteer-run, had reviewed ~500 papers by early 2025, does not publish findings but contacts authors directly; reports ~10% false positives; tested prompts with OpenAI o1 and Claude 3.5. YesNoError (founder Matt Schlicht, funded by its own cryptocurrency) scanned >37,000 papers in ~2 months and flags publicly; of 100 flagged math errors, all responding authors but one confirmed the error; critics worry about reputational harm and floods of trivial flags — [heise](https://www.heise.de/en/news/No-more-calculation-errors-AI-checks-papers-for-errors-Why-that-s-not-enough-10321469.html); [Black Spatula Day Five (Steve Newman)](https://secondthoughts.ai/p/black-spatula-day-five); [JKMS editorial 2025](https://jkms.org/DOIx.php?id=10.3346%2Fjkms.2025.40.e342); per-paper analysis cost "15 cents to a few dollars" — [Academica summary of Nature piece](https://academica.ca/top-ten/how-ai-tools-are-being-used-to-identify-errors-in-research-papers-opinion/)
- A later Nature piece (reported August 2026) says AI agents checking the literature are finding decades-old errors in papers and reference databases, including a 75-year-old wrong boiling-point value in a widely used chemistry database; tools catch objective errors (typos, units, calculations) "only after humans verify the source and rerun checks" — [TagTeam feed of Nature article](https://tagteam.harvard.edu/hub_feeds/4669/feed_items/18613215); [Bibby summary](https://trybibby.com/blog/nature-reports-ai-agents-finding-longstanding-errors-in-research) (aggregators; Nature original not fetched)
- "To Err Is Human" (Bianchi, Zou et al., Dec 2025): a GPT-5-based checker on published AI papers; of 316 flagged items experts confirmed 263 real mistakes (precision 83.2%); mistakes per paper rose from 3.8 (NeurIPS 2021) to 5.9 (NeurIPS 2025) — [arXiv 2512.05925](https://arxiv.org/abs/2512.05925); a 45-expert evaluation of AI reviewers on Nature-family papers found AI reviewers 6–10 points less correct than the top human reviewer (GPT-5.2 at 86.2% vs 92.3%) but raising more significant issues — [arXiv 2605.20668](https://arxiv.org/html/2605.20668); FLAWS benchmark of 713 paper–error pairs — [arXiv 2511.21843](https://arxiv.org/pdf/2511.21843)
- Image tools: ImageTwin and Proofig are subscription products (reported ~US$27/article and US$35–50/manuscript in 2024); a few sleuths (e.g., Jana Christopher) got free ImageTwin access in exchange for feedback; no general free-access programme for independent sleuths was found; Proofig is strong on Western blots, ImageTwin on overlapping microscopy; MDPI signed with Proofig (Sept 2025) and ASM piloted ImageTwin — [AI Insider 2023](https://theaiinsider.tech/2023/10/10/ai-beats-human-sleuth-at-finding-problematic-images-in-research-papers/); [Science Integrity Digest FAQ (Bik)](https://scienceintegritydigest.com/frequently-asked-questions/); [Olhar Digital 2024](https://olhardigital.com.br/2024/03/21/pro/detetives-de-dados-softwares-estao-ajudando-a-detectar-manipulacao-de-imagens-em-pesquisas/); [CASRAI news](https://casrai.org/news/ai-image-integrity-screening-mdpi-asm-adoption); [MSKCC pilot](https://library.mskcc.org/blog/?p=35262)
- PubPeer norms: comments must stick to checkable facts; "an image looks rearranged" is acceptable, "authors deliberately pasted in a band" is not; the FAQ tells commenters to imagine defending the truth of each statement in court and to avoid speculating about motives; PubPeer expects to be sued for libel one day — [PubPeer misconduct page](https://pubpeer.com/static/misconduct); [PubPeer FAQ](https://pubpeer.com/faq)
- Sarkar v. Does (2014–): Wayne State researcher sued anonymous PubPeer commenters; PubPeer argued "look similar" is subjective opinion and not actionable; a later Wayne State investigation found Sarkar responsible for image manipulation — [Public Citizen](https://www.citizen.org/litigation/sarkar-v-does/); [Retraction Watch 2014](https://retractionwatch.com/2014/12/10/pubpeer-files-motion-dismiss-sarkar-defamation-case); [The Scientist](https://www.the-scientist.com/pubpeer-requests-that-court-consider-misconduct-investigation-32668); a 2023 Harvard professor's complaint that PubPeer comments were used to "defame and badger" him — [Retraction Watch 2023](https://retractionwatch.com/2023/12/04/cyberstalking-pits-harvard-professor-against-pubpeer); in 2021 French researchers filed a police complaint against Bik for harassment; it never led to legal action — [FAPESP](https://revistapesquisa.fapesp.br/en/the-limits-of-anonymous-accusations/)
- An individual mathematician revised a preprint after "an adversarial review by Claude" found a wrong inequality, wrong constant and wrong letter; disclosed in the paper's AI statement (revision Aug 2026) — [arXiv 2504.02795](https://arxiv.org/pdf/2504.02795)
- Canadian integrity cases exist but are older: Western University dismissed cardiovascular researcher Morris Karmazyn after image problems raised by a former lab member; University of Toronto husband-and-wife team investigated for images/data (third retraction); University of Ottawa investigation led to four JBC retractions — [Retraction Watch Canada category](https://retractionwatch.com/category/by-country/canada/page/14); a 2025 US example: eight Duke papers retracted for alleged image duplication — [Retraction Watch 2025](https://retractionwatch.com/2025/09/29/duke-scientists-lose-eight-papers-for-alleged-image-manipulation/)

### Inferences
- Image-duplication sleuthing is the most precedent-rich and press-covered path (Bik, David) but is now crowded, tool-gated (paid software) and carries the highest legal/ethical exposure; it is the worst fit for an unsupervised undergraduate unless restricted to factual PubPeer comments on a small set of papers.
- Numerical forensics (GRIM/SPRITE/statcheck) remains tractable with free tools and Claude Code; mass screens exist only for psychology, so a bounded screen of Canadian health/psychology journals or of a field never screened (e.g., kinesiology, nursing, nutrition) is a defensible "open niche" absent contrary evidence (see Gaps).
- LLM error hunting is crowded at the "scan the whole literature" level (YesNoError, Black Spatula, academic checkers, Nature-reported agents). The differentiator for an amateur is (a) a corpus nobody has claimed (e.g., Ontario-affiliated medRxiv preprints), (b) rigorous human verification, (c) author contact before publicity, mirroring Black Spatula's norm.
- The safest publishable output is a methods-style report ("X% of papers in journal Y have reporting inconsistencies; here are N corrected") rather than individual accusations; this is how Nuijten and Ziemann got coverage.

### Gaps
- Could not fetch the heise, Chemistry World or Second Thoughts pages directly; details come from search excerpts.
- No source found on YesNoError's 2026 status (search returned only a token-listing page), nor on Black Spatula's current activity level.
- No evidence found either way on whether anyone has run statcheck/GRIM across Canadian journals or medical journals in 2024–2026; "open niche" rating is based on absence of evidence.
- The Nature August 2026 "AI agents" article could not be read directly; details (75-year-old boiling point) come from aggregators.

## Key Question 2: Public-dataset error precedents and unscrutinised Canadian/Ontario datasets

### Takeaway
Precedents show that a student replicating a famous result (Herndon/Reinhart–Rogoff) or scanning supplementary files for mechanical corruption (Ziemann's Excel gene-name errors, 30.9% of papers) can produce an internationally covered finding; reference databases (GenBank/RefSeq contamination in >2M entries; AlphaFold DB staleness) are documented as error-prone and "relatively unmitigated". For Canada, the clearest under-analysed public datasets are the brand-new national wastewater drug dashboard (Dec 2025) and Ontario Health's ED-time series that just had a comparability break (Dec 2025).

### Cited Findings
- Thomas Herndon (UMass Amherst PhD student) found in April 2013, while trying to replicate Reinhart–Rogoff for a class project, that a spreadsheet omitted Australia, Austria, Belgium, Canada and Denmark; corrected growth for >90% debt was 2.2% not −0.1%; the authors admitted a "coding error" — [Chronicle](https://www.chronicle.com/article/UMass-Graduate-Student-Talks/138763); [Chronicle (spreadsheet error)](https://www.chronicle.com/article/they-said-at-first-that-they-hadnt-made-a-spreadsheet-error-when-they-had/); [NPR](https://www.npr.org/transcripts/177721491)
- Ziemann group's 2021 PLoS Comp Biol follow-up screened PMC supplementary files 2014–2020 and found Excel gene-name conversion errors in 30.9% (3,436/11,117) of articles with supplementary Excel gene lists, worse than the ~20% found in 2016; HGNC renamed the worst genes (SEPT2, MARCH1) — [DOAJ record, PLoS Comp Biol 2021](https://doaj.org/article/8b429b7b5d454a8c9aeef110207e3418); [TechXplore](https://techxplore.com/news/2021-08-excel-autocorrect-errors-plague-genetic.pdf); 2016 original — [PMC5359807](https://pmc.ncbi.nlm.nih.gov/articles/5359807)
- Conterminator (Steinegger & Salzberg, Genome Biology 2020) flagged 2,161,746 contaminated sequences in RefSeq, 114,035 in GenBank and 14,148 in NR; >95% of GenBank contamination was in eukaryotic genomes — [PMC7218494](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7218494/); a 2024 review says contamination "remains relatively unmitigated in most analyses" and lists taxonomic errors and sequence-content errors as other common reference-database issues — [Frontiers in Bioinformatics 2024](https://frontiersin.org/articles/10.3389/fbinf.2024.1278228)
- ML benchmark label errors: an MIT-led study estimated an average 3.4% of test-set labels wrong across 10 widely used datasets — [MIT Technology Review](https://www.technologyreview.com/2021/04/01/1021619/ai-data-errors-warp-machine-learning-progress/amp/); [AI Business](https://aibusiness.com/ml/machine-learning-benchmarks-revealed-to-contain-pervasive-labeling-errors)
- Ontario ED wait times: Ontario Health's public "Time Spent in Emergency Departments" reporting (source: CIHI NACRS) lists January 2026 average wait to first physician assessment of 1.7 hours; "as of the December 2025 data refresh, 43 additional sites were added ... Data exported after this time should not be compared to any data exported earlier" — [Ontario Health](https://ontariohealth.ca/system/reporting/performance/time-spent-in-emergency-departments); the record-level ERNI dataset on data.ontario.ca is restricted (personal health information) — [data.ontario.ca ERNI](https://data.ontario.ca/en/dataset/emergency-room-national-ambulatory-reporting-system-initiative-erni); HQO pages now redirect attribution to Ontario Health — [HQO](https://www.hqontario.ca/System-Performance/Time-spent-in-emergency-departments)
- A CCPA study (May 2026) reported 90% of Ontario ER patients waited up to 4.5 hours for initial physician assessment in 2024/25, up from 2.7 hours in 2020/21, and 55% of hospitals ran deficits in 2024-25 — [CP24](https://www.cp24.com/local/toronto/2026/05/11/under-immense-strain-wait-times-at-ontario-emergency-rooms-have-spiked-over-past-5-years-study-says/); Fraser Institute's 2025 median referral-to-treatment wait: 28.6 weeks — [HR Reporter](https://www.hrreporter.com/focus-areas/payroll/lost-economic-output-medical-wait-times-in-canada-still-at-286-weeks-in-2025/393843); CIHI (2010) warned inter-provincial wait-time differences may reflect definitions rather than real waits — [CMAJ 2010](https://www.cmaj.ca/content/182/8/E340)
- Health Canada launched the National Wastewater Drug Surveillance dashboard in December 2025 with data from seven provinces/territories (incl. Ontario), Jan 2023–Jul 2025, quarterly updates — [Health Canada](https://www.canada.ca/en/health-canada/news/2025/12/health-canada-launches-national-wastewater-drug-surveillance-dashboard-to-inform-overdose-crisis-response-and-to-share-data-on-drug-use-in-canada.html); [CP24](https://www.cp24.com/news/canada/2025/12/04/new-public-dashboard-shows-drug-use-data-through-wastewater-analysis/); Toronto publishes overdose surveillance dashboards — [toronto.ca/OverdoseData](https://toronto.ca/OverdoseData); a 2025 Frontiers paper found Ontario unregulated-substance data "fragmented, inconsistently collected, and poorly shared" — [Frontiers in Public Health 2025](https://www.frontiersin.org/articles/10.3389/fpubh.2025.1477539/full); a Durham Region study tracked opioids via 24-h composite samples at six plants — [Laurentian SETAC abstract](https://laurentiansetac.ca/abstracts-2024-chemistry-method-dev/tyler-dow)
- Drug Shortages Canada database: mandatory manufacturer reporting since March 2017; 23.4% of prescription drugs reported in shortage in 2017–18 — [CTV](https://www.ctvnews.ca/health/nearly-a-quarter-of-drugs-marketed-in-canada-reported-shortages-study-1.5088570?cache=); 44.7% (n=5,953) had ≥1 shortage event over five years; single-generic-manufacturer markets most vulnerable; shortages peaked at 2,345 in April 2020 — [CMAJ 2022](https://www.cmaj.ca/content/194/23/E801); [PMC8091649](https://pmc.ncbi.nlm.nih.gov/articles/PMC8091649); [PMC9262135](https://pmc.ncbi.nlm.nih.gov/articles/PMC9262135); a JAMA-reported comparison found only 34% of Canadian shortage reports led to actual shortages in 2023–24 — [Pharmaceutical Commerce](https://www.pharmaceuticalcommerce.com/view/study-supply-chain-issues-less-likely-result-drug-shortages-canada-compared-united-states); [UBC summary](https://www.advancinghealth.ubc.ca/research-in-action/one-quarter-of-prescription-drugs-in-canada-may-be-in-short-supply/)

### Inferences
- The Ontario Health December 2025 comparability break is a ready-made, low-risk watchdog project: check whether any public report, news article or political statement in 2026 compared pre- and post-refresh ED numbers (which Ontario Health itself says is invalid). It needs only scraped monthly tables and careful documentation.
- The national wastewater drug dashboard is less than a year old and quarterly; nobody outside government has had time to cross-correlate it with municipal overdose/EMS data, so the niche is open by timing (no contrary evidence found).
- Drug Shortages Canada is academically well-studied (UBC, CMAJ) so the "general patterns" angle is some-competition; a timely 2025–26 update or an Ontario-specific/single-manufacturer watch list is still plausible and newsworthy.
- Reference-database integrity (GenBank/BOLD mislabels, AlphaFold staleness) is documented as a problem but mitigated mostly by big-lab tools; focused, taxon-specific audits by an individual are plausible contributions.

### Gaps
- No case found of an amateur finding an error in Statistics Canada, Our World in Data or NOAA data (one search; absence of evidence, not evidence of absence).
- I did not verify specific download endpoints on data.ontario.ca, Public Health Ontario or CIHI for open aggregate tables; only the Ontario Health reporting page and the restricted ERNI entry were confirmed.
- No source found on whether Ziemann's group has published a 2024–2026 update of the gene-name scan.

## Key Question 3: Genomics and proteins (SRA metagenomes, unannotated genes, AlphaFold DB anomalies); credited outsider findings 2024–2026

### Takeaway
Bulk novel-virus discovery in SRA is crowded (Serratus: 132,260 novel RNA-virus species-like units; Kawasaki: ~900 hidden infections; German HPC group: >150k viral sequences), but Logan (2024) now exposes an SRA-wide k-mer index that answers arbitrary queries in under 5 minutes, making targeted laptop-scale searches realistic; AlphaFold DB has documented staleness and misprediction issues (295 sequence-length mismatches; 188k–2.4M possibly mismodelled knotted proteins) but no comprehensive audit. I found no 2024–2026 case of a non-academic getting a credited genomics finding this way.

### Cited Findings
- Serratus (Nature 2022, Edgar et al.) searched 5.7M samples / 10.2 petabases for RdRP and reported 132,260 novel species-like units (>10% diverged), a 9.8× increase over ~15,000 known RNA viruses — [Nature via IDEAS](https://ideas.repec.org/a/nat/nature/v602y2022i7895d10.1038_s41586-021-04332-2.html); [Broad Institute](https://www.broadinstitute.org/node/1137491); [AWS blog](https://aws.amazon.com/blogs/publicsector/preventing-next-pandemic-how-researchers-analyze-millions-genomic-datasets-with-aws); the project began at a UBC hackathon proposed by Artem Babaian, then "an independent researcher" — [UBC CIC](https://cic.ubc.ca/?p=2713); the successor "Open Virome" is described at — [UBC CIC](https://cic.ubc.ca/?p=3115)
- Kawasaki et al. (mBio 2021) screened 33 RNA viral families in public mammalian/avian data and found ~900 hidden infections and five novel viruses — [DOAJ](https://doaj.org/article/d47b6c171b3845e9ac2574fd3e02fd53); a German HPC group analysed >1M SRA datasets and found >150k viral sequences — [NHR](https://nhr-verein.de/en/node/126); Institut Pasteur's method discovered novel coronavirus families from public data — [Pasteur](https://www.pasteur.fr/en/home/research-journal/news/innovative-genomic-data-analysis-method-leads-discovery-novel-coronavirus-families)
- Logan (Chikhi et al.): assembly of 96% of SRA as of December 2023 (~27M accessions), 44.1 petabases reduced to 0.9 petabases of contigs; Logan-Search is a k-mer index that searches a query against the full unitig index "in less than 5 min" with hits mapped to geographic origin; data hosted free on AWS Open Data with tutorials on GitHub — [PMC12424806](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC12424806/); [GitHub IndexThePlanet/Logan](https://github.com/IndexThePlanet/Logan); [AWS listing](https://aws.amazon.com/marketplace/pp/prodview-rlhwd2eacntxo)
- AlphaFold DB: "The AlphaFold Database Ages" preprint finds models built on April 2021 sequences diverge from current UniProt, with 295 sequence-length mismatches — [bioRxiv 2025](https://www.biorxiv.org/content/10.1101/2025.06.22.660930.full.pdf); [PMC7618723](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7618723/); a knot-theory preprint estimates 188,320 to 2,379,680 AFDB proteins incorrectly modelled (extrapolated from knotted-protein misprediction rates) — [arXiv 2412.11229](https://arxiv.org/pdf/2412.11229); a late-2025 whole-proteome QA preprint notes reports of wrong predictions "have so far remained anecdotal" — [bioRxiv "Fold or flop"](https://www.biorxiv.org/content/10.64898/2025.12.19.695427.full.pdf); AlphaFold3 "hallucinations" at 22% of residues for disordered proteins — [arXiv 2510.15939](https://arxiv.org/html/2510.15939v2)
- GenBank/RefSeq contamination and taxonomic-error findings: see KQ2 ([PMC7218494](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7218494/); [Frontiers 2024](https://frontiersin.org/articles/10.3389/fbinf.2024.1278228))

### Inferences
- "Find a new virus in SRA" as a headline is crowded; "find where a specific, locally relevant pathogen (e.g., a tick-borne or wildlife virus of Ontario interest) shows up unexpectedly in public data" via Logan-Search is a tractable, targeted variant with a Toronto angle, confirmable by virologists.
- AlphaFold DB staleness audits for one proteome (listing models whose sequences no longer match UniProt, or implausible knots) are feasible with the free AFDB and UniProt downloads, but the payoff is a database correction and a campus-paper story rather than a mainstream one.
- The Serratus founder's current affiliation (reportedly University of Toronto) would be an ideal Toronto confirmation route, but I did not verify it in this research (see Gaps).

### Gaps
- No search result documented a 2024–2026 credited genomics finding by a non-academic from public data; "open niche" vs "crowded" here rests on precedent absence.
- Artem Babaian's current affiliation was not verified; sources only call him an "independent researcher" at the UBC hackathon.
- Whether a Logan release newer than the Dec 2023 freeze exists was not checked.
- "Unannotated gene" and GWAS-Catalog/Open Targets re-analysis angles were not searched; no evidence collected.

## Key Question 4: Bioacoustics and biodiversity (Xeno-canto, Macaulay, iNaturalist audio, BirdNET, Perch); amateur precedents; Ontario angle

### Takeaway
Citizen audio has already produced real taxonomic outputs: a new cricket species (Indigryllus sagani) was described after iNaturalist observations, an iNaturalist user found three first US state records for crickets in one week by browsing audio observations, and iNaturalist photos produced the first Canadian record of a crayfish in Windsor, Ontario. Google's Perch 2.0 (Aug 2025) adds vector search over sound embeddings and helped find a new Plains-wanderer population. No systematic ML audit of Xeno-canto/Macaulay labels or an Ontario-focused audio first-record hunt was found, so those are open niches.

### Cited Findings
- Xeno-canto has >575,000 recordings of >10,000 species; identifications are crowd-validated — [Wikipedia: Xeno-canto](https://EN.wikipedia.com/wiki/Xeno-canto); 170,000 sound records added to GBIF — [GBIF news](https://tools.gbif.org/news/VqABDXdrK6ceAM6CY2aY4); BirdNET invites uploads to Xeno-canto and uses them for training — [BirdNET](https://birdnet.cornell.edu/contribute/)
- Perch 2.0 ("The Bittern Lesson for Bioacoustics", Aug 2025) trained on ~1.5M recordings of ≥14,500 species, outperformed whale-specific models on whale sounds — [The Decoder](https://the-decoder.com/google-deepminds-new-bioacoustic-model-shows-the-power-of-generalization-by-detecting-whales-with-bird-training/); [36kr](https://eu.36kr.com/en/p/3418126184435078); Perch offers vector search from a single example and fast classifier training; credited with helping find a new Plains Wanderer population with BirdLife Australia and speeding honeycreeper detection in Hawaii — [CO/AI](https://getcoai.com/news/google-deepmind-expands-perch-ai-to-track-endangered-wildlife-sounds)
- A 2024 arXiv dataset built from Xeno-canto recordings of 10 species in three US regions targets dialect effects — [arXiv 2406.08517](https://arxiv.org/html/2406.08517v1); a Xeno-canto forum notes BirdNET suggestions were "of little use" for Somalia/Kenya recordings due to sparse training data — [Xeno-canto forum](https://www.xeno-canto.org/forum/topic/44774); after IOC list updates, split-species recordings were auto-reassigned but "some others may need to be manually reviewed" — [Xeno-canto news](https://www.xeno-canto.org/news/691); a 2008 contributor's wren-babbler set included "the first ever recording of the recently split Naga Wren-babbler" — [Xeno-canto 2008 archive](https://www.xeno-canto.org/news/archives/2008)
- Indigryllus sagani sp. nov. (Kerala) was described following "a collaboration initiated by citizen science observations on the website iNaturalist", with acoustic signals documented — [Zootaxa](https://mapress.com/zt/article/view/47497); an iNaturalist journal post: "In just the last week of browsing audio observations of crickets ... I managed to find first documented state records for three species and three states", many such recordings not yet research grade — [iNaturalist post 115259](https://www.inaturalist.org/posts/115259)
- Paintedhand Mudbug: first Canadian records at three Windsor, Ontario sites; "iNaturalist ... was instrumental in facilitating this discovery" — [Canadian Field-Naturalist](https://canadianfieldnaturalist.ca/index.php/cfn/article/view/2223); [Ontario Parks blog](https://www.ontarioparks.ca/parksblog/?p=21703); California Tortoiseshell 2025: only the fourth Ontario record (Kingston) and 11 Algoma iNaturalist reports vs 4 historical — [Kingston Field Naturalists](https://kingstonfieldnaturalists.org/kingston-butterfly-summary-for-2025/); [Butterflies of Algoma journal](https://inaturalist.ca/projects/butterflies-of-algoma/journal/117307-california-tortoiseshell-reported-a-number-of-times-in-ontario-during-2025)

### Inferences
- The most realistic bioacoustic "positive finding" for a laptop user is a first provincial/regional record or range extension of a singing insect or frog drawn from Ontario iNaturalist audio, using Perch/BirdNET embeddings to cluster "needs ID" recordings and then recruiting an identifier; the Canadian Field-Naturalist already publishes such notes, which is a natural confirmation route.
- A Perch-embedding audit of Xeno-canto/Macaulay labels (nearest-neighbour outliers, post-split recordings needing review) is unglamorous but directly useful to the archives and apparently undone at scale; confirmation is by archive admins.
- A new bird species from Ontario recordings is implausible; a dialect/song-variant map is plausible but is "some competition" because academic dialect datasets exist.

### Gaps
- No source found on any Ontario-specific BirdNET/Perch citizen project or on an amateur's discovery of a bird dialect; the famous White-throated Sparrow song-shift precedent was not searched and is not cited here.
- Whether anyone has run a systematic ML label audit on Xeno-canto or Macaulay was not established (absence of evidence only).
- iNaturalist sound-observation export mechanics (GBIF/API) were not verified in this research.

## Key Question 5: Public health and epidemiology (Ontario/Canada open data on wait times, drug shortages, overdoses, wastewater, flu/COVID)

### Takeaway
The data most likely to hold unexamined patterns are those released recently (national wastewater drug dashboard, Dec 2025) or with known comparability issues (Ontario ED time series after Dec 2025; CIHI definitional variation). Think-tanks (CCPA, Fraser) and academics (UBC drug-shortage group) already produce headline stats, so an amateur's edge is consistency checking and cross-linking rather than another descriptive summary. No individual-citizen Ontario data-discovery story surfaced in searches.

### Cited Findings
- All Ontario/Canada public-health findings are listed under KQ2 (Ontario Health ED comparability warning; CCPA 4.5-hour 90th-percentile wait; Health Canada wastewater dashboard; Toronto overdose dashboards; Frontiers 2025 on fragmented substance-use data; Drug Shortages Canada studies; JAMA 34% figure).
- Health Canada's dashboard analyses wastewater from seven provinces and territories including Ontario and "will be updated quarterly" — [Health Canada](https://www.canada.ca/en/health-canada/news/2025/12/health-canada-launches-national-wastewater-drug-surveillance-dashboard-to-inform-overdose-crisis-response-and-to-share-data-on-drug-use-in-canada.html)

### Inferences
- A "series-break audit" of ED wait-time reporting and a "wastewater-vs-overdose concordance" analysis are the two Ontario projects with the clearest novelty-by-timing and lowest ethical risk (aggregate data only).
- Drug-shortage work is some-competition; the fresh angle is the JAMA finding that most Canadian shortage reports do not become actual shortages, which invites a Canada-only re-analysis of 2024–2026 reports by therapeutic class and single-source status.

### Gaps
- No search found any individual (non-institutional) analyst's newsworthy finding in Ontario health open data; the question "what is still unexamined in 2026" is answered only by inference from release dates.
- Flu/COVID surveillance (Public Health Ontario respiratory tools) was not searched specifically.

## Key Question 6: Drug/compound re-analysis from open screening data (ChEMBL, PubChem BioAssay, halicin/abaucin datasets, COVID Moonshot)

### Takeaway
Volunteer computational contributions to drug discovery are real (COVID Moonshot: >200 volunteer scientists from 25 countries, >18,000 designs, >2,400 compounds synthesised, data released without IP restrictions, contributing to the approved antiviral ensitrelvir) but the contributors were mostly professional chemists and the model depended on a funded synthesis/assay pipeline. For a lone undergraduate, flagging a candidate from ChEMBL/PubChem and getting a lab to test it is low-probability without a pre-arranged collaborator.

### Cited Findings
- COVID Moonshot results (Science, Nov 2023): >200 volunteer scientists from 25 countries, >18,000 compound designs, >2,400 synthesised compounds, >500 crystal structures, >10,000 assay measurements; all data public without IP restrictions; contributed crystallographic data to ensitrelvir — [MIT Technology Review](https://www.technologyreview.com/2023/11/10/1083222/covid-moonshot-drug-discovery-open-source/amp/); [Oxford Zitzmann lab](https://zitzmannlab.web.ox.ac.uk/node/3655581); early phase: >4,500 designs from 280 contributors; a volunteer chemist (Spencer) submitted ~100 ideas and shipped compounds from his university lab — [IEEE Spectrum](https://spectrum.ieee.org/covid-moonshot-can-ai-algorithms-and-volunteer-chemists-design-a-knockout-antiviral); [Sussex](https://www.sussex.ac.uk/news/research?id=51989); triage led by MedChemica, computation by MSKCC, synthesis by Enamine — [Weizmann USA](https://weizmann-usa.org/news-media/in-the-news/covid-moonshot-can-ai-algorithms-and-volunteer-chemists-design-a-knockout-antiviral/)
- Halicin (MIT, 2020): model trained on E. coli activity, screened ~6,000 Drug Repurposing Hub compounds then >100M ZINC15 molecules; validated in mice against pan-resistant A. baumannii — [Chemistry World](https://chemistryworld.com/news/ai-tool-screens-107-million-molecules-discovers-potent-new-antibiotics/4011233.article); [MIT Technology Review](https://www.technologyreview.com/2020/04/15/999303/ai-vs-bacteria/amp/); Chemprop teaching notes reproduce the workflow — [UVA notes](https://learning.rc.virginia.edu/notes/dl-drug-discovery/application-2-chemprop/)

### Inferences
- A computational hit is only a "finding" once assayed; the realistic amateur route is to join an existing open consortium (Moonshot-style) or to pre-arrange a U of T/McMaster lab partner before investing effort; otherwise this is a portfolio project, not a discovery.
- Rating: crowded (well-funded AI antibiotic groups) and structurally blocked for a no-lab individual; include only as a stretch option.

### Gaps
- No source found on any independent re-analysis of the halicin/abaucin datasets producing a lab-validated hit; the search returned only original-study coverage.
- ChEMBL/PubChem BioAssay-specific amateur precedents were not searched.

## Key Question 7: 2025–2026 examples of an individual using an AI coding agent to obtain a credited finding, and how it was covered

### Takeaway
The clearest 2026 precedent is outside biology: in October 2026 developer Pavel Rabtsevich used Claude Code and Codex on TESS data, submitted a candidate ~1.4-Earth-radius exoplanet to NASA, which scheduled follow-up observations; coverage framed it as "amateur + AI agent" and stressed his 74 attempts to disprove the signal. In life sciences, coverage of Claude-driven discoveries has been institutional (Anthropic's enzyme-system claim, with a credit dispute) and expert-verified ("Claude-shaped science: 36 papers, experts required"), so an amateur life-science credit via an agent is still unprecedented in what I found.

### Cited Findings
- Rabtsevich used Claude Code and OpenAI Codex to search TESS light curves; NASA scheduled follow-up observations; candidate ~1.4× Earth radius; he ran 74 tests with Claude Code trying to disprove it — [Cybernews](https://cybernews.com/tech/claude-code-possible-exoplanet-found-in-nasa-data/); [Gizmodo](https://gizmodo.com/did-claude-help-an-amateur-astronomer-discover-a-new-planet-2000824393)
- Anthropic reported that a research version of Claude improved a lower bound on Riemann-zeta zeros over two Claude Code sessions (31M output tokens) — [Anthropic](https://www.anthropic.com/research/riemann-zeta); Anthropic said Claude agents discovered a new enzyme system; its life-sciences lead denied training on Mario Rodriguez Mestre's work and pledged to credit him — [Endpoints News](https://endpoints.news/qa-anthropics-life-sciences-team-talk-claudes-first-scientific-discovery/); a commentary on Matthew Schwartz's essay reports ~400 candidates narrowed to 36 manuscripts with experts required — [explainx](https://explainx.ai/blog/claude-shaped-science-bootloops-schwartz-2026); a reproducibility critique notes a Claude discovery was missed in 10 reruns — [Medium](https://medium.com/the-generator/claude-made-a-new-scientific-discovery-then-missed-it-in-10-reruns-269018f71a94)
- A solo mathematician credited "an adversarial review by Claude" for finding errors and revised his preprint (Aug 2026) — [arXiv 2504.02795](https://arxiv.org/pdf/2504.02795)
- LLM error-detection at scale (Black Spatula, YesNoError, Bianchi/Zou, Nature Aug 2026 agents) — see KQ1 citations

### Inferences
- Press pattern: amateur + agent stories get covered when (a) an institution agrees to follow up (NASA), (b) the person documents adversarial self-checks, and (c) the claim is specific and falsifiable. The same template applies to a database correction accepted by NCBI/EMBL-EBI or a retraction/correction triggered by a verified error.
- Credit disputes (Mestre/Anthropic) show the importance of documenting provenance and prior literature before announcing an "AI-found" result.

### Gaps
- No life-science or public-health example of an amateur's AI-agent-assisted credited finding in 2025–2026 was found; the exoplanet case is the only amateur precedent located.
- No source found on the "Matteo Paz"-type student-AI stories or on YesNoError-triggered corrections in 2026.

## Key Question 8: Vetted shortlist of candidate projects (what, data, method, confirmation, effort, saturation with evidence, risk)

### Takeaway
Fifteen candidates below; the strongest fits for a Toronto math undergraduate with Claude Code are the numerical-forensics sweep of Canadian journals (P1), the Excel gene-name re-scan (P2), the Ontario ED series-break audit (P8), the wastewater–overdose concordance study (P9), and the Ontario iNaturalist audio first-records hunt (P11); image-forensics (P4) and drug-candidate flagging (P14) are included for completeness but rated crowded/high-risk or structurally blocked.

### Cited Findings
- Evidence for each saturation rating is cross-referenced to KQ1–KQ7 citations; additional dataset-access facts: statcheck scans folders of PDFs/HTML — [CRAN](https://ftp.fau.de/cran/web/packages/statcheck/refman/statcheck.html); Logan-Search answers arbitrary queries in <5 min with geographic mapping — [PMC12424806](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC12424806/); Perch supports vector search from a single example — [CO/AI](https://getcoai.com/news/google-deepmind-expands-perch-ai-to-track-endangered-wildlife-sounds); Ontario Health comparability warning — [Ontario Health](https://ontariohealth.ca/system/reporting/performance/time-spent-in-emergency-departments); wastewater dashboard quarterly, Jan 2023–Jul 2025 at launch — [Health Canada](https://www.canada.ca/en/health-canada/news/2025/12/health-canada-launches-national-wastewater-drug-surveillance-dashboard-to-inform-overdose-crisis-response-and-to-share-data-on-drug-use-in-canada.html); PubPeer fact-only norm — [PubPeer](https://pubpeer.com/static/misconduct); Black Spatula contacts authors privately, ~10% false positives — [heise](https://www.heise.de/en/news/No-more-calculation-errors-AI-checks-papers-for-errors-Why-that-s-not-enough-10321469.html)

### Inferences
(Each card: 1 discovery; 2 data/access; 3 method; 4 confirmation; 5 effort; 6 saturation + evidence; 7 main risk. Effort estimates are my judgement. URLs for data portals are top-level unless verified above.)

**P1. Numerical-consistency sweep (statcheck + GRIM/SPRITE) of Canadian open-access health and psychology journals** — Watchdog.
1. Rate of statistical reporting inconsistencies and impossible means in, e.g., CMAJ Open, Canadian Journal of Public Health, Canadian Journal of Behavioural Science, Paediatrics & Child Health; a handful of "gross" errors that flip a p < .05 conclusion.
2. PubMed Central open-access full text (pmc.ncbi.nlm.nih.gov, OA subset bulk download) and publisher sites; tools: statcheck (R; statcheck.io), GRIM/SPRITE (open-source implementations); Claude Code to parse non-APA stats tables into (M, SD, N).
3. Download XML/PDF; run statcheck; extract means from integer-scale items and GRIM-test them; manually verify every flag against the paper; classify as typo / rounding / decision-changing.
4. Email corresponding authors with the arithmetic; then journal editors; factual PubPeer notes only; community: Nuijten/Heathers/Brown-style statistics sleuths; U of T psychology/epidemiology methodologists could co-sign a methods note.
5. 4–8 weeks part-time.
6. Some competition: mass statcheck scans exist for psychology (≈30k articles, ~half with ≥1 inconsistency) and statcheck is used in Psychological Science peer review ([PMC7540394](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7540394/)); LLM projects scan broadly ([heise](https://www.heise.de/en/news/No-more-calculation-errors-AI-checks-papers-for-errors-Why-that-s-not-enough-10321469.html)); no Canadian-journal or medical-journal statcheck/GRIM scan found (gap, KQ1).
7. GRIM false positives when scales are not integer or N is misreported; naming authors — mitigate with PubPeer's checkable-facts rule and author-first contact; the press story should be the aggregate rate, not individuals.

**P2. Re-scan of 2021–2026 supplementary Excel files for gene-name corruption and other mechanical data errors** — Watchdog (dataset errors).
1. Whether Excel date-conversion of gene names (SEPT2 → 2-Sep) and similar corruptions persist after HGNC renaming and Microsoft's 2023 autocorrect toggle; a per-journal/per-institution league table (e.g., Canadian-affiliated papers).
2. PMC OA supplementary files (bulk FTP); Ziemann group's open scanner code (GitHub, per 2021 paper).
3. Crawl supplements; parse xlsx/csv; detect date-formatted cells in gene columns; extend to other corruptions (leading-zero loss in IDs, locale decimal errors); verify a sample by hand.
4. Journals issue corrections; Mark Ziemann (Deakin) is the obvious external validator; HGNC.
5. 3–6 weeks.
6. Some competition: Ziemann's group did 2014–2020 (30.9% of 11,117 papers) ([DOAJ](https://doaj.org/article/8b429b7b5d454a8c9aeef110207e3418)); no 2024–2026 update found (gap). The angle "still happening in 2026, including at Canadian labs" is fresh by timing.
7. Low ethical risk (honest errors, no fraud framing); newsworthiness depends on the rate being non-trivial.

**P3. Black-Spatula-style LLM error scan of a bounded Canadian corpus with full human verification** — Watchdog.
1. Verified calculation/unit/citation errors in, e.g., all 2024–2026 medRxiv/bioRxiv preprints with Ontario affiliations, or a single Canadian society journal.
2. bioRxiv/medRxiv (API and full-text TDM), PMC OA; Claude Code with chain-of-verification prompts; Black Spatula's open-source prompts/pipeline ([Second Thoughts](https://secondthoughts.ai/p/black-spatula-day-five)).
3. Extract every numeric claim; recompute from tables; flag; verify by hand; contact authors privately; publish only aggregate and author-acknowledged cases.
4. Authors (corrections), preprint servers, journal editors; Black Spatula volunteers as peer check.
5. 6–10 weeks; compute cost ~US$0.15–few dollars per paper ([Academica](https://academica.ca/top-ten/how-ai-tools-are-being-used-to-identify-errors-in-research-papers-opinion/)).
6. Crowded for the generic idea (YesNoError 37k papers; Black Spatula 500; academic checkers at 83% precision; Nature-reported agents finding decades-old errors — KQ1); open niche only through corpus choice (no Canadian-focused effort found).
7. ~10% false positives → reputational harm if published prematurely; follow Black Spatula's private-first norm; crypto-funded YesNoError is a cautionary example of public flagging.

**P4. Image-duplication sleuthing (Bik/Sholto David model) on a small Ontario-affiliated corpus** — Watchdog; included for completeness, not recommended as a first project.
1. Duplicated/manipulated Western blots or micrographs in a defined set of papers.
2. PMC OA figures; free methods: manual comparison, open-source duplicate finders; commercial ImageTwin/Proofig cost ~US$27–50 per paper and have no general free sleuth programme ([Olhar Digital](https://olhardigital.com.br/2024/03/21/pro/detetives-de-dados-softwares-estao-ajudando-a-detectar-manipulacao-de-imagens-em-pesquisas/); [AI Insider](https://theaiinsider.tech/2023/10/10/ai-beats-human-sleuth-at-finding-problematic-images-in-research-papers/)).
3. Extract figures, compute perceptual hashes/feature matches within and across papers, inspect by eye, annotate.
4. PubPeer (facts only), journal integrity offices, institutional research-integrity officers; Retraction Watch for coverage.
5. 8–16 weeks; expertise-heavy.
6. Crowded: Bik, David, publisher-side screening (MDPI–Proofig, ASM–ImageTwin) ([CASRAI](https://casrai.org/news/ai-image-integrity-screening-mdpi-asm-adoption)); Canadian cases exist historically ([Retraction Watch Canada](https://retractionwatch.com/category/by-country/canada/page/14)).
7. Highest legal/ethical exposure: accusations against named people; Sarkar/Gino litigation shows factual comments survive but intent claims do not ([Public Citizen](https://www.citizen.org/litigation/sarkar-v-does/); [Poets&Quants](https://poetsandquants.com/2024/09/12/judge-dismisses-francesca-ginos-defamation-claims-against-harvard-data-colada/)); police complaint against Bik ([FAPESP](https://revistapesquisa.fapesp.br/en/the-limits-of-anonymous-accusations/)).

**P5. Reference-database constant/property error hunt (chemistry and biology look-up values)** — Watchdog (dataset errors).
1. Wrong or internally inconsistent physical-property or annotation values propagated for decades in open databases (PubChem experimental vs computed properties; UniProt annotations; GenBank feature coordinates).
2. PubChem (pubchem.ncbi.nlm.nih.gov, REST/FTP), ChEMBL (ebi.ac.uk/chembl), UniProt (uniprot.org, REST), NCBI; Claude Code to cross-check values across sources and primary citations.
3. Pull the same field from multiple sources; flag disagreements beyond tolerance; trace to the original citation; report with evidence.
4. Database curators (PubChem/UniProt helpdesks accept corrections); chemistry/biochemistry faculty for sanity checks.
5. 4–8 weeks.
6. Some competition: Nature (Aug 2026) reports AI agents already doing this (75-year-old boiling point) ([TagTeam/Nature](https://tagteam.harvard.edu/hub_feeds/4669/feed_items/18613215)); no systematic amateur campaign found.
7. Low ethical risk; verification may need paywalled primary literature; coverage likely niche unless the error is famous.

**P6. AlphaFold DB staleness and implausibility audit for one proteome** — Watchdog (dataset errors) with a structural-biology confirmation route.
1. A curated list of AFDB entries whose sequences no longer match current UniProt, plus models with implausible topology (knots) or pLDDT patterns, for the human proteome or an Ontario-relevant pathogen.
2. AlphaFold DB bulk downloads (alphafold.ebi.ac.uk), UniProt releases; open knot-detection code from the knot-theory preprint.
3. Diff sequences; run knot/geometry checks; summarise; submit to AFDB team.
4. EMBL-EBI AFDB team; U of T structural biologists (e.g., at Donnelly Centre) for a sanity read.
5. 3–6 weeks.
6. Some competition: preprints already found 295 length mismatches and estimate 188k–2.4M mismodelled knotted proteins ([bioRxiv](https://www.biorxiv.org/content/10.1101/2025.06.22.660930.full.pdf); [arXiv](https://arxiv.org/pdf/2412.11229)); whole-proteome QA still "anecdotal" per [Fold or flop](https://www.biorxiv.org/content/10.64898/2025.12.19.695427.full.pdf).
7. Low ethical risk; modest press value (campus paper); must avoid duplicating the preprints' exact scope.

**P7. Mislabelled DNA barcode / contaminated sequence hunt for Ontario fauna (BOLD + GenBank + GBIF)** — Watchdog/dataset errors with a Guelph/ROM confirmation route.
1. COI barcodes or GenBank entries for Ontario fish, insects or amphibians whose nearest neighbours are a different species (mislabels) or that carry contamination.
2. BOLD (boldsystems.org, public data portal), GenBank/RefSeq (NCBI), GBIF occurrences (gbif.org); Conterminator-style all-vs-all tools.
3. Download taxon-restricted sequences; cluster; flag sequences inconsistent with their label; check voucher/occurrence metadata; report.
4. BOLD curators at the Centre for Biodiversity Genomics (Guelph, Ontario); NCBI contamination reporting; ROM taxonomists.
5. 4–8 weeks.
6. Some competition: Conterminator found >2M contaminated RefSeq entries ([PMC7218494](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7218494/)); 2024 review says the problem is "relatively unmitigated" ([Frontiers](https://frontiersin.org/articles/10.3389/fbinf.2024.1278228)); no Ontario-taxon-specific audit found.
7. Low ethical risk; taxonomic ambiguity (cryptic species, introgression) can masquerade as error.

**P8. Ontario ED wait-time series-break and reconciliation audit** — Watchdog (government data).
1. Whether 2026 reports, articles or statements compared ED-time figures across Ontario Health's December 2025 refresh (43 added sites; "should not be compared"), and how Ontario Health, CIHI and think-tank (CCPA/Fraser) figures reconcile.
2. Ontario Health "Time Spent in Emergency Departments" monthly tables ([Ontario Health](https://ontariohealth.ca/system/reporting/performance/time-spent-in-emergency-departments)); CIHI indicators (cihi.ca); CCPA/Fraser reports; news archive.
3. Scrape monthly exports before/after the break (Wayback Machine for pre-refresh), compute hospital-level deltas, search media for cross-break comparisons, document.
4. Ontario Health/CIHI data teams; health-policy faculty (U of T IHPME); the news outlets that published comparisons.
5. 3–5 weeks.
6. Some competition on wait-time headlines (CCPA May 2026; Fraser 2025) ([CP24](https://www.cp24.com/local/toronto/2026/05/11/under-immense-strain-wait-times-at-ontario-emergency-rooms-have-spiked-over-past-5-years-study-says/)); open niche for the series-break check (nothing found).
7. Low ethical risk (aggregate data; record-level ERNI is restricted); political sensitivity; must quote Ontario Health's own caveat accurately.

**P9. Wastewater drug signals vs overdose/EMS data concordance for Ontario cities** — Positive finding/watchdog (public health).
1. Lead/lag relationships or divergences between the national wastewater drug dashboard (fentanyl, stimulants) and Toronto/Ontario overdose, EMS and coroner counts; cities where wastewater rose but reported overdoses did not (or vice versa).
2. Health Canada National Wastewater Drug Surveillance dashboard (quarterly, Jan 2023–Jul 2025 at launch) ([Health Canada](https://www.canada.ca/en/health-canada/news/2025/12/health-canada-launches-national-wastewater-drug-surveillance-dashboard-to-inform-overdose-crisis-response-and-to-share-data-on-drug-use-in-canada.html)); Toronto overdose dashboards ([toronto.ca/OverdoseData](https://toronto.ca/OverdoseData)); Public Health Ontario opioid tool (publichealthontario.ca); Ontario Data Catalogue (data.ontario.ca).
3. Align by site/month; cross-correlate; test for structural breaks; present as hypotheses for public-health analysts.
4. Public Health Ontario, Toronto Public Health epidemiologists; wastewater-epidemiology academics (e.g., the Durham Region group).
5. 4–6 weeks.
6. Open niche by timing: dashboard launched Dec 2025; Ontario substance-use data described as fragmented ([Frontiers 2025](https://www.frontiersin.org/articles/10.3389/fpubh.2025.1477539/full)); no external analysis found.
7. Ecological fallacy and reporting-lag artefacts; sensitive topic (stigma); use aggregate data only.

**P10. Drug Shortages Canada 2024–2026 re-analysis: reports that never became shortages; single-source generics watch list** — Watchdog (public data).
1. Share of 2024–26 shortage reports that resolved without supply disruption; current single-manufacturer markets at risk; Ontario Drug Benefit formulary overlap.
2. Drug Shortages Canada database (drugshortagescanada.ca, downloadable/API), Health Canada Drug Product Database (DIN linkage), Ontario Drug Benefit formulary (data.ontario.ca).
3. Link by DIN; classify markets by manufacturer count; time-series; compare with JAMA's 34% conversion figure.
4. UBC/Toronto pharmaceutical-policy researchers; Health Canada; CMAJ-style brief.
5. 4–6 weeks.
6. Some competition: multiple CMAJ/UBC studies (23.4%, 44.7%, single-source risk, COVID peak) ([CMAJ 2022](https://www.cmaj.ca/content/194/23/E801); [CTV](https://www.ctvnews.ca/health/nearly-a-quarter-of-drugs-marketed-in-canada-reported-shortages-study-1.5088570?cache=)); the "reports vs actual shortages" angle is recent ([Pharmaceutical Commerce](https://www.pharmaceuticalcommerce.com/view/study-supply-chain-issues-less-likely-result-drug-shortages-canada-compared-united-states)).
7. Low ethical risk; naming manufacturers requires care; database reporting quality itself is a variable.

**P11. Ontario first records and range extensions from iNaturalist audio (crickets, katydids, cicadas, frogs)** — Positive finding (bioacoustics).
1. First provincial/regional records of singing insects or anurans hidden in un-identified Ontario iNaturalist sound observations.
2. iNaturalist (inaturalist.ca; sound observations exportable via API/GBIF), Xeno-canto/Macaulay reference calls, Perch/BirdNET embeddings (open models), Orthoptera call references.
3. Pull all Ontario audio observations lacking research-grade ID; embed with Perch; nearest-neighbour against reference calls; shortlist anomalies; recruit expert identifiers on iNaturalist; write a note.
4. Orthopterists/herpetologists (ROM; Canadian Field-Naturalist publishes first-record notes, as with the mudbug paper); iNaturalist curators.
5. 4–8 weeks (summer recordings are best).
6. Open niche for Ontario: precedents are a US user finding three first state records in a week ([iNaturalist post](https://www.inaturalist.org/posts/115259)), a new cricket species described after iNaturalist observations ([Zootaxa](https://mapress.com/zt/article/view/47497)) and an Ontario first-Canadian record via iNaturalist ([CFN](https://canadianfieldnaturalist.ca/index.php/cfn/article/view/2223)); no Ontario audio-mining effort found.
7. Low risk; false positives from model bias on under-represented taxa ([Xeno-canto forum on BirdNET limits](https://www.xeno-canto.org/forum/topic/44774)); need expert sign-off before any claim.

**P12. Perch-embedding label audit of Xeno-canto / Macaulay Library recordings (Ontario subset first)** — Watchdog (dataset errors).
1. Recordings whose embeddings sit with another species (mislabels, background-species confusion, post-split reassignment errors).
2. Xeno-canto (xeno-canto.org API, CC-licensed audio), Macaulay Library (macaulaylibrary.org; download by request), Perch 2.0 (open weights).
3. Embed; per-species outlier detection; manual listening; report batches to archive admins.
4. Xeno-canto admins (crowd-validation forum), Macaulay Library curators; Cornell BirdNET team.
5. 4–6 weeks.
6. Some competition: archives already crowd-validate and auto-reassign splits with manual review needed ([Xeno-canto news](https://www.xeno-canto.org/news/691)); no systematic ML audit found (gap).
7. Low risk; value is to the archive and model training rather than headlines; press angle is modest.

**P13. Song-dialect or song-change map for an Ontario bird using archive recordings** — Positive finding (bioacoustics).
1. Geographic structure or temporal shift in a common Ontario species' song (candidates: White-throated Sparrow, Song Sparrow, Chaffinch-like dialect species) across decades of Xeno-canto/Macaulay/iNaturalist recordings.
2. Same archives as P12 plus eBird metadata (ebird.org).
3. Segment songs; cluster syllable types; map by year/location; test for spread.
4. Ornithologists (U of T EEB; Birds Canada); Macaulay Library.
5. 6–10 weeks.
6. Some competition: academic dialect datasets built from Xeno-canto exist ([arXiv 2406.08517](https://arxiv.org/html/2406.08517v1)); the specific Ontario time-series angle not found (but the well-known White-throated Sparrow song-shift literature was not searched here — gap).
7. Low risk; recording bias by observer density; needs ornithologist input to avoid rediscovering known results.

**P14. Targeted pathogen/virus search across all SRA with Logan-Search (e.g., Ontario-relevant tick-borne or wildlife viruses)** — Positive finding (genomics).
1. Unreported hosts, geographies or years for a specific virus (or a novel close relative) found in public sequencing runs not intended for virus discovery.
2. Logan unitigs/contigs on AWS Open Data and Logan-Search (<5 min/query) ([GitHub](https://github.com/IndexThePlanet/Logan)); NCBI SRA metadata; Serratus/Open Virome resources.
3. Query reference genome k-mers; map hits to BioSample metadata; assemble local contigs; phylogenetics; check contamination controls.
4. Virologists (Serratus/Open Virome team; U of T/PHO virology); NCBI for sequence submission.
5. 6–12 weeks.
6. Crowded for bulk novel-virus discovery (Serratus 132k; Kawasaki ~900 hidden infections) ([Nature via IDEAS](https://ideas.repec.org/a/nat/nature/v602y2022i7895d10.1038_s41586-021-04332-2.html); [DOAJ](https://doaj.org/article/d47b6c171b3845e9ac2574fd3e02fd53)); some competition for targeted queries; index frozen at Dec 2023.
7. Contamination/index-hopping false positives; low ethical risk; needs expert confirmation before any "new host" claim.

**P15. Reinhart–Rogoff-style replication of a widely cited Canadian health-policy study from its open data** — Watchdog (replication).
1. A coding/spreadsheet error or non-robust result in an influential Canadian study whose data are public (e.g., StatCan public-use microdata, CIHI tables).
2. Statistics Canada (statcan.gc.ca PUMFs/tables), CIHI (cihi.ca), the paper's supplementary data.
3. Reproduce the headline estimate; vary reasonable choices; contact authors with discrepancies.
4. Authors, journal editors; U of T economics/epidemiology faculty.
5. 4–10 weeks depending on target.
6. Open niche in principle (precedent: Herndon 2013 ([Chronicle](https://www.chronicle.com/article/UMass-Graduate-Student-Talks/138763))); success depends entirely on picking a target with available data; no Canadian replication-by-student precedent found.
7. Naming authors; frame as replication not accusation; risk of wasted effort if replication succeeds (which is itself publishable only modestly).

(Dropped from consideration: computational antibiotic/drug-candidate flagging from ChEMBL/PubChem/halicin data — rated crowded and structurally blocked for a no-lab individual; see KQ6. A pre-arranged wet-lab partner would change this.)

### Gaps
- Effort estimates and several dataset endpoints are my judgement, not sourced.
- Saturation ratings rely on absence of evidence in web searches for P1, P2 (post-2020), P8, P9, P11, P12, P13; a deeper literature search (Google Scholar/OpenAlex) before starting any project is advised.
- Whether Ontario Health, PHO and CIHI publish machine-readable aggregate downloads sufficient for P8/P9 was not verified page-by-page.
