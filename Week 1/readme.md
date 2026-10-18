# Foundations of Corpus Linguistics

---

## 📖 Overview

Welcome to the section 1 of course repository for **Corpus Linguistics**. This section is taken from the Corpus Linguistics course at "Lancaster University — ESRC Centre for Corpus Approaches to Social Science (CASS)" delivered by Professor Vaclav Brezina. This course explores the intersections between language, big data, and technology—guiding learners from foundational principles to advanced applications in public discourse analysis, sociolinguistics, language learning, and language testing.

Long before the modern AI boom, corpus linguistics worked at the heart of large-scale language computation, using specialized software such as **#LancsBox X** to analyze and visualize millions or billions of words to answer empirical questions about language use and society.

---

## 🗂️ Table of Contents

1. [What is a Corpus? & A Brief History](#1-what-is-a-corpus--a-brief-history)
2. [Core Lenses: Concordance & Frequency](#2-core-lenses-concordance--frequency)
3. [Semantic Prosody & Concordance Annotation](#3-semantic-prosody--concordance-annotation)
4. [Corpus Linguistics in the Age of AI](#4-corpus-linguistics-in-the-age-of-ai)
5. [Software Guide: Getting Started with #LancsBox X](#5-software-guide-getting-started-with-lancsbox-x)
6. [Tutorial: Mastering the KWIC Tool](#6-tutorial-mastering-the-kwic-tool)
7. [Community Research Showcase & FAQ](#7-community-research-showcase--faq)

---

## 1. What is a Corpus? & A Brief History

### Formal Definition
According to McEnery, Xiao, and Tono, a **corpus** is a collection of **electronic**, **naturally occurring** texts (written or spoken) which are **selected** to be **representative** of a particular language or language variety:
* **Electronic:** Available in digital format so computers can process it with specialized software.
* **Naturally Occurring:** Real-world written or spoken language rather than experimental data.
* **Selected (Sampled):** Sampled systematically from the vast amount of language in use.
* **Representative:** Structured to reflect the general use of a target language or variety.

### Historical Timeline
* **Pre-Computational Concordances:** In medieval and early modern times, concordances were compiled by hand. Alexander Cruden’s *Concordance of the Holy Scriptures* indexed every word of the Bible and took one year of work at 18 hours a day.
* **1970 & The Birth of Modern Corpus Linguistics:** Six years after Lancaster University was founded (with Bailrigg House standing as its oldest campus building), computer technology became prevalent across universities and institutions. In *The Times* newspaper in 1970, the word *computer* (singular and plural) appeared **6,323 times**—more than twice as often as new UK Prime Minister Edward Heath (>3,000 mentions across ~300 articles) and over seven times more than the Apollo 13 space program (833 mentions across 264 articles).
* **The LOB Corpus (1970–1978):** In 1970 at Lancaster, Geoffrey Leech began collecting a 1-million-word dataset of written British English modeled on the **Brown Corpus** (compiled at Brown University in Providence, Rhode Island). After nearly a decade of negotiating copyright for ~500 texts with primitive computing resources, collaboration with Stig Johansson in Oslo and colleagues in Bergen produced the **Lancaster-Oslo/Bergen (LOB) Corpus** in 1978.
* **Major English Corpora Milestones:**
  * **British English:** London-Lund Corpus, COBUILD Corpora, British National Corpus (BNC 1994), and BNC 2014.
  * **American English:** American National Corpus (ANC) and Corpus of Contemporary American English (COCA).
  * **International & Historical:** International Corpus of English (ICE), Wellington Corpus of New Zealand English, and *The Times* Corpus (all issues since 1785; the 1970 subcorpus alone approaches 500 million words).

---

## 2. Core Lenses: Concordance & Frequency

> *"If asked what is one benefit that corpora can provide and that cannot be provided by other means, I would reply 'information about frequency.'"* — **Geoffrey Leech**

Concordance and frequency serve as two primary lenses for observing linguistic data: **concordance reveals a word's meaning (usage in context)**, and **frequency reveals a word's importance**.

### Concordances (KWIC)
A **concordance** is a collection of occurrences of a search term—called the **Node** or **Keyword in Context (KWIC)**—displayed with its surrounding **Left (L)** and **Right (R)** context.

### Frequency Metrics
Always report frequency using **both** absolute and relative values:

| Metric | Definition | Analytical Value |
| :--- | :--- | :--- |
| **Absolute (Raw) Frequency** | The total number of hits/occurrences of a word or phrase in a corpus. | Shows exact sample size of observed instances. |
| **Relative (Normalized) Frequency** | Frequency per a standard number of words (typically **per 1 million words**), shown in parentheses in `#LancsBox X`. | Estimates probability of occurrence and allows comparison across corpora or genres of different sizes. |
| **Dispersion / Distribution** | How an expression is spread across different texts, genres, and registers. | Indicates whether a term is broadly used or concentrated in a few texts. |

#### Relative Frequency Equation
```text
Relative Frequency = (Absolute Frequency / Total Running Words [Tokens]) × Normalization Basis (1,000,000)
```

### Zipf's Law
Detailed in *Statistics in Corpus Linguistics: A Practical Guide* (2018), **Zipf's Law** states that regardless of corpus size, the frequency of a word is inversely proportional to its rank in a frequency list:
* The **1st** most frequent word (`the` in English, ~6 million hits in a 100M-word corpus) has twice the frequency of the **2nd** (`of`, ~3 million hits), three times the frequency of the **3rd** (`and`), and so on.
* Grammatical words occupy the top ranks, followed by high-frequency content words (*people, time, year*), before trailing off into a long tail of mid- and low-frequency words.
* **Takeaway:** Words are rare; large corpora (millions or billions of words) are necessary to observe meaningful patterns.

---

## 3. Semantic Prosody & Concordance Annotation

### Semantic Prosody
**Semantic prosody** is the evaluative aura (negative, neutral, or positive) a word or phrase acquires through its typical co-occurrence patterns.
* **Example (`sit through` in the BNC):**
  * **Left Context:** *bravely*, *rather than*, *forced to*, *had to* (`have/had to sit through` makes up ~10% of all concordance lines).
  * **Right Context:** *10 hours of*, *it again*, *the painful lecture*, *those meetings about nothing*.
  * **Finding:** `sit through` has a distinctly **negative semantic prosody**, used when enduring long, boring, or unpleasant events.

### Annotating Concordances in #LancsBox X
1. Filter or generate a **random sample** of concordance lines (e.g., 10 lines for illustration).
2. Define a custom category (e.g., `Evaluation`) with levels such as **Negative** (Red), **Neutral** (Amber), and **Positive** (Green), removing unused default levels.
3. Open the annotation view, inspect expanded context, and click single or multiple concordance lines to assign categories. `#LancsBox X` automatically counts occurrences per category.

---

## 4. Corpus Linguistics in the Age of AI

Referencing the 2025 paper *"Corpus Linguistics and AI"* and Adam Kilgarriff’s 2007 paper *"Googleology is Bad Science"*, corpus linguistics cautions against delegating analytical agency to a single black-box tool ("ChatGPT-ology is bad science"). What happens if the human analyst is engineered out of the loop and one computer simply talks to another?

### Empirical Comparison: LLMs vs. Corpus Evidence

| Task | ChatGPT (LLM) Response | Corpus Evidence (`#LancsBox X` / BNC / Web) |
| :--- | :--- | :--- |
| **Relative Frequency Query:** *"How frequent is 'people' per million words, and is it more frequent than 'time'?"* | Produces a comprehensive-looking breakdown citing BNC 1994, BNC 2014, and COCA per-million figures. | **Inaccurate Estimates:** Direct checks against BNC 1994, BNC 2014, and COCA show the AI's numbers are far off actual corpus data. |
| **Collocation Test:** *"What does the phrase 'education and courage' mean?"* (From the *Frequency Dictionary of Multiword Expressions in British English* test) | Defines both words, invents combined meanings, and generates a motto-like quote. | **Non-Collocational Foil:** Appears **0 times** in BNC 2014 and only ~26 times on Google (mostly split by punctuation or errors) |

**Conclusion:** AI and Large Language Models (LLMs) **complement, not replace**, corpus analysis. Direct corpus tools remain indispensable for **transparency, replicability, and critical evaluation**.

---

## 5. Software Guide: Getting Started with #LancsBox X

### Installation & Corpora Management
1. Download `#LancsBox X` for free at **[lancsbox.lancs.ac.uk](https://lancsbox.lancs.ac.uk)** (auto-selects Windows, macOS, or Linux installers; manuals, videos, exercises, and helpdesk are on the same page).
2. Add corpora via three methods:
   * **Corpus Hub:** Download pre-built corpora such as **BNC 2014 v.2**.
   * **Own Data:** Select local files, name the corpus, pick the language, and enable grammatical (POS) and semantic annotation.
   * **Web Scraping:** Enter corpus name, language, seed URLs, maximum websites to scrape, and external link depth, then click **Create corpus**.

### Multi-Tool Workspace
* Combine windows for **KWIC**, **Text**, **GraphColl**, and **Words**.
* Hold `Ctrl` + click to highlight multiple tool tabs and search across all active tools simultaneously.

### Search Syntax Cheat Sheet (Case-Insensitive by Default)

```text
# 1. Simple Word & Phrase Searches
love                                              # Exact word form (case-insensitive)
new zealand                                       # Multi-word phrase
I love going                                      # Exact expression

# 2. Wildcard Searches
new*                                              # Matches 'new', 'newspaper', etc.

# 3. Smart Searches (Type in ALL CAPS)
PASSIVE                                           # Verb 'to be' + optional adverbials + past participle
TIME                                              # All words in the 'Time' semantic category
ADJECTIVE NOUN VERB                               # Grammatical POS sequence

# 4. Corpus Query Language (CQL) — Enclosed in Square Brackets []
[word="new"]                                      # Word attribute match
[word="new" & pos="J.*"]                          # 'new' tagged as an adjective (regex POS)
[sem="E2.*"]                                      # Words in semantic category E2 (Emotion)
[hw="sit" & pos="V.*"] [word="through"] within s  # All verb variants of lemma 'sit' (sit, sits, sat, sitting)
                                                  # followed by 'through' within a single sentence (s)
```

---

## 6. Tutorial: Mastering the KWIC Tool

Worked example searching `study` in **BNC 2014 v.2**:

1. **Basic Summary Metrics:**
   * **Absolute Frequency:** `32,530` hits.
   * **Relative Frequency:** `(317.97)` per million words.
   * **Text Distribution:** Occurs in `6,177` out of `88,171` texts.
   * Hover over any line for a copy-pasteable broader context, or use the **Text** tool for full-text inspection.
2. **Sorting & Context Filtering:**
   * Click **Left** (e.g., *a study, another study, case study*) or **Right** (e.g., *study and, study at, study by, study conducted*) to sort alphabetically.
   * Hover over the **Right** header -> click **Filter** -> set span `R1` to `R5` (1 to 5 words to the right) -> type `participants` -> click **Apply**. This returns **382 hits** (`3.73` per million words across `240` texts).
3. **Viewing Annotations (`Detail` Menu):**
   * Open **Detail** in the top menu and select `pos` and `sem` to view inline tags (e.g., `study` tagged as singular noun + `P1` Education).
4. **Metadata Columns & Filtering (`Genre` and `Date`):**
   * Add `genre` and `date` columns from corpus metadata.
   * **Filter by Genre:**
     * *Informal speech:* `487` hits (`44.15` per million words — much lower than the `317.97` corpus average).
     * *Academic prose:* `1,298.97` per million words — much higher than average.
   * **Filter by Date:** Use the date picker (e.g., `01/01/2017` to `2020`) to isolate recent usage (`2,398` hits).
5. **Summary Table (Top-Right Icon):**
   * Quantifies left/right n-grams and metadata automatically (use `Ctrl+C` / `Cmd+C` to copy tables into reports):
     * **Left Context Chunks:** `the`, `this` (1-word); `in this`, `in the`, `of the`, `the present`, `the current` (2-word); `in the present`, `in the current`, `used in this`, `aim of this`, `according to a`, `results of this` (3-word).
     * **Right Context Chunks:** `of`, `the`, `was`, `in` (1-word); `of the`, `was found`, `that in`, `published in`, `showed that` (2-word); `published in the`, `was approved by`, `has shown that`, `is the first`, `was to investigate`, `was to determine` (3-word).
     * **Genre Breakdown:** Automatically sorts genres by relative frequency, showing `study` is most frequent in *Academic prose*, followed by *Magazines* and *Newspapers*, and least frequent in *Informal speech* and *Written-to-be-spoken*.

---

## 7. Community Research Showcase & FAQ

### 🌍 Cohort Research Projects
* **Social Media, Discourse & Representation:** Anti-migrant sentiment and hate speech in Libyan dialect Arabic on Facebook (`Al_Zwawi`); public conflation of *autistic meltdown* and *temper tantrum* (`ElizabethODonovan`); misogynistic language in film/TV transcripts (`Tibahaider123`); streaming platform feedback (`Yi970912`); and language around home, farm, and wild animals in conservation (`an_nguyenh54`).
* **Healthcare & Clinical Linguistics:** Multilingual (English, Urdu script/Romanised, Quranic Arabic) forum corpus on antenatal anxiety in Pakistan (`Faiza_0808`); perceptions and pain descriptions among Kerala nurses in the US (`renee5646`, `heyakate`); and Jeffersonian transcription of aphasic speech (`ElizabethODonovan`).
* **Education (TESOL/EAP) & AI:** Modal verbs in Japanese EFL textbooks vs. native corpora (`mariko_53`); learner corpora, Data-Driven Learning (DDL), and Academic Word List (AWL) collocations (`heyakate`, `QD_2504_SF4R`); and syntax/semantics of ChatGPT student responses (`xtiancuaderno`).
* **Dialectology, Historical & Workplace:** Generational vocabulary change in Hainanese (`YawTsek`); spoken Najdi Arabic noun phrase morphosyntax (`mfaalshahrani1`); German and Latin lexical similarities (`Marcos-Escobedo`); W.E.B. Du Bois political theory concordances (`RobertWms`); and corporate values across company websites vs. HR policies (`eloiseleeson-smith`).

### 🛠️ Frequently Asked Questions
* **Is `#LancsBox 6.0` the same as `#LancsBox X`?** No; `#LancsBox X` is the newer release used throughout this course with updated CQL, Smart Searches, Corpus Hub, and Summary Tables.
* **Why did searching `carry` give different results in the activity?** Typing `carry` only searches the exact word form *carry*. To include inflected forms (*carries, carried, carrying*), use lemma/headword search or Smart Search.
* **What does sorting by the `Node` column do?** It sorts concordance lines alphabetically by the word form in the node position (helpful when your query matches multiple word forms via wildcards, lemmas, or Smart Searches); if every node is identical, clicking Node resets/randomizes the order.
* **Where do I report OS/Java crashes or script rendering issues?** For issues like Alpine Linux OpenJDK `libprism_es2.so` crashes, macOS installation blocks, or blank Arabic script lines in KWIC, use the helpdesk form at **[lancsbox.lancs.ac.uk](https://lancsbox.lancs.ac.uk)**.
