# Amateur discovery projects in history, archives, ciphers and cultural heritage (laptop + Claude Code + open data)

Research date: 2026-10-21. Research constraints encountered: the Firecrawl connector was out of credits; the shared WebSearch budget ran out after ~45 queries; and the session's outbound proxy refused tunnels (403) to every non-search host tried (paradigm.xyz, crkn-rcdr.ca, ruraldiaries.lib.uoguelph.ca, canadianpoetry.org, meta.wikimedia.org, scienceblogs.de, genealogyalacarte.ca, nli.ie, rrauction.com, colab.bac-lac.gc.ca). All findings below therefore rest on search-result excerpts, not full-page reads. Where a fact could not be sourced it is listed under Gaps rather than asserted.

---

## Key question 1: Ciphers and undeciphered texts — status as of Oct 2026, AI/LLM attacks, and which are dead ends

### Takeaway
Every famous cipher on the user's list is either (a) now effectively closed (Kryptos K4: plaintext found in Sanborn's archived papers in 2025 and sold; a paid verifier now exists), (b) considered too short to be solvable (Zodiac Z13/Z32, Dorabella, Tamam Shud line, McCormick), (c) a probable hoax (Beale), or (d) a corpus-starved ancient script where professional teams with deep-learning pipelines are already competing (Voynich, Indus, Linear A, rongorongo, Cascajal). The realistic amateur wins of the last three years were not famous ciphers but "codebook" puzzles (Silk Dress cryptogram, Feynman/Olum ciphers) solved by cross-referencing digitized reference books, which is a reproducible, laptop-scale method.

