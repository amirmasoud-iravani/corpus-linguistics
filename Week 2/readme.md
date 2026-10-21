# 📚 Corpus Linguistics: Method, Analysis, Interpretation (Week 2)
*Course delivered by Lancaster University*

Welcome to the Week 2 repository module for **Corpus Linguistics**. Building upon the foundational frequency lists introduced in Week 1, this week explores how to manipulate and exploit frequency data to uncover deeper linguistic, cognitive, and social insights. We cover core methodological techniques—**collocation**, **keyword analysis**, and **corpus statistics**—alongside practical tutorials using `#LancsBox` and conversations with pioneering linguists.

---

## 📑 Table of Contents
1. [Collocation, Colligation, and Related Features](#-1-collocation-colligation-and-related-features)
2. [Keywords, Change Over Time, and Lockwords](#-2-keywords-change-over-time-and-lockwords)
3. [Corpus Linguistics in a Multi-Method Approach](#-3-corpus-linguistics-in-a-multi-method-approach)
4. [Practical Lab: Identifying and Visualizing Collocations in #LancsBox](#-4-practical-lab-identifying-and-visualizing-collocations-in-lancsbox)
5. [Expert Conversations: History & Theory](#-5-expert-conversations-history--theory)
   - [Prof. Geoffrey Leech: The History of Modern Corpora](#51-in-conversation-with-prof-geoffrey-leech-the-history-of-modern-corpora)
   - [Prof. Michael Hoey: Collocation & Lexical Priming](#52-in-conversation-with-prof-michael-hoey-collocation--lexical-priming)
6. [Statistics Meets Corpus Linguistics](#-6-statistics-meets-corpus-linguistics)
7. [References & Further Reading](#-7-references--further-reading)

---

## 🔗 1. Collocation, Colligation, and Related Features
*Based on Lectures 2.3 & 2.4 by Prof. Tony McEnery*

While basic frequency lists show the most common words in a corpus, the top 10 words across different corpora are almost always grammatical function words (e.g., *the, of, and*). To gain deeper insights into meaning, we examine **collocation**.

### What is Collocation?
> *"You shall know a word by the company it keeps."* — J.R. Firth (1957)

**Collocation** is the systematic co-occurrence of words in text and discourse. Because certain words frequently appear together, they begin to determine or influence one another's meanings.
* **Intuition vs. Empirical Reality:** While we have hunches about words that go together (e.g., *telephone* + *operator*, *tell* + *story*), human intuition is often incomplete. 
* **Example (`diamond` in the BNC):** Beyond expected collocates like *solitaire*, *bracelet*, and precious stones (*pearl, ruby, sapphire*), corpus data reveals the collocate *tricks*—highlighting the card game Bridge, where "diamond" refers to a suit of cards.

### Setting Collocation Parameters
When extracting collocates around a **node word** (the word of interest), analysts must establish clear parameters:
1. **Collocation Window (Span):** Empirically, a window of **$\pm 5$ words** (5 words to the left, 5 words to the right) is widely considered productive.
2. **Minimum Frequency Threshold:** To avoid coincidental co-occurrences in large corpora, analysts typically set a cutoff (e.g., a minimum of $10$ co-occurrences).
3. **Sentence Boundaries:** Analysts must decide whether to allow the collocation window to cross sentence boundaries (many prefer to restrict collocates to the same sentence).

### Measuring Collocation: Raw Frequency vs. Association Measures
Relying solely on raw co-occurrence frequency around a node word like `company` yields mostly punctuation and high-frequency function words (*the, of, in*). To filter out words that simply occur everywhere, we use statistical **association measures**:

| Measure | Characteristics | Pros & Cons |
| :--- | :--- | :--- |
| **Mutual Information (MI)** | Compares how often two words occur *together* vs. how often they occur *apart*. | Highlights exclusive, high-affinity terms (e.g., *ec-listed, anglo-persian, worshipful* with `company`). **Downside:** Overstates the importance of low-frequency words unless a minimum frequency cutoff (e.g., $\ge 10$) is applied. |
| **Dice / Log Dice** | Scales association strength while balancing frequency and exclusivity. | Highlights exclusive *and* fairly frequent collocates; less biased toward rare words than MI. |

### Colligation, Semantic Preference, and Discourse Prosody
Looking through the lens of collocation allows us to observe three distinct linguistic phenomena:

1. **Colligation:** Where a word has a strong affinity not with a specific word, but with a **grammatical class** (e.g., *he* colligates with verbs; *Mrs* colligates with proper nouns; determiners colligate with nouns).
2. **Semantic Preference** *(developed by Bill Louw)*: The relation between a lemma/word-form and a **set of semantically related words**.
   * *Example 1:* `diamond` shows a semantic preference for precious stones (*pearl, ruby, sapphire*).
   * *Example 2:* `glass of` in the BNC shows a strong semantic preference for drinkable liquids (*wine, sherry, champagne, beer, water, juice, milk, whiskey*).
3. **Discourse Prosody:** How collocates characterize or reveal a **speaker's attitude** (positive or negative evaluation).
   * *Classic Example (Michael Stubbs):* If asked to define the verb `cause`, people usually give a neutral definition ("making something happen"). However, corpus evidence shows `cause` systematically co-occurs with negative outcomes: *problems, damage, death, disease, concern, cancer, pain, trouble, accident, chaos, crisis, suffering*. Thus, `cause` carries a strong **negative discourse prosody**.

---

## 🔑 2. Keywords, Change Over Time, and Lockwords
*Based on Lectures 2.5 & 2.6 by Prof. Tony McEnery*

### What are Keywords?
In corpus linguistics, a **keyword** is a word that occurs with unusual frequency (statistically significantly more often) in **Corpus A** (the target/study corpus) when compared against **Corpus B** (the reference corpus).

* **Statistical Tests:** Calculated using significance tests such as **Chi-square ($\chi^2$)** or **Log-likelihood**, which normalize for corpus size differences.
* **Thresholds & Filtering:** 
  * Because tests return hundreds of candidate words, analysts typically rank them by statistical significance and examine the **top 10, 50, or 100**.
  * A minimum frequency threshold (often around $20$) is applied.
  * **Dispersion Check:** Analysts use concordancing to ensure a keyword is well-distributed across the corpus rather than clustered in a single paragraph of a single text.
* **Why Use Keywords?** They provide an objective, replicable, and unbiased way to uncover salient features that humans cannot predict in advance.

### Three Common Types of Keywords
1. **Proper Nouns:** Highlighting key actors or locations (e.g., comparing British political news to scientific articles will surface the names of British politicians).
2. **Markers of Style, Genre, or Variety:** Highlighting grammatical patterns or spelling conventions (e.g., British *colour* vs. American *color*).
3. **Indicators of "Aboutness":** Key nouns and verbs that provide a telegraphic "gisting" of what a text collection is fundamentally about.

---

### Case Study: Change Over Time in British English (Baker, 2011)
Paul Baker (2011) investigated lexical stability and change in British English across four diachronic corpora from the **Brown Family** (built between Lancaster and Freiburg Universities), covering four sampling points: **1931, 1961, 1991, and 2006**.

```
[1931: B-LOB] ➔ [1961: LOB] ➔ [1991: FLOB] ➔ [2006: BE06]
```

Baker categorized high-frequency words into three trajectories:

#### 1. Declining Words (More key in the past)
* **Terms of Address (*Mr, Mrs, sir*):** Steady decline reflecting a shift toward a more informal British society.
* **Strong Modal Verbs (*shall, must, should*):** Declining partly due to grammatical shifts, and partly reflecting a "democratization" of discourse—speakers are less comfortable imposing overt, strong obligations on others.
* **Full/Longer Forms:** Giving way to contractions.

#### 2. Lockwords (Staying the same over time)
> **Lockwords** are words whose frequencies remain remarkably stable ("locked in place") across time periods.
* **Weaker Modality:** Contrasting with the decline of strong modals.
* **Wh- Question Words:** *who, what, whether, where*.
* **Body Parts:** Mentioned at a constant rate across decades.
* **Core Existential/Social Nouns:** *money, life, world, government*.

#### 3. Increasing Words (More key in the present)
* **Contracted Forms & Numeric Figures (e.g., *10* instead of *ten*):** Supporting the **densification hypothesis**—the modern tendency to pack as much information as possible into as short a space as possible.
* **Social Terms:** *family, children, child, people, social, health, help*.

#### Deep Dive: Why is the word `children` surging?
`children` is among the top 10 fastest-growing words in modern British English. Concordance and collocation analysis across the time periods reveals a major shift in social discourse:
* **In 1931:** `children` primarily collocated within the traditional family unit (*women and children*, *men, women, and children*).
* **By 1991–2006:** `children` is increasingly problematized and framed around **moral panics**, threat, and victimhood (co-occurring with *welfare, supporting, obesity, paedophiles, poor literacy, poverty, knives, AIDS, adoption, media protection, parental smoking, asthma*).
* **Takeaway:** A statistical keyword in a corpus often mirrors a **socially salient keyword** and an emerging dominant discourse in society.

---

## 🛠️ 3. Corpus Linguistics in a Multi-Method Approach
*Based on Lecture 2.7 by Prof. Tony McEnery*

* **What Corpora Do Best:** Provide empirical insight into the mechanics of language and society on a massive scale that is impossible to achieve by hand and eye alone. They excel at tracking change over time and decoding argumentation strategies.
* **What Corpora Cannot Do:** Corpora cannot answer *every* research question on their own.
* **The Toolbox Metaphor:** 
  * Do not view corpus linguistics as isolated from history, sociology, or other linguistic methods.
  * Think of corpus linguistics as a powerful tool in your methodological **toolbox**. It bridges **quantitative** and **qualitative** analysis, and works best when integrated with other research methods.

---

## 💻 4. Practical Lab: Identifying and Visualizing Collocations in `#LancsBox`
*Based on Tutorials 2.9 & 2.10 by Dr. Vaclav Brezina*

`#LancsBox` (and `#LancsBox X`) features **GraphColl**, a dedicated module for identifying collocates, computing association measures, and generating visual collocation networks.

### Core Concepts in Collocation Analysis
When moving beyond basic frequency, GraphColl allows researchers to evaluate:
1. **Distance:** Defined by the collocation window/span (default in `#LancsBox X` is $\pm 5$ words: $5$ left, $5$ right).
2. **Frequency & Exclusivity:** Operationalized via association measures:
   * *Exclusivity-focused (often infrequent):* MI score, $\mu$ (mu).
   * *Balanced (exclusive + frequent):* Dice, **Log Dice** (the default in `#LancsBox X`), $\text{MI}^2$, $\text{MI}^3$, Log-likelihood.
3. **Dispersion:** How evenly collocates are distributed across different texts/sub-corpora.
4. **Directionality ($\Delta P$ / Delta P):** Tests whether the association is **symmetrical** or **asymmetrical** (i.e., does the node attract the collocate with the same strength that the collocate attracts the node? Computed via *Delta P forward* and *Delta P backward*).
5. **Type-Token Distribution:** Competition between different types of collocates in a given slot.
6. **Connectivity:** Moving from **first-order collocates** (collocates of the node) to **second-order collocates** (collocates of the collocates) to build complex **Collocation Networks**.

---

### Step-by-Step Guide to Using `GraphColl` in `#LancsBox X`

#### 1. Running a Search
1. Open `#LancsBox X`, select your corpus (e.g., *BNC 2014 v2*), and open the **GraphColl** tool.
2. Enter your search query (supports single words, phrases, grammatical structures, smart searches, or **CQL**).
3. *Example Query:* `imagination` in the BNC 2014:
   * **Total Occurrences:** $1,944$ times (Relative frequency: $\approx 19$ per million words).
   * **Dispersion:** Occurs across $1,277$ out of $88,171$ texts.
   * **Co-occurring Words:** $4,543$ total words co-occur within the $\pm 5$ span, of which **$34$ qualify as statistically significant collocates** under default thresholds (Log Dice). Top collocates include *captured* (Log Dice = $8.8$) and *figment*.

#### 2. Reading the GraphColl Table & Concordances
* ** Positional Distribution:** Shows exact frequencies at positions L5 to R5, indicating whether a collocate typically precedes or follows the node.
* **Quick Concordance Preview:** Hovering your mouse over any collocate displays instant concordance lines showing the node and collocate in context (can be copied via `Ctrl+C` / `Cmd+C` directly into a research report).

#### 3. Interpreting the Visual Collocation Graph
GraphColl maps four dimensions of data onto the visual network:
* **Center Node:** The search term (`imagination`) sits in the center like a magnet.
* **Distance (Edge Length):** Represents **association strength** (default: Log Dice). Stronger collocates (*captured, figment*) are pulled closer to the central node.
* **Spatial Position (Left/Right):** Reflects **positionality** in text—whether the collocate predominantly occurs to the left or right of the node.
* **Circle Size:** Represents **collocation frequency** (how often the collocate co-occurs with the node).
* **Circle Color (Blue to Red Scale):** Represents the **overall corpus frequency** of the collocate *anywhere* in the corpus. 
  * *Example:* The preposition `beyond` is colored red because it is highly frequent across the entire BNC, even though *beyond imagination* is also a strong collocation.

#### 4. Filtering by Unit & Part of Speech (POS)
* **Unit Selection:** Switch the display unit from *Word (lowercase)* to *Case-sensitive* or **Lemma** (which groups inflectional morphology under the same word class, surfacing `creativity_N` as a top lemma collocate).
* **POS Filtering:** Hover over the `Collocate` column header, click the filter icon, and filter by POS tags:
  * Type `_N` (Select & Apply to all) to isolate **Noun** collocates.
  * Type `_V` (Select & Apply to all) to isolate **Verb** collocates.

#### 5. Building Collocation Networks (Multi-Node Searches)
You can compare how multiple concepts are framed in discourse by plotting two or more nodes in the same graph:
* **Example:** Searching for the lemmas `alcohol` and `drug` (noun) in the BNC 2014.
* **Visual Output:** Displays collocates unique to `alcohol` at the bottom, collocates unique to `drug` at the top, and **shared collocates** in the middle (*17 shared collocates*, including *cannabis, drink, smoking, problems, booze, misuse, influence, illicit, reduce*).
* Clicking the intersection icon generates a downloadable summary table comparing co-occurrence metrics across both nodes.

---

## 🎙️ 5. Expert Conversations: History & Theory

### 5.1 In Conversation with Prof. Geoffrey Leech: The History of Modern Corpora
*Based on Video 2.15 — Prof. Tony McEnery interviews Prof. Geoffrey Leech (Professor Emeritus, Lancaster University)*

* **1960s: The Pre-Computer Survey of English Usage (UCL):**
  * Initiated by **Randolph Quirk** (later Lord Quirk) at University College London, alongside researchers like **Jan Svartvik**, **Sidney Greenbaum**, **David Crystal**, and student **Norman Fairclough**.
  * Inspired by the empirical, "bottom-up" philosophy of 1940s/1950s **American Structuralism** (collecting field data first to build grammar, contrasting with Chomsky's later "top-down" generative approach).
  * Speech was recorded on reel-to-reel tapes, transcribed by hand, and stored on paper slips inside massive **fireproof metal filing cabinets**. It enabled the landmark *A Grammar of Contemporary English* (Quirk et al., 1972).
* **1970s: The Brown Corpus & The Birth of the LOB Corpus:**
  * In the 1960s, **Nelson Francis** and **Henry Kučera** at Brown University created the **Brown Corpus**—the first computerized corpus of American English ($1\text{ million}$ words).
  * After moving to Lancaster University, Geoffrey Leech proposed building a British English equivalent to match Brown's exact sampling frame.
  * Facing severe funding shortages (starting with just a $£3,200$ grant from Longman) and copyright hurdles with British publishers, the project nearly collapsed in 1976 until **Stig Johansson** (University of Oslo) and **Knut Hofland** (University of Bergen) stepped in with Norwegian funding and computing expertise—creating the **LOB (Lancaster-Oslo/Bergen) Corpus** and founding **ICAME** (*International Computer Archive of Modern and Medieval English*).
* **1980s: Probabilistic POS Tagging (CLAWS) & IBM:**
  * While Brown's early rule-based tagger (`TAGGIT` by Greene & Rubin) achieved $\approx 70\%$ accuracy, Lancaster's team (**Roger Garside**, **Geoffrey Leech**, and **Ian Marshall**) used the tagged Brown corpus as a training corpus on heavy magnetic tapes.
  * By combining probabilistic/stochastic algorithms with rule-based idiom lists, they created **CLAWS**, pushing automated Part-of-Speech tagging accuracy to **$\approx 96\%$**.
  * Throughout the late 1980s, Lancaster collaborated with **IBM** and speech recognition pioneer **Fred Jelinek**, whose data-driven statistical methodology revolutionized NLP and speech-to-text systems.
* **1990s: The British National Corpus (BNC):**
  * Initiated around 1991 (spearheaded by Simon Murison-Bowie at Oxford University Press) with UK government and industrial backing.
  * A massive four-year consortium between **Oxford University Press**, **Lancaster University** (handling grammatical annotation), and **Longman** (collecting the $10\text{-million-word}$ orthographically transcribed spontaneous spoken component), resulting in the $100\text{-million-word}$ BNC.

---

### 5.2 In Conversation with Prof. Michael Hoey: Collocation & Lexical Priming
*Based on Video 2.16 — Prof. Tony McEnery interviews Prof. Michael Hoey (University of Liverpool)*

While collocation is traditionally defined statistically, Michael Hoey argues that a corpus does not represent any single person's exact linguistic experience. To explain *why* words co-occur, we need a **psychological definition** of collocation, where corpus data serves as simulated evidence of human exposure to language.

#### Psychological Foundations: Priming
Drawing on psycholinguistic experiments from the 1970s where informants read word pairs and their reaction times are measured in microseconds:
1. **Semantic Priming:** Seeing a first word speeds up (or slows down) recognition of a second word.
   * `cow` $\rightarrow$ `milk`: **Speeds up** recognition (words are closely associated in the mental lexicon).
   * `cathedral` $\rightarrow$ `milk`: **No change** in recognition speed.
   * `horse` $\rightarrow$ `milk`: **Slows down** recognition in Western cultures due to cognitive dissonance (whereas in Mongolia, where horse milk is drunk, it would prime positively—proving priming is cultural and experience-driven).
2. **Repetition Priming:** If an informant is shown an arbitrary pair of words (e.g., `onion` + `scarlet`) and then shown the exact same pair a significant time later, the first word speeds up recognition of the second.

#### The Theory of Lexical Priming (Hoey, 2005)
* **Language Stored as Encountered:** Repetition priming suggests that the human brain does not immediately strip incoming language into abstract grammatical rules and isolated dictionary entries (as Steven Pinker argued). Instead, we absorb and store language as **strings of memories in the order encountered**.
* **Everyday Evidence of Priming:**
  * Our ability to spot plagiarism or recognize literary allusions years after reading a text.
  * **Long-range lexical cohesion:** Remembering specific phrasing from Chapter 1 of a novel (e.g., Julian Barnes's *Flaubert's Parrot*) to connect it with the final chapter.
  * **Subconscious Collocation (`threadbare` + `carpet`):** In a school workshop conducted by Tony McEnery, a teenager insisted he had never heard the word *threadbare*. When told to write the very first word that popped into his head anyway, he wrote *carpet*—the #1 statistical collocate of *threadbare* in the BNC.
  * **Pragmatic Priming in Childhood (`maybe later`):** Hoey's $2.5\text{-year-old}$ grandson pushed away a disliked book and said *"maybe later"* instead of *"no"*—having subconsciously noticed from his father that the word combination *maybe + later* functions pragmatically as a polite refusal.
* **Fluency & Second Language Acquisition:**
  * Aligning with Krashen's distinction between *knowing a language* (subconscious priming) and *knowing about a language* (conscious grammatical analysis).
  * Over-reliance on conscious grammar-translation rules slows down real-time spoken fluency because learners are not sufficiently primed for spontaneous spoken collocations.

---

## 📊 6. Statistics Meets Corpus Linguistics
*Based on Lecture 2.19 by Dr. Vaclav Brezina*

### What is Statistics?
* **Formal Definition (Diggle & Chetwynd):** *"The science of collecting and interpreting data."*
* **Practical Definition (Brezina):** *"A discipline which helps us make sense of quantitative data whenever we have numbers."*

### Three Core Functions of Statistics
1. **Generalise (Measuring Central Tendency):**
   * Summarizing a dataset with a single representative number (an **average**).
   * *Example:* Measuring adjective frequencies across $11$ randomly sampled fiction writers from the BNC:
     * **Mean:** Sum of all values divided by the number of observations ($\text{Mean} = 591.41$).
     * **Median:** The middle value when observations are ordered from lowest to highest ($\text{Median} = 567$).
2. **Find Relationships (Correlation & Regression):**
   * Plotting two variables on a scatter plot—e.g., **Adjectives** ($x\text{-axis}$) vs. **Verbs** ($y\text{-axis}$) among British fiction writers—and fitting a **regression line (line of best fit)**.
   * Reveals an *inversely proportional relationship*: the more adjectives a fiction writer uses, the fewer verbs they use, and vice versa.
3. **Build Models:**
   * Using mathematical equations to approximate complex real-world phenomena.
   * *Analogy:* Estimating the geographic area of Great Britain using geometric shapes. A rectangle or circle fits poorly, but a **triangle** fits well. Using Google Maps measurements and the area formula:
     $$\text{Area} = \frac{\text{height} \times \text{base}}{2} \approx 234,000\text{ km}^2$$
     This simple mathematical model comes remarkably close to the true area of Great Britain—just as statistical models capture the complex reality of language.

---

### Two Branches of Statistics in Corpus Linguistics

| Descriptive Statistics | Inferential Statistics |
| :--- | :--- |
| **Describes** the data we have in front of us. | **Infers** whether patterns in our corpus sample hold true for the wider language population. |
| *Key Concepts:* Datasets, frequencies, dispersions, graphs, collocations, means, standard deviations. | *Key Concepts:* Statistical tests, $p\text{-values}$, $95\%$ confidence intervals, null hypotheses ($H_0$). |

---

### How Hypothesis Testing Works
When testing a research question, we follow a structured inferential workflow:

1. **Formulate Research Hypothesis ($H_1$):** e.g., *"Men and women use language differently."*
2. **Formulate Null Hypothesis ($H_0$):** The reverse hypothesis stating no effect exists—e.g., *"There is no difference between how men and women use language."*
3. **Collect Corpus Data & Compare:** Suppose a linguistic variable occurs $16$ times in a Male Corpus and $14$ times in a Female Corpus. Is $16$ vs. $14$ a genuine difference, or just random chance?
4. **Compute the $p\text{-value}$:**
   > **Definition:** The **$p\text{-value}$** is the probability of observing values at least as extreme as those in our data *if the null hypothesis ($H_0$) were true*.
5. **Evaluate Against the Cutoff ($\alpha = 0.05$):**
   * **If $p < 0.05$ ($5\%$):** The result is **statistically significant**. We reject $H_0$.
   * **If $p > 0.05$ ($5\%$):** There is **not enough evidence** to reject $H_0$ (Note: we *never* "accept" $H_0$; we simply fail to reject it and may need more data).

---

### The Four Dimensions of Statistical Analysis
Statistical significance ($p\text{-value}$) is only one small part of quantitative corpus analysis. A complete study moves through four distinct levels:

| Dimension | Key Question | Tools & Measures |
| :--- | :--- | :--- |
| **1. Data Exploration** | *What are the main tendencies in the data?* | Descriptive statistics: graphs, means, standard deviations. |
| **2. Inferential Statistics** | *Do we have enough evidence to reject the null hypothesis ($H_0$)?* | Statistical significance tests, $p\text{-values}$, Confidence Intervals (CIs). |
| **3. Effect Sizes** | *How large/strong is the observed effect?* | Standardized magnitude measures: **Cohen's $d$**, **$r$**. |
| **4. Interpretation** | *Is the observed effect socially and linguistically meaningful?* | Connecting corpus findings to linguistic and social theory. |

> ⚠️ **Crucial Takeaway:** **Statistical significance**, **practical importance (effect size)**, and **linguistic meaningfulness** are three separate dimensions. They must be considered, understood, and interpreted separately.

---

### Data Visualization Techniques
Effective visualizations summarize patterns in corpus data without hiding important underlying features:
1. **$95\%$ Confidence Interval (CI) Error Bars:**
   * Plots the mean value for each corpus alongside red error bars showing the $95\%$ CI.
   * **No overlap between error bars:** Guaranteed statistically significant difference.
   * **Large overlap:** No statistical significance.
   * **Tiny overlap:** Run a formal statistical test to confirm.
2. **Geo-Mapping:**
   * Mapping corpus frequencies onto a world map (e.g., plotting place names following travel verbs in the BNC). Dot size reflects frequency—highlighting *London* and UK cities domestically, and *Paris, Rome,* and *New York* internationally.

---

## 📖 7. References & Further Reading
* **Baker, P. (2011).** *Times May Change, But We Will Always Have Money: Diachronic Variation in Recent British English*. Journal of English Linguistics, 39(1), 65–88.
* **Brezina, V. (2018).** *Statistics in Corpus Linguistics: A Practical Guide*. Cambridge University Press.
* **Brezina, V., McEnery, T., & Wattam, S. (2015).** *Collocations in context: A new perspective on collocation networks*. International Journal of Corpus Linguistics, 20(2), 139–173.
* **Garside, R., Leech, G., & Sampson, G. (Eds.). (1987).** *The Computational Analysis of English: A Corpus-Based Approach*. Longman.
* **Hoey, M. (2005).** *Lexical Priming: A New Theory of Words and Language*. Routledge.
* **Louw, B. (1993).** *Irony in the text or insincerity in the writer? The diagnostic potential of semantic prosodies*. In M. Baker, G. Francis, & E. Tognini-Bonelli (Eds.), *Text and Technology* (pp. 157–176). John Benjamins.
* **Quirk, R., Greenbaum, S., Leech, G., & Svartvik, J. (1972).** *A Grammar of Contemporary English*. Longman.
* **Stubbs, M. (1995).** *Collocations and semantic profiles: On the cause of the trouble with quantitative studies*. Functions of Language, 2(1), 23–55.
