# Astronomy and space-science discovery projects for a laptop-only amateur with Claude Code (status as of 2026-10-21)

Research-method note for the report writer: web search worked for ~40 queries, but every page-fetch route (WebFetch, curl via the egress proxy, Firecrawl) was blocked or out of credit in this session, and the shared WebSearch budget ran out before the last five planned queries (Hubble/JWST archive asteroid trails, NEOWISE archive mining, GMN data-portal licence, Active Asteroids 2025 results, Malik 2025 details). All "Cited Findings" below therefore come from search-result snippets of the linked pages, not full-text reads. Where I rely on prior knowledge that I could not verify this session, I say so explicitly and put it under Gaps or label it "unverified".

## Q1. Has the "amateur found an exoplanet in TESS data with Claude Code" niche already been taken, and which TESS/Kepler products still yield candidates to amateurs?

### Takeaway
Yes, the headline story already exists: in October 2026 Pavel Rabtsevich, a Spain-based product manager with no telescope, used Claude Code, OpenAI Codex and a third agent to flag a 1.4-Earth-radius, 3.18-day candidate around the nearby K dwarf TIC 4206066; it is unconfirmed and TESS re-observes it 31 Oct–26 Nov 2026. Short-period, small-planet "pipeline-miss" searches on bright stars are therefore now crowded (and professional FFI catalogues such as COUNTESS and transformer-based FFI searches compete there), whereas single-transit long-period candidates in FFI light curves are still producing new planets credited to volunteers (TOI-6692 b, Jan 2026).