### Cited Findings
- Kryptos K4: In September 2025 journalists Jarett Kobek and Richard Byrne found the K4 plaintext while going through Jim Sanborn's papers at the Smithsonian's Archives of American Art — [Royal Examiner](https://royalexaminer.com/the-cias-35-year-old-puzzle-was-cracked-by-accident/). Sanborn had included it by mistake while gathering his papers during cancer treatment about a decade earlier; the files are now sealed until 2075 — [Artnet](https://news.artnet.com/art-world/cia-kryptos-sculpture-code-auction-2677451).
- The researchers agreed not to release the text; the RR Auction sale closed November 20, 2025 — [The Journal (AP)](https://www.the-journal.com/?p=143352); auction announced via [FFXnow, Nov 12 2025](https://www.ffxnow.com/2025/11/12/solution-to-kryptos-sculpture-at-cias-mclean-hq-up-for-auction/).
- RR Auction's own framing is "Discovered, Not Solved": it says headlines calling K4 "solved" are misleading and that the archived material was not the original K4 plaintext/encryption materials — [RR Auction](https://content.rrauction.com/kryptos-k4-discovered-not-solved-heres-what-actually-happened/).
- Buyer: Paradigm (crypto-focused VC) states it now holds the K4 answer and, with Sanborn, built an automated checker using one-way cryptographic functions and secure hardware so that no one at Paradigm sees the answer; solvers pay a $1 fee per submission to deter brute force; K1–K3 answers are published on the site; Sanborn also supplied a new 97-character puzzle "K5" to be released later — [Paradigm: Project Kryptos](https://www.paradigm.xyz/writing/kryptos); [Paradigm: About Kryptos](https://paradigm.xyz/kryptos/about). Sale price reports conflict: "almost a million dollars", Sanborn receiving $770,000 — [goodfest.westfield.com (secondary, low-authority)](https://goodfest.westfield.com/2026/06/crypto-guys-bought-the-answer-to-the-cias-mysterious-kryptos-sculpture/); versus "above $200,000" — [Chip.pl](https://www.chip.pl/2025/11/kryptos-rzezba-siedziba-cia-zagadka-szyfr). Unresolved.
- Zodiac Z13/Z32: David Oranchak (leader of the 2020 Z340 solve) said it is "practically impossible to determine if any" proposed Z13/Z32 solutions are correct because the ciphers are too short to pin down a key; Fayçal Ziraoui's 2021 claims ("My Name is KAYE") were disputed by Oranchak and cryptographer Rémi Géraud — [Boston Globe, June 2021](https://www.bostonglobe.com/2021/06/23/world/ive-cracked-zodiac-french-engineer-says-online-sleuths-are-skeptical); [Audacy](https://www.audacy.com/national/news/zodiac-killer-cipher-solution-divides-experts-enthusiasts). Z340 was solved in Dec 2020 by Oranchak, Blake and van Eycke — [Schmeh, Klausis Krypto Kolumne](https://scienceblogs.de/klausis-krypto-kolumne/readers-of-this-blog-solve-zodiac-killer-message-after-51-years/). A 2025–26 "Marvin Merrill" Z13 claim by "Alex Baber" appears only on a low-quality mirrored page and has no expert acceptance — [mirror page, treat as unverified](https://live.museum.manchester.ac.uk/zodiac/unsolved-zodiac-cipher-z13.html).
- Beale ciphers: only cipher #2 is solved; Craig Bauer argues the whole story is a hoax and the ciphers unsolvable — [Wikipedia: Unsolved! (Bauer)](https://en.wikipedia.org/wiki/Unsolved!). A prediction market on all three being solved by 2032 exists — [Manifold](https://manifold.markets/strutheo/will-someone-solve-all-three-beale).
- Ricky McCormick notes (1999): a 2026 article says no one has cracked them; the FBI says analysts need another sample of the same code or a similar code to progress — [All That's Interesting](https://allthatsinteresting.com/ricky-mccormick); FBI public appeal — [Help Net Security](https://www.helpnetsecurity.com/?p=31196). Schmeh maintains a list of unsolved criminal-case ciphers — [Cipherbrain](https://scienceblogs.de/klausis-krypto-kolumne/unsolved-criminal-cases-with-unsolved-encryptions/).
- Dorabella (1897, 87 symbols): listed as unsolved — [Wikipedia: List of ciphertexts](https://en.wikipedia.org/wiki/List_of_ciphertexts).
- Tamam Shud: Derek Abbott and Colleen Fitzpatrick identified the Somerton Man as Carl "Charles" Webb (b. 1905, Melbourne) via DNA from hair in the plaster death mask, 2022; South Australia Police/FSSA had not verified at time of reporting — [Mental Floss](https://www.mentalfloss.com/posts/somerton-man-dna-results); [ODT](https://www.odt.co.nz/node/2579935). The code line itself remains unsolved — [Schmeh](https://scienceblogs.de/klausis-krypto-kolumne/has-the-somerton-man-been-identified/).
- Feynman ciphers: all three are now solved — David Vierra solved the remaining two in May 2023 (one is Housman's "Terence, This is Stupid Stuff", the other the opening of Feynman's 1953 helium paper) — [Futility Closet, Mar 2025](https://www.futilitycloset.com/2025/03/25/late-progress/). Separately, Paul Relkin solved Paul Olum's two Manhattan Project challenge ciphers after 75+ years — [Research Outreach](https://researchoutreach.org/articles/secret-manhattan-project-ciphers-finally-solved).
- Silk Dress cryptogram: Wayne Chan, a research computer analyst at the University of Manitoba, recognized the structure of late-1800s weather telegrams and matched the text against the 1892 US Signal Service Weather Code; decoded as weather observations from May 27, 1888 (Bismarck ND, plus Winnipeg, Calgary, Thunder Bay); published in Cryptologia, Aug 2023 — [CTV Winnipeg](https://winnipeg.ctvnews.ca/cracking-the-code-messages-found-in-silk-dress-decoded-by-manitoba-researcher-1.6694454); [The Weather Network](https://www.theweathernetwork.com/en/news/science/earth-science/silk-dress-cryptogram-canadian-researcher-cracks-135-year-old-unsolvable-code); [UM Today](https://news.umanitoba.ca/?p=187205).
- LLM "solutions" get rejected fast: in late Aug 2026 Vals AI claimed an LLM decoded the 1653 Urquhart cipher (#28 on Schmeh's Top 50 unsolved list); a day later Reticuli researchers published a GitHub rebuttal arguing the book has no such numerical couplet at all — [pasqualepillitteri.it (German secondary; unverified)](https://pasqualepillitteri.it/de/news/16170/claude-fable-5-1-knackt-urquhart-chiffre).
- Voynich: a 2026 arXiv preprint by Nicolas Turenne (INRAE/IRD) uses LLMs to argue the text was generated by a grammar ("pastiche hypothesis") — [arXiv 2609.20835](https://arxiv.org/pdf/2609.20835). The 2018 Kondrak/Hauer (U Alberta) algorithmic work proposed Hebrew with ~80% dictionary hits for alphagrams but the authors said meaning remained unknown — [U Alberta](https://www.ualberta.ca/research/our-research/news/using-ai-to-uncover-the-mystery-of-an-ancient-manuscript.html); [Smithsonian](https://www.smithsonianmag.com/smart-news/artificial-intelligence-takes-crack-mysterious-voynich-manuscript-180967983/).
- Indus script: Tamil Nadu CM M.K. Stalin announced a US$1M prize (Jan 2025) for a decipherment that satisfies archaeological experts; deep-learning teams are active; no accepted decipherment — [Archaeology Magazine](https://archaeologymag.com/2025/01/prize-offered-to-decipher-indus-valley-script/); [YourStory](https://yourstory.com:443/2025/01/ai-power-4500-year-indus-script-translation); [ThePrint](https://theprint.in/feature/here-are-two-indians-whove-tried-to-crack-the-indus-script-in-last-10-years/2452190/).
- Linear A: University of Melbourne is training deep models on Linear A to test cognacy — [UniMelb MDAP](https://www.unimelb.edu.au/mdap/research/2024-collaborations/using-deep-neural-network-models-in-the-decipherment-of-linear-a); a Feb 2025 review covers the minimum-cost-flow and phonetic-comparison ML approaches and their limits — [Manoj & Perono Cacciafoco 2025](https://anale-lingvistica.reviste.ucv.ro/index.php/laucv/article/view/134); the 2019 MIT method worked on Linear B only because Greek was known — [MIT Technology Review](https://www.technologyreview.com/s/613899/machine-learning-has-been-used-to-automatically-translate-long-lost-languages/). A 2026 amateur "AI engineer decoded Linear A" claim is unconfirmed — [braindetox.kr](https://braindetox.kr/en/posts/ai_decodes_linear_a_2026.html).
- Rongorongo: Ferrara et al. (Sci. Rep., Feb 2024) radiocarbon-dated four Rome tablets; one mid-15th century, three 19th century; script still undeciphered — [PMC10837134](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10837134/).
- Cascajal block: debate remains over authenticity, dating (~900 BCE inferred from associated sherds) and affiliation; its script "apparently left no descendants" — [Wikipedia: Olmec hieroglyphs](https://en.wikipedia.org/wiki/Olmec_hieroglyphs); [HAL 02502631](https://hal.archives-ouvertes.fr/hal-02502631).
- Reference for the whole field: Dunin & Schmeh, *Codebreaking: A Practical Guide* (2023) names Voynich and K4 as having withstood all attempts and notes 3 of 4 Zodiac messages unsolved — [No Starch](https://nostarch.com/codebreaking).

### Inferences
- Dead ends for an amateur with months, not years: Zodiac Z13/Z32, Dorabella, Tamam Shud code line, McCormick (all too short — the leading solver of Z340 says proposed answers are unverifiable), Beale 1 & 3 (likely hoax), Voynich (century of effort; LLM angles already taken by Turenne 2026 and Kondrak 2018), Indus/Linear A/rongorongo/Cascajal (no bilingual, tiny corpora, funded teams; the $1M prize makes Indus the most crowded of all).
- Kryptos K4 is now "pay $1, get a yes/no" — a lottery, not research. K5 (97 chars) will be a fresh, crowded race the day it drops; only worth a weekend.
- The replicable amateur pattern of 2023–26 is "it's a codebook, not a cipher": Chan (weather code), Vierra and Relkin (literary/scientific plaintext). The method — hypothesize a published code/telegraph book, pull it from Internet Archive/HathiTrust, auto-match — is exactly what Claude Code is good at. The scarce input is an unsolved *document*, so the project is really an archive hunt for coded telegrams/postcards/diaries (see shortlist).
- LLM-only "solutions" to famous ciphers draw instant expert rejection (Urquhart, Ziraoui). Any cipher claim must come with a key, a method and reproducible code, and should be submitted to Schmeh's Cipherbrain or Cryptologia rather than press.

### Gaps
- Could not read RR Auction's or Paradigm's pages directly (proxy blocked); the "$1 fee / secure hardware" details come from search excerpts of Paradigm's own site and are self-reported.
- No authoritative 2025–26 FBI/academic statement on Z13/Z32 was found; status inferred from expert comments of 2021 and absence of accepted solutions.
- Could not retrieve Schmeh's current Top-50 list to see which items were solved in 2024–26.

---

## Key question 2: Stylometry and attribution — LLM-era attribution of anonymous Canadian works; open attribution questions

### Takeaway
No computational attribution study of anonymous 19th/early-20th-century Canadian newspaper columns, pamphlets or poems was found; the one well-documented open Canadian attribution question — the anonymous 1829 "Canadian Boat-Song" with 6–8 candidate authors — has been argued only on archival/qualitative grounds, making it a genuinely open niche for a stylometric test (with the caveat that a short poem yields only probabilistic results).

### Cited Findings
- "Canadian Boat-Song" appeared anonymously in Blackwood's Magazine, Sept 1829; candidates proposed include Dunlop, Galt, Lockhart, Moir, Scott and Wilson; the strongest arguments point to Moir — [Wikipedia](https://en.wikipedia.org/wiki/Canadian_Boat-Song). Dowler counts eight names "for whom the laurel of authorship has been claimed"; Needler's *The Lone Shieling* argued Galt's Upper Canada experience as source with Moir as poet; the Eglinton "translation" attribution (1849) and Newbigging's alternative fourth stanza were rejected by 1934 — [Dowler, Canadian Poetry vol. 6](https://canadianpoetry.org/volumes/vol6/dowler.html); [Waterston, "John Galt and The Lone Shieling"](https://canadianpoetry.org/volumes/vol6/waterston.html); [Draper](https://canadianpoetry.org/volumes/vol6/draper.html); Needler's book — [49th Shelf](https://49thshelf.com/Books/T/The-Lone-Shieling).
- Method caveats: Grieve (2023) argues register variation largely explains stylometric authorship results — [Corpus Linguistics and Linguistic Theory](https://research.birmingham.ac.uk/files/183727630/10.1515_cllt_2022_0040.pdf); Furbank & Owens call stylometry "only an aspiration" rather than a science — [Open University](https://oro.open.ac.uk/21562); text length is a key problem for short texts — [Musil study, Univ. of Verona](https://iris.univr.it/handle/11562/986592).
- Closest analogous periodical project: "Hidden Authors and Reading Machines" on the Edinburgh Review 1814–20 — [Open University](https://oro.open.ac.uk/56492).
- Closest analogous journalism-attribution project: a DH study applying stylometry to Willa Cather's unsigned/pseudonymous early journalism (158 texts), noting quantitative methods are reasonable only when external evidence fails — [DH Abstracts](https://dh-abstracts.library.virginia.edu/works/1895).
- Hemingway's Toronto Star pieces were authenticated in 1992 by William McGeary/William Burrill through stylistic (non-quantitative) analysis and archival searches — [St. Thomas Research Online](https://researchonline.stthomas.edu/esploro/outputs/journalArticle/Following-the-fascinating-trail-through-the/991015131546703691).
- Example of a recovered pseudonymous Canadian journalist: a Saskatchewan thesis "Discovering Lily Lewis: a Canadian journalist and new woman" — [HARVEST, U Sask](https://harvest.usask.ca/items/abd639c8-a257-4911-8d54-fab8c3412fbb/full).
- Pseudonymous/anonymous 19th-century Canadian periodical content is indexed at scale: Thomas B. Vincent's index covers 137,943 records of prose, poetry, drama and fiction from 203 nineteenth-century Canadian periodicals, much of it available through Canadiana (reported in search results around the Canadiana Serials dataset — [Érudit dataset record](https://datasets.docs.erudit.org/i18n/en/datasets/crkn_canadiana_serials.html); exact page hosting the Vincent description not verified).

### Inferences
- The Canadian Boat-Song is the single best-defined stylometry target: candidate corpora (Galt, Moir, Lockhart, Wilson, Scott, Dunlop) are all public-domain and on Project Gutenberg/Internet Archive/HathiTrust; a register-matched verse corpus plus Burrows's Delta / General Imposters would be a first. Expect a probabilistic ranking, not proof; the right venue is *Canadian Poetry* (Western) or *Studies in Scottish Literature*, and the Wikipedia talk page.
- A larger, lower-risk stylometry project is pseudonym resolution in Toronto newspapers 1880–1930 (e.g., women's-page columnists and pseudonymous poets in the Globe/Star/World), using Vincent's index for 19th-century items; nobody appears to have done it computationally.

### Gaps
- Search for "Canadian Boat-Song" + stylometric/computational could not be run (budget exhausted); novelty is inferred from the absence of any such study in the attribution-focused results and in the Canadian Poetry essays.
- No source found on LLM-era attribution of any Canadian anonymous text.

---

## Key question 3: Lost works and lost media — precedents, Canadian authors with incomplete bibliographies, recent activity

### Takeaway
The database-sweep precedents are strong and recent (Whitman 2016, Chopin 2017, Higginson, Stoker Oct 2024 — the last by an amateur), and in Canada the Hemingway/Toronto Star, Leacock and Montgomery bibliographies are explicitly known to be incomplete ("Lost Leads", "long lost stories"), but no post-2017 systematic digital sweep of Canadian newspapers for any of them was found.

### Cited Findings
- Walt Whitman's novel *Jack Engle* was found by graduate student Zachary Turpin by searching character names from Whitman's notebooks in a newspaper database (New York Sunday Dispatch, 1852) — [UNL Research](https://research.unl.edu/blog/roots-of-whitmans-lost-novel-discovery-traced-to-nebraska); [CS Monitor](https://proof.csmonitor.com/Books/2017/0221/Found-a-lost-novel-by-Walt-Whitman).
- Bram Stoker's "Gibbet Hill" was found by amateur researcher Brian Cleary in an 1890 Christmas supplement of the Daily Express (Dublin), unknown to biographers for 130+ years; announced Oct 2024 — [National Library of Ireland](https://www.nli.ie/news-stories/news/hidden-bram-stoker-story-unearthed-nlis-archives-amateur-researcher).
- Kate Chopin's "Her First Party" recovered via American Periodical Series Online — [Kent State](https://www.kent.edu/node/616996); two unrecovered Ella Higginson poems found via Readex Early American Newspapers — [WWU](https://wp.wwu.edu/ellahigginson/?p=984).
- Trove-scale precedent: ANU researchers built a database of ~21,000 works of newspaper fiction, most never catalogued — [InfoDocket 2018](https://www.infodocket.com/2018/03/01/australian-national-university-researchers-discover-lost-literary-treasure-trove/); Katherine Bode's *A World of Fiction* analyses ~10,000 works in Trove — [OAPEN record](https://oalib-perpustakaan.upi.edu/Record/oapen_2024_20_500_12657_23996/Description). No Canadian equivalent database was found; Canadiana Serials covers newspapers to 1930 — [Érudit](https://datasets.docs.erudit.org/i18n/en/datasets/crkn_canadiana_serials.html).
- Hemingway/Toronto Star: *Dateline: Toronto* (1985) has 172 articles — [Wikipedia](https://en.wikipedia.org/wiki/Dateline:_Toronto); a 1992 Toronto Star cache added pieces not in prior compilations — [UPI, Mar 1992](https://www.upi.com/Archives/1992/03/02/Cache-of-Hemingway-articles-found/6540699512400/); [Baltimore Sun](https://develop.baltimoresun.com/1992/03/04/world-class-byline); Burrill's *Hemingway: The Toronto Years* (1994) reprints 25 previously overlooked pieces (20 definite + 5 probable per the Star) — [CBRA, U of T](https://cbra.library.utoronto.ca/items/show/6003); [St. Thomas](https://researchonline.stthomas.edu/esploro/outputs/book/Hemingway-The-Toronto-Years/991015131920903691). No computational re-examination found (see KQ2).
- Leacock: Spadoni's *A Bibliography of Stephen Leacock* (1998) includes a "Lost Leads" section of items not located, plus a directory of 200+ newspaper accounts — [ECW Press](https://ecwpress.com/products/bibliography-of-stephen-leacock); review — [Project MUSE](https://muse.jhu.edu/article/516736/pdf); McGill holds a notebook listing ~225 articles in 67 publications 1901–1925 — [Fontanus, McGill](https://fontanus.library.mcgill.ca/article/view/92/104); Leacock fonds MSG 668 — [McGill Archival Collections](https://archivalcollections.library.mcgill.ca/index.php/stephen-butler-leacock-fonds-1).
- Montgomery: *After Many Years: Twenty-One "Long Lost" Stories* (Nimbus 2017), ed. Collins & Woster; Woster "provided hundreds of new citations to the updated Annotated Bibliography of L.M. Montgomery's Stories and Poems" — [49th Shelf](https://49thshelf.com/Books/A/After-Many-Years); [CBC 2017](https://www.cbc.ca/1.4189787). Montgomery published 500+ poems and stories in periodicals — [Nimbus](https://nimbus.ca/store/after-many-years-twenty-one-long-lost-stories-by-lm-montgomery.html).
- Atwood/Frye: Acta Victoriana (Victoria College) is "the oldest publication of this type in Canada"; contributors include Atwood, Frye, Jay Macpherson, E.J. Pratt; *Acta Victoriana 1878–1990: An Index with a Subject Authority List* is on the Internet Archive and "some volumes are available online" — [Victoria University Library research guide](https://library.vicu.utoronto.ca/node/105778).
- Maria Campbell's *Halfbreed*: a doctoral student recovered a passage cut by the publisher; published in *Canadian Literature* — [CWRC](https://cwrc.ca/node/170) (date not given in result).
- Lost film: *Back to God's Country* (1919), "the first Canadian feature film, which was considered lost and rediscovered in an archive", new restoration screened by the Association of Canadian Archivists, April 15 2026 — [CanFilmDay](https://canfilmday.ca/event/association-of-canadian-archivists-presents-back-to-gods-country/); *Secrets of the Night* (1924) found at U of T Libraries 2017 — [U of T News](https://www.utoronto.ca/news/lost-silent-film-rediscovered-u-t-libraries); Dawson Film Find (1978, 372 titles) — [Wikipedia](https://en.wikipedia.org/wiki/Dawson_Film_Find).

### Inferences
- Lost-work hunting in Canada is "some competition" for Montgomery (an active collector/scholar community; the annotated bibliography is maintained) and Hemingway (Star's own librarian swept the files in 1992), but the method used in all precedents was human keyword search. A code-driven sweep (fuzzy OCR search on distinctive phrases, titles, pseudonyms and signature lines across Canadiana, OurOntario, Internet Archive and ProQuest) has not been reported for any Canadian author and is cheap to run.
- Leacock's "Lost Leads" is the most concrete target: it is a published list of items known to exist but not located. Closing even a handful would be publishable in *Canadian Literature* or *Papers of the Bibliographical Society of Canada* and would interest the Leacock Museum (Orillia) and Orillia/Toronto press.
- Lost film discovery is not a computational project (it requires physical archives), so it is out of scope for a laptop-only amateur except for provenance/cross-referencing of catalogue records.

### Gaps
- Could not confirm whether any Hemingway scholar has re-swept the ProQuest Toronto Star since 1994 (no evidence found either way).
- Did not find the current state of the Montgomery annotated bibliography (post-2017 additions) or the list of items in Spadoni's "Lost Leads".
- Whether Acta Victoriana volumes from the 1950s–60s (Atwood's student years) are online and whether Atwood's student pieces are already fully indexed in her published bibliographies was not confirmed.

---

## Key question 4: Local history (Toronto/Ontario) — what is digitized, what local historians find, obvious gaps

### Takeaway
The Toronto Star (1894–2016) and Globe and Mail are fully searchable through library subscriptions, but the Toronto Telegram is not digitized at all, Canadiana's platform currently has no full-text search/API for most newspapers, and Toronto's Chinese-language daily (Shing Wah, 1923–1990) is digitized but currently offline — so the biggest "unexamined" seams are structural (access), not topical. Recent scholarship on the 1918 flu in Toronto is thin (one thesis plus journalism), and Black and Chinese Ontario press are digitized but under-mined.

### Cited Findings
- Toronto Star historical archive (ProQuest) covers 1894–2016, scanned from microfilm print masters — [UNCW Library](https://library.uncw.edu/eresources/toronto_star_proquest_historical_newspapers); Globe and Mail historical archive is searchable cover to cover — [TPL blog](https://blogs.tpl.ca/local-history-genealogy/2016/10/the-globe-and-mail-historical-newspaper-archive/); Jamie Bradburn's guide lists the Toronto Telegram as not yet available online (photo archive at York University) — [Genealogy à la carte](https://genealogyalacarte.ca/?p=42536).
- 1918 influenza: Stacey Hallman's McMaster thesis on infant mortality in Toronto 1917–1921 using Ontario death registrations — [MacSphere](https://macsphere.mcmaster.ca/handle/11375/9427); journal version — [Canadian Studies in Population](https://journals.library.ualberta.ca/csp/index.php/csp/article/view/18968); ~1,750 Torontonians died — [NOW Toronto](https://nowtoronto.com/news/pandemics-past-influenza-hit-toronto-like-a-cyclone/); second wave Sept–Oct 1918 deadliest — [Georgia Straight](https://www.straight.com/living/influenza-pandemic-of-1918-second-wave-was-deadliest-to-hit-toronto); the Globe's own retrospective calls its 1918 under-coverage "puzzling" — [Globe and Mail](https://www.theglobeandmail.com/canada/article-how-the-globe-covered-two-pandemics-a-century-apart).
- Black Ontario press: OurDigitalWorld's Abolitionist Newspapers portal (2019) gives full-text search of *Voice of the Fugitive*, *Provincial Freeman*, *True Royalist* — [OurDigitalWorld](https://ourdigitalworld.org/2019/08/28/announcing-the-odw-abolitionists-collection/); 161 issues 1852–1857 supplied to Canadiana — [Genealogy à la carte](https://genealogyalacarte.ca/?p=44314); Cheryl Thompson's "Mapping Ontario's Black Archive" presented at McMaster, March 6 2025 — [McMaster Library](https://library.mcmaster.ca/digital-assets-black-histories-where-archive-and-technology-collide); Archives of Ontario Black history guide — [AO](https://archives.gov.on.ca/en/access/black_history.aspx); UWindsor SW Ontario Black history exhibits — [UWindsor](https://collections.uwindsor.ca/omeka-s/sw-ontario-black-history/digital-exhibits).
- Chinese Toronto press: *Shing Wah Daily News* ran 1922–1990; digitized issues May 29 1923–Sept 29 1990; the SFU copy is no longer hosted; the Multicultural History Society of Ontario offers on-site access and "is securing future online access via the Internet Archive" — [SFU Library](https://newspapers.lib.sfu.ca/swdn2-collection); CNDHI lists issues and says all CNDHI content migrates to CRKN by June 30 2026 — [CNDHI](https://www.cndhi-ipnpc.ca/en/taxonomy/term/556?page=2); U of T's Canada-Hong Kong Library holds Shing Wah clippings 1940s–50s — [U of T](https://collections.library.utoronto.ca/view/rclc-hkl:root); sample translated items in an iSchool Omeka exhibit — [U of T iSchool](https://omeka.ischool.utoronto.ca/items/show/362).
- Ontario community newspapers: University of Windsor and OurDigitalWorld have digitized Ontario newspapers since 2007 using open-source Tesseract OCR — [IFLA 2017, Rhyno (CC BY 4.0)](https://cf-www.ifla.org/wp-content/uploads/2019/05/assets/newspapers/2017_Iceland/2017-rhyno-en.pdf); OurOntario newspapers described as full text from communities across Ontario, often back to the 19th century — [Laurier Library](https://library.wlu.ca/research/resources/our-ontario-newspapers).
- A student built a conversational AI search over a century of a university newspaper in one semester (Lehigh's *Brown and White*) — [CustomGPT case study](https://customgpt.ai/wp-content/uploads/2024/03/Lehigh-The-Brown-and-White-Case-Study.pdf).

### Inferences
- The 1918 flu in Toronto is under-studied at the daily, street-level scale: a day-by-day reconstruction from Star/Globe death notices, Board of Health bulletins and the Ontario death registrations (FamilySearch) would be new and is the kind of thing the Star's "Once Upon a City" style local-history coverage and *Ontario History* publish.
- Shing Wah is the biggest untouched corpus: ~67 years of a Toronto Chinese daily with no known text-mining project; modern VLM OCR for vertical traditional Chinese newsprint makes it feasible, but online access must first be restored (MHSO/Internet Archive).
- Abolitionist press entity extraction and linking to 1851/1861 census and Wikidata is feasible now (full text exists) but overlaps with Thompson's funded "Mapping Ontario's Black Archive" — coordinate rather than compete.
- The Telegram gap cannot be closed computationally (not digitized).

### Gaps
- Could not verify whether U of T offers ProQuest TDM Studio (text-mining access) for the Toronto Star; the search was blocked by budget. ProQuest/TPL terms generally prohibit bulk download — this is the primary legal risk for any Star-based project and must be checked.
- No specific 2024–26 local-history "discovery" news item from Toronto newspapers was found via the single query run.
- Great Fire of 1904 and Toronto Chinese-Canadian 1900–1930 historiography were not searched specifically.

---

## Key question 5: Handwriting recognition on untranscribed Canadian archives — scale, precedents, open collections

### Takeaway
The scale is enormous and documented (Héritage: 41M pages, ~60% handwritten), institutions have begun HTR at scale (CRKN/LAC transcribed ~600,000 pages of RG10 Indian Affairs letterbooks with Transkribus by Oct 2024 at 5–7% character error), and there are open crowdsourced collections (LAC Co-Lab; Guelph's Rural Diary Archive, ~550 Ontario diaries with explicit "untranscribed" tags) where an amateur HTR + entity-extraction pass has not been reported.

### Cited Findings
- LAC launched Co-Lab in April 2018 for transcription, tagging, translation and description, with themed "challenges" (e.g., Laurier's letters to Zoé Lafontaine, Borden–Hughes correspondence, Rosemary Gilliat Eaton's Arctic diary) and peer review of contributions — [Canada.ca news release](https://www.canada.ca/en/library-archives/news/2018/04/library-and-archives-canada-launches-co-lab.html); [Co-Lab home](https://colab.bac-lac.gc.ca/eng).
- CRKN's Héritage collection: 41 million pages of archival records, ~60% handwritten; pilot transcription project with LAC support — [CRKN pilot](https://crkn-rcdr.ca/en/crkn-launches-pilot-transcription-project); [CRKN–LAC partnership](https://crkn-rcdr.ca/en/crkn-and-library-and-archives-canada-partner-improve-access-digitized-handwritten-materials).
- Oct 2024: Departmental Letterbooks (LAC RG 10, Indian Affairs 1871–1929) "fully transcribed" via Transkribus ICR — first batch ~600,000 pages, full scope ~2 million images, begun March 2023; handwriting error rate 5–7%, typewritten 1–2%; CRKN and LAC to assess sensitivity before release — [CRKN announcement](https://www.crkn-rcdr.ca/en/departmental-letterbooks-fully-transcribed-through-intelligent-character-recognition-icr-pilot); [Scholars Portal Days 2024 slides](https://docs.scholarsportal.info/download/Main/SP/SPDay/Scholars_Portal_Days_2024/WebHome/Presenter%20Slides%20-%20Jason%20Friedman%20%28LT%29.pdf?rev=1.1).
- Rural Diary Archive (University of Guelph): ~550 digitized Ontario diaries, each tagged "transcribed"/"untranscribed" with a Transcription Progress field; volunteer transcription open; e.g., Roseltha Goble diary 1916–1918 (done), Mary Agnes Cooper diary 1906 (untranscribed) — [Browse](https://ruraldiaries.lib.uoguelph.ca/transcribe/items/browse); [Goble item](https://ruraldiaries.lib.uoguelph.ca/transcribe/items/show/336).
- Transkribus is a mature, widely used HTR platform (381 papers 2015–2020 in a systematic review) — [PMC9205146](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9205146/); origins and sustainability issues — [Mühlberger et al., J. Documentation 2019](https://boris.unibe.ch/137985).
- 1931 Census: images online June 1 2023; Ancestry and FamilySearch used AI to produce a fully verified transcription; free name search on LAC's Census Search and FamilySearch — [LAC](https://www.canada.ca/en/library-archives/news/2023/06/the-1931-census-is-now-online.html); [FamilySearch](https://www.familysearch.org/en/newsroom/familysearch-announces-free-1931-census-of-canada); [Genealogy à la carte](https://genealogyalacarte.ca/1931-canada-census-now-searchable-and-free-on-library-and-archives-canadas-website/).

### Inferences
- Institutions are doing bulk HTR on their own priority fonds (RG10), which are also the most sensitive. The amateur opportunity is in small, non-sensitive, already-public collections where nobody will run HTR soon: the Rural Diary Archive's untranscribed diaries and Co-Lab challenges with low completion. HTR output plus LLM entity extraction (people, places, prices, weather, illness) turns diaries into queryable data and surfaces checkable "firsts" (e.g., local reactions to the 1918 flu, the 1913 storm, early automobiles).
- Verification path is unusually clean: Guelph's project team and LAC's Co-Lab reviewers already exist to check transcriptions, and diaries are local-news-friendly.

### Gaps
- Could not load the live Co-Lab challenge list or the Rural Diary Archive's exact untranscribed count (proxy blocked).
- Did not confirm the Rural Diary Archive's image reuse terms or whether the project has itself tested HTR.
- No HTR project on Hudson's Bay Company Archives (Archives of Manitoba) was found; that search returned only generic Transkribus literature.

---

## Key question 6: Wikipedia/Wikidata gaps and errors — systematic LLM error-finding, newsworthiness

### Takeaway
Systematic LLM-assisted error finding has been done at corpus scale (EMNLP 2025 "CLAIRE"/WikiCollide: ≥3.3% of English Wikipedia facts contradict another fact; editors found 64.7% more inconsistencies with the tool), so the method is crowded, but a locally scoped audit (Toronto/Ontario history articles against the Dictionary of Canadian Biography and digitized newspapers) is an open niche with a mixed newsworthiness outlook.

### Cited Findings
- "Detecting Corpus-Level Knowledge Inconsistencies in Wikipedia with Large Language Models" (EMNLP 2025) introduced CLAIRE; random sampling found at least 3.3% of English Wikipedia facts contradict another fact; editors found 64.7% more inconsistencies in the same time with CLAIRE; best AUROC on the WikiCollide benchmark 75.1%, so LLMs are "effective copilots" not automators — [Wikimedia Research Newsletter, Nov 2025](https://meta.wikimedia.org/wiki/Research:Newsletter/2025/November); community discussion — [Lemmy thread](https://lemmy.mariusdavid.fr/post/426784/1351534).
- An informal opinion piece claimed ChatGPT flagged what the author considered valid errors in 28 of 31 featured articles; commenters disputed severity — [PieFed post (opinion)](https://piefed.nullspace.lol/post/65579).
- Historian Timothy Messer-Kruse corrected a sourced error in his specialty and was reverted within minutes — [ArtsJournal](https://www.artsjournal.org/?p=65879); a 24-year-old amateur's year-long rescue of the Washington, D.C. article was newspaper-profiled — [HNN](https://www.historynewsnetwork.org/article/118918).

### Inferences
- "I found N errors in Toronto history articles" is publishable on-wiki (WikiProject Toronto, article talk pages) and plausible for *The Varsity* or a TPL local-history blog; mainstream coverage would depend on at least one error being substantive (a misdated landmark, a misattributed first, a wrong death date for a notable Torontonian) and on primary-source proof (DCB entry, newspaper page image).
- Risks: Wikipedia's revert culture (Messer-Kruse), triviality of most inconsistencies, and the ease with which this reads as "AI critiques Wikipedia" rather than a discovery.

### Gaps
- Could not read the EMNLP paper or the newsletter page directly; no study was found that applied LLM error-checking to local-history articles specifically.

---

## Key question 7: Music, art, film — feasibility for a computational amateur

### Takeaway
AI painting attribution is an active, contested commercial field (Art Recognition's 2025 Caravaggio and Rubens claims are disputed by the Met's former curator and the Centrum Rubenianum; a 2025 benchmark finds vision-language models weak at attribution), lost-film finds require physical archive access, and no lost-Canadian-music angle was researched — this domain is the weakest fit for a laptop-only amateur seeking credible, verifiable findings.

### Cited Findings
- Art Recognition claims a *Lute Player* long catalogued as a copy is a Caravaggio (85.7% by the artist), disputing Sotheby's and the Met; Keith Christiansen had written that no modern scholar would entertain the idea — [Hyperallergic](https://hyperallergic.com/1045583/ai-company-says-it-has-outsmarted-caravaggio-experts/); [Art History News](https://arthistorynews.com/articles/8985_Caravaggio_gets_the_AI_Treatment).
- Rubens *Bath of Diana*: of 29 patches, 10 "authentic" >80%, 8 at 60–80%, 7 inconclusive, 4 inauthentic; Nils Büttner (Centrum Rubenianum) challenged it; CEO Carina Popovici called it "an authenticity evaluation not a confirmation" and acknowledged dataset limits — [Artnet](https://news.artnet.com/art-world/rubens-attribution-ai-authentication-2622500).
- Aug 2025 arXiv study on ~40,000 paintings by 128 artists: vision-language models "have limited capabilities to perform canvas attribution" — [arXiv 2508.01408 via papers.cool](https://papers.cool/arxiv/2508.01408).
- Film precedents: see KQ3 (*Back to God's Country* restoration 2026; *Secrets of the Night* 2017; Dawson 1978).

### Inferences
- An amateur AI attribution of a painting would be dismissed without technical/provenance evidence; the field's own commercial actors are not accepted by connoisseurs. Not recommended.
- Film: the computational contribution would be catalogue cross-referencing (e.g., matching LAC/TIFF/Cinémathèque holdings against "lost film" lists), which is a plausible low-glamour project but was not researched here.

### Gaps
- No search was run on lost Canadian compositions or music manuscripts (budget exhausted). No evidence either way.

---

## Key question 8: Genealogy and cold cases — open datasets, unidentified persons, amateur precedents with code

### Takeaway
The 1931 census is free and fully indexed, and Ontario cold cases have recently been solved by genetic genealogy (DNA Doe Project: Nation River Lady, Algonquin Park John Doe, Montreal River John Doe), but no precedent was found of an amateur making a newsworthy Canadian identification with code or newspaper-archive mining alone; this domain is high-sensitivity and low-probability for a solo student.

### Cited Findings
- Nation River Lady (1975) identified as Jewell Parchman Langford, "believed to be the first case in Canada where remains were identified using this method"; charges later laid — [Global News](https://globalnews.ca/news/9811833/1975-cold-case-ontario-nation-river-lady); [DNA Doe Project](https://dnadoeproject.org/case/nation-river-lady-jane-doe-1975).
- Algonquin Park John Doe (1980) identified after 45 years as Eric "Ricky" Singer of Cleveland — [CTV Barrie](https://www.ctvnews.ca/barrie/article/human-remains-found-in-algonquin-park-45-years-ago-identified/); [DNA Doe Project](https://dnadoeproject.org/case/algonquin-park-john-doe-1980/).
- Montreal River Harbour John Doe (2017) identified via GEDmatch second cousins with OPP — [DNA Doe Project](https://dnadoeproject.org/case/montreal-river-john-doe-2017/); [CBC](https://www.cbc.ca/1.6897628).
- 1931 Census: free, AI-assisted transcription verified by Ancestry/FamilySearch; see KQ5 citations.

### Inferences
- A defensible, non-sensitive genealogy-adjacent project is data-quality work on open indexes (e.g., cross-checking 1931 census AI transcriptions against 1921 and vital records to flag systematic errors), but it is unlikely to be newsworthy.
- Unidentified-persons work should be left to police-partnered genetic genealogists; an amateur's newspaper cross-referencing could at most generate tips for Canada's Missing, not a publishable "finding".

### Gaps
- Canada's Missing / NamUs-style datasets were not reached in search results; no amateur-coder precedent found (absence, not evidence of absence).

---

## Access routes and constraints (cross-cutting)

### Takeaway
Free, machine-readable text is available for Ontario community papers (OurDigitalWorld/OurOntario, Tesseract OCR), abolitionist papers, Internet Archive, HathiTrust and Gutenberg; Canadiana is free but currently lacks full-text search/API for most newspapers (a rebuild with bulk download and API is planned); the Toronto Star/Globe are library-licensed (ProQuest) with text-mining terms unverified.

### Cited Findings
- Canadiana free since Jan 1 2019 — [UWaterloo Library](https://uwaterloo.ca/library/node/1636); ~65 million pages; current platform offers only partial bulk download and no full-text search or IIIF API querying; the planned platform lists bulk download, API access, full-text search/download and machine access for large-scale research — [CRKN: Future Canadiana](https://www.crkn-rcdr.ca/en/future-canadiana); CRKN lists "APIs for research and data mining" among services — [CRKN](https://crkn-rcdr.ca/en/node/16561); single-page PDFs available for documents with OCR data — [Genealogy à la carte](https://genealogyalacarte.ca/?p=38497). Example of a newspaper record with 422 images and "0 with full-text search" — [Canadian Free Press 1849–56](https://www.canadiana.ca/view/oocihm.N_00300_184901).
- Canadiana joined JSTOR's Open Community Collections — [JSTOR](https://about.jstor.org/news/canadiana-joins-jstors-open-community-collections).
- Rights statements are per-item (About tab) under Canadiana Terms of Service — [CRKN](https://crkn-rcdr.ca/en/node/18283).
- Ontario community newspaper OCR built with open-source Tesseract since 2007 — [IFLA 2017](https://cf-www.ifla.org/wp-content/uploads/2019/05/assets/newspapers/2017_Iceland/2017-rhyno-en.pdf).

### Inferences
- For Canadiana newspapers today the practical route is scraping page-level OCR PDFs/IIIF images per item and re-OCRing locally where needed; this is laptop-feasible for a single title/decade but not for the whole corpus.
- Any Toronto Star project must either use the library UI manually (slow but allowed) or obtain TDM access; bulk scraping of ProQuest would breach terms and is the single biggest project-killer.

### Gaps
- ProQuest TDM Studio availability at U of T, OurDigitalWorld API terms, and Canadiana's current IIIF endpoints were not verified (searches/fetches blocked).

---

## Vetted shortlist of candidate projects (ranked; saturation ratings with evidence)

### Takeaway
Twelve projects survive vetting; the top five (Leacock "Lost Leads" closure; Canadian Boat-Song stylometry; Rural Diary Archive HTR; Toronto 1918-flu day-level reconstruction; Canadian "codebook cryptogram" hunt) combine open data, a clear verifier, a plausible newspaper angle, and no evidence of prior computational work. Famous ciphers and AI art attribution are explicitly excluded as dead ends.

### Cited Findings
- All evidence for the cards below is cited in KQ1–KQ8 and the Access section above; each card references the relevant key question rather than repeating URLs, except where a new specific source applies.

### Inferences (project cards)

**P1. Close Leacock's "Lost Leads" (and extend the serial bibliography)**
- Discovery: locate newspaper/magazine pieces that Spadoni's 1998 bibliography lists as known-but-unlocated, plus unrecorded reprints/first appearances in Canadian papers to 1930.
- Data: Spadoni (library copy); McGill Leacock fonds notebook of ~225 articles (KQ3); Canadiana Serials newspapers to 1930; OurOntario community papers; Internet Archive/HathiTrust magazines; Toronto Star/Globe via TPL/U of T (UI search only unless TDM confirmed).
- Method: build a target list from "Lost Leads" (title, approximate date, venue); generate OCR-tolerant fuzzy queries (title variants, first lines, signature "Stephen Leacock", known pseudonyms); batch-search open OCR corpora with Claude Code; manually confirm page images.
- Verification: Carl Spadoni / McGill Rare Books; Leacock Museum (Orillia); publish in *Papers of the Bibliographical Society of Canada* or *Canadian Literature*.
- Effort: 4–8 weeks.
- Saturation: some competition — Spadoni's work is the standard and a 2016–17 McGill *Fontanus* article exists, but no post-1998 digital sweep reported (KQ3).
- Risk: ProQuest ToS; OCR quality on 1900s–20s newsprint; "lost" items may be in sources not digitized.

**P2. Stylometric attribution of the "Canadian Boat-Song" (1829)**
- Discovery: a quantitative ranking of Galt, Moir, Lockhart, Wilson, Dunlop, Scott (and the Eglinton "translation" hypothesis) against register-matched verse corpora — the first computational contribution to a 195-year-old debate.
- Data: Project Gutenberg, Internet Archive, HathiTrust editions of each candidate's verse; Blackwood's 1829 scan on HathiTrust/Internet Archive.
- Method: Burrows's Delta, General Imposters (Koppel/Kestemont), with bootstrapped short-text controls; publish code.
- Verification: *Canadian Poetry* (Western) editors; Scottish literature scholars; Wikipedia talk page; Globe and Mail arts desk has covered the poem before (KQ2).
- Effort: 3–6 weeks.
- Saturation: open niche — all published arguments (Dowler, Waterston, Needler) are archival; no computational study surfaced (KQ2), though that specific query could not be run.
- Risk: 32 short lines → low statistical power; result will be "most consistent with X", not proof; register confounds (Grieve).

**P3. HTR + entity extraction on untranscribed Rural Diary Archive diaries**
- Discovery: first-hand Ontario accounts of datable events (1918 flu, 1913 Great Lakes storm, eclipses, prices, first cars/phones) in diaries nobody has read since digitization; a queryable dataset.
- Data: Rural Diary Archive (Guelph) untranscribed items; cross-reference OurOntario newspapers and FamilySearch Ontario vital records.
- Method: run Transkribus public models / TrOCR / Claude vision on page images; LLM extraction of people, places, weather, illness; cross-check against newspapers for the same day.
- Verification: Guelph project staff review transcriptions (volunteer pipeline exists); local historical societies; *Ontario History*.
- Effort: 6–10 weeks.
- Saturation: open niche for HTR-assisted analysis — the archive relies on volunteer typing; no HTR mention found (KQ5), though the site could not be loaded to confirm.
- Risk: image reuse terms; HTR error rate 5–7% on 19th-century hands; findings may be "charming" rather than newsworthy unless tied to a known event.

**P4. Toronto 1918–19 influenza, day-by-day and street-by-street**
- Discovery: a reconstructed daily death/case curve and neighbourhood map from death notices, Board of Health bulletins and Ontario death registrations; identification of under-reported waves or institutions (schools, barracks, hospitals).
- Data: Ontario death registrations 1918–19 (FamilySearch, free); Toronto Star/Globe (library UI); City of Toronto Archives Board of Health reports; Hallman's thesis as baseline (KQ4).
- Method: extract deaths with cause "influenza/pneumonia" and addresses; geocode to 1918 wards; compare with newspaper reporting volume per day.
- Verification: U of T history of medicine faculty; City of Toronto Archives; *Canadian Bulletin of Medical History*; the Globe's own retrospective shows editorial appetite (KQ4).
- Effort: 8–12 weeks.
- Saturation: some competition — Hallman (infant mortality) and journalism exist; no spatial/daily reconstruction found.
- Risk: ProQuest ToS if automated; address-level mapping of deaths is sensitive but historical (100+ years).

**P5. Canadian "codebook cryptogram" hunt (Silk-Dress method at scale)**
- Discovery: decode coded telegrams/postcards/ledger entries in Canadian archives by matching against digitized commercial/weather/railway codebooks.
- Data: Internet Archive/HathiTrust codebooks (e.g., Signal Service weather codes, ABC/Bentley commercial codes); candidate documents from Canadiana Héritage, Co-Lab, Archives of Ontario, local museums; Schmeh's Cipherbrain unsolved-postcard posts.
- Method: index codebooks into a lookup; write a matcher that scores a document against each codebook; triage candidates with Claude Code.
- Verification: Cryptologia / Klaus Schmeh's blog (the venue that validated Chan); the holding archive.
- Effort: 4–8 weeks, mostly spent finding documents.
- Saturation: open niche — Chan's 2023 solve was a one-off; no systematic codebook-matching tool was found (KQ1).
- Risk: no guarantee of a candidate document; findings are small ("a weather report") unless the document has a story.

**P6. Shing Wah Daily News (Toronto, 1923–1990) OCR and index**
- Discovery: the first searchable index of Toronto's Chinese-language daily — events, organizations and people of Chinatown through the Exclusion era, war, and post-1967 immigration.
- Data: MHSO/Internet Archive scans once online (KQ4); U of T Canada-Hong Kong Library clippings.
- Method: VLM OCR of vertical traditional Chinese newsprint; named-entity extraction; bilingual index.
- Verification: Multicultural History Society of Ontario; Chinese Canadian Museum; U of T Richard Charles Lee Library; coverage plausible in Toronto Star, Sing Tao, Ming Pao.
- Effort: 10–16 weeks after access.
- Saturation: open niche — no text-mining project found; the barrier is access, not competition.
- Risk: scans currently offline; OCR difficulty; needs Chinese reading ability or a collaborator.

**P7. Prosopography of Ontario's abolitionist press (1851–57) linked to census and Wikidata**
- Discovery: a structured list of every person/business named in *Voice of the Fugitive*, *Provincial Freeman*, *True Royalist*, linked to 1851/1861 census entries and Wikidata; surfacing people with no Wikipedia/DCB presence.
- Data: OurDigitalWorld abolitionist portal and Canadiana (full text); FamilySearch census; Wikidata.
- Method: LLM NER + record linkage; publish as open dataset and Wikidata items.
- Verification: Ontario Black History Society; Chatham-Kent Black Historical Society; Cheryl Thompson's project team (coordinate); *Ontario History*.
- Effort: 6–10 weeks.
- Saturation: some competition — Thompson's "Mapping Ontario's Black Archive" and UWindsor exhibits (KQ4) are active; the entity-linked dataset angle was not found.
- Risk: overlap with funded academic work; requires care with naming and descendants.

**P8. Hemingway's Toronto Star: quantitative re-test of the 25 "Burrill" pieces and a sweep for more**
- Discovery: a stylometric verdict on Burrill's five "probable" pieces and any unsigned 1920–24 Star pieces whose style matches Hemingway's signed work.
- Data: *Dateline: Toronto* (172 signed pieces) as training set; Toronto Star 1920–24 via TPL/U of T.
- Method: Delta/SVM on function words with short-text controls; candidate generation by date windows when Hemingway was on staff.
- Verification: Hemingway Society / *The Hemingway Review*; Toronto Star (owner of the archive) is the natural outlet.
- Effort: 6–10 weeks.
- Saturation: some competition — Star librarians swept the morgue in 1992; no computational study found (KQ2, KQ3).
- Risk: ProQuest ToS for bulk text; short news items defeat stylometry; Burrill may have been exhaustive.

**P9. Wikipedia Toronto/Ontario history audit against DCB and primary newspapers**
- Discovery: a documented set of factual errors/inconsistencies in ~1,000 local-history articles, with primary-source fixes.
- Data: Wikipedia dumps; Dictionary of Canadian Biography (free online); Canadiana/OurOntario page images.
- Method: CLAIRE-style claim extraction and cross-article/DCB contradiction detection with Claude; human verification; on-wiki corrections.
- Verification: WikiProject Toronto; TPL local-history librarians; *The Varsity*.
- Effort: 4–6 weeks.
- Saturation: method crowded (EMNLP 2025), local application open (KQ6).
- Risk: triviality; reverts; "AI vs Wikipedia" framing.

**P10. Bode-style "Canadian newspaper fiction" database (1850–1930)**
- Discovery: a catalogue of serialized fiction/poetry in Canadian newspapers — reprints of foreign authors, unrecorded Canadian authors, pseudonyms — the Canadian equivalent of Trove's ~21,000-work database.
- Data: Canadiana Serials newspapers; OurOntario; Vincent's 19th-century periodical index as seed.
- Method: page-level OCR scraping; fiction/poetry classifier; title/author dedup; cross-match to known bibliographies (Montgomery, Leacock, Duncan, Johnson).
- Verification: Canadian Writing Research Collaboratory (CWRC); *Canadian Literature*; L.M. Montgomery Institute for any Montgomery hits.
- Effort: 3–5 months (largest project).
- Saturation: open niche for Canada (KQ3); Australian method is established.
- Risk: Canadiana's lack of API means heavy scraping; OCR noise; Montgomery-specific finds compete with an active collector community.

**P11. Co-Lab challenge completion with HTR as a draft layer**
- Discovery: making a low-completion LAC Co-Lab handwritten challenge (e.g., political correspondence) fully searchable and extracting newsworthy letters.
- Data: Co-Lab images (KQ5).
- Method: HTR draft → human correction → contribution through Co-Lab; LLM summarization to find notable letters.
- Verification: LAC's Co-Lab review process; LAC blog.
- Effort: 4–8 weeks.
- Saturation: some competition — CRKN/LAC HTR roadmap covers 2M images, but on RG10, not Co-Lab challenges.
- Risk: Co-Lab terms may not permit uploading machine-generated transcriptions; duplication of LAC's own plans.

**P12. Acta Victoriana juvenilia check (Atwood, Frye, Macpherson, Pratt)**
- Discovery: student pieces absent from published bibliographies.
- Data: 1878–1990 index on Internet Archive; online volumes (KQ3).
- Method: parse index; diff against author bibliographies; confirm in scans.
- Verification: Victoria University (E.J. Pratt) Library archivists; *The Strand*/*The Varsity* would cover.
- Effort: 2–4 weeks.
- Saturation: likely crowded for Atwood (professional bibliographers); unknown for Macpherson/Pratt.
- Risk: copyright on living author; index already comprehensive; low news value.

**Explicitly excluded (dead ends for a months-scale amateur):** Kryptos K4 (answer sold; $1-a-guess verifier), Zodiac Z13/Z32, Dorabella, McCormick, Tamam Shud code line, Beale 1 & 3, Voynich, Indus, Linear A, rongorongo, Cascajal (KQ1); AI painting attribution (KQ7); unidentified-remains identification (KQ8).

### Gaps
- Saturation ratings for P2, P3, P5 and P10 rest on absence of results in the queries that could be run; the specific confirmatory searches (Boat-Song + stylometry; Rural Diary Archive + Transkribus; Cipherbrain postcards; OurDigitalWorld API) were blocked by the search budget and proxy.
- Legal/text-mining terms for ProQuest (Toronto Star), Canadiana and OurDigitalWorld were not verified and must be checked before any automated collection.
