# 📚 Corpus Linguistics: Method, Analysis, Interpretation (Week 3)

*Course delivered by Lancaster University*

Welcome to the Week 3 repository module for **Corpus Linguistics**. This week transitions from foundational tools to applied, socially-motivated research, demonstrating how corpus linguistics integrates with **Critical Discourse Analysis (CDA)** and the wider social sciences. Through an in-depth ESRC-funded case study on how the UK press represents **Refugees, Asylum Seekers, and Immigrants (RASIM)**, alongside `#LancsBox` tutorials on frequency, dispersion, and keywords, and interviews with researchers across Social Science, Accounting & Finance, and International Relations, we explore how quantitative patterns and qualitative close reading work hand in hand.

---

## 📑 Table of Contents

1. [Corpus-Based Discourse Analysis: Methodological Foundations](#-1-corpus-based-discourse-analysis-methodological-foundations)
2. [Case Study: Refugees, Asylum Seekers, and Immigrants (RASIM) in the UK Press](#-2-case-study-refugees-asylum-seekers-and-immigrants-rasim-in-the-uk-press)
   * [2.1 Corpus Building & Query Design](#21-corpus-building--query-design)
   * [2.2 Keywords & Discourse *Topoi* (Themes)](#22-keywords--discourse-topoi-themes)
   * [2.3 Collocates & Metaphors of Quantity and Plight](#23-collocates--metaphors-of-quantity-and-plight)
   * [2.4 Key Clusters: `illegal` and Forced Discourse Equivalence](#24-key-clusters-illegal-and-forced-discourse-equivalence)
   * [2.5 In Focus: The Cluster `POSE AS` and Newspaper Stance](#25-in-focus-the-cluster-pose-as-and-newspaper-stance)
   * [2.6 Direct vs. Indirect Framing: `suffocated` and `drowned`](#26-direct-vs-indirect-framing-suffocated-and-drowned)
   * [2.7 Case Study Conclusions](#27-case-study-conclusions)
3. [Practical Lab: Frequencies, Dispersion, and Keywords in `#LancsBox`](#-3-practical-lab-frequencies-dispersion-and-keywords-in-lancsbox)
4. [Expert Conversations: Corpus Applications Across Disciplines](#-4-expert-conversations-corpus-applications-across-disciplines)
   * [4.1 Prof. Paul Baker: Corpus-Assisted Critical Discourse Analysis](#41-in-conversation-with-prof-paul-baker-corpus-assisted-critical-discourse-analysis)
   * [4.2 Prof. Steve Young: Corpus Methods in Accounting & Finance](#42-in-conversation-with-prof-steve-young-corpus-methods-in-accounting--finance)
   * [4.3 Dr. Basil Germond: Corpus Approaches to International Relations & Maritime Security](#43-in-conversation-with-dr-basil-germond-corpus-approaches-to-international-relations--maritime-security)
5. [References & Resources](#-5-references--resources)

---

## 🔍 1. Corpus-Based Discourse Analysis: Methodological Foundations

*Based on Lecture 3.3 by Prof. Tony McEnery*

### Core Characteristics of the Corpus-Based Approach
* **Scale:** Analyzing tens or hundreds of millions of words across thousands of texts to see the "big picture."
* **Frequency Manipulation:** Moving beyond raw counts to normalized frequencies, collocations, and keyness.
* **Pattern Hunting:** Identifying systematic co-occurrences to explore how meaning is constructed in context.
* **Annotation & Grouping:** Categorizing words with shared meanings or grammatical roles into thematic groups.
* **Quantification & Statistical Significance:** Accurately measuring *how many* and *where*, and testing whether observed differences are statistically reliable.

### Bridging Quantitative and Qualitative Analysis (Triangulation)
Corpus linguistics does not reject qualitative analysis. Instead, it enables **triangulation**:
1. **Gisting ("Aboutness"):** Quantitative tools (keywords, key clusters) rapidly summarize massive text collections.
2. **Concordancing (Close Reading):** Researchers drill down into individual concordance lines to inspect how specific patterns operate in context.
3. **Core Techniques Used This Week:**
   * **Keywords** & **Key Clusters** (2- or 3-word sequences occurring with statistically unusual frequency in one corpus vs. another).
   * **Collocation** as a lens for observing **Semantic Prosody** and **Discourse Prosody**.

---

## 📰 2. Case Study: Refugees, Asylum Seekers, and Immigrants (RASIM) in the UK Press

*Based on Lectures 3.3, 3.4, 3.5, 3.6, & 3.7 by Prof. Tony McEnery (ESRC-Funded Project)*

Throughout this case study, the acronym **RASIM** is used to refer collectively to **R**efugees, **A**sylum **S**eekers, **I**mmigrants, and **M**igrants.

### 2.1 Corpus Building & Query Design

To build a representative corpus of UK newspaper coverage from **1996 to 2005** (a decade of intense public and political debate over immigration in the UK), articles were extracted from news databases (**LexisNexis** / **Factiva**).

#### Designing the Search Query
Rather than guessing search terms purely by intuition, the team used a two-step empirical process:
1. **Pilot Corpus Keyword Extraction:** Collected a small pilot corpus using basic terms (`refugee`, `asylum seeker`) and compared it against a general English reference corpus to identify "aboutness" keywords.
2. **Concordance Verification & Exclusion:** Inspected concordance lines to include relevant morphological variants and exclude "false friends" (e.g., Spanish football team *Deportivo* or the noun *deportment* when searching for `deport*`).

**Final Database Query:**
```text
refugee* OR asylum OR deport* OR immigr* OR emigr* OR migrant* 
OR "illegal alien" OR "illegal entry" OR "leave to remain" 
AND NOT deportivo AND NOT deportment
```

#### Corpus Architecture: Tabloids vs. Broadsheets
The collected data was divided into two sub-corpora representing the two major tiers of the UK national press:

| Newspaper Category | Description | Articles Collected | Total Word Count |
| :--- | :--- | :---: | :---: |
| **Tabloids** | Populist newspapers (e.g., *The Sun, Daily Mirror, Daily Star, Daily Mail, Daily Express*) | $> 50,000$ | $\approx 29\text{ million words}$ |
| **Broadsheets** | "Quality" journalism (e.g., *The Guardian, The Independent, The Times, The Daily Telegraph*) | $\approx 100,000$ | $> 87\text{ million words}$ |

> 💡 **Methodological Note on Corpus Size:** The fact that the broadsheet corpus contains nearly three times as many words ($87\text{M}$ vs. $29\text{M}$) does **not** mean broadsheets were more obsessed with RASIM. Broadsheet articles are simply much longer on average than tabloid articles. Therefore, all cross-corpus comparisons must use **normalized frequencies (per million words)** or statistical significance tests.

---

### 2.2 Keywords & Discourse *Topoi* (Themes)

In Critical Discourse Analysis (CDA), a **topos** (plural: **topoi**) refers to a broad overarching theme or argumentation warrant in discourse. 

To identify the defining keywords of Tabloids vs. Broadsheets, the researchers set an extremely stringent statistical significance threshold: a probability of error lower than $1\text{ in }100\text{ billion}$ ($p < 10^{-11}$). Keywords were then grouped into thematic *topoi*:

| Topos (Theme) | Sub-Themes / Examples | Dominant Press Sector |
| :--- | :--- | :--- |
| **1. Query & Related Terms** | Core terms (`refugee`, `asylum`, `immigrant`, etc.) unevenly distributed across press types. | Split (Tabloid & Broadsheet variants) |
| **2. Entry** | • *General:* `arrivals`, `arrive`, `arrived`, `arriving`, `passengers`<br>• *Mode of transport, Place/Route, Legality of entrance* | 🔴 **100% Tabloid Keywords** (Zero Broadsheet keywords) |
| **3. Number (Quantity)** | Quantification of arrivals. (Only `dozens` is key in Broadsheets). | 🔴 **Heavily Tabloid** |
| **4. Abuse, Cost, Finances, Profit & Threat** | Framing RASIM as financial burdens, system abusers, or security threats. | 🔴 **Heavily Tabloid** |
| **5. Residence, System Issues & Unwelcome** | Living arrangements, administrative failure, and rejection. (Only `authentic` and `legitimacy` under *Legality* are key in Broadsheets). | 🔴 **Heavily Tabloid** |
| **6. Plight** | • **Broadsheets (Geopolitical/Structural):** `airstrikes`, `ceasefire`, `conflict`, `conflicts`, `coup`, `displaced`, `dissident`, `dissidents`<br>• **Tabloids (Emotional/Sensational):** `desperate`, `desperately`, `devastated`, `devastating`, `horrific`, `horrified`, `horror` | 🔵 **Shared, with more keywords in Broadsheets** |

**Key Insight:** Tabloids dominate almost all negative and administrative *topoi* (Entry, Number, Cost, Abuse, Residence). **Plight** is the only theme shared evenly—and where Broadsheets actually contribute more distinct keywords—though Tabloids frame plight through sensationalist emotion while Broadsheets frame it through geopolitical conflict.

---

### 2.3 Collocates & Metaphors of Quantity and Plight

Many of the thematic keywords above also function as direct **collocates** of `refugees` (tested again at $p < 10^{-11}$).

#### 1. Quantity Metaphors Collocating with `refugees`
Both press sectors draw heavily on dehumanizing **water, weather, animal, and cargo metaphors** to describe the volume of refugees:
* **Tabloid-Only Collocates ($10$ word-forms / $6$ headwords):** `convoy`, `flock`, `flocking`, `herded`, `overcrowded`, `storm`, `stream`, `swamp`, `swamping`, `swarmed`.
* **Broadsheet-Only Collocates ($8$ word-forms / $5$ headwords):** `flocked`, `flooded`, `freight`, `load`, `million`, `numbering`, `streamed`, `swells`.
* **Shared by Both ($6$ word-forms / $4$ headwords):** Overlapping quantity terms used at similar rates.

#### 2. Plight Collocates with `refugees`
When examining collocates of `refugee(s)` within the *Plight* theme, the distribution is remarkably balanced:
* **Tabloid-specific:** $24$ word-forms
* **Broadsheet-specific:** $19$ word-forms
* **Shared by both:** $19$ word-forms

---

### 2.4 Key Clusters: `illegal` and Forced Discourse Equivalence

Moving from single words to multi-word units (**key clusters**), the researchers concordanced all instances of `illegal` and **right-sorted** the concordance lines to identify recurring patterns (including modifying adjectives of origin, ethnicity, race, age, religion, or work).

#### Six Cluster Themes Around `illegal`
1. **Illegal Entry**
2. **Illegal Residence**
3. **Illegal Means**
4. **Illegal Work**
5. **Miscellaneous Problems**
6. **Coordination Clusters with `and`**

Across these categories, every cluster is either statistically equal across both sectors or significantly more frequent in **Tabloids** (none are specific to Broadsheets). When normalized per million words, Tabloids use `illegal` clusters slightly more often for *entry*, *means*, and *work*, but **spectacularly more often for `illegal residence`**.

#### Forced Equivalence via `and` Coordination
Right-sorting revealed a striking syntactic pattern: coordinating `illegal immigration/immigrants` with criminal categories using the conjunction `and`:
* `illegal immigration and crime`
* `illegal immigrants and criminals`
* `illegal immigration and fraud`
* `illegal immigration and terrorism`

> ⚠️ **Discourse Analytical Insight:** Coordinating two distinct nouns with `and` forces a **discourse equivalence** (conjunction of discourses). Even though immigration has no inherent logical connection to fraud or terrorism, bracketing them together repeatedly primes readers to view them as part of the same threat.

---

### 2.5 In Focus: The Cluster `POSE AS` and Newspaper Stance

To see how corpus frequency combines with qualitative evaluation of **stance** (attitude), the researchers examined the cluster `POSE AS` (both in general and specifically in relation to RASIM):

| Metric (Normalized per Million Words) | Tabloids | Broadsheets | Ratio (Tabloid : Broadsheet) |
| :--- | :---: | :---: | :---: |
| **`POSE AS` (Overall in Corpus)** | $24.19\text{ pmw}$ | $8.66\text{ pmw}$ | $\approx 3 : 1$ |
| **`POSE AS` (In Relation to RASIM)** | $7.16\text{ pmw}$ | $0.89\text{ pmw}$ | $\approx 8 : 1$ |

Close concordance analysis of all RASIM-related `POSE AS` instances revealed **four distinct semantic patterns** and stark differences in editorial stance:

```
Pattern 1: [X] POSE AS [RASIM] to gain entry
  └── X = beggars, criminals, crooks, fanatics, foreigners, gangs, militants, spies, terrorists
  └── Presented as taken-for-granted fact supporting tougher measures:
        • Tabloids: 51.4% negative stance (0% challenging/alternative view)
        • Broadsheets: 58.9% negative stance, BUT 11.5% report a politician's view challenging tough measures / neutral-positive to RASIM.

Pattern 2: [X] POSE AS [RASIM] to expose problems with the asylum system
  └── X = police, investigative reporters
  └── Positive stance toward undercover stings / tougher border controls:
        • Tabloids: 22.9% of instances
        • Broadsheets: 16.7% of instances

Pattern 3: [RASIM] POSE AS [X] to exploit the system or citizens
  └── X = artists, athletes, doctors, EU citizens, nurses, scientists, sports fans, students, taxi drivers, tourists, workers
  └── Negative stance toward RASIM deception:
        • Tabloids: 23.4% of instances (e.g., Daily Star)
        • Broadsheets: 0% (No negative-stance instances found)

Pattern 4: [Criminals] POSE AS [X] to exploit or harm RASIM
  └── X = aid workers, peacekeepers
  └── Minor pattern in Tabloids (1.9% of instances); 0% negative stance in Broadsheets.
```

---

### 2.6 Direct vs. Indirect Framing: `suffocated` and `drowned`

Finally, the researchers examined tragedies where RASIM lost their lives in transit (e.g., the June 2000 Dover tragedy where 58 Chinese migrants suffocated in a lorry trailer) by analyzing concordances of `suffocated` and `drowned`. They coded whether victims were framed as *illegal* **directly** or **indirectly**:

1. **Direct Attribution:** Modifying the victims directly with `illegal` or dehumanizing phrases like `illegal cargo` (e.g., *"58 illegal immigrants from China suffocated"*, *"killing 58 Chinese immigrants... illegal cargo"*).
2. **Indirect Framing:** Situating the report of the deaths inside broader discussions of `suspected asylum seekers`, `sneaking across perilous straits`, `smuggling`, `trafficking`, `illegal entry`, or the laxity of the immigration system.

| Framing Type | Target Word | Tabloids (%) | Broadsheets (%) | Observed Tendency |
| :--- | :--- | :---: | :---: | :--- |
| **Direct Attribution** | `suffocated` | $28.3\%$ | $19.6\%$ | Proportionately higher in **Tabloids** |
| **Direct Attribution** | `drowned` | $36.2\%$ | $23.3\%$ | Proportionately higher in **Tabloids** |
| **Indirect Framing** | `suffocated` | $17.5\%$ | $26.2\%$ | Proportionately higher in **Broadsheets** |
| **Indirect Framing** | `drowned` | $17.2\%$ | $15.8\%$ | Broadly similar |

* **Statistical Caveat & Interpretation:** Overall negative representation (Direct + Indirect combined) is high in both sectors with **no statistically significant difference** between them. While Tabloids show a tendency toward *direct* attribution and Broadsheets toward *indirect* framing, this difference does not reach statistical significance. Both sectors project a humane face while simultaneously implying that because the victims participated in an illegal act, they bore partial responsibility for their fate.

---

### 2.7 Case Study Conclusions

1. **Collapsed Distinctions (RASIM):** Although dictionaries define *refugees*, *asylum seekers*, and *immigrants* differently, the UK press uses them with heavily overlapping phraseology and interchangeable negative discourse prosodies.
2. **Differences of Degree vs. Absolutes:** Most differences between Tabloids and Broadsheets are matters of degree, though some are absolute (e.g., only Broadsheets give column inches to counter-arguments in `POSE AS`; only Tabloids use `[RASIM] POSE AS [Workers/Students]` negatively).
3. **Granularity Matters:** Grouping newspapers into "Tabloids" vs. "Broadsheets" is a useful macro-distinction, but individual newspapers within each group exhibit internal variation that warrants closer inspection.
4. **Macro-to-Micro Workflow:** Effective corpus-based discourse analysis continually oscillates between large-scale automated metrics and close qualitative reading of concordance lines.

---

## 💻 3. Practical Lab: Frequencies, Dispersion, and Keywords in `#LancsBox`

*Based on Tutorials 3.9 & 3.10 by Dr. Vaclav Brezina*

The **Words** tool in `#LancsBox` (demonstrated using the **BNC 2014 v2**) computes frequency lists, dispersion metrics, and keyword comparisons across corpora and sub-corpora.

### 3.1 Absolute vs. Relative (Normalized) Frequency

* **Absolute Frequency ($f$):** The raw count of occurrences of a word/item in a corpus.
* **Relative Frequency ($rf$):** Normalized frequency allowing fair comparison across corpora of different sizes. Computed as:

$$\text{Relative Frequency} = \left( \frac{\text{Absolute Frequency}}{\text{Total Tokens in Corpus}} \right) \times \text{Basis for Normalisation}$$

* **Worked Example (`of` in the BNC):**
  * Absolute frequency $= 3,049,564$; Corpus size $\approx 98,542,825\text{ words}$; Basis for normalisation $= 10,000\text{ words}$ (note: `#LancsBox X` defaults to $1,000,000\text{ words}$):

$$\text{rf}_{\text{per } 10\text{k}} = \left( \frac{3,049,564}{98,542,825} \right) \times 10,000 = 309.46\text{ per }10,000\text{ words}$$

* **Zipfian Distribution:** Plotting a corpus word list on a graph shows that a tiny handful of grammatical words (e.g., *the*, *of*, *and*) have massive frequencies, followed by a dramatic, steep drop-off into a long tail of rare words.

---

### 3.2 Quantifying Dispersion

A high frequency count can be misleading if all occurrences are clustered in a single text. **Dispersion** quantifies how evenly a word is distributed across different files or sections of a corpus.

`#LancsBox` automatically computes multiple dispersion and combined measures in the **Words** table:
* **Range & Range %:** The raw number and percentage of corpus texts in which the item occurs at least once.
* **ARF (Average Reduced Frequency):** A metric that combines raw frequency and dispersion, discounting occurrences that are tightly clustered together.
* **Standard Deviation & Coefficient of Variation ($CV$):** Measures of variability across corpus sections.
* **Juilland's $D$:** Classical dispersion coefficient.
* **DP (Deviation of Proportions):** Gries's measure comparing observed proportions in corpus parts against expected proportions based on text sizes.

---

### 3.3 Comparing Corpora: Positive Keywords, Negative Keywords, and Lockwords

When comparing a **Corpus of Interest ($C$)** against a **Reference Corpus ($R$)**, every word falls into one of three categories:

```
   [ Corpus C (Target) ]                 [ Corpus R (Reference) ]
            │                                       │
            ├── 📈 More frequent in C than R  ➔  POSITIVE KEYWORDS (Typical of C)
            ├── ⚖️ Comparable in C and R     ➔  LOCKWORDS         (Stable across both)
            └── 📉 Less frequent in C than R  ➔  NEGATIVE KEYWORDS (Underrepresented in C)
```

* **Example (Academic Writing vs. General English):** Positive keywords include cross-disciplinary **content words** (`figure`, `different`, `data`, `social`, `model`) and **grammatical/discourse markers** (`this`, `however`, `is`, `due`, `also`, `order`, `therefore`).

---

### 3.4 Step-by-Step Workflows in `#LancsBox` Words Tool

#### Workflow A: Comparing Sub-Corpora & Filtering by Dispersion
1. Open the **Words** tool with *BNC 2014 v2* ($858,450$ total items).
2. Select a pre-defined sub-corpus from the dropdown:
   * **Academic Prose:** Top word is `the`.
   * **Informal Speech:** Top word is the first-person pronoun `I` ($59,247$ total items).
3. **Hover for KWIC:** Hovering your mouse over any item displays an instant **KeyWord In Context (KWIC)** preview.
4. **Filter by Range %:** To find core conversational vocabulary in *Informal Speech*, set the `Range %` column filter from `10` to `100`. Out of $59,247$ items, just over $2,000$ items occur in at least $10\%$ of informal speech texts.

#### Workflow B: Selecting Units & Extracting Core Academic Verbs
1. Use the **Unit Selector** to group items by:
   * `Word (lowercase)` *(default)*
   * `Word (case-sensitive)` *(useful for proper nouns/sentence-initial words)*
   * `Word class` / `POS (Part of Speech)` / `Headword` / `Semantic tag`
   * `Lemma` *(headword + POS category, grouping inflections)*
   * `Lexeme` *(lemma + POS category + semantic domain tag)*
2. **Practical Task — Finding Core Academic Verbs to Teach/Learn:**
   * Select the **Academic** sub-corpus and switch the Unit Selector to **Lemma** ($335,019$ lemmas).
   * Filter the `Term` column by typing `_V` (Select all & Apply) $\rightarrow$ isolates $17,785$ academic verb lemmas.
   * Filter the `Range %` column to `10–100` (appearing in at least $10\%$ of academic texts) $\rightarrow$ narrows the list to a manageable **$550$ core academic verbs** (e.g., *calculate, write, establish, play, reveal, seek, carry, address, refer, highlight, begin, continue, estimate*).

#### Workflow C: Defining a Custom Sub-Corpus & Running a Keyword Analysis
1. Click **New Subcorpus** $\rightarrow$ select `Genre: E-language` and `Subgenre: Email` $\rightarrow$ Click **OK**.
2. `#LancsBox` computes and caches the word list for the new **Email sub-corpus** ($56,000\text{ words}$).
3. Switch Unit Selector to `Word (lowercase)` and click the **Keywords** icon.
4. Select `E-language` (the whole electronic language sub-corpus) as the **Reference Corpus** to see what makes emails unique compared to other digital texts.
5. **Available Keyword Statistics in `#LancsBox`:**
   * **Simple Maths Parameter** *(default sort)*
   * **Log-likelihood**
   * **Percentage Difference (%DIFF)**
   * **Log Ratio**
6. **Resulting Email Keywords:** Salutations, sign-offs, scheduling terms, and metadata (`hi`, `wishes`, `email`, `regards`, personal names, `carers`, `corpus`, `dear`, `shall`, `Wednesday`, dates, and places). Copy results directly with `Ctrl+C` / `Cmd+C`.

---

## 🎙️ 4. Expert Conversations: Corpus Applications Across Disciplines

### 4.1 In Conversation with Prof. Paul Baker: Corpus-Assisted Critical Discourse Analysis

*Based on Video 3.15 — Prof. Tony McEnery interviews Prof. Paul Baker (Lancaster University)*

* **Path into Corpus Linguistics:**
  * Started his PhD studying **Polari** (a historical cryptolect/slang used by gay men in the UK) without corpus tools. When expanding his research to examine how gay men were represented across vast archives of newspapers, legal debates (Hansard), magazines, and personal ads, he turned to corpus linguistics to achieve comprehensive coverage.
* **Formulating Research Questions:**
  * Researchers can start with broad, open-ended questions (*"How is group X represented?"*), specific comparative/diachronic questions (*"How do newspapers differ in representing Muslims over time?"*), or allow **emergent questions** to surface from the data (e.g., discovering that `men` and `women` were top collocates of `Muslim`, which sparked a new investigation into gender and Islam in the press).
* **Data Sources & Ethics:**
  * Primarily uses digital databases like **Nexis UK** (newspapers) and **Hansard** (UK Parliamentary debates from the House of Commons and House of Lords on topics like fox hunting and gay equality), avoiding the OCR errors of manual scanning and the privacy/ethical hurdles of private letters or diaries.
* **Comparing Corpus Software Packages:**

| Software / Platform | Strengths | Limitations |
| :--- | :--- | :--- |
| **WordSmith Tools** | Powerful, comprehensive functionality; handles large local corpora well. | Paid license; multi-window interface can feel complex or clunky for beginners. |
| **AntConc** | Free, lightweight, and intuitive; ideal for smaller corpora (e.g., $\approx 200,000\text{ words}$). | Slower on massive datasets; slightly fewer advanced features than WordSmith. |
| **Online Interfaces (e.g., COHA)** | Instant web access to massive historical datasets (Mark Davies's corpora). | Cannot view full texts; restricted to built-in web query tools. |
| **Sketch Engine** | Online platform; **Word Sketch** automatically groups collocates by grammatical relations (e.g., verbs where the node is **Agent/Subject** vs. **Patient/Object**—showing *"who does what to whom"*). | Paid subscription; uploading custom corpora can occasionally be tricky. |

* **Strengths of Corpus-Assisted CDA:**
  * Overcomes the primary criticism of traditional qualitative CDA—**cherry-picking** a handful of texts to prove a pre-existing ideological point.
  * Captures the **cumulative ("drip, drip, drip") effect of discourse**, where subtle collocations repeatedly position a social group positively or negatively over time.
* **Pitfalls, Limitations, and Researcher Bias:**
  1. **De-contextualization & Negation:** Reading only a $\pm 5$ collocation window without expanding concordance lines to full paragraphs can mislead analysts (e.g., a writer quoting a negative stereotype only to *negate* or refute it later in the paragraph).
  2. **Loss of Multimodality:** Plain-text corpora strip away visual layout, typography, and photographs unless explicitly annotated.
  3. **The "Difference Mindset" of Keywords:** Keyword tools train researchers to look only for *differences*, potentially overstating divisions and ignoring profound *similarities* across texts (mitigated by comparing across 3 or 4 reference corpora and examining lockwords).
  4. **Accounting for Production & Reception:** Textual data alone cannot explain *why* a pattern exists. Analysts must look outside the corpus to press regulations, historical events (e.g., 9/11), demographic/attitude surveys, and audience reception (e.g., **Press Complaints Commission [PCC]** records).
  5. **Bias Reduction, Not Elimination:** Principles like *total accountability* reduce bias, but researchers still make subjective choices regarding research topics, statistical cutoffs, and which top keywords to discuss within journal word limits.
* **Public Engagement & Policy Impact:**
  * Collaborated with **ENGAGE** (an organization promoting British Muslim civic engagement) and presented findings to the **All-Party Parliamentary Group on Islamophobia** at the UK Parliament. Emphasizes that non-academic audiences need concise, visually engaging summaries (graphs, charts) rather than dense methodological jargon.

---

### 4.2 In Conversation with Prof. Steve Young: Corpus Methods in Accounting & Finance

*Based on Video 3.16 — Prof. Tony McEnery interviews Prof. Steve Young (Head of Department of Accounting & Finance, Lancaster University)*

* **Why Study Language in Accounting?**
  * While accounting research historically focused purely on financial numbers, numbers only occupy the final 20–30 pages of a corporate **Annual Report**. The front half consists of extensive **narrative reporting**, supplemented by CEO presentations, investor meetings, and earnings/acquisition press releases.
  * Narratives contextualize—and sometimes "spin"—financial numbers, while capturing strategic dimensions (like customer satisfaction or future business strategy) that raw earnings figures cannot quantify.
* **Overcoming the Scale Barrier:**
  * Previously, qualitative accounting researchers manually coded small samples (e.g., $200$ Chairman's Statements), which US-based quantitative journals often dismissed as subjective and ungeneralizable.
  * Partnering with computer scientist **Prof. Paul Rayson** (Lancaster) and **Prof. Martin Walker** (Manchester University) on an ESRC-funded project (and within Lancaster's **CASS** — *ESRC Centre for Corpus Approaches to Social Science*), Young's team scaled analysis up to **thousands of UK annual reports**.
* **Technical Challenge: Parsing Unstructured PDFs:**
  * Unlike standardized US filings, UK firms publish annual reports as **unstructured PDFs** with complete discretion over section headings and document layout.
  * **Solution:** The team built automated software that extracts and parses each PDF's **Table of Contents**, maps section headings to create an "X-ray" of the report's structure, and computes linguistic metrics within specific sections (e.g., comparing whether management emphasizes past performance vs. future outlook, whether narrative tone matches the back-end financial numbers, and how firms justify **executive remuneration** in governance disclosures).

---

### 4.3 In Conversation with Dr. Basil Germond: Corpus Approaches to International Relations & Maritime Security

*Based on Video 3.17 — Prof. Tony McEnery interviews Dr. Basil Germond (Department of Politics, Philosophy and Religion, Lancaster University)*

* **Research Focus:**
  * Specializes in International Relations, naval/maritime security in the post-Cold War era, and the geopolitical ambitions of the **European Union (EU)**—specifically how the EU constructs maritime security threats (such as **piracy**) and normalizes practices of **power projection** beyond its external borders.
* **Why Corpus Linguistics in International Relations?**
  * The EU is a massive multi-level actor (comprising the supranational **European Commission**, the intergovernmental **Council**, specialized agencies, and individual **Member States** like the UK, France, and Germany).
  * Analyzing how EU discourse interacts with or diverges from national Ministry of Defence discourses generates a volume of official policy documents far too large for traditional close reading.
* **When Corpus Data Challenges Academic Consensus:**
  * **Hypothesis:** In IR scholarship, the **"Comprehensive Approach to Security"** (tackling root causes alongside symptoms using both civilian/foreign aid and military instruments) is widely considered the EU's trademark foreign policy narrative. Germond expected this phrase/concept to dominate EU maritime security and counter-piracy texts.
  * **Corpus Finding:** Preliminary corpus analysis within CASS revealed that the "comprehensive approach" is **surprisingly absent** from the EU's actual maritime security and piracy discourse—forcing a productive reframing of existing IR hypotheses.
* **Real-World Impact Beyond Academia:**
  * **Naval Practitioners** actively collaborate with the project and share unclassified doctrinal documents because understanding how maritime threats and naval roles are discursively constructed helps navies align their strategic narratives and justify defense budgets to policymakers.

---

## 📖 5. References & Resources

* **Baker, P. (2006).** *Using Corpora in Discourse Analysis*. Continuum.
* **Baker, P., Gabrielatos, C., Khosravinik, M., Krzyżanowski, M., McEnery, T., & Wodak, R. (2008).** *A useful methodological synergy? Combining critical discourse analysis and corpus linguistics to examine discourses of refugees and asylum seekers in the UK press*. Discourse & Society, 19(3), 273–306.
* **Baker, P., Gabrielatos, C., & McEnery, T. (2013).** *Discourse Analysis and Media Attitudes: The Representation of Islam in the British Press*. Cambridge University Press.
* **Brezina, V. (2018).** *Statistics in Corpus Linguistics: A Practical Guide*. Cambridge University Press.
* **Gabrielatos, C. (2007).** *Selecting query terms to build a specialised corpus from a restricted-access database*. ICAME Journal, 31, 5–43.
* **Germond, B., & McEnery, T. (2016).** *Corpus-based approaches to maritime security and international relations*. ESRC Centre for Corpus Approaches to Social Science (CASS), Lancaster University.
* **online Resources Mentioned in Lectures:**
  * **#LancsBox:** [corpora.lancs.ac.uk/lancsbox](http://corpora.lancs.ac.uk/lancsbox/)
  * **UK Parliament Hansard:** [hansard.parliament.uk](https://hansard.parliament.uk/)
  * **ESRC Centre for Corpus Approaches to Social Science (CASS):** [cass.lancs.ac.uk](http://cass.lancs.ac.uk/)