### Cited Findings
- Pavel Rabtsevich, a 28-year-old product manager in Spain with no astronomy training and no telescope, used Anthropic's Claude Code and OpenAI's Codex to search a dataset of measurements of over 126,000 stars; the candidate is roughly 1.4 Earth radii with a ~3-day orbit; he spent about 2 weeks, ran 74 analyses and wrote more than 1,000 scripts; TESS has queued observations for November to test it; the candidate remains unconfirmed — [Gizmodo](https://gizmodo.com/did-claude-help-an-amateur-astronomer-discover-a-new-planet-2000824393); [XDA](https://www.xda-developers.com/dont-get-too-excited-but-claude-code-may-have-just-discovered-a-new-planet/); [Cybernews](https://cybernews.com/tech/claude-code-possible-exoplanet-found-in-nasa-data/)
- The star is TIC 4206066, a K dwarf about 116 light-years away; the main signal repeats every 3.18 days with a 0.04–0.05% depth; a second, weaker 11.13-day signal is reported; he fed the data to three agents (TypeSafe's Jev, Claude Code, Codex) and iteratively shortened the candidate list; Greg Laughlin (Yale) called the case for at least one planet "solid"; TESS will observe the star at 2-minute cadence from October 31 to November 26 and Rabtsevich pre-registered nine transit times on Zenodo on October 6 — [Scientific American](https://www.scientificamerican.com/article/amateur-astronomer-harnesses-ai-to-find-a-possible-hidden-exoplanet/); Zenodo record "Two Transit-like Signals in TESS Photometry of the Nearby K Dwarf TIC 4206066" indexed at [NLM dataset catalog](https://datasetcatalog.nlm.nih.gov/dataset?q=0003338261)
- A Spanish-language report says the preprint itself states there is no statistical validation — [antihype.com.br](https://antihype.com.br/c/ciencia/claude-code-possivel-planeta-dados-nasa-tess/)
- The case has already spawned third-party replication repos and a public gist ("AI-assisted TESS exoplanet candidate: TIC 4206066") — [GitHub gist](https://gist.github.com/MrBoostie/b7a34b9ec96fbfb37e8fd250ba6debba); [xaviercallens/TIC4206066-Exoplanet-Verification](https://github.com/xaviercallens/TIC4206066-Exoplanet-Verification)
- Social amplification: "this guy found an exoplanet using Claude Code ... vibe code astronomy now" — [Ian Nuttall on X](https://x.com/iannuttall/status/2107865515129446467); "A Reddit user may have discovered an exoplanet using Claude Code ... 116 light-years away ... 1.4 times Earth's radius" — [Threads](https://www.threads.com/@cyrus_in_the_i/post/DePv_onDU4j/video-a-reddit-user-may-have-discovered-an-exoplanet-using-claude-code-the-possible). A low-quality aggregator claims a Hacker News thread with 49 points and 14 comments — [PromptZone](https://www.promptzone.com/elena_liu/claude-code-spots-new-exoplanet-in-public-data-5bm0) (unverified)
- A LessWrong post "How I discovered an Exoplanet & the science apocalypse" says TESS scanned the star twice (August 2022 and May 2025), which pinned the period, and that the author had 25 candidates as of writing — [LessWrong](https://www.lesswrong.com/posts/kdybMpcFJ5iwCDJsd/how-i-discovered-an-exoplanet-and-the-science-apocalypse) (could not fetch full text; authorship not confirmed to be Rabtsevich)
- Single-transit route still productive: TOI-6692 b, a ~130-day eccentric Jupiter-sized planet, was spotted by Visual Survey Group (VSG) volunteers as a single transit in Sector 39 during a focused long-period search; SPOC did not flag it as a TOI because only one transit was seen; it was first a community TOI; the paper (accepted 22 Jan 2026) lists several amateur astronomers and citizen scientists as authors — [arXiv 2601.16357](https://arxiv.org/html/2601.16357)
- Precedent: TOI-2180 b (~260 d) was first flagged by VSG citizen scientists in December 2019 — [Wikipedia](https://en.wikipedia.org/wiki/TOI-2180_b); HD 21520 b was first proposed as a single-transit candidate by Planet Hunters TESS — [arXiv 2406.09595](https://arxiv.org/pdf/2406.09595); TOI-4465 b (single transit, Sector 40, ~102 d) was confirmed with ground photometry from 24 citizen scientists filling a 12-hour window — [arXiv 2506.20019](https://arxiv.org/html/2506.20019); [Universe Today](https://www.universetoday.com/articles/worldwide-team-of-citizen-scientists-help-confirm-a-tricky-exoplanet)
- Planet Hunters TESS has moved toward ML: Malik et al. 2025, "Accelerating Long-period Exoplanet Discovery by Combining Deep Learning and Citizen Science", reports a model trained on volunteer labels that recovers TOIs at precision and recall exceeding volunteers — [AJ/IOPscience](https://iopscience.iop.org/article/10.3847/1538-3881/add46d); listed under PHT on [Zooniverse publications](https://www.zooniverse.org/about/publications)
- Scale of prior citizen effort: PHT II had over 22,000 citizen scientists inspect the first 26 sectors — [MNRAS](https://academic.oup.com/mnras/article/501/4/4669/6027708); Planet Hunters NGTS had >8,000 volunteers review 138,198 light curves and reported five short-period giant candidates — [arXiv 2404.15395](https://arxiv.org/abs/2404.15395)
- Professional competition in the same data: COUNTESS I is "A Uniformly Vetted Catalog of Known and New Transiting Exoplanets in the TESS Northern Continuous Viewing Zone" (June 2026) — [arXiv 2606.13789](https://arxiv.org/pdf/2606.13789); a transformer-based algorithm searches TESS FFIs for transit candidates — [arXiv 2502.07542](https://arxiv.org/pdf/2502.07542)
- Pipeline counts: NASA Exoplanet Archive listed 6,451 confirmed planets and 8,151 TESS Project Candidates in mid-October 2026, with data for more than 8,000 candidates uploaded to ExoFOP — [NASA Exoplanet Archive](https://exoplanetarchive.ipac.caltech.edu/); Wikipedia (14 Oct 2026): 8,148 TESS candidates, 1,008 confirmed; CTOIs are assigned by independent researchers, TOIs by the TESS team — [Wikipedia TESS](https://en.wikipedia.org/wiki/Transiting_Exoplanet_Survey_Satellite)
- TESS mission status: Extended Mission 3 began September 2025 — [TESS EM planning guide](https://Heasarc.Gsfc.Nasa.gov/docs/tess/docs/Guide-to-TESS-for-EM-planning.pdf); a January 2026 AAS document says TESS is in the sixth year of its extended mission and has mapped >98.6% of the sky (reported via search snippet; the HEASARC sector page's latest listed field is Cycle 7 beginning October 2024 — [TESS sector page](https://heasarc.gsfc.nasa.gov/docs/tess/sector.html))
- Amateur follow-up pathway: qualified amateurs join TESS Follow-up (TFOP SG1) to identify false positives and refine ephemerides, uploading to ExoFOP-TESS per SG1 guidelines — [Conti, AAVSO presentation](https://astrodennis.com/LocalGroupTESSPresentation.pdf)
- Kepler/K2: no 2024–2026 citizen-science Kepler/K2 planet discoveries surfaced; the most recent are K2 Campaign 19's last planets (K2-416 b, K2-217 b, plus single-transit candidate EPIC 246251988 b still needing follow-up) found with Exoplanet Explorers volunteers — [MNRAS 2023](https://academic.oup.com/mnras/article/523/1/474/7178009); [Sky at Night](https://www.skyatnightmagazine.com/news/kepler-space-telescope-last-exoplanets); K2-288Bb (2019) — [arXiv 1902.02789](https://arxiv.org/pdf/1902.02789); 17 new candidates from a full-Kepler search (2020) — [arXiv 2003.04397](https://arxiv.org/pdf/2003.04397)

### Inferences
- The exact Rabtsevich recipe (2-min SPOC light curves of bright nearby stars, BLS/TLS re-search for shallow short-period transits missed by SPOC/QLP, agentic vetting) is now the most crowded amateur niche in astronomy: it has the news story, replication repos, and professional uniform-vetting catalogues (COUNTESS) in the same parameter space. A second such story would not be newsworthy unless the object were exceptional (habitable-zone, very nearby, etc.).
- Single-transit, long-period candidates in FFI light curves of stars SPOC/QLP do not search (fainter or outside 2-min target lists) remain a demonstrated volunteer discovery channel (TOI-6692 b in 2026) but are dominated by a small, organised group (VSG) and by PHT's ML model; "some competition" rather than "open niche".
- Kepler/K2 are over-mined for new planets; the only plausible laptop angle is cross-mission period recovery (K2 single-transit candidates such as EPIC 246251988 b re-observed by TESS), which I could not find anyone claiming, but also could not confirm as undone.

### Gaps
- I could not fetch the ExoFOP CTOI submission page, so the exact CTOI form requirements (prior knowledge, unverified: an ExoFOP account, TIC ID, period, epoch, depth, duration, and vetting notes/figures) are not sourced.
- Whether Rabtsevich's candidate was formally logged as a CTOI on ExoFOP, and whether it was promoted to a TOI, could not be verified.
- No Hacker News primary thread was found; only the aggregator claim.

## Q2. Which archives are under-mined vs over-mined: Gaia DR3/DR4, WISE/NEOWISE (Backyard Worlds), ZTF, SDSS, Kepler residuals?

### Takeaway
Backyard Worlds (WISE/NEOWISE) is crowded but still productive and welcomes ML-savvy volunteers; ZTF light curves are the one archive with documented recent amateur batch discoveries (50 new variables added to VSX in 2024); Gaia DR3 binaries/white dwarfs are mined by professionals with no amateur discoveries found, but Gaia DR4 (2 Dec 2026) is a time-boxed opening for a prepared pipeline. SDSS and Kepler residual mining could not be assessed in this session.

### Cited Findings
- Backyard Worlds: Planet 9 volunteers have roughly doubled the known brown-dwarf population with over 3,000 discoveries in ten years, and the project is still sifting through more than 2 billion WISE/NEOWISE-R sources (NASA report dated 5 May 2026) — [NASA Science](https://science.nasa.gov/get-involved/citizen-science/nasa-volunteers-double-known-population-of-brown-dwarfs/)
- A neural-network code written by citizen scientist Dan Caselden found 118 new low-temperature sources, two confirmed as new T dwarfs (Nov 2024) — [NASA](https://www.nasa.gov/solar-system/citizen-scientists-discover-dozens-of-new-cosmic-neighbors-in-nasa-data/); citizen scientists flagged CWISE J1249+3621, an L subdwarf moving at ~456 km/s near Galactic escape velocity — [UCSD Cool Star Lab](https://www.coolstarlab.org/research/brown-dwarf-discovery)
- Backyard Worlds spin-offs/papers: spectroscopic survey of citizen-found T subdwarfs (ApJ 2025); three new brown-dwarf spectral-binary candidates — [NSF PAR](https://par.nsf.gov/biblio/10533775-investigation-new-brown-dwarf-spectral-binary-candidates-from-backyard-worlds-planet-citizen-science-initiative); follow-on project Backyard Worlds: Cool Neighbors targets faint Y dwarfs — [Wikipedia](https://en.wikipedia.org/wiki/Backyard_Worlds); results page — [Zooniverse](https://www.zooniverse.org/projects/marckuchner/backyard-worlds-planet-9/about/results)
- A high-school researcher working with the Cool Star Lab reported over 100 new high-proper-motion stars from the UKIRT Hemisphere Survey (Nov 2025) — [UCSD Cool Star Lab](https://www.coolstarlab.org/research/brown-dwarf-discovery)
- ZTF amateur discoveries: in November 2024 amateur Jiashuo Zhang had a batch of 50 new variable stars (43 EA, 5 EA+BY, 1 EB, 1 BY) added to VSX, using ZTF data he described as "very precise"; batch submission was adopted because per-star submission was labour-intensive — [Cloudy Nights thread](https://www.cloudynights.com/forums/topic/943451-my-first-major-discovery-50-new-variable-stars%EF%BC%81/)
- VSX had already imported ~665,000 objects from the ZTF catalogue of periodic variables (2020) and ZTF positions corrected misidentifications — [AAVSO](https://www.aavso.org/vsx-surpassed-2000000-object-milestone); AAVSO's site now lists 10.4M variable stars and 74M+ observations — [AAVSO](https://aavso.org/)
- A 2025 arXiv study, "What ZTF Saw Where Rubin Looked: Anomaly Hunting in DR23", shows professionals are already anomaly-mining the newest ZTF data release — [arXiv 2507.06217](https://arxiv.org/pdf/2507.06217)
- Gaia DR3 variable white dwarfs vetted with ZTF yielded 67 newly identified periodically variable white dwarfs (A&A, 2026) — [A&A](https://www.aanda.org/articles/aa/full_html/2026/08/aa57350-25/aa57350-25.html)
- Gaia DR3 binaries are professional territory: ~30,000 WD–main-sequence binary candidates from XP spectra, 1,700 high-confidence — [arXiv 2501.14494](https://arxiv.org/abs/2501.14494); 347 WDMS candidates within 100 pc from Gaia+GALEX, 188 new — [arXiv 2509.06910](https://arxiv.org/html/2509.06910); three wide binaries with possible compact companions from Gaia DR3+LAMOST — [arXiv 2308.03255](https://arxiv.org/pdf/2308.03255); review "Gaia's binary star renaissance" — [arXiv 2403.12146](https://arxiv.org/pdf/2403.12146). No amateur-credited Gaia DR3 binary discovery surfaced.
- Gaia DR4 is planned for Wednesday 2 December 2026 (announced 7 May 2026); it is the first principal release, covering 5.5 years; a pre-release of DR4 astrometric time series was issued 29 June 2026 — [ESA Gaia news 2026](https://www.cosmos.esa.int/web/gaia/news-2026); [ESA Gaia on X](https://x.com/ESAGaia/status/2059281103861551436); the NASA Exoplanet Archive notes DR4 should bring the first large set of astrometric exoplanet candidates — [Exoplanet Archive Gaia page](https://exoplanetarchive.ipac.caltech.edu/docs/GaiaMission.html); Gaia stopped scanning on 15 January 2025 — [ESA Gaia news](https://www.cosmos.esa.int/web/gaia/news)
- ESA ran a "Gaia Vari" citizen project to classify Gaia variables ahead of the next release — [Phys.org](https://phys.org/news/2023-03-amateur-astronomers-stars-gaia.html); the 17th Gaia Science Alerts workshop (31 Aug–4 Sep 2026) had a session on citizen science and amateur astronomy — [GSA WG](https://gsawg.wiki.ast.cam.ac.uk/index.php?title=Workshop2026%3Amain)
- A Hugging Face mirror of the VSX catalogue exists for offline cross-matching — [Hugging Face](https://huggingface.co/datasets/juliensimon/aavso-vsx-variable-stars)

### Inferences
- Over-mined by professionals: Gaia DR3 binaries/WDs, Kepler planets, ZTF periodic variables with high amplitude and short period. Under-registered (not necessarily unknown to science, but absent from VSX with discoverer credit): low-amplitude or long-period eclipsing binaries and rotational variables in ZTF DR20+ epochs, especially in crowded northern fields; the Zhang batch shows VSX still accepts such finds from archival ZTF data.
- Backyard Worlds is "crowded" for ordinary L/T dwarfs but has a demonstrated opening for someone who brings their own ML pipeline (Caselden precedent) and for odd kinematics (hypervelocity objects).
- Gaia DR4 on 2 Dec 2026 is the single best time-boxed opportunity in this list: whoever has a tested pipeline (e.g., epoch-photometry eclipsing-binary finder cross-matched to VSX, or astrometric-acceleration companions) can produce VSX-registrable or RNAAS-publishable finds in the first weeks, before professional catalogues land.

### Gaps
- SDSS spectra for odd objects, Kepler residuals, and Hipparcos/Tycho were not searched (budget exhausted); treat as unassessed.
- No source quantifies how many new variables amateurs add to VSX per year; only anecdotal batches (50 by Zhang; 82 lifetime by Romanov, see Q4).

## Q3. Minor planets and comets: lost-asteroid recovery, archival precovery (DASCH), SOHO/LASCO comets (Sungrazer) — how crowded?

### Takeaway
Archival precovery is a proven, high-impact amateur niche (Sam Deen's 2024 YR4, 3I/ATLAS and C/2025 D1 work) but the MPC introduced a verification process for public-archive submissions in July 2025; Sungrazer remains the most reliable route to a named comet (5,204 SOHO comets by spring 2026, new GOES-19/CCOR-1 imagery since 2025) but is crowded and SOHO's end date is uncertain; Zooniverse asteroid projects produce thousands of reports but mostly to the Isolated Tracklet File, not individual designations. DASCH plates (DR7, Dec 2024) show no amateur precovery work in my results.

### Cited Findings
- Sam Deen (California amateur) and Derek Lam searched iPTF and other public archives and found 2016 pre-discovery images of 2024 YR4 (four from Palomar, two from Subaru, one from CTIO); the refined orbit showed a ~22,000 km Moon miss, matching JWST — [Sky & Telescope](https://skyandtelescope.org/astronomy-news/lunar-impact-from-asteroid-2024-yr4-ruled-out/); he also searched 2016 Subaru images to exclude ~80% of impacting trajectories — [Sky & Telescope](https://skyandtelescope.org/astronomy-news/newly-discovered-asteroid-has-slight-chance-of-earth-impact-in-2032/)
- Deen found ATLAS pre-discovery observations of interstellar comet 3I/ATLAS from 5–25 June 2025 and explained the miss by Galactic-Centre star fields — [Wikipedia 3I/ATLAS](https://en.wikipedia.org/wiki/3I/ATLAS); he found pre-discovery images of C/2025 D1 (Groeller) back to 2018 and is a co-author — [Astronomy.com](https://www.astronomy.com/science/astronomers-have-spotted-the-most-distant-comet-ever-discovered/); his precovery confirmed 2023 FW13's 1:1 Earth resonance — [Tony Dunn on X](https://x.com/tony873004/status/1643213390712836101); interviews on his methods — [skaw.sk](http://www.skaw.sk/interview-with-sam-deen.html), [Felix](https://felixonline.co.uk/articles/detecting-asteroids-in-conversation-with-sam-deen/)
- MPC policy change: the July 2025 newsletter says everyone wishing to submit observations from public archives must go through a verification process — [MPC Newsletter Jul 2025](https://www.minorplanetcenter.net/media/newsletters/MPC_Newsletter_Jul2025.pdf); the October 2025 newsletter lists archives and their observatory codes (ATLAS, CSS, Cerro Tololo, DECam) and describes the Singletons and Archival Submission Committee (SARC) — [MPC Newsletter Oct 2025](https://minorplanetcenter.net/media/newsletters/MPC_Newsletter_Oct2025.pdf)
- MPC credit mechanics: every submission must carry observer (OBS), measurer (MEA) and telescope header lines, with the observatory code (COD) first — [MPC ObsDetails](https://www.minorplanetcenter.net/iau/info/ObsDetails.html); [MPC optical format](https://www.minorplanetcenter.net/iau/info/OpticalObs.html); report only detections with SNR high enough to survive independent image review; single positions cause the whole submission to be rejected — [MPC Guide to Minor Body Astrometry](https://www.minorplanetcenter.net/iau/info/Astrometry.html)
- Observatory codes require qualifying measurements (secondary summary: at least seven numbered minor planets incl. one NEO, fainter than 14th mag, on two nights) — [BAA](https://britastro.org/asteroids/Astrometry%20-%20Obs%20Code.htm); community thread on applying — [Cloudy Nights](https://www.cloudynights.com/forums/topic/954678-applying-for-an-mpc-observatory-code/)
- Large-scale archival reprocessing is also being done professionally: NEAT survey images were reprocessed and reported to the MPC (2025) — [arXiv 2503.20032](https://arxiv.org/pdf/2503.20032)
- Sungrazer: the 5,000th SOHO comet was found 25 March 2024 by Hanjie Tan, a participant since age 13 who has found >200 comets since 2009 — [NRL](https://www.nrl.navy.mil/Media/News/Article/3720019/nrls-sungrazer-project-discovers-5000th-comet/); [NASA](https://science.nasa.gov/science-research/heliophysics/esa-nasa-solar-observatory-discovers-its-5000th-comet/); SOHO had 5,204 sungrazing comets by spring 2026 — [Universe Today](https://www.universetoday.com/articles/comet-r3-panstarrs-at-perihelion); 2025 confirmation batches include the first comets from NOAA GOES-19/CCOR-1 — [Sungrazer](https://sungrazer.nrl.navy.mil/)
- SOHO status: ESA fact sheet lists mission end as 31 December 2025 — [ESA](https://sci.esa.int/web/soho/-/47368-fact-sheet); ESA planned a two-year post-operations phase from 1 January 2026 — [The Register](https://www.theregister.com/AMP/2024/12/03/soho_29_years/); Karl Battams said SOHO is expected to continue at least until September 2026 with no formal end announced — [Sky & Telescope](https://skyandtelescope.org/astronomy-news/the-solar-and-heliospheric-observatory-celebrates-30-years-in-space/); Sungrazer states it intends to outlive SOHO using SECCHI, WISPR and planned telescopes — [Sungrazer](https://sungrazer.nrl.navy.mil/)
- Zooniverse asteroid projects: The Daily Minor Planet (Mount Lemmon images) says new discoveries are usually placed in the Isolated Tracklet File; it lists 4,687 main-belt and 110 NEAs reported — [Zooniverse results](https://www.zooniverse.org/projects/fulsdavid/the-daily-minor-planet/about/results); 2023 TW was the closest NEA found by a citizen-science initiative — [U Arizona](https://news.arizona.edu/news/citizen-science-project-nets-new-asteroid-and-its-close-one); a Bok Telescope workflow was added in March 2026 — [Zooniverse blog](https://blog.zooniverse.org/2026/03/)
- IASC's Zooniverse project on Pan-STARRS candidates (Nov 2025): validated finds are reported to the MPC; volunteers have spotted more than 19,000 previously unreported asteroids — [NASA Science](https://science.nasa.gov/get-involved/citizen-science/new-way-you-can-discover-asteroids/)
- Designation flow example: 2025 PN7 got an internal survey ID (P12dHmP) and then the MPC provisional designation on announcement — [Wikipedia](https://en.wikipedia.org/wiki/2025_PN7)
- Active Asteroids (Zooniverse, DECam images): citizen scientists found fifteen active asteroids — [Universe Today](https://www.universetoday.com/articles/citizen-scientists-find-fifteen-active-asteroids); project results page notes Deen independently flagged 2019 OE31 — [Zooniverse](https://www.zooniverse.org/projects/orionnau/active-asteroids/about/results); Rubin Comet Catchers (comet/solar-system activity) promoted March 2026 — [Zooniverse blog](https://blog.zooniverse.org/2026/03/)
- DASCH: scanning finished 28 March 2024 with 435,763 plates; DR7 (29 Dec 2024) delivers all-sky light curves ~1880–1990 calibrated to APASS — [arXiv 2501.12977](https://arxiv.org/abs/2501.12977); [AAS news](https://aas.org/posts/news/2024/03/harvards-dasch-scanning-project-now-complete); [DASCH](https://dasch.cfa.harvard.edu/about/); VO table access — [GAVO](http://dc.g-vo.org/tableinfo/dasch.narrow_plates). No source linked DASCH to asteroid precovery or amateur work.
- Telescope-based amateur context (not laptop-only): Filipp Romanov found NEA 2026 CQ3 (Feb 2026) using remote telescopes; his tally is 82 variable stars, 10 planetary-nebula candidates, 3 novae, 3 supernovae, 13 asteroids — [Universe Today](https://www.universetoday.com/articles/dedicated-amateur-beats-all-sky-surveys-to-asteroid-discovery); [Universe Today pair](https://www.universetoday.com/articles/amateur-astronomer-makes-pair-of-asteroid-discoveries)

### Inferences
- Precovery/arc extension of newsworthy objects (new NEOs with non-zero impact probability, interstellar objects, quasi-satellites, record-perihelion comets) is the highest-leverage laptop niche in small bodies: each success is newspaper-worthy and credits the measurer in the MPC record. Competition is "some" (Deen plus a few others), but the July 2025 MPC verification step means a newcomer must plan for an onboarding hurdle and must submit multi-position tracklets, not singletons.
- "Lost asteroid recovery" (re-finding objects with stale orbits in modern survey archives) was not specifically evidenced in my results; it is methodologically identical to precovery and plausibly open, but I found no 2023–2026 amateur example, so rate "unverified".
- Sungrazer is "crowded" (a handful of hunters find hundreds each) but has guaranteed credit; the new CCOR-1 stream (first confirmations in 2025) is a fresh sub-niche with fewer experienced eyes, time-limited by SOHO's uncertain future.
- Zooniverse asteroid clicking is "crowded" and produces ITF entries rather than personal designations; not suited to the user's goal of a nameable finding.

### Gaps
- No DASCH-based amateur result found; whether an amateur can submit DASCH-derived astrometry to the MPC under the archival process is unknown (prior knowledge: DASCH astrometry is coarse and mostly used for photometry).
- Sungrazer's current reporting rules, and whether automated detection pipelines are permitted, were not read this session.
- SOHO operational status after September 2026 could not be confirmed.

## Q4. Variable stars and transients: how many new variables are amateurs still registering in VSX, with what data, and is there an under-examined dataset?

### Takeaway
No source gives an annual count of amateur VSX additions, but individual amateurs are still registering tens of new variables each (a 50-star ZTF batch in 2024; 82 lifetime for Romanov; six ground+TESS variables in a 2026 arXiv paper), VSX moderators actively coach first-time submitters, and TESS FFI multiple-star oddities (52 eclipsing quadruple candidates, Oct 2025) are a live amateur co-authorship channel. TNS is open to amateurs and accepts archival non-detection info, so an archival transient report is procedurally possible.

### Cited Findings
- VSX accepts amateur batch discoveries: 50 new variables from ZTF added in one batch (Nov 2024) — [Cloudy Nights](https://www.cloudynights.com/forums/topic/943451-my-first-major-discovery-50-new-variable-stars%EF%BC%81/); a January 2025 AAVSO forum thread shows a first-time submitter being guided by VSX team member Sebastián Otero on light-curve classification — [AAVSO forum](https://forums.aavso.org/t/how-to-vsx-and-variable-star-discovery/1490)
- An amateur (Maksym Pyatnytskyy) published six new variables found with a small telescope and characterised with TESS data, using his own tools LCV and VS-fit (arXiv Apr 2026) — [arXiv 2604.27176](https://arxiv.org/html/2604.27176)
- "52 Eclipsing Quadruple Star Candidates Discovered in TESS Full Frame Images" (Oct 2025) lists several amateur astronomers and Zooniverse citizen scientists among its authors — [arXiv 2510.27470](https://arxiv.org/pdf/2510.27470)
- Older AAVSO note on cross-matching TESS FFI photometry (sectors 1–5) against VSX "VAR" entries — [AAVSO](https://www.aavso.org/tess-full-frame-images-and-vsx-type-var); VSX historically described as >400,000 variables found by amateurs and professionals, now far larger after survey imports — [AAVSO](https://www.aavso.org/vsx-surpassed-2000000-object-milestone)
- Professional TESS FFI variable searches exist (e.g., subdwarf-B variability series clarifying 2,995 targets and finding 1,403 variables) — [MNRAS](https://dx.doi.org/10.1093/mnras/stac3676)
- Transients: SN 2025umq was discovered by amateur Filipp Romanov and classified as a fading Type Ia — [Universe Today](https://www.universetoday.com/articles/dedicated-amateur-discovers-supernova-in-remote-galaxy); SN 2025coe (Ca-rich Type Ib) was detected by amateur Koichi Itagaki and followed up via Astro-COLIBRI/RAPAS — [arXiv 2507.10226](https://arxiv.org/pdf/2507.10226)
- TNS rules: registration is open to professionals and amateurs; a discovery (AT) report needs a last non-detection and a mandatory discovery photometry point, but archival information and comments may be given in place of a measured non-detection; reporting group and data source can be the same (amateur case); AT designation first, SN name after a spectrum — [TNS getting started](https://www.wis-tns.org/content/tns-getting-started); [TNS AstroNote 2019-136](https://www.wis-tns.org/astronotes/astronote/2019-136); [TNS 2025 presentation](https://www.wis-tns.org/sites/default/files/presentations/TNS_SoXS_Sep_2025.pdf)
- Rubin context for transients: first world-public alerts went to brokers on 24 Feb 2026 — [NOIRLab](https://noirlab.edu/science/news/announcements/sci26008); alert archive available via RSP since 18 June 2026 and Early Data Preview 2 since 27 July 2026 — [RSP updates](https://rsp.lsst.io/updates/index.html); fuller DP2 expected Oct–Dec 2026 — [CASRAI](https://casrai.org/news/lsst-data-preview-2-researcher-data-access); DR1 expected ~2 years after survey start — [RTN-011](https://rtn-011.lsst.io/v/SP-2280/RTN-011.pdf); the 10-year survey reportedly began 30 June 2026 with up to 7 million alerts/night — [TechTimes (secondary)](https://www.techtimes.com/articles/319434/20260701/rubin-observatory-begins-lsst-nightly-7-million-alert-stream-will-test-if-dark-energy-evolves.htm); [APS Physics](https://physics.aps.org/articles/v19/31)

### Inferences
- The under-examined dataset for VSX-registrable discoveries is the newest ZTF data releases (DR20+ epochs after the 2020 VSX import) and TESS FFI light curves for faint/crowded-field stars, filtered for types that pipelines under-report (long-period EAs with few eclipses, low-amplitude rotational variables, eclipsing systems with extra eclipses). The Zhang batch is direct evidence the ZTF route works for an individual.
- Archival-only supernova discovery on TNS is procedurally allowed but practically crowded: ZTF/ATLAS/Rubin brokers report in near-real time, so an archival-only amateur find would be a historical, unreported transient (e.g., in older ZTF/PTF/DASCH data), which is publishable (RNAAS/JAAVSO) but unlikely to win a "SN" name without a spectrum.

### Gaps
- No annual statistics on amateur VSX submissions; AAVSO annual report not reachable.
- VSX's formal acceptance criteria for survey-only discoveries could not be read (prior knowledge, unverified: VSX requires period, epoch, range, type, a light-curve plot, and a check against VSX/Gaia DR3/ZTF catalogues; moderation typically takes days to weeks).

## Q5. Pulsars and FRBs: public radio data where amateurs have found pulsars, and laptop feasibility

### Takeaway
Volunteer pulsar discoveries come through Einstein@Home (distributed compute, >90 neutron stars in 20 years) and its Zooniverse spin-off Pulsar Seekers (240,000 PALFA candidates classified, >4,400 flagged promising, no credited discovery yet); CHIME's own daily stacking search (CHAMPSS) and single-pulse pipelines dominate CHIME data, and I found no evidence that CHIME or FAST search-mode data are open in a form an amateur laptop could search. Rate: open-niche-in-theory, infeasible-in-practice.

### Cited Findings
- Einstein@Home has discovered more than 90 neutron stars and helped find 39 gamma-ray pulsars in Fermi data; >500,000 volunteers — [AEI 20th anniversary](https://www.aei.mpg.de/1226437/happy-20th-birthday-einstein-home); [Einstein@Home](https://einsteinathome.org./); a Nov 2025 ApJ search near the Galactic Centre found four new gamma-ray pulsars — [Einstein@Home news](https://einsteinathome.org/news)
- Pulsar Seekers (Zooniverse, launched Oct 2023, led by Rahul Sengar, UWM): volunteers made millions of classifications on >240,000 PALFA candidates; >4,400 classified as promising after scientist review; volunteers whose computers contributed will be credited if pulsars are confirmed — [Einstein@Home update](https://einsteinathome.org/content/update-%E2%80%9Ceinsteinhome-pulsar-seekers%E2%80%9D); [MPG](https://www.mpg.de/21023035/a-new-citizen-science-project-allows-you-to-search-for-pulsars-from-home); [UWM](https://uwm.edu/physics/in-focus-citizen-scientists-can-now-also-use-their-brains-to-help-find-new-pulsars/)
- PALFA single-pulse discoveries paper (Aug 2026) with timing of five RRATs — [arXiv 2608.08754](https://arxiv.org/abs/2608.08754)
- CHIME: CHAMPSS found eleven new isolated pulsars in a two-month commissioning patch, code on GitHub, ~1 ms resolution limits MSP sensitivity — [arXiv 2504.16293](https://arxiv.org/html/2504.16293v2); CHIME/FRB single-pulse searches produced new pulsars and RRATs — [ApJ 2021](https://iopscience.iop.org/article/10.3847/1538-4357/ac1da6); CHIME J0630+25, a 421-s long-period transient — [ApJL](https://iopscience.iop.org/article/10.3847/2041-8213/adfa8e); CHIME's publications page links public FRB data and pulsar data releases — [CHIME](https://chime-experiment.ca/fr/publications/)

### Inferences
- The only realistic amateur route to a credited pulsar is Pulsar Seekers or Einstein@Home compute; both are collective credit, not individual discovery, and no new discovery has been credited to Pulsar Seekers yet.
- A laptop single-pulse or FFA search on a small, public, already-dedispersed CHIME/FRB or GBT data product is conceivable in principle (CHAMPSS code is public) but I found no public search-mode data product sized for a laptop. Rate as "not recommended" for the user's goal.

### Gaps
- FAST open-data policy, GBT/Parkes (CSIRO Data Access Portal) and LOFAR public pulsar survey data were not searched (budget). Prior knowledge (unverified): CSIRO DAP hosts Parkes raw data with an 18-month proprietary period, which is laptop-searchable only in small chunks.

## Q6. Meteors and fireballs: GMN open data, new showers, Canadian angle

### Takeaway
GMN is Canadian-led (Denis Vida, Western University), has >450 cameras in 23 countries including Ontario, and reported roughly eight new showers in 2025 alone (M2025-F1, -S1, -S2, -U1, -V1, -Y1, plus Eridanus and Aries) with 418 showers identified cumulatively, so new-shower discovery from GMN orbits is demonstrably still happening; the work is done by a small circle, giving "some competition" rather than "crowded".

### Cited Findings
- GMN 2025 report: 418 different meteor showers identified among the network's orbits; new 2025 showers listed include M2025-S1 (Delphinus), M2025-S2 (Hydrus), M2025-U1 (Pegasus), M2025-V1 (Monoceros), plus one in Eridanus and one in Aries — [eMeteorNews GMN report 2025](https://www.emeteornews.net/2026/02/06/global-meteor-network-report-2025/); 2024 report — [eMeteorNews](https://www.emeteornews.net/2025/02/15/global-meteor-network-report-2024/)
- M2025-F1 (Puppis) detected 18–22 March 2025, weak — [AMS outlook](https://www.amsmeteors.org/2026/03/meteor-activity-outlook-for-march-21-27-2026/); M2025-Y1: strong mid-December outburst, 370 GMN meteors, linked to a dust-trail encounter and possibly the December kappa-Draconids — [eMeteorNews GMN report 2025](https://www.emeteornews.net/2026/02/06/global-meteor-network-report-2025/)
- Confirmations: M2024-S1 returned 21–23 Sept 2025 with 89 meteors recorded 19–30 Sept — [eMeteorNews](https://www.emeteornews.net/2025/10/28/m2024-s1-activity-confirmed-in-2025/); M2024-N1 (Fornax) recurred 30 June–5 July 2025 with 38 meteors — [eMeteorNews](https://www.emeteornews.net/2025/12/24/m2024-n1-activity-confirmed-in-2025/)
- Method paper: "Meteoroid orbit shower identification method and its application in meteor shower case studies" (March 2026) — [eMeteorNews](https://www.emeteornews.net/2026/03/20/meteoroid-orbit-shower-identification-method-and-its-application-in-meteor-shower-case-studies/)
- A researcher describes finding a new shower whose parent is an asteroid being broken down by the Sun — [The Conversation](https://theconversation.com/i-found-a-new-meteor-shower-and-it-comes-from-an-asteroid-getting-broken-down-by-the-sun-277557); SETI Institute/CAMS report on Volantids 2025–26 and chi Cygnids 2025 — [SETI](https://www.seti.org/news/volantid-meteors-2025-2026/), [SETI](https://www.seti.org/news/chi-cygnid-meteor-shower-2025/)
- GMN is led by Denis Vida at Western University; >450 cameras hosted by amateurs and professionals in 23 countries; first system installed at Western in 2017; cameras in Ontario, Quebec and Alberta — [Western News](https://news.westernu.ca/2021/07/global-meteor-network/); GMN methods paper — [MNRAS](https://academic.oup.com/mnras/article/506/4/5046/6347233)
- Western also runs the Southern Ontario Meteor Network (SOMN) with more than a dozen all-sky cameras; the 17 April 2022 Lake Simcoe fireball likely dropped meteorites near Argyle, Ontario — [Western media relations](https://mediarelations.uwo.ca/2022/04/18/lake-simcoe-possible-meteorites/); [Western News](https://news.westernu.ca/2022/04/westerns-sky-cameras-capture-fireball-event/); [Space.com](https://www.space.com/fireball-alert-meteorites-possible-ontario-canada); NASA's fireball event pages list Ontario-region events — [NASA fireballs](https://fireballs.ndc.nasa.gov/skyfalls/events/20230220-015040)

### Inferences
- New-shower discovery is "some competition": most 2025 reports come from the GMN core team and a few European amateurs writing in eMeteorNews. An amateur can plausibly contribute (a) a new minor shower or outburst via orbit clustering on the most recent season's data, (b) a parent-body linkage (orbital similarity to a numbered asteroid/comet) for one of the 2025 "M2025-xx" showers, which is exactly what the Conversation piece describes, or (c) an Ontario-specific fireball/orbit analysis.
- Validation path: report to the IAU Meteor Data Center (provisional designation and inclusion in the shower working list) and publish in eMeteorNews or WGN; the GMN team is reachable and has co-authored with amateurs.

### Gaps
- GMN open-data URL and licence could not be confirmed this session (prior knowledge, unverified: orbit data are published daily at globalmeteornetwork.org/data under CC BY 4.0 in CSV/JSON).
- Whether any of the 2025 showers already have parent-body identifications was not verified.
- Radio meteor (RMOB) and Canadian Meteor Orbit Radar open data were not searched.

## Q7. Exoplanet-archive re-analysis: can an amateur find errors, resonances or TTV signals in published systems?

### Takeaway
I found no 2025–2026 case of an amateur overturning or materially correcting a published exoplanet result from archival re-analysis; amateur TTV work is dominated by telescope-based timing (ETD, Exoplanet Watch), and a 2015 benchmark found amateur timing data too noisy for secure long-term TTVs. With 6+ years of TESS baselines the orbital-decay/precession search is now professional territory; rate "some competition" but low newsworthiness.

### Cited Findings
- A study of the Exoplanet Transit Database (ETD) reports evidence of long-term period variations drawn largely from amateur timings — [arXiv 2209.10752](https://arxiv.org/pdf/2209.10752)
- Undergraduate students maintained exoplanet ephemerides (HAT-P-54 b, 14 new light curves) showing citizen science is viable for ephemeris maintenance — [arXiv 2406.18487](https://arxiv.org/pdf/2406.18487); NASA's Exoplanet Watch rationale — [arXiv 1903.07716](https://arxiv.org/pdf/1903.07716)
- 2015 benchmark of amateur observatories for TTV detection: no TTV series showed a long-term quadratic variation at ≥2σ; amateur data "often have only a moderate quality" — [MNRAS](https://academic.oup.com/mnras/article/450/3/3101/1066663)
- Citizen scientists' role in 2025 confirmations is observational (TOI-4465 b: TFOP SG1, Unistellar network, TSTPC working group) — [Universe Today](https://www.universetoday.com/articles/worldwide-team-of-citizen-scientists-help-confirm-a-tricky-exoplanet); amateur observing guide — [Conti guide](https://astrodennis.com/Guide.pdf)
- The NASA Exoplanet Archive is the public master table (6,451 confirmed planets, mid-Oct 2026) — [NASA Exoplanet Archive](https://exoplanetarchive.ipac.caltech.edu/); 2026 news archive — [Exoplanet Archive news](https://exoplanetarchive.ipac.caltech.edu/docs/exonews_archive.html)

### Inferences
- A laptop TTV/orbital-decay re-analysis across all TESS hot Jupiters is doable with lightkurve + batman/juliet, but professionals publish such catalogues regularly, so the chance of a genuinely new result is modest; a narrower, more defensible target is a candidate-level anomaly (e.g., a TESS-only TTV signal for a system with no RV mass) written up as an RNAAS note. No evidence either way that this is "done" for any specific system.

### Gaps
- No search was possible for RNAAS notes by amateurs 2025–2026 (budget).

## Q8. Official recognition pathways open to individuals and what each requires

### Takeaway
Four pathways are confirmed open to individuals with no institution: MPC (archival submissions now need verification via SARC; measurer credit via MEA header; a personal observatory code needs telescope astrometry), AAVSO VSX (accepts survey-data batch discoveries with discoverer credit), ExoFOP CTOI (independent researchers assign CTOIs; promotion to TOI by the TESS team), and TNS (registration open to amateurs; archival non-detections allowed). Sungrazer and the IAU Meteor Data Center are domain-specific equivalents. ATel, IAU naming and RNAAS/JAAVSO policies were not verified this session.

### Cited Findings
- MPC: archival-data submitters must pass a verification process (July 2025) — [MPC Newsletter Jul 2025](https://www.minorplanetcenter.net/media/newsletters/MPC_Newsletter_Jul2025.pdf); archive observatory codes and SARC — [MPC Newsletter Oct 2025](https://minorplanetcenter.net/media/newsletters/MPC_Newsletter_Oct2025.pdf); OBS/MEA/COD header credit — [MPC](https://www.minorplanetcenter.net/iau/info/ObsDetails.html); observatory code issued after qualifying measurements with placeholder code XXX — [MPC Astrometry guide](https://www.minorplanetcenter.net/iau/info/Astrometry.html), [BAA](https://britastro.org/asteroids/Astrometry%20-%20Obs%20Code.htm)
- VSX: amateur batch of 50 ZTF variables accepted (2024) — [Cloudy Nights](https://www.cloudynights.com/forums/topic/943451-my-first-major-discovery-50-new-variable-stars%EF%BC%81/); moderator guidance to new submitters — [AAVSO forum](https://forums.aavso.org/t/how-to-vsx-and-variable-star-discovery/1490)
- ExoFOP: CTOIs are assigned by independent researchers, TOIs by the TESS team — [Wikipedia TESS](https://en.wikipedia.org/wiki/Transiting_Exoplanet_Survey_Satellite); >8,000 candidates on ExoFOP — [NASA Exoplanet Archive](https://exoplanetarchive.ipac.caltech.edu/); TOI-6692 b went CTOI → TOI → confirmed with amateur co-authors — [arXiv 2601.16357](https://arxiv.org/html/2601.16357)
- TNS: open registration for amateurs; AT report fields; archival info may replace a measured non-detection — [TNS getting started](https://www.wis-tns.org/content/tns-getting-started)
- Sungrazer: SOHO comets are credited to the reporting volunteer (e.g., Hanjie Tan, >200 comets) — [NRL](https://www.nrl.navy.mil/Media/News/Article/3720019/nrls-sungrazer-project-discovers-5000th-comet/)
- Meteor showers: new GMN showers receive "M2025-xx" style provisional designations and are published in eMeteorNews — [eMeteorNews GMN report 2025](https://www.emeteornews.net/2026/02/06/global-meteor-network-report-2025/)
- Zooniverse: 31 NASA-sponsored projects since 2020; 1 billion classifications reached June 2026; ~60–70 active projects — [NASA](https://science.nasa.gov/get-involved/citizen-science/nasa-volunteers-help-zooniverse-reach-1-billion-classifications/), [Adler](https://www.adlerplanetarium.org/news/one-billion-volunteer-contributions-zooniverse/); current astronomy projects include Rubin: Blobs and Blurs, Artifact InSPECtor, Looking for Strange Galaxies — [Zooniverse projects](https://www.zooniverse.org/projects); Galaxy Zoo "What the Shell?" in development (Oct 2026) — [Zooniverse blog](https://blog.zooniverse.org/)

### Inferences
- For a Toronto undergraduate the lowest-friction credited pathways are VSX (days–weeks, no institution) and CTOI (account only), then the IAU MDC/eMeteorNews route for showers (GMN is at Western, two hours away), then MPC archival measurement (verification hurdle, but highest news value), then Sungrazer (guaranteed credit, steep learning curve).

### Gaps
- ATel posting policy for non-institutional authors, IAU naming rules, RNAAS and JAAVSO author eligibility were not verified this session (prior knowledge, unverified: RNAAS accepts any author with an AAS account for a fee or waiver; JAAVSO is explicitly amateur-friendly; ATel requires registration and is typically professional).

## Q9. Vetted shortlist of candidate projects (synthesis of Q1–Q8)

### Takeaway
Twelve laptop-only, free-data projects are listed below with the seven requested attributes. The strongest combination of novelty, verifiability and news value for a Toronto maths undergraduate is: (1) archival precovery/arc-extension of newly announced NEOs and comets; (2) a new minor meteor shower or parent-body link from GMN orbits (Western University angle); (3) a Gaia DR4 release-day pipeline (2 Dec 2026); (4) ZTF/TESS batch discovery of new eclipsing binaries registered in VSX; (5) single-transit long-period candidates in TESS FFIs submitted as CTOIs. The Rabtsevich-style short-period TESS re-search is rated crowded.

### Cited Findings
- Evidence for each project's saturation rating is given in Q1–Q8 above; key anchors repeated here: Rabtsevich/TIC 4206066 (Oct 2026) — [Scientific American](https://www.scientificamerican.com/article/amateur-astronomer-harnesses-ai-to-find-a-possible-hidden-exoplanet/); TOI-6692 b single-transit volunteer discovery (Jan 2026) — [arXiv 2601.16357](https://arxiv.org/html/2601.16357); 50 ZTF variables into VSX (Nov 2024) — [Cloudy Nights](https://www.cloudynights.com/forums/topic/943451-my-first-major-discovery-50-new-variable-stars%EF%BC%81/); ~8 new GMN showers in 2025 — [eMeteorNews](https://www.emeteornews.net/2026/02/06/global-meteor-network-report-2025/); Deen's 2024 YR4 precovery — [Sky & Telescope](https://skyandtelescope.org/astronomy-news/lunar-impact-from-asteroid-2024-yr4-ruled-out/); MPC archival verification (Jul 2025) — [MPC](https://www.minorplanetcenter.net/media/newsletters/MPC_Newsletter_Jul2025.pdf); Gaia DR4 on 2 Dec 2026 — [ESA](https://www.cosmos.esa.int/web/gaia/news-2026); Backyard Worlds 3,000+ discoveries (May 2026) — [NASA](https://science.nasa.gov/get-involved/citizen-science/nasa-volunteers-double-known-population-of-brown-dwarfs/); SOHO 5,204 comets and uncertain end date — [Universe Today](https://www.universetoday.com/articles/comet-r3-panstarrs-at-perihelion), [Sky & Telescope](https://skyandtelescope.org/astronomy-news/the-solar-and-heliospheric-observatory-celebrates-30-years-in-space/); Rubin public alerts since 24 Feb 2026 — [NOIRLab](https://noirlab.edu/science/news/announcements/sci26008); DASCH DR7 — [arXiv 2501.12977](https://arxiv.org/abs/2501.12977); 52 TESS eclipsing quadruple candidates with amateur co-authors — [arXiv 2510.27470](https://arxiv.org/pdf/2510.27470); Pulsar Seekers status — [Einstein@Home](https://einsteinathome.org/content/update-%E2%80%9Ceinsteinhome-pulsar-seekers%E2%80%9D)

### Inferences
The project cards below are my synthesis; data-access URLs marked (pk) are from prior knowledge and were not verified this session.

**P1. Archival precovery / arc extension of newly announced NEOs, comets and interstellar objects (Sam Deen model)**
1. Discovery: pre-discovery detections of a just-announced object (NEOCP/MPEC list) in public survey images (ZTF, PTF/iPTF, Pan-STARRS DR, DECam via NOIRLab Astro Data Archive, SkyMapper, ATLAS), extending the arc by years; can flip impact probabilities, confirm quasi-satellite/resonant orbits, or find an interstellar object's early trail.
2. Data: MPC NEOCP and MPECs (minorplanetcenter.net); JPL Horizons/Scout for ephemerides; image archives: IRSA ZTF/PTF (irsa.ipac.caltech.edu) (pk), NOIRLab Astro Data Archive (astroarchive.noirlab.edu) (pk), Pan-STARRS DR2 cutouts at MAST (pk), CADC SSOIS (Canadian Astronomy Data Centre Solar System Object Image Search, cadc-ccda.hia-iha.nrc-cnrc.gc.ca) (pk, Canadian angle).
3. Method: compute the object's ephemeris with covariance back 5–15 years; query SSOIS/archives for frames covering the uncertainty ellipse; download cutouts; detect faint moving sources; measure astrometry against Gaia DR3; submit multi-position tracklets.
4. Validation: MPC accepts under the archive's observatory code with the measurer named (MEA); since July 2025 archival submitters must pass SARC verification; successful precoveries appear in MPECs and are cited (Deen is a co-author on C/2025 D1).
5. Time: days per object once tooling exists; 2–6 weeks to build the pipeline and clear verification.
6. Done already? "Some competition": Deen and a few others do this regularly (2024 YR4, 3I/ATLAS, C/2025 D1, 2023 FW13); professionals reprocess whole surveys (NEAT). No evidence of an AI-assisted amateur doing it; newsworthy per object when the target is itself newsworthy.
7. Difficulty: medium-high. False-positive risk: mistaking artefacts/known asteroids for the target; single positions are rejected outright; verification hurdle for newcomers.

**P2. New minor meteor shower, outburst, or parent-body link from Global Meteor Network orbits (Ontario/Western University angle)**
1. Discovery: a previously unlisted shower (gets an "M2026-xx" provisional designation), confirmation of a 2024/2025 shower's return, or identification of a parent asteroid/comet for one of the ~8 new 2025 showers.
2. Data: GMN public orbit database (globalmeteornetwork.org/data, daily CSV, CC BY 4.0) (pk); IAU Meteor Data Center shower list; MPC/JPL small-body orbits for parent search.
3. Method: load all GMN orbits for a season; cluster in orbital-element or geocentric radiant/velocity space (DBSCAN/D-criteria as in the March 2026 method paper); exclude known showers; test significance against sporadic background; for parents, compute D-criterion similarity to all numbered asteroids/comets and integrate orbits.
4. Validation: report to IAU MDC; publish in eMeteorNews/WGN; GMN team (Vida, Western) routinely co-authors with amateurs.
5. Time: 3–8 weeks.
6. Done already? "Some competition": GMN reported M2025-F1/S1/S2/U1/V1/Y1 plus Eridanus and Aries showers in 2025; confirmations of M2024-S1 and M2024-N1 in 2025; a Conversation author found an asteroid-parented shower. The field is small and still finding new showers every year; parent-body links for the 2025 showers were not verified as done (gap).
7. Difficulty: medium. False-positive risk: random clustering of sporadics, small-number statistics, duplicating an existing IAU MDC entry under a different name.

**P3. Gaia DR4 release-day pipeline (2 December 2026): new eclipsing binaries / astrometric companions from epoch data**
1. Discovery: eclipsing binaries or periodic variables in DR4 epoch photometry not in VSX; or astrometric-acceleration/orbital-solution companions (brown dwarf/planet candidates) cross-matched against nothing known.
2. Data: Gaia archive (gea.esac.esa.int) DR4 on 2 Dec 2026; the 29 June 2026 DR4 astrometric time-series pre-release for testing; VSX and ZTF for cross-check.
3. Method: build and test the pipeline on DR3 + the pre-release now; on release day run period searches on epoch photometry for a sky region (e.g., northern high-latitude), cross-match VSX/Gaia DR3 vari, submit a batch to VSX within days; or filter DR4 astrometric binary solutions for sub-stellar mass companions around nearby stars and write an RNAAS note.
4. Validation: VSX entry (discoverer credit); RNAAS/JAAVSO note; CTOI if transiting counterpart exists in TESS.
5. Time: 4–8 weeks prep plus 1–3 weeks post-release.
6. Done already? "Open niche for weeks, then crowded": no amateur Gaia discovery found in 2023–2026; professionals will publish DR4 catalogues within months, so the window is the first weeks.
7. Difficulty: medium. False-positive risk: Gaia scanning-law aliases in periodograms; duplicates with Gaia's own DR4 variability tables (check the release's own classification tables first).

**P4. New variable stars and eclipsing binaries from ZTF (DR20+) light curves, batch-submitted to VSX**
1. Discovery: tens of new EA/EB/EW/rotational variables with discoverer credit.
2. Data: ZTF data releases via IRSA (irsa.ipac.caltech.edu/Missions/ztf.html) (pk) and the ZTF light-curve API; ATLAS/ASAS-SN light curves for confirmation (pk); VSX catalogue mirror on Hugging Face for offline cross-match.
3. Method: choose a sky region or target class (e.g., Gaia DR3 stars with high RUWE or specific colours); pull ZTF g/r light curves; run BLS/Lomb–Scargle; cut on amplitude/period significance; cross-match VSX, Gaia DR3 vari, ZTF periodic catalogue; produce phased plots; submit as a batch.
4. Validation: VSX moderation (team member Sebastián Otero coaches submitters); optional JAAVSO paper.
5. Time: 2–6 weeks for a batch of 20–50.
6. Done already? "Some competition": Zhang's 50-star batch (2024) proves the route; Romanov's 82 lifetime variables; the 2020 VSX import of 665k ZTF periodic variables removed the easy, high-amplitude cases. Not newsworthy per star, but a batch of 50+ earned a forum "major discovery" post and is a solid, verifiable first result.
7. Difficulty: low-medium. False-positive risk: blends in crowded fields, ZTF artefacts, objects already in Gaia DR3 or ZTF catalogues (VSX may still accept if not yet in VSX, but checking is mandatory).

**P5. Single-transit, long-period planet candidates in TESS FFI light curves submitted as CTOIs (VSG model)**
1. Discovery: a long-period (50–500 d) giant or sub-Neptune candidate that SPOC/QLP never flagged.
2. Data: MAST TESS FFI light curves (TESS-SPOC and QLP HLSPs; TESScut) via lightkurve; Gaia DR3 for host properties; ExoFOP for existing TOIs/CTOIs.
3. Method: loop over bright (Tmag < ~11) dwarf stars in recent sectors (EM3 sectors from Sept 2025 are least picked-over); detrend; search for isolated box-shaped dips of 4–20 h; vet with centroid shift, odd-even, momentum-dump timing, nearby-star contamination, Gaia neighbours; estimate period from duration + stellar density.
4. Validation: CTOI on ExoFOP; TFOP SG1 may schedule follow-up; promotion to TOI; co-authorship when confirmed (TOI-6692 b precedent).
5. Time: 4–10 weeks.
6. Done already? "Some competition": VSG volunteers and PHT (now with ML) actively search; TOI-6692 b published Jan 2026; still yielding. Newsworthiness is moderate unless confirmed.
7. Difficulty: medium-high. False-positive risk: scattered light, momentum dumps, eclipsing binaries and blended eclipses — single events are notoriously hard to validate.

**P6. Rabtsevich-style re-search of 2-min/20-s SPOC light curves for shallow short-period transits (listed for completeness)**
1. Discovery: a small (1–2 R_Earth) planet candidate around a nearby bright star missed by pipelines.
2. Data: MAST SPOC light curves; lightkurve; TLS/BLS.
3. Method: as in the TIC 4206066 case: iterative agent-driven search and vetting of ~10^5 stars.
4. Validation: CTOI; TESS re-observation; pre-registration on Zenodo.
5. Time: ~2 weeks (Rabtsevich).
6. Done already? "Crowded": the AI-assisted amateur story broke in October 2026 (Gizmodo, Scientific American, X, Threads, replication repos); professional uniform-vetting catalogues (COUNTESS, June 2026; transformer FFI search, 2025) cover the same space.
7. Difficulty: medium. False-positive risk: high (0.04% depth signals near noise floor; the preprint itself claims no statistical validation).

**P7. Sungrazer comet hunting in SOHO/LASCO and GOES-19 CCOR-1 imagery**
1. Discovery: a new Kreutz-group (or other) sungrazing comet, credited to the finder (SOHO-#### then C/2026 Xn (SOHO) designation).
2. Data: near-real-time LASCO C2/C3 FITS/GIFs from soho.nascom.nasa.gov; CCOR-1 imagery (new in 2025); Sungrazer reporting form (sungrazer.nrl.navy.mil).
3. Method: automated difference imaging/track detection on hourly C3/C2 frames (within Sungrazer's reporting rules, which I could not read this session), then human confirmation and report.
4. Validation: Sungrazer/NRL confirmation batches; MPEC designation.
5. Time: weeks to first find for experienced hunters; variable.
6. Done already? "Crowded": 5,204 SOHO comets; a handful of hunters find hundreds each; but CCOR-1 is new (first confirmations 2025) and SOHO's future beyond Sept 2026 is uncertain — a time-limited sub-niche.
7. Difficulty: medium. False-positive risk: cosmic rays, planets/stars, instrument artefacts; strict reporting rules.

**P8. Backyard Worlds / CatWISE ML search for cold brown dwarfs and unusual-kinematics objects**
1. Discovery: a new T/Y dwarf or hypervelocity substellar object candidate.
2. Data: CatWISE2020, unWISE, NEOWISE-R via IRSA; WiseView; Gaia DR3 for non-detections; Backyard Worlds: Planet 9 / Cool Neighbors on Zooniverse.
3. Method: train/apply a classifier (Caselden precedent) to CatWISE motion/colour features; visually vet with WiseView blinks; submit to the project team for spectroscopy.
4. Validation: project team follow-up spectroscopy; co-authorship on discovery papers.
5. Time: months (spectroscopic confirmation is professional and slow).
6. Done already? "Crowded": 3,000+ discoveries, >2 billion sources still being sifted, ML by volunteers already in use (118 sources, 2024); still productive but credit is shared.
7. Difficulty: medium-high. False-positive risk: latents, blends, artefacts; cannot self-confirm.

**P9. TESS FFI eclipsing-multiple oddities (extra eclipses, triply eclipsing triples, eclipsing quadruples)**
1. Discovery: a new eclipsing quadruple/triple candidate.
2. Data: TESS FFI light curves (MAST); VSX; Gaia DR3.
3. Method: screen known eclipsing binaries in TESS FFIs for a second eclipse period or eclipse-timing variations; Zooniverse-style visual vetting.
4. Validation: VSX update; RNAAS; the Oct 2025 paper "52 Eclipsing Quadruple Star Candidates" credits amateur/Zooniverse co-authors.
5. Time: 4–8 weeks.
6. Done already? "Some competition": an organised amateur-professional group publishes these; newest sectors least examined.
7. Difficulty: medium. False-positive risk: blended neighbouring eclipsing binaries within 21-arcsec pixels.

**P10. DASCH century-long light curves of recently discovered transients/variables (historical outbursts, precovery of novae, dwarf novae, changing-look objects)**
1. Discovery: a historical outburst or long-term trend for an object discovered only in 2020–2026 (e.g., a Gaia/ZTF nova or dwarf nova with 1880–1990 plate detections).
2. Data: DASCH DR7 light curves (dasch.cfa.harvard.edu; VO tables at GAVO); TNS/VSX/Gaia Alerts for target lists.
3. Method: cross-match recent transients against DASCH photometry; flag significant historical brightenings; vet plate defects by inspecting scans.
4. Validation: RNAAS/JAAVSO note; VSX remark update.
5. Time: 3–6 weeks.
6. Done already? "Unverified/open": DR7 is less than two years old; I found no amateur DASCH work and no professional "recent transients in DASCH" catalogue in my results, but could not search specifically (budget).
7. Difficulty: medium. False-positive risk: plate flaws, blends, variable limiting magnitudes.

**P11. Rubin alert-stream filtering via public brokers for rare transient classes**
1. Discovery: an early or rare transient (e.g., fast blue optical transient, nuclear transient) reported to TNS before others.
2. Data: Rubin alerts public since 24 Feb 2026 via brokers (ALeRCE, Fink, Lasair, ANTARES) (pk); Rubin Science Platform alert archive (since 18 June 2026).
3. Method: write a broker filter; monitor nightly; cross-match archival; submit AT reports.
4. Validation: TNS AT designation (amateur registration allowed); classification needs a spectrum from others.
5. Time: continuous, weeks to first credited report.
6. Done already? "Crowded and evolving": brokers and survey teams report in near real time; Rubin Comet Catchers and Rubin: Blobs and Blurs exist on Zooniverse.
7. Difficulty: high. False-positive risk: bogus alerts, artefacts; credit contested with automated reporters.

**P12. K2 single-transit candidates re-observed by TESS: period recovery**
1. Discovery: the orbital period of a K2 single-transit candidate (e.g., EPIC 246251988 b, still needing follow-up per the 2023 K2 C19 paper) by finding a second transit in TESS FFI/2-min data.
2. Data: K2 light curves (MAST), TESS FFIs (TESScut), ExoFOP.
3. Method: list all published K2 single-transit candidates; retrieve all TESS sectors covering them; search for matching-depth/duration events; fit period.
4. Validation: CTOI update on ExoFOP; RNAAS note.
5. Time: 2–4 weeks.
6. Done already? "Unverified": no source found claiming this for recent TESS sectors; Kepler/K2 planet-finding generally is over-mined, but this cross-mission angle was not disproved as done.
7. Difficulty: low-medium. False-positive risk: unrelated systematics mimicking the second event.

Not recommended for the user's goal: Zooniverse asteroid clicking (crowded; ITF entries, not personal designations), pulsar searching (no laptop-sized public search-mode data; Pulsar Seekers has no credited discovery yet), Gaia DR3 binary mining (professional saturation), Kepler planet re-search (over-mined), exoplanet TTV re-analysis (professional saturation, low newsworthiness).

### Gaps
- Hubble/JWST archive asteroid-trail projects, NEOWISE archive mining after the mission's end, SDSS odd-object searches, Active Asteroids 2025 results, and Malik 2025 PHT candidate counts could not be searched (WebSearch budget exhausted).
- All archive URLs marked (pk) and the GMN data licence are from prior knowledge and must be re-verified.
- Rabtsevich's TESS re-observation (31 Oct–26 Nov 2026) will resolve after the date of this note; the newsworthiness of P6 may change if the candidate is confirmed or refuted.
