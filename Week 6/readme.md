# 📚 Corpus Linguistics: Method, Analysis, Interpretation (Week 6)

*Course delivered by Lancaster University*

Welcome to the Week 6 repository module for **Corpus Linguistics**. This week launches a two-week block examining the transformative impact of corpus linguistics on **Language Testing, Assessment, and Learning**. We explore how testing organizations and classroom teachers use corpora to define Target Language Use (TLU) domains, validate high-stakes exams, track L2 proficiency development, and design exam preparation materials. In our practical lab, we cover batch processing and integrated `R` statistical modeling using the **Wizard** meta-tool in `#LancsBox X`. Finally, our expert conversations feature leading voices in **Language Testing**, **Corpus Lexicography (COBUILD)**, **Computational Lexical Semantics**, **Literary Spatiality**, **Historical GIS**, and the **History of Science**.

---

## 📑 Table of Contents

1. [Course Overview & Warm-Up Activity](#-1-course-overview--warm-up-activity)
2. [Corpora in Language Testing and Assessment](#-2-corpora-in-language-testing-and-assessment)
   * [2.1 Core Objectives & Types of Language Assessment](#21-core-objectives--types-of-language-assessment)
   * [2.2 Describing the Target Language Use (TLU) Domain](#22-describing-the-target-language-use-tlu-domain)
   * [2.3 Measuring L2 Proficiency & Validating Exams](#23-measuring-l2-proficiency--validating-exams)
   * [2.4 Classroom Assessment: Diagnostic & Formative Approaches](#24-classroom-assessment-diagnostic--formative-approaches)
   * [2.5 Preparing L2 Learners for Specific Exams](#25-preparing-l2-learners-for-specific-exams)
3. [Practical Lab: Batch Analysis & Statistical Modeling with `#LancsBox X` Wizard](#-3-practical-lab-batch-analysis--statistical-modeling-with-lancsbox-x-wizard)
   * [3.1 The Data Tab: Running Batch Searches Across Tools](#31-the-data-tab-running-batch-searches-across-tools)
   * [3.2 The Processing Tab: Integrated `R` Scripts (ANOVA & MDA)](#32-the-processing-tab-integrated-r-scripts-anova--mda)
4. [Practical Worksheet & Discussion Prompts](#-4-practical-worksheet--discussion-prompts)
5. [Expert Conversations: Testing, Lexicography, WSD & Digital Humanities](#-5-expert-conversations-testing-lexicography-wsd--digital-humanities)
   * [5.1 Prof. Luke Harding: Washback, Validity, Aptis, and AI in Language Testing](#51-in-conversation-with-prof-luke-harding-washback-validity-aptis-and-ai-in-language-testing)
   * [5.2 Michael Rundell & Prof. Michael Hoey: The Birth of Corpus Lexicography & COBUILD](#52-in-conversation-with-michael-rundell--prof-michael-hoey-the-birth-of-corpus-lexicography--cobuild)
   * [5.3 Dr. Adam Kilgarriff: Word Sense Disambiguation, Polysemy, and Senseval](#53-in-conversation-with-dr-adam-kilgarriff-word-sense-disambiguation-polysemy-and-senseval)
   * [5.4 Prof. Sally Bushell: Romanticism, Manuscripts, and Deep Mapping](#54-in-conversation-with-prof-sally-bushell-romanticism-manuscripts-and-deep-mapping)
   * [5.5 Prof. Ian Gregory: Geographical Information Systems (GIS) and Historical Corpora](#55-in-conversation-with-prof-ian-gregory-geographical-information-systems-gis-and-historical-corpora)
   * [5.6 Dr. Stephen Pumfrey: Early English Books Online (EEBO) and the History of Science](#56-in-conversation-with-dr-stephen-pumfrey-early-english-books-online-eebo-and-the-history-of-science)
6. [Core Readings & References](#-6-core-readings--references)

---

## 🎯 1. Course Overview & Warm-Up Activity

*Based on Documents 6.1 & 6.2*

This week begins a two-week focus on **language testing and language learning**, alongside advanced corpus query and batch-processing workflows.

### Warm-Up Reflection
Before diving into the lecture notes, reflect on your own experience with language exams:
> *Have you ever helped someone prepare for a language exam (as a teacher), or prepared for a language exam yourself (as a learner)? What resources did you rely on to know what vocabulary, grammar, or genres would appear on the test?*

---

## 📝 2. Corpora in Language Assessment

*Based on Lectures 6.3, 6.4, & 6.5*

This module addresses three central questions:
1. **Why are corpora important for developing and validating language tests?**
2. **How can corpora help with measuring L2 proficiency?**
3. **How can corpora assist teachers and learners with classroom assessment and exam preparation?**

### 2.1 Core Objectives & Types of Language Assessment

Language assessments take place across diverse contexts:
* **Diagnostic Assessment:** Conducted at the start of a course or prior to a pedagogical intervention to identify learners' current strengths and needs.
* **Formative Assessment:** Ongoing classroom checks (e.g., before and after a teaching unit) to evaluate instructional effectiveness and track learner progress.
* **Summative Assessment:** End-of-unit or end-of-course evaluation of achievement.
* **High-Stakes Standardized Testing:** Gatekeeping exams used for university admission, professional registration, or immigration/visas (e.g., **TOEFL**, **IELTS**, **PTE Academic**, **OET**, **Aptis**, **Trinity GESE**).

> **Core Objective of Language Assessment:** The systematic gathering of language-related behavior in order to make valid inferences about an individual's language ability and capacity for real-world language use.

Major testing organizations—including **ETS (Educational Testing Service)**, **Pearson**, **Trinity College London**, and the **British Council**—now routinely rely on corpus linguistics to design, revise, and validate their assessments.

---

### 2.2 Describing the Target Language Use (TLU) Domain

At the heart of any test design is the **Target Language Use (TLU) domain**—the real-world environment in which test takers will ultimately need to communicate (e.g., an English-medium university or a hospital workplace).

While test developers traditionally relied on expert interviews and small text samples to understand the TLU domain, corpora provide **large-scale quantitative empirical evidence** of the authentic linguistic features test takers must master, as well as authentic source texts for test item writing:

| Testing Programme | Corpus Application to the TLU Domain |
| :--- | :--- |
| **TOEFL (Late 1990s / 2000s Revision)** | ETS commissioned the **TOEFL 2000 Spoken and Written Academic Language (T2K-SWAL) Corpus** to empirically describe spoken and written university registers and overhaul the TOEFL exam. |
| **TOEFL (Technologically Mediated Learning Study)** | Researchers built a specialized corpus of modern digital university genres—such as **instructional videos** and **online student discussion forum posts**—to evaluate how well TOEFL tasks reflect changing, tech-mediated academic communication. |
| **PTE Academic (Pearson)** | Built the **Pearson International Corpus of Academic English (PICAE)** across diverse academic spoken and written genres. Used to inform test design and generate the ** Pearson Academic Collocation List (ACL)** for test prep materials. |

---

### 2.3 Measuring L2 Proficiency & Validating Exams

#### 1. Distinguishing Stages of L2 Proficiency
Corpus studies of learner production help establish what linguistic features distinguish learners across proficiency bands (e.g., CEFR levels A1–C2), informing **rating scales** and revealing what features human examiners subconsciously value:
* **Example — Lexical Bundles in L2 Writing:** Multiple corpus studies demonstrate that the **frequency, structural type, and functional range of lexical bundles** (multi-word sequences) strongly correlate with L2 writing proficiency levels.

#### 2. Exam Corpora for Test Validation
To determine whether a test is "doing its job" (**test validity**), researchers compile **exam corpora** of test-taker performances and evaluate whether the test elicits language representative of the TLU domain and reliably separates proficiency levels.

**Notable Exam & Proficiency-Rated Learner Corpora:**
* **Trinity Lancaster Corpus (TLC):** $>2,000$ spoken transcripts ($>4\text{M}$ words) from the **GESE (Graded Examinations in Spoken English)** administered by Trinity College London.
* **Guangwai-Lancaster Chinese Learner Corpus:**Freely accessible via Sketch Engine; a rare non-English exam corpus capturing **spoken and written L2 Chinese exam performances** across proficiency levels (built by Lancaster University and Guangdong University of Foreign Studies).
* **British Council–Lancaster Aptis Corpus:** Computer-mediated L2 speaking and writing exam performances.

#### 3. Two Validation Case Studies

```
┌────────────────────────────────────────────────────────────────────────────┐
│ CASE STUDY A: External Domain Comparison (Staples et al. — TOEFL iBT)      │
│ • Compared language elicited in TOEFL iBT writing tasks against authentic  │
│   disciplinary university student writing across departments.              │
│ • Finding: Alongside many similarities, TOEFL iBT essays elicited fewer    │
│   features of high informational density (fewer nominalizations,           │
│   attributive adjectives, and abstract nouns) than real university papers. │
├────────────────────────────────────────────────────────────────────────────┤
│ CASE STUDY B: Internal Task Comparison (Trinity Lancaster Corpus — GESE)   │
│ • Compared stance-taking markers across 4 distinct speaking tasks within   │
│   the GESE exam (1 monologic presentation task vs. 3 dialogic tasks).      │
│ • Finding: The monologic task elicited significantly fewer stance markers  │
│   than the 3 dialogic tasks—validating that the exam tasks successfully    │
│   elicit the expected register differences.                                │
└────────────────────────────────────────────────────────────────────────────┘
```

---

### 2.4 Classroom Assessment: Diagnostic & Formative Approaches

Teachers can compile small classroom corpora of their own students' work (analyzed in tools like `#LancsBox`) for **diagnostic** (needs analysis at the start of term) and **formative** (pre- vs. post-intervention) assessment:
* **What to Analyze:** Lexical range/sophistication, academic vocabulary, collocations, target grammatical structures, or error patterns.
* **Practical Tip for Spoken / Handwritten Production:** While electronic essays are easy to load into a corpus tool, transcribing student speech or handwritten essays is time-consuming for a teacher. **Solution:** Turn transcription into a **collaborative student learning activity**—have students record and transcribe their own speaking tasks or presentations, using guided worksheets to notice features of their own spoken grammar and fluency.

---

### 2.5 Preparing L2 Learners for Specific Exams

Teachers can combine published corpus findings, DIY exam corpora, and **Data-Driven Learning (DDL)** to prepare students for high-stakes exams:

1. **Austrian Standardized School-Leaving Exam (*Matura* Reform, 2009):**
   * *Challenge:* A national reform introduced standardized English and French exams requiring students to write unfamiliar real-world genres (**emails, blogs, and reports**) alongside traditional essays.
   * *Corpus Solution:* Austrian teachers conducted corpus searches and drew on genre studies—such as **Grieve et al.'s corpus study of blogs** (distinguishing personal vs. expert blogs)—to identify the exact lexical and grammatical conventions needed to teach those genres and design local mock exams.
2. **IELTS Reading Preparation (Vocabulary Load):**
   * *Challenge:* Students struggled with dense, unknown vocabulary in IELTS Reading passages.
   * *Corpus Solution:* The teacher compiled a small DIY corpus of past IELTS Reading texts, generated a frequency word list, and built targeted classroom exercises around the **top 100 lexical words**.
3. **IELTS Writing Preparation (Passive Constructions):**
   * *Challenge:* Improving task-appropriate grammar and vocabulary for IELTS Writing prompts.
   * *Corpus Solution:* The teacher compiled a model corpus of **50 essays written by IELTS examiners**, analyzed the most frequent **passive constructions**, and designed both teacher-led exercises and student-centered **Data-Driven Learning (DDL)** concordance activities.
4. **Trinity GESE Speaking Preparation (Communicative Strategies):**
   * *Challenge:* Helping learners succeed in interactive speaking exams and general spoken fluency.
   * *Corpus Solution:* Researchers compared **high-scoring vs. low-scoring candidates** in the *Trinity Lancaster Corpus*, identifying key differences in how successful speakers ask questions, backchannel (show active listening), manage turn-taking, repair communication breakdowns/misunderstandings, and replace filled/unfilled pauses with natural **discourse markers**. These findings were turned into free classroom worksheets.

---

## 🧙‍♂️ 3. Practical Lab: Batch Analysis & Statistical Modeling with `#LancsBox X` Wizard

*Based on Tutorial 6.7 by Dr. Vaclav Brezina*

The **Wizard** tool (accessed via the top-right Wizard icon in `#LancsBox X`) is a **meta-tool** that sits above all individual `#LancsBox` modules. It performs automated **batch searches** in the background and integrates directly with the **`R` statistical environment** for advanced statistical modeling.

### 3.1 The `Data` Tab: Running Batch Searches Across Tools

In the **Data** tab, you select a target corpus (e.g., *BNC 2014*, $100\text{M}$ words / $88,000+$ files), configure any `#LancsBox` tool, paste a list of queries (one per line), choose an output folder, and click **Run**. Multiple batch jobs can run simultaneously in the background while a progress indicator tracks completion.

| Tool in Wizard | Batch Configuration & Output | Example Use Case |
| :--- | :--- | :--- |
| **1. KWIC** | Paste $100$ query terms (1 per line). Select display layers (**Word**, **POS tag**) and metadata columns (**Genre**). Exports $100$ Excel-ready concordance tables in $<10\text{ minutes}$. | Generating $100$ separate POS-tagged, genre-coded concordances for offline qualitative coding. |
| **2. GraphColl** | Enter query term(s) (e.g., `beautiful` or $100$ different nodes). Set association measure (**Log Dice**, plus **$\text{MI}^2$**) and filter to **top 20 collocates**. | Automatically saving high-resolution collocation network graphs and collocate tables for dozens of words at once. |
| **3. Text** | Select output metrics (**File Name, Tokens, Relative Frequency**; optionally toggle off lexical density). Enter multiple smart searches or CQL queries (e.g., `nice`, `_N` [nouns], `_V` [verbs], passives). | Generating a massive **file-by-variable relative frequency matrix** across all $88,171$ BNC files for statistical analysis in Excel or `R`. |
| **4. Words** | Queries optional. Extract $1\text{-grams}$ (single words) up to $5\text{-grams}$ by lowercase word, case-sensitive word, POS, semantic tag, lemma, or lexeme, with full frequency and dispersion stats. | Batch-generating $n$-gram and lemma frequency/dispersion lists across multiple corpora. |

---

### 3.2 The `Processing` Tab: Integrated `R` Scripts (ANOVA & MDA)

The **Processing** tab loads data tables generated by the **Text** tool and runs fully commented, customizable **`R` scripts** to produce statistical outputs and visualizations:

#### 1. One-Way / Multi-Way ANOVA with Tukey's HSD Post-Hoc Tests
* **Input Table:** File names, relative frequencies of a target word (e.g., `lovely`), and `Genre` metadata across the BNC 2014.
* **Execution:** Select the built-in **ANOVA** `R` script and click **Run**.
* **Output:**
  * Full ANOVA summary table ($F$-value, $p$-value).
  * **Tukey's HSD (Honestly Significant Difference)** post-hoc pairwise comparisons across all genre pairs, corrected for multiple testing, with lower and upper $95\%$ Confidence Intervals.
  * **Visual Confidence Interval Plot:** Pairwise genre comparisons (e.g., *Written-to-be-spoken* vs. *Official documents*) are plotted horizontally:
    * 🔴 **Red bars** (not crossing $0$): **Statistically significant difference**.
    * 🔵 **Blue bars** (crossing $0$): **Not statistically significant**.

#### 2. Multi-Dimensional Analysis (MDA — Biber's Framework)
* **Input Table:** File names, `Register` metadata, and relative frequencies for the **$67$ standard Biber linguistic variables** extracted via the Text tool.
* **Execution:** Select the **Multi-Dimensional Analysis** script, specify the number of factors (e.g., a **6-factor solution**), and select which Dimension to plot (e.g., `Dimension 1` or `Dimension 2`).
* **Output:**
  * Factor loading table for all variables (using an absolute factor loading cutoff of $|\ge 0.35|$, where variables below the threshold are set to $0$ and each variable loads onto its primary factor).
  * **Dimension Score Visualization:**
    * *Dimension 1:* Plots registers along a continuum from **General Fiction / Romance / Humour** at one pole to **Academic Writing / Government Documents** at the opposite pole, with **Newspapers** in the middle.
    * *Dimension 2 (Narrative vs. Non-Narrative):* Re-running for Factor 2 highlights narrative time markers versus nominalizations.

---

## 📋 4. Practical Worksheet & Discussion Prompts

*Based on Documents 6.8 & 6.10*

* **Practical Activity (6.8 — Aptis Corpus Worksheet):**
  * Download the **Aptis Corpus Worksheet** and complete Tasks 1–3 using real-world computer-mediated exam data. Reflect on any challenges encountered when interpreting learner production data.
* **Week 6 Discussion Prompt (6.10):**
  > *Can you think of practical uses of corpora in your own context in relation to test or exam preparation? How would you incorporate the techniques you have learned this week?*

---

## 🎙️ 5. Expert Conversations: Testing, Lexicography, WSD & Digital Humanities

### 5.1 In Conversation with Prof. Luke Harding: Washback, Validity, Aptis, and AI in Language Testing

*Based on Video 6.11 — Dr. Vaclav Brezina interviews Prof. Luke Harding (Lancaster University)*

* **Pathway into Language Testing & Positive Washback:**
  * Started as an English language teacher before completing his MA and PhD in Applied Linguistics at the University of Melbourne, where he worked on the **Occupational English Test (OET)** for overseas-trained healthcare professionals.
  * **Washback:** The impact of a test on classroom teaching and learning.
    * *Negative Washback:* Narrow "teaching to the test," high learner anxiety, and rote grammar memorization.
    * *Positive Washback:* Intentional test design that encourages learning a rich array of communicative skills aligned with curriculum goals, alongside broader assessment paradigms (**peer assessment, self-assessment, portfolio assessment**) and a strong commitment to **Equality, Diversity, and Inclusion (EDI)**.
* **Three Core Uses of Corpora in Language Testing:**
  1. **Describing the Target Language Use (TLU) Domain:** Building corpora of the target environment (e.g., university lectures/seminars for TOEFL) to establish what language features a test must sample.
  2. **Supporting Score Validity Arguments:** Using exam performance corpora (e.g., *Trinity Lancaster Corpus*, *Aptis Corpus*) to verify empirically whether candidates awarded a higher score (e.g., Band 8 vs. Band 6 in writing) actually produce significantly greater lexical sophistication or syntactic complexity.
  3. **Exploratory Investigation of the Test as a Communicative Event (The Aptis Case Study):**
     * The British Council's **Aptis** speaking test is **computer-mediated and semi-direct** (candidates speak into a microphone to a computer rather than a live human interlocutor).
     * *Serendipitous Corpus Finding (Gablasova, Harding, Brezina, & Dunlea, 2024):* Researchers assumed that without a live human listener, candidates would rarely use interpersonal **epistemic stance markers**. Surprisingly, corpus analysis revealed high frequencies of epistemic stance markers comparable to face-to-face human interviews—showing that humans naturally bring a social frame even to human–computer interaction. This finding can be fed back into rating scales to foster positive washback.
* **The Future of Language Testing in the Age of AI & LLMs:**
  * AI is rapidly transforming **automated item generation** and **automated speech/writing scoring** (shifting from transparent feature-based algorithms to black-box machine learning models).
  * **Utopian Vision:** Using corpus techniques to gather learner language "in the wild" for continuous, individualized, learning-centered diagnostic feedback.
  * **Dystopian Vision:** Relying on fully automated digital tests purely for commercial expediency, which narrows the tested construct because current chatbots/dialogue systems still struggle to replicate authentic, zero-lag human **interactional competence**.
  * **Corpus Literacy as part of Language Assessment Literacy (LAL):** Because AI scoring engines and LLMs are only as good as their training corpora (which often contain baked-in social biases), language testers need **corpus literacy** to critically audit the balance and representativeness of AI training data.
* **Advice for Early Career Researchers:** Read flagship journals (*Language Testing*, *Language Assessment Quarterly*), join professional associations (**ILTA**, **UKALTA**), explore programs like Lancaster's part-time distance **MA in Language Testing**, and gain hands-on experience actually designing and building tests.

---

### 5.2 In Conversation with Michael Rundell & Prof. Michael Hoey: The Birth of Corpus Lexicography & COBUILD

*Based on Videos 6.12 & 6.17 — Prof. Tony McEnery interviews Michael Rundell (Editor-in-Chief, Macmillan Dictionary) and Prof. Michael Hoey (University of Liverpool)*

* **Pre-Corpus Lexicography (Before 1980):**
  * When Michael Rundell entered lexicography in 1980, dictionary-making relied on three flawed sources: handmade paper citation slips (like the OED), looking at what rival dictionaries had written, and **introspecting** into one's own mental lexicon to invent definitions and made-up examples.Even pioneering learner dictionaries like **A.S. Hornby's** *Oxford Advanced Learner's Dictionary* had to rely on intuition because computer corpora did not exist.
* **The Birmingham Pioneers & The 1970 *OSTI Report*:**
  * In 1970, **John Sinclair** and his collaborators produced the **OSTI Report**—the first computationally driven study of collocation (which nearly went extinct, surviving at one point in only six photocopies treasured by Michael Hoey before being republished online).
  * Alongside Geoffrey Leech at Lancaster, John Sinclair at Birmingham founded modern corpus linguistics.
* **Launching the Collins COBUILD Project (1980–1987):**
  * Appointed in 1979 as Birmingham's English Language Research Officer, **Michael Hoey** co-wrote the proposal with **Beryl (Sue) Atkins** (John Sinclair's sister) that secured a massive **£1 million grant** from Collins Publishers in 1981 (50 times larger than the £20,000 LOB Corpus budget, terrifying Birmingham's finance office!).
  * Managed by **John Sinclair**, **Antoinette Renouf** (initial editor), **Patrick Hanks** (second editor), **Jeremy Clear** (computer officer), and **Michael Hoey**, compiling the initial corpus required shutting down the entire University of Birmingham computing service for three weekends—crashing the mainframe on the first attempt until the text was processed in smaller blocks.
* **Three Camps of Lexicographers & The Culture Shock of Data:**
  * Hoey observed that the lexicographers hired for COBUILD fell into three groups:
    1. *Traditional Lexicographers:* Struggled to unlearn old introspective habits ("like asking a champion tennis player to play badminton"); one respected veteran resigned after a year because he could not adapt to corpus evidence.
    2. *Non-Native Speakers:* Sometimes missed subtle L1 pragmatic nuances in concordance lines.
    3. *Trained Linguists (including Michael Rundell, Gwyneth Fox, Patrick Hanks):* Thrived on daily empirical discoveries and later spread the "COBUILD revolution" like apostles across Longman, Macmillan, and Oxford University Press.
* **Eureka Moments & Theoretical Breakthroughs from COBUILD:**
  1. **Discovering Unrecorded Senses (`represent` as a Copula):** Reading dot-matrix paper concordances at COBUILD, Rundell noticed that in newspaper prose, `represent` frequently functioned not as "symbolize" or "stand for a constituency in Parliament," but as a simple **copular verb meaning `is`** (e.g., *"This represents an enormous breakthrough"*), a high-frequency usage completely absent from previous dictionaries.
  2. **Sinclair's Collocation Criterion for Sense Division:** Two dictionary senses are only justified if there is at least one collocation (or grammatical pattern) present in one sense that does not occur in the other (the seed of Hoey's *Lexical Priming* and "drinking problem" sense-avoidance syndrome).
  3. **Sinclair's Idiom Principle:** Grew out of Jeremy Clear's team workshops where a single masked word from a text was shown on screen and lexicographers found they could predict the preceding and following words $80\%$ of the time from narrow collocational choices.
  4. **Authentic Examples & Frequency-Ordered Senses:** Post-COBUILD dictionaries rank senses by observed corpus frequency and use authentic corpus examples to carry collocational, grammatical, and pragmatic information.

---

### 5.3 In Conversation with Dr. Adam Kilgarriff: Word Sense Disambiguation, Polysemy, and Senseval

*Based on Video 6.14 — Prof. Tony McEnery interviews Dr. Adam Kilgarriff (Lexical Computing / Creator of Sketch Engine)*

* **From Philosophy & AI to Lexical Semantics:**
  * After studying philosophy (where he found Wittgenstein, Austin, and Searle's theories of meaning bafflingly abstract) and Artificial Intelligence, Kilgarriff focused his PhD on how word meanings are represented and disambiguated.
* **Why Word Sense Disambiguation (WSD) is Harder Than `bank`:**
  * In NLP, textbooks always illustrate **Word Sense Disambiguation (WSD)** with `bank` (*river bank* vs. *money bank*).
  * However, Kilgarriff's research showed that most real-world sense distinctions are not neat homonyms, but subtle, overlapping **polysemy continua**:
    * What about a *bank of clouds*, a *blood bank*, or a *"bullet bank"* (an earthen mound in the woods where WWII bullets were fired and stored—which is simultaneously a raised earth mound *and* a storage repository)?
* **Organizing `Senseval` (now `SemEval`, 1998–Present):**
  * Because WSD researchers tested their algorithms on different texts and different dictionaries, claimed accuracy rates (e.g., "$93\%$") were impossible to compare.
  * In **1998**, Kilgarriff founded **Senseval**, a standardized international shared-task competition using a common human-annotated gold-standard dataset ("crib sheet") and dictionary.
  * **The "Sense Inventory" Problem:** Senseval proved that there is no single universal list of word senses (*sense inventory*); the required granularity depends entirely on the task. Modern SemEval tasks bypass fixed dictionary inventories by evaluating **sentence similarity** or **cross-lingual translation equivalents**.
  * **Commercial Applications:** Web search engines (like Google) use WSD and **Named Entity Disambiguation** (e.g., distinguishing which *James Taylor* a web page refers to) to match queries to documents.

---

### 5.4 In Conversation with Prof. Sally Bushell: Romanticism, Manuscripts, and Deep Mapping

*Based on Video 6.15 — Prof. Tony McEnery interviews Prof. Sally Bushell (Department of English & Creative Writing, Lancaster University)*

* **Triangulating Manuscript, Process, and Place in Wordsworth:**
  * Specializes in late 18th/early 19th-century Romanticism—particularly **William Wordsworth**, whose original manuscripts are housed at **Dove Cottage (Grasmere)** in the Lake District just north of Lancaster.
  * Combines textual criticism, editorial rigor, and spatial analysis (e.g., the digital project *From Goslar to Grasmere*), examining how a poem's meaning is layered across:
    1. The physical layout and eye-movement across the **handwritten manuscript page**.
    2. The chronological **layers of draft revisions**.
    3. The **physical geographical spot** where Wordsworth stood when inspired or where he chose to compose the poem.
* **Beyond Pure "Text Mining" to Qualitative Digital Humanities:**
  * Cautions against reductive "text mining" that treats literary works merely as "data" and strips out the human reader. Instead, advocates a **cyclical workflow** (shared with Tony McEnery) that moves from digital concordancing/collocation (e.g., tracing `path` and `pathway` in the *Wordsworth Concordance*) back into close literary reading.
  * **Deep Mapping (David Bodenhamer) & Mobile Literary Hotspots:** Envisions multi-layered digital editions that link manuscript facsimiles, variant drafts, and 18th-century picturesque illustrations directly to **Geographical Information Systems (GIS)**—including location-aware mobile apps that trigger layers of poetic and manuscript meaning when a walker stands at that exact spot in the Lake District.

---

### 5.5 In Conversation with Prof. Ian Gregory: Geographical Information Systems (GIS) and Historical Corpora

*Based on Video 6.16 — Prof. Tony McEnery interviews Prof. Ian Gregory (Department of History, Lancaster University)*

* **From Quantitative Census GIS to Textual Geographies:**
  * Began by digitizing changing historical parish/administrative boundaries to map structured **19th-century quantitative records** (Census data and Registrar General records of births, marriages, and deaths) to study the **19th-century mortality transition** (why infant mortality dropped from $\approx 15\%$ in 1850 to modern levels—debating Disraeli-era sanitation/sewage reforms vs. rising nutrition/living standards).
  * **The Blind Spot of Numeric Data:** Quantitative GIS fails whenever historical actors did not collect numbers (e.g., 19th-century campaigns promoting breastfeeding). However, people *wrote* about those topics in newspapers and reports.
* **Bridging Corpus Linguistics and GIS (*Mapping the Lakes* & ERC Project):**
  * **Pilot Study (*Mapping the Lakes* with Sally Bushell & David Cooper):** Manually extracted and mapped place names from two $10,000$-word travel texts of the Lake District.
  * **Scaling Up with Automated Geo-Parsing (with Andrew Hardie):** Secured a major **European Research Council (ERC)** grant to automatically extract place names from a **$1.5\text{-million-word}$ Lake District corpus** (spanning early modern travel writing to 1900) as well as **19th-century British Library newspapers** and official reports, combining **collocation** and **GIS mapping** to see *what* was being said about *which places*.
* **Two Historical Case Studies Combining Corpora & GIS:**
  1. **Rural Suffolk Mortality Puzzle:** Quantitative records showed three neighbouring rural districts in Suffolk had vastly different infant mortality trajectories for no obvious numeric reason. Searching place names and health themes in the *19th Century British Library Newspapers* corpus revealed that the struggling district had a dysfunctional local government structure that failed to invest in water drainage.
  2. **Mapping Epidemic Reality vs. Media Panic (19th-Century Cholera):**
     * *Mid-19th Century Cholera Outbreaks:* Comparing newspaper place-name mentions against actual death records revealed a strong **London-centric media bias**, alongside reporting on sanitation improvements.
     * *Late-19th Century Cholera Scare:* Corpus frequency of `cholera` spiked dramatically in newspapers while actual British death rates remained near zero—mapping the **geographic spread of a media panic** as cholera swept from India toward Europe, even though improved British sanitation prevented an actual domestic outbreak!
* **Modern Applications:** Geo-parsing unstructured digital text (emails, social media, local government complaint logs) provides a rapid, low-cost way to identify spatial inequalities (e.g., testing whether middle-class neighborhoods receive more council attention than working-class ones) before deploying expensive household panel surveys.

---

### 5.6 Dr. Stephen Pumfrey: Early English Books Online (EEBO) and the History of Science

*Based on Video 6.18 — Prof. Tony McEnery interviews Dr. Stephen Pumfrey (Department of History, Lancaster University)*

* **The Digital Revolution in Early Modern History: EEBO & EEBO-TCP:**
  * **Early English Books Online (EEBO)** contains facsimile images of all **$127,000$ books** published in England or in English from the dawn of English printing (**1473**) to **1700**.
  * Through the **Text Creation Partnership (EEBO-TCP)**, over **$44,000$ books** ($\approx 1.2\text{ to }2\text{ billion words}$) have been manually keystroked into machine-readable text.
  * Through Lancaster's interdisciplinary **CREME (*Corpus Research in Early Modern English*)** group (noting that `creme` was the standard Tudor spelling of *cream*!), ProQuest provided the raw keystroked texts to UCREL (Paul Rayson & Alistair Baron), who processed the entire billion-word collection with **VARD** (spelling normalization), **CLAWS** (POS tagging), **USAS** (semantic tagging), collocation tools, and diachronic publication-date normalization (`EEBO v3`).
* **Three Case Studies in the History of Early Modern Science ("Natural Philosophy"):**
  1. **The Rise and Fall of `Momus` and `Zoilus` (1570–1610):**
     * While reading Elizabethan and Jacobean scientific patronage dedications, Pumfrey kept encountering references to **Zoilus** (an ancient Greek critic who disparaged Homer) and **Momus** (the Greek god of carping criticism who complained that bulls' horns were misplaced and humans lacked a window into their hearts).
     * What took Pumfrey a week of manual tallying on slow EEBO web pages—and took Paul Rayson **10 minutes** using corpus tools—revealed that the *Momus/Zoilus* trope surged in English book prefaces strictly between **1570 and 1610** before vanishing.
  2. **The Surprising Puritan Pre-History of the Word `experiment`:**
     * Before the late 17th-century Scientific Revolution (e.g., Robert Boyle and the Royal Society), `experiment` was synonymous with passive everyday `experience` (e.g., knowing the sun rises by "daily experiment").
     * When Pumfrey searched `experiment` across EEBO to trace its shift toward controlled scientific testing, he discovered **"unknown unknowns"**: thousands of hits in the **1640s and 1650s** occurred not in natural philosophy tracts, but in **Puritan sermons** discussing *"experimental Christianity"* (having the inner felt "experiment"/experience of grace in one's heart)—a crucial religious bridge in the word's semantic history that historians of science had completely missed because they never read Puritan sermons.
  3. **Semantic Tagging of `liberty`:**
     * Using **USAS semantic tags** on EEBO v3 allows historians to automatically separate political uses of `liberty` (*liberty of conscience*, property rights) from theological uses (*liberty from sin*) across **$2\text{ billion}$ words**—while remaining mindful of historical semantic shifts between 1600 and present-day English.

---

## 📖 6. Core Readings & References

*Based on Document 6.9 & Lecture Bibliographies*

### Required Readings for Week 6
* **Brezina, V., & Gablasova, D. (2015).** *Is there a core general vocabulary? Introducing the New General Service List*. Applied Linguistics, 36(1), 1–22.
* **Brunfaut, T. (2023).** *Future challenges and opportunities in language testing and assessment: Basic questions and principles at the forefront*. Language Testing, 40(1), 15–23.
* **Gablasova, D., Harding, L., Brezina, V., & Dunlea, J. (2024).** *Expressions of epistemic stance in computer-mediated L2 speaking assessment: A corpus-based approach*. International Journal of Learner Corpus Research, 10(1), 183–215.
* **Pill, J., Bandman, J., Bottini, R., Brunfaut, T., Davidson, N., Davila Perez, G., Harding, L., Jung, Y., Lestari, S., Ramos Galvez, C., & Rossi, O. (2024).** *Shaping a language testing curriculum: Insights from an oral history of a Masters programme*. In B. Baker & L. Taylor (Eds.), *Language assessment literacy and competence: Volume 1 Research and reflections from the field* (pp. 168–191). Cambridge University Press.

### General Reference Handbooks & Cited Studies
* **Biber, D., Conrad, S., Reppen, R., Byrd, P., & Helt, M. (2002).** *Speaking and writing in the university: A multidimensional comparison*. TESOL Quarterly, 36(1), 9–48.
* **Fulcher, G., & Harding, L. (Eds.). (2022).** *The Routledge Handbook of Language Testing* (2nd ed.). Routledge.
* **Gregory, I., & Hardie, A. (2011).** *Visual GISting: Bringing together corpus linguistics and Geographical Information Systems*. Literary and Linguistic Computing, 26(3), 297–314.
* **Grieve, J., Biber, D., Friginal, E., & Nekrasova, T. (2010).** *Variation among blogs: A multi-dimensional analysis*. In A. Mehler, S. Sharoff, & M. Santini (Eds.), *Genres on the Web* (pp. 303–322). Springer.
* **Kilgarriff, A. (1997).** *I don't believe in word senses*. Computers and the Humanities, 31(2), 91–113.
* **Sinclair, J. (Ed.). (1987).** *Looking Up: An Account of the COBUILD Project in Lexical Computing*. Collins ELT.
* **Staples, S., Egbert, J., Biber, D., & McClair, A. (2013).** *Formulaic sequences and EAP writing development: Lexical bundles in the TOEFL iBT writing section*. Journal of English for Academic Purposes, 12(3), 214–225.
* **Winke, P., & Brunfaut, T. (Eds.). (2021).** *The Routledge Handbook of Second Language Acquisition and Language Testing*. Routledge.
