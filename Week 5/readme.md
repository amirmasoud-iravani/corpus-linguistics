# 📚 Corpus Linguistics: Method, Analysis, Interpretation (Week 5)

*Course delivered by Lancaster University*

Welcome to the Week 5 repository module for **Corpus Linguistics**. This week explores the methodological synergy between **Corpus Linguistics** and **Sociolinguistics** (as well as Historical Pragmatics, Forensic Linguistics, and Corpus Tool Development). Moving beyond prescriptive grammar rules and static dictionary definitions, we examine how spoken and written language varies systematically across social groups, regions, time periods, and linguistic contexts. We also cover hands-on tutorials for **`BNClab`** and **`CQPweb`**, followed by conversations with leading scholars in sociolinguistics, historical pragmatics, forensic linguistics, and corpus software engineering.

---

## 📑 Table of Contents

1. [Corpus Linguistics Meets Sociolinguistics](#-1-corpus-linguistics-meets-sociolinguistics)
   * [1.1 Two Approaches to Variation: Labovian vs. Ambient Variables](#11-two-approaches-to-variation-labovian-vs-ambient-variables)
   * [1.2 Case Study 1: Gender and Personal Pronouns (Ambient Variation)](#12-case-study-1-gender-and-personal-pronouns-ambient-variation)
   * [1.3 Case Study 2: Possessives (`'s` vs. `of`) in Spoken English (Labovian Variation)](#13-case-study-2-possessives-s-vs-of-in-spoken-english-labovian-variation)
   * [1.4 Methodological Synergy](#14-methodological-synergy)
2. [Practical Lab 1: Exploring Spoken Variation with `BNClab`](#-2-practical-lab-1-exploring-spoken-variation-with-bnclab)
3. [Practical Lab 2: Searching Corpora with `CQPweb`](#-3-practical-lab-2-searching-corpora-with-cqpweb)
   * [3.1 Introduction & Architecture of `CQPweb`](#31-introduction--architecture-of-cqpweb)
   * [3.2 Running Standard Queries](#32-running-standard-queries)
   * [3.3 Navigating the Concordance Screen](#33-navigating-the-concordance-screen)
   * [3.4 Running Restricted Queries (Metadata Filtering)](#34-running-restricted-queries-metadata-filtering)
4. [Expert Conversations: Sociolinguistics, Pragmatics, Forensics & Tool Design](#-4-expert-conversations-sociolinguistics-pragmatics-forensics--tool-design)
   * [4.1 Prof. Miriam Meyerhoff: Variationist Sociolinguistics, Fieldwork, and Resampling the BNC](#41-in-conversation-with-prof-miriam-meyerhoff-variationist-sociolinguistics-fieldwork-and-resampling-the-bnc)
   * [4.2 Prof. Jonathan Culpeper: Historical Pragmatics, Impoliteness, and Hate Speech](#42-in-conversation-with-prof-jonathan-culpeper-historical-pragmatics-impoliteness-and-hate-speech)
   * [4.3 Dr. Claire Hardaker: Forensic Corpus Pragmatics, Deception, and Online Abuse](#43-in-conversation-with-dr-claire-hardaker-forensic-corpus-pragmatics-deception-and-online-abuse)
   * [4.4 Dr. Mike Scott: The History of Concordancers, WordSmith Tools, and Keywords](#44-in-conversation-with-dr-mike-scott-the-history-of-concordancers-wordsmith-tools-and-keywords)
5. [References & Resources](#-5-references--resources)

---

## 🗣️ 1. Corpus Linguistics Meets Sociolinguistics

*Based on Lectures 5.3, 5.4, 5.5, & 5.6 by Dr. Vaclav Brezina*

Language variation across speakers, genders, age groups, regions, and socioeconomic classes is never random ("free variation"); rather, it is conditioned by systematic **internal (linguistic)** and **external (social)** constraints. By comparing the **Spoken BNC 1994** and the **Spoken BNC 2014** (sampled 20 years apart), researchers can investigate both contemporary British speech and real-time diachronic change over a 20-year window.

### 1.1 Two Approaches to Variation: Labovian vs. Ambient Variables

| Dimension | 1. Labovian (Traditional Variationist) Approach | 2. Biber's Functional / "Ambient" Variable Approach |
| :--- | :--- | :--- |
| **Core Concept** | **Sociolinguistic Variable:** *"Different ways of saying the same thing"* (Labov). | **Ambient Variable:** Lexico-grammatical or discourse choices from a broad inventory that are not in strict meaning-preserving competition. |
| **Mechanism** | Direct competition between two or more variants that occupy the exact same structural slot without changing truth-conditional meaning. | Functional variation across registers/speakers; variants can appear anywhere in discourse—or nowhere at all. |
| **Spoken Example** | **Negative Concord vs. Standard Any:**<br>• *"I don't think we should go out **any** more."*<br>• *"I don't think we should go out **no** more."*<br>*(Direct competition between `any` and `no`)* | **Discourse Hedges:**<br>• *"Well, you know, you see, I don't know, I suppose..."*<br>*(Mitigate utterance strength and signal informal dialogic speech, but do not compete with a specific "unhedged" counterpart)* |

---

### 1.2 Case Study 1: Gender and Personal Pronouns (Ambient Variation)

While both male and female speakers must use personal pronouns (*I, you, she, he, we, they*) to construct sentences in informal conversation, corpus evidence across hundreds of speakers in the **BNC 1994** and **BNC 2014** reveals systematic quantitative tendencies:

1. **Consistent Gender Effect:** Plotting mean frequencies with **$95\%$ Confidence Interval (CI) error bars** shows a statistically significant difference in both 1994 and 2014: **female speakers consistently use personal pronouns more frequently than male speakers**.
2. **Diachronic Shift (1994 vs. 2014):** There is an overall drop in personal pronoun frequency between 1994 and 2014 across both genders. Intriguingly, because of this overall decline, **Female speakers in 2014 use personal pronouns at roughly the same frequency rate as Male speakers did in 1994**.

---

### 1.3 Case Study 2: Possessives (`'s` vs. `of`) in Spoken English (Labovian Variation)

*Based on research by Vaclav Brezina, Miriam Meyerhoff, Susan Reichelt, and Dana Gablasova*

#### The Sociolinguistic Variable
Consider two ways of expressing the exact same possessive relationship between a **Possessor** (*farmer*) and a **Possessum** (the object possessed: *field*):
* **Option 1 (`'s` Genitive):** `[Possessor] + 's + [Possessum]` $\rightarrow$ *"the farmer's field"*
* **Option 2 (`of` Genitive):** `[Possessum] + of + [Possessor]` $\rightarrow$ *"the field of the farmer"*

#### Dataset & Coding
Searching the Spoken BNC 1994 and Spoken BNC 2014 yielded **$>5,000$ target tokens** ($2,792$ `'s` constructions and $2,219$ `of` constructions), which were semi-automatically and manually coded for both **internal linguistic constraints** and **external social constraints**.

#### Why Multivariate Modelling is Essential (Avoiding the Naive Frequency Trap)
At first glance, plotting the raw proportion of `'s` genitives across age groups ($0\text{–}14$ up to $75\text{–}95$) suggests that the `'s` genitive was used less frequently in 2014 than in 1994. **However, this surface impression is an artifact of internal sampling differences:**
* Human/animate possessors strongly favor the `'s` genitive.
* In the 1994 dataset, **$59\%$** of tokens had a human possessor, whereas in the 2014 dataset, only **$41\%$** had a human possessor.

When all internal and external variables are entered into a **multivariate statistical model** simultaneously, the true constraints emerge:

1. **Animacy Constraint (Strongest Internal Factor):**
   * **Animate Human Possessor + Animate Human Possessum** (e.g., *"Peter's friend"*, kinship and ownership) overwhelmingly favors the **`'s` genitive**.
   * **Inanimate Possessor + Inanimate Possessum** (e.g., *"the roof of a house"*) strongly favors the **`of` genitive**.
2. **Phonological Constraint (Final Sibilants):**
   * Possessors ending in a sibilant consonant ($/\text{s}/, /\text{z}/, /\int/, /\text{d}\mathfrak{z}/$) disfavor the `'s` genitive due to ease of articulation (e.g., *"the death of Socrates"* is preferred over *"Socrates' death"* to avoid pronouncing consecutive sibilants).
3. **External Social Variables (Gender & Age):**
   * In the **1994** corpus, female speakers favored the `'s` genitive significantly more than male speakers, **but this gender effect disappears completely in the 2014 corpus**.
   * No other external social variables (age, class, region) significantly condition the choice.
4. **Real Diachronic Trend (Blurring of Territory):**
   * Over the 20-year period, the boundary between `'s` and `of` has become **more blurred**, with the `'s` genitive encroaching into inanimate territory previously dominated by the `of` construction.

---

### 1.4 Methodological Synergy

```
┌──────────────────────────────────────┐       ┌──────────────────────────────────────┐
│         CORPUS LINGUISTICS           │       │     VARIATIONIST SOCIOLINGUISTICS    │
│ • Large, representative corpora      │  +    │ • Deep attention to social context   │
│ • Automated extraction & processing  │ ────► │ • Multivariate statistical modelling │
│ • Broad lexico-grammatical coverage  │       │ • Internal + external constraints    │
└──────────────────────────────────────┘       └──────────────────────────────────────┘
```

---

## 🧪 2. Practical Lab 1: Exploring Spoken Variation with `BNClab`

*Based on Tutorial 5.9 by Dr. Vaclav Brezina*

**`BNClab`** (`corpora.lancs.ac.uk/bnclab`) is an online corpus analysis and visualization platform built at Lancaster University as part of the ESRC-funded project *The British National Corpus as a Sociolinguistic Dataset*. It enables instant comparison between the **Spoken BNC 1994** and the **Spoken BNC 2014**.

### Key Features & Analytical Views in `BNClab`

1. **Teaching & Learning Resources:** Clicking the **Resources** button provides downloadable PDF handouts and worksheets tailored for A-level English Language teachers/students and EFL/ESL classrooms.
2. **Live Search Bar:** Supports words (e.g., `ain't`), phrases, POS patterns, semantic categories, and combinations using parentheses:
   * *POS Pattern Example:* `_N _V` (all nouns followed by verbs $\rightarrow$ $>120,000$ hits like *Steven started, market is, children are*).
   * *Semantic Tag Example:* Searching for the semantic category of **colour** (`white, black, colour, red, green`) or combining it with a verb (`{colour} is` $\rightarrow$ *yellow is, vivid is, green is*).
3. **Seven Interactive Analysis Tabs (Example Query: `ain't`):**

| Tab / View | What It Shows & How It Works |
| :--- | :--- |
| **1. Concordance** | Displays dialogic speech with **color-coded speaker turns**, an adjustable context slider (to expand left/right context), and toggleable metadata checkboxes for **Gender, Age, Social Class, Region, Corpus Year (1994 vs. 2014),** and **Speaker Pseudonym**. |
| **2. Gender** | Interactive bar chart comparing **1994 (Blue)** vs. **2014 (Orange)** across Male and Female speakers. |
| **3. Age** | Scatter plot of individual speakers (hover to view speaker pseudonyms and frequencies) overlaid with **regression lines of best fit** comparing age trends in 1994 vs. 2014. |
| **4. Social Class** | Breakdown across Working Class, Middle Class, Students, Retired, and Unknown—revealing that **Social Class is a major factor in the use of `ain't`** (Working Class speakers use non-standard `ain't` substantially more than Middle Class speakers in both 1994 and 2014). |
| **5. Region** | Side-by-side choropleth maps of the UK for **1994** and **2014**, shading regions with higher relative frequencies in darker colors (e.g., highlighting Southern England in 1994 for `ain't`). |
| **6. Speakers** | Exportable table of $>500$ individual speakers listing both absolute and relative frequencies per speaker. |
| **7. Summary (ANOVA)** | Runs an automated **Multi-Way ANOVA** in the background to test the statistical significance of main effects and interactions (e.g., confirming statistically significant effects for *Change over time [1994 vs. 2014]*, *Social Class*, and the interaction of *Gender $\times$ Age $\times$ Class $\times$ Region*). |

---

## 🌐 3. Practical Lab 2: Searching Corpora with `CQPweb`

*Based on Tutorials 5.13, 5.14, 5.15, & 5.16 by Dr. Andrew Hardie (Lead Developer of `CQPweb`)*

### 3.1 Introduction & Architecture of `CQPweb`

* **What is `CQPweb`?** A browser-based graphical interface (`cqpweb.lancs.ac.uk`, demonstrated on v3.0.5 / v3.0.15) that sits on top of the **IMS Open Corpus Workbench (CWB)** and its **Corpus Query Processor (CQP)**.
* **Client–Server Model:** Users issue queries through any web browser; the remote server searches indexed corpora (e.g., *American English 2006 [AmE06]*, *British English 2006 [BE06]*) and returns paginated HTML results.
* **User Authentication & Licensing:** Login credentials control access because certain corpora (e.g., *Longman Spoken American Corpus*) are bound by restrictive publisher licenses. Each corpus uses a distinct visual color scheme to help users keep track of which corpus they are currently querying.

---

### 3.2 Running Standard Queries

Located at the top of the left-hand navigation menu, the **Standard Query** screen provides core search controls:

1. **Query Mode:**
   * **Simple Query (ignore case) *(Default)*:** Case-insensitive search supporting simplified wildcards/lemma syntax. Typing `however` or `HOWEVER` retrieves `however`, `However`, and `HOWEVER` ($617$ hits across $277$ texts in *BE06*).
   * **Simple Query (case-sensitive):** Matches exact capitalization only (e.g., searching `However` retrieves only sentence-initial/capitalized instances; `HOWEVER` retrieves only the single all-caps instance).
   * **CQP Syntax:** Unlocks the full regular-expression and attribute-value power of the underlying Corpus Query Processor for advanced users.
2. **Number of Hits Per Page:**
   * Defaults to **$50$ hits per page** (can be increased to $250+$, e.g., when searching `the`, which comprises $\approx 6\%$ of any English corpus—yielding $\approx 58,000$ hits in the $1\text{M}$-word *BE06* corpus).
   * Selecting **`Count hits`** bypasses the concordance view and immediately returns the summary frequency banner.
3. **Quick Restriction Dropdown:**
   * Restricts the search to one of the corpus's primary macro-divisions (e.g., in *BE06*: *Fiction, General Non-Fiction, Learned/Academic,* or *Press*).
   * Filtering `however` to **Learned/Academic** ($180,000+$ words) eliminates quoted fictional dialogue.
   * Selecting **`Last restrictions`** re-applies the previous filter (including complex custom filters) without re-entering checkboxes.
   * Clicking **`Reset query`** restores all dropdowns to factory defaults.
4. **Built-in Help Links:** Direct PDF links to **Corpus Documentation** (e.g., Paul Baker's documentation for *BE06*) and the **Simple Query Language** syntax guide.

---

### 3.3 Navigating the Concordance Screen

*(Demonstrated with the lemma query `{break}` in the American English 2006 [AmE06] corpus)*

* **Top Summary Header:**
  * Displays the exact query string executed, total hits ($232$), dispersion across texts ($162\text{ out of }500\text{ texts}$), total corpus word count ($1,175,000\text{ words}$), and **Normalized Frequency per million words (pmw)**:
    $$\text{Frequency (pmw)} = \left( \frac{\text{Hits}}{\text{Total Corpus Words}} \right) \times 1,000,000$$
  * Appends an audit trail of post-query actions (e.g., `, ordered randomly`) and reports execution time (e.g., `0.169 seconds [retrieved from cache]`).
* **Display Modes:**
  * **KWIC (KeyWord In Context) View *(Default)*:** Centers the node word in a middle column flanked by left and right context.
  * **Line View:** Toggles to continuous paragraph/sentence extracts without centering.
* **Interactive Links in Every Concordance Row:**
  * **Line Number:** Reference ID for qualitative coding.
  * **Text ID Link:**
    * *Hover:* Displays a tooltip with file word count, broad genre (e.g., *Press*), sampling method (*Multiple sample*), and text category.
    * *Click:* Opens the full **Text Metadata Page** (article titles, authors, publication dates).
  * **Node Word Link:**
    * *Hover:* Displays a tooltip showing the concordance line with **primary annotation (POS tags)** attached via underscores (`word_TAG`).
    * *Click:* Opens the **Extended Context Screen** to read the wider surrounding passage.
* **Crucial Sampling Control — `Show in random order` / `Randomise`:**
  * By default, concordances are listed in **corpus file order** (meaning the first 50 hits all come from Section A: *News Texts*).
  * Whenever you plan to manually analyze a subset of concordance lines (e.g., 100 or 200 hits), **always click `Show in random order` first** so your sample is representative of the entire corpus rather than biased toward the first genre section.
* **Pagination & Analysis Dropdown:** Navigate via `|<<` (First), `<` (Prev), `>` (Next), `>>|` (Last), or jump to a specific page number, and use the top-right dropdown to launch post-processes (*Collocations, Distribution, Frequency breakdown, Sort, Thin, Categorise*).

---

### 3.4 Running Restricted Queries (Metadata Filtering)

Clicking **Restricted Query** on the left-hand menu opens an advanced metadata matrix (demonstrated on the combined **Brown Family** corpus):

* **Independent Classification Schemes:** Texts in the Brown Family are cross-classified across five independent metadata dimensions:
  1. **Broad Genre ($4$ categories):** *Press, General Prose, Learned, Fiction*
  2. **Source Corpus ($6$ options):** *B-LOB, LOB, FLOB, BE06, Brown, AmE06*
  3. **Fine Text Category ($15$ options):** *A (Press: Reportage) through R (Humour)*
  4. **Time Period ($4$ categories):** *1931, 1961, 1991, 2006*
  5. **Regional Variety ($2$ categories):** *British English, American English*
* **Boolean Combination Logic:**
  * **Within a single column (OR logic):** Ticking multiple boxes in the same column includes texts matching *any* of those boxes (e.g., ticking *Press + General Prose + Learned* searches all **Non-Fiction**). Leaving a column completely unticked means *all* categories in that column are permitted.
  * **Across multiple columns (AND logic):** Ticking boxes in different columns restricts the search to the intersection of those criteria (e.g., ticking `Fiction` + `British English` reduces the search pool from $756$ total fiction texts to $504$ British fiction texts).
  * **Relative Frequency Recalculation:** The concordance header automatically recalculates the **per-million-word frequency** against the exact word count of the restricted sub-corpus, *not* the whole corpus.
  * **Empty Intersection Warning:** Selecting mutually exclusive criteria (e.g., `1931` + `American English` in a setup lacking *B-Brown*) returns a clear alert that zero texts match the restriction.

---

## 🎙️ 4. Expert Conversations: Sociolinguistics, Pragmatics, Forensics & Tool Design

### 4.1 In Conversation with Prof. Miriam Meyerhoff: Variationist Sociolinguistics, Fieldwork, and Resampling the BNC

*Based on Video 5.21 — Dr. Vaclav Brezina interviews Prof. Miriam Meyerhoff (Victoria University of Wellington, New Zealand)*

* **Two Roots of Variationist Sociolinguistics:**
  1. **Historical Linguistics:** Provides core theoretical questions—the **actuation problem** (*where and why does a linguistic change start?*) and the **diffusion/transition problem** (*how does change spread through a system and community?*).
  2. **Anthropological Linguistics:** Highlights human **agency**, social structure, and the aesthetic, emotional, and playful dimensions of language use.
  * *Critique of the "Internal vs. External" Divide:* Meyerhoff argues that separating "internal" linguistic constraints from "external" social/cognitive constraints is an artificial ideological boundary; both are inextricably part of the language system.
* **Pioneers of Mixed Methods:**
  * Long before "mixed methods" became a buzzword in the social sciences, sociolinguists combined quantitative modeling with qualitative ethnography—exemplified by **William Labov's (1963) Martha's Vineyard study** and his later work on identifying the social profiles of linguistic innovators ("leaders of language change").
* **Fieldwork Experiences:**
  * **ICE-New Zealand:** Collected natural spoken data by hosting months of dinner parties for friends (with signed consent forms).
  * **Vanuatu (*Bislama* & Language Documentation):** Spent over 20 years conducting fieldwork in Vanuatu, comparing urban township vs. rural village variation in **Bislama** (an English-lexified creole and national language) and intersecting language documentation with variationist analysis. Emphasizes the "active listening" and human connection required to elicit personal narratives.
  * **L2 Sociolinguistic Competence:** Co-authored research on **Polish teenagers who migrated to the UK**, showing how L2 learners subconsciously analyze and adopt local native sociolinguistic variation patterns.
* **The Tradeoff Between Ethnographic Fieldwork and Large Corpora (Resampling the BNC):**
  * Fieldworkers recording 40–60 speakers over a year possess rich qualitative context about every speaker, whereas a $10\text{M}$-word corpus like the Spoken BNC offers massive statistical power (where even $300$ well-sampled tokens can yield robust models) at the cost of thinner contextual metadata.
  * **Collaborative Project:** Resampling the Spoken BNC to create a sociolinguistically balanced dataset that maximizes speaker metadata and contextual accessibility for variationist researchers.

---

### 4.2 In Conversation with Prof. Jonathan Culpeper: Historical Pragmatics, Impoliteness, and Hate Speech

*Based on Video 5.22 — Prof. Tony McEnery interviews Prof. Jonathan Culpeper (Lancaster University)*

* **Reconstructing Spoken Conversation from 400 Years Ago (1600–1750):**
  * With no audio recordings or living native speakers from Early Modern English, how do we study historical spoken interaction? Culpeper (with Merja Kytö) compiled a corpus of **"speech-related" / "speech-like" written genres**:
    1. **Trial Proceedings & Witness Depositions:** Unlike modern formulaic courtrooms, 17th-century courts were rowdy and conversational, transcribed from notes by clerks.
    2. **Play Scripts / Drama:** Fictional, but deliberately crafted to simulate natural spoken dialogue.
    3. **Didactic Handbooks in Dialogue Form:** A popular Early Modern genre teaching practical skills or debating politics via fictional dialogues (e.g., between a farmer and a land surveyor, or a Papist and a Puritan).
  * By triangulating across these distinct genres, features that appear in all three—but are absent from standard expository prose—can be reliably identified as genuine features of Early Modern speech.
* **Case Study 1: Historical "Pragmatic Noise":**
  * Investigated interjections and emotional backchannels (`oh`, `ah`, `ha`, `fie`, `hem`, `um`). Virtually absent from non-speech-related writing ($<10$ hits across thousands of texts), but systematic in speech-like texts:
    * **Hesitation Markers (`um`, never `er`/`erm`):** Early Modern English never spelled hesitation markers with `r` (`er`/`erm`) because **all English accents at the time were rhotic** (speakers would have pronounced a consonant $/r/$ sound!). Instead, texts used `um` or `hem`.
    * **Anger (`fie`):** *"Fie on you!"* was a high-frequency marker of anger/indignation for two centuries before disappearing without a direct modern equivalent.
    * **Disgust & Pain:** Modern `yuck / ick / eww` vs. Early Modern `hem`. Echoing **Charles Darwin's** work on the expression of emotions, vocalizations blend natural articulatory tendencies (e.g., back rounded vowels for pain/surprise: `oh, ah`) with culturally specific conventions.
* **Case Study 2: Impoliteness & Metalanguage in the 2-Billion-Word Oxford English Corpus:**
  * During a 3-year ESRC Fellowship resulting in *Impoliteness: Using Language to Cause Offence* (2011), Culpeper combined 15 years of qualitative video/audio recordings with the **$2\text{-billion-word}$ Oxford English Corpus (OEC)**:
    * **Slot Modification (`you [X] [Y] bastard`):** Corpus queries revealed that insulting vocatives regularly allow up to **two** intervening adjective modifiers (*"you [adj] [adj] bastard"*), rarely more.
    * **Contextual Disambiguation (`shut up`):** Concordance sampling showed that bare `"shut up"` is rarely genuinely impolite in everyday speech—it overwhelmingly functions as friendly banter/disbelief unless exacerbated by intensifiers or prosody.
    * **Metalanguage ("Talk about Talk"):** In $2\text{ billion}$ words, the academic term `impoliteness` occurs only **$30$ times**, whereas lay metalinguistic evaluators like `rude` occur **$\approx 10,000$ times**. Concordancing `rude` reveals the exact conversational triggers that ordinary speakers evaluate as offensive.
* **Real-World Impact: Policing Hate Speech:**
  * Collaborating with criminologist **Prof. Paul Iganski** and UK police forces to study **hate speech** and verbal aggression as forms of **social harm**. By analyzing corpus narratives of how victims describe the emotional impact of hate speech, they discovered that standard **police victim impact questionnaires** were asking about the wrong emotional categories—providing an empirical basis to redesign police assessment forms.

---

### 4.3 Dr. Claire Hardaker: Forensic Corpus Pragmatics, Deception, and Online Abuse

*Based on Video 5.23 — Prof. Tony McEnery interviews Dr. Claire Hardaker (Lancaster University)*

* **What is a "Forensic Corpus Pragmatician"?**
  * **Forensic Linguistics:** Analyzing legal/criminal texts (e.g., forged suicide notes, SMS authorship attribution on seized mobile phones) or legal discourse processes (e.g., police interview coercion).
  * **Pragmatics:** Studying "meaning between the lines" (implicature, intent)—specifically **aggression, deception, manipulation, and threats**.
  * **Role of Corpus Linguistics in Court:** Qualitative impressions of a single text are vulnerable to challenge. Corpus methods provide **scalability, baseline frequency testing, and empirical rigor**. Linguistic evidence is never a standalone "magic bullet"; it contributes to the **weight of evidence** and is most frequently used by the **defense** to establish *reasonable doubt*.
* **Landmark Forensic Cases:**
  1. **The Unabomber (US):** Authorship identification linking Ted Kaczynski's known writings to the anonymous Unabomber manifesto via distinctive, shared multi-word phrases and idioms.
  2. **The "Twitter Joke Trial" — *Chambers v Director of Public Prosecutions* (UK):** When snow closed Robin Hood Airport, Paul Chambers tweeted in frustration: *"Crap! Robin Hood airport is closed. You've got a week and a bit to get your shit together otherwise I'm blowing the airport sky high!!"* Arrested under counter-terrorism/malicious communications laws and initially convicted, his conviction was ultimately overturned at the High Court/Supreme Court after examining the pragmatic context of his tweet corpus to establish that it was hyperbole/jest rather than a credible threat.
* **ESRC Project on Online Misogyny & Threat Networks:**
  * Awarded a $£200,000$ ESRC grant following the July 2013 Twitter abuse campaign against feminist campaigner **Caroline Criado-Perez** (who successfully campaigned to keep a woman, Jane Austen, on Bank of England banknotes and subsequently received barrages of rape, death, and bomb threats).
  * **Research Goals & Policy Impact:** Building a massive corpus of abusive tweets to map offender networks, evaluate whether existing UK communications legislation is fit for purpose, advise **MPs, the House of Lords, and Ofcom**, and empower everyday internet users, parents, schools, and teachers.
* **Two Fundamental Hurdles in Online Forensics:**
  1. **Multi-Jurisdictional Complexity:** If an offender in the UK tweets a threat to a victim in Australia via Twitter servers located in the US, three separate legal jurisdictions are simultaneously involved.
  2. **The Attribution / "Keyboard Proof" Problem:** Proving that a threat originated from a specific IP address or shared office computer does not automatically prove *which human fingers* were on the keyboard at that moment—requiring forensic stylistic and pragmatic analysis.

---

### 4.4 Dr. Mike Scott: The History of Concordancers, WordSmith Tools, and Keywords

*Based on Video 5.24 — Prof. Tony McEnery interviews Dr. Mike Scott (Aston University, Creator of WordSmith Tools)*

* **1970s–1980s: From Programmable Calculators & Punch Cards to the `NewBrain`:**
  * While teaching in northern Mexico in the 1970s, Scott taught himself basic programming loops on a **Texas Instruments programmable calculator** and took a university humanities course in **SPSS** using **80-column Hollerith punch cards** (where a single typo on column 14 meant throwing the card away and waiting days for mainframe batch output).
  * In 1982, on the advice of **Tim Johns** (pioneer of Data-Driven Learning at Birmingham), Scott bought a **NewBrain** microcomputer and took it to Brazil, teaching himself assembly/BASIC `PEEK` and `POKE` memory operations from a 150-page manual to program a custom word processor with automatic word-wrap.
* **1993: Collaboration with Tim Johns on `MicroConcord`:**
  * When Tim Johns visited Brazil and asked Scott to provide local user support for his early concordancing program, Scott wrote his own experimental concordancer to fix several limitations. Johns generously proposed merging the best features of both programs, resulting in **MicroConcord** (published by Oxford University Press in **1993**), which overcame the tiny $20\text{k–}30\text{k}$ word limits of earlier tools like the *Longman Mini Concordancer*.
* **1996: The Birth of `WordSmith Tools` and the Accidental Discovery of `Keywords`:**
  * **The `WordList` Module:** Created for Scott's Malaysian MA student, **Fadilah**, who needed a way to generate and compare vocabulary lists across textbook units (Unit 1 vs. Unit 2 vs. Unit 5) to see whether EFL textbooks systematically recycled vocabulary.
  * **The Saturday-Morning Discovery of `KeyWords`:** Scheduled to give a staff seminar on a Tuesday with nothing prepared on Saturday morning, Scott experimented with comparing a short word list from a newspaper article about **horse racing** against a reference collection of *The Guardian* (supplied by his brother, who worked at *The Guardian*) using the **Chi-square ($\chi^2$) test**.
  * Words that were statistically characteristic of the text leapt out—alongside unexpected proper-noun noise like *Sunshine* and *Star* (the names of racehorses!), immediately revealing the need for **minimum frequency thresholds**.
  * Launched by OUP in **1996**, **WordSmith Tools v1.0** combined three core modules—**Concord, WordList, and KeyWords**—democratizing corpus linguistics so MA/PhD students and discourse analysts (like Norman Fairclough) could analyze millions of words on personal computers without needing a mainframe lab or computer science degree.
* **Evolution Through User Feedback & Theoretical Shifts:**
  * **Shift to Multi-Word Units:** Moved from viewing single words in isolation (1990s) to recognizing the centrality of **collocation, n-grams, skipgrams, concgrams, and collocational frameworks** (Sinclair & Renouf), noting Sinclair's observation that beyond $\pm 4$ words, statistical noise rapidly obscures collocational patterning.
  * **"Provide and Don't Preclude" (Language Neutrality):** Designed WordSmith to be completely language-independent (supporting Polish, Lithuanian, Farsi, Medieval Greek poetry, etc.) and added user-requested switches such as **case-sensitivity in word lists** and **Concordance Dispersion Plots** (inspired by discussions with Tony McEnery on Alphonse Juilland's dispersion work) as well as text-range counts.
* **The Future of Corpus Tools & Empirical Humility:**
  * Predicts a shift beyond plain text toward **multimodal concordancing** (aligning text with audio, video, images, captions, and equations, as in TED Talk corpora).
  * **Empirical Falsification & Humility:** Reflects on how corpus evidence routinely falsifies dogmatic claims about what is "impossible" or "incorrect" in English, encouraging researchers to approach language with empirical humility.

---

## 📖 5. References & Resources

* **Biber, D. (1988).** *Variation across Speech and Writing*. Cambridge University Press.
* **Brezina, V. (2018).** *Statistics in Corpus Linguistics: A Practical Guide*. Cambridge University Press.
* **Culpeper, J. (2011).** *Impoliteness: Using Language to Cause Offence*. Cambridge University Press.
* **Culpeper, J., & Kytö, M. (2010).** *Early Modern English Dialogues: Spoken Interaction as Writing*. Cambridge University Press.
* **Hardaker, C. (2010).** *Trolling in asynchronous computer-mediated communication: From user discussions to academic definitions*. Journal of Politeness Research, 6(2), 215–242.
* **Hardie, A. (2012).** *CQPweb — combining power, flexibility and usability in a corpus analysis tool*. International Journal of Corpus Linguistics, 17(3), 380–409.
* **Labov, W. (1972).** *Sociolinguistic Patterns*. University of Pennsylvania Press.
* **Meyerhoff, M. (2018).** *Introducing Sociolinguistics* (3rd ed.). Routledge.
* **Scott, M. (1997).** *PC analysis of key words — and key key words*. System, 25(2), 233–245.
* **Scott, M., & Johns, T. (1993).** *MicroConcord*. Oxford University Press.
* **Online Platforms & Tools Mentioned in Week 5:**
  * **BNClab:** [corpora.lancs.ac.uk/bnclab](http://corpora.lancs.ac.uk/bnclab)
  * **Lancaster CQPweb Server:** [cqpweb.lancs.ac.uk](https://cqpweb.lancs.ac.uk/)
  * **WordSmith Tools:** [lexically.net/wordsmith](https://www.lexically.net/wordsmith/)
