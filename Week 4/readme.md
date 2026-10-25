# 📚 Corpus Linguistics: Method, Analysis, Interpretation (Week 4)

*Course delivered by Lancaster University*

Welcome to the Week 4 repository module for **Corpus Linguistics**. This week focuses on the science and practice of **building, annotating, and pre-processing corpora**. We explore how corpora operate as representative samples of a vast "ocean" of daily language production, examine three landmark corpus-building projects at Lancaster University (*BNC 2014*, *Trinity Lancaster Corpus*, and *Guangwai-Lancaster Corpus*), walk through practical tutorials for building your own DIY corpus in `#LancsBox` and applying automatic semantic tagging with **USAS** / **PyMUSAS**, and hear from experts working on multimodal sign language corpora, historical spelling normalization (**VARD**), spoken corpus design, and computational semantic analysis.

---

## 📑 Table of Contents

1. [A Drop in the Ocean: Corpora as Samples of Language](#-1-a-drop-in-the-ocean-corpora-as-samples-of-language)
   * [1.1 The Scale of Daily Language vs. The Corpus Sample](#11-the-scale-of-daily-language-vs-the-corpus-sample)
   * [1.2 Representativeness, Balance, and Sampling](#12-representativeness-balance-and-sampling)
   * [1.3 Major Types of Corpora](#13-major-types-of-corpora)
2. [Building Corpora: Design, Development, and Annotation](#-2-building-corpora-design-development-and-annotation)
   * [2.1 Corpus Design: The British National Corpus 2014 (BNC 2014)](#21-corpus-design-the-british-national-corpus-2014-bnc-2014)
   * [2.2 Corpus Development & Transcription: The Trinity Lancaster Corpus (TLC)](#22-corpus-development--transcription-the-trinity-lancaster-corpus-tlc)
   * [2.3 Corpus Annotation: The Guangwai-Lancaster Corpus of L2 Chinese](#23-corpus-annotation-the-guangwai-lancaster-corpus-of-l2-chinese)
   * [2.4 Five Golden Tips for Building Your Own Corpus](#24-five-golden-tips-for-building-your-own-corpus)
3. [Practical Lab 1: Building a DIY Corpus & Using the `Text` Tool in `#LancsBox`](#-3-practical-lab-1-building-a-diy-corpus--using-the-text-tool-in-lancsbox)
   * [3.1 How to Collect a Mini DIY Newspaper Corpus](#31-how-to-collect-a-mini-diy-newspaper-corpus)
   * [3.2 Exploring Files, Lexical Diversity, and Context in the `#LancsBox X` Text Tool](#32-exploring-files-lexical-diversity-and-context-in-the-lancsbox-x-text-tool)
4. [Practical Lab 2: Semantic Annotation with the USAS Web Tagger & `PyMUSAS`](#-4-practical-lab-2-semantic-annotation-with-the-usas-web-tagger--pymusas)
5. [Expert Conversations: Multimodal, Historical, Spoken, and Computational Corpora](#-5-expert-conversations-multimodal-historical-spoken-and-computational-corpora)
   * [5.1 Dr. Kearsy Cormier: The British Sign Language (BSL) Corpus & Multimodal Data](#51-in-conversation-with-dr-kearsy-cormier-the-british-sign-language-bsl-corpus--multimodal-data)
   * [5.2 Dr. Alistair Baron: Spelling Variation, Normalization, and VARD](#52-in-conversation-with-dr-alistair-baron-spelling-variation-normalization-and-vard)
   * [5.3 Dr. Vaclav Brezina: DIY vs. Public Corpora, Spoken Data Ethics, and the BNC 64](#53-in-conversation-with-dr-vaclav-brezina-diy-vs-public-corpora-spoken-data-ethics-and-the-bnc-64)
   * [5.4 Prof. Paul Rayson: CLAWS, USAS, Wmatrix, and Real-World NLP Applications](#54-in-conversation-with-prof-paul-rayson-claws-usas-wmatrix-and-real-world-nlp-applications)
6. [References & Resources](#-6-references--resources)

---

## 🌊 1. A Drop in the Ocean: Corpora as Samples of Language

*Based on Lectures 4.3 & 4.24 by Dr. Vaclav Brezina*

### 1.1 The Scale of Daily Language vs. The Corpus Sample

Every day, humanity produces an unfathomable volume of spoken and written language:
* An average person utters approximately **$16,000\text{ words per day}$**.
* With roughly **$400\text{ million}$ L1 speakers** of English and hundreds of millions of L2 speakers worldwide, daily spoken English production alone is on the order of **trillions of words** ($1\text{ trillion} = 10^{12} = 1,000,000,000,000$—comparable to the number of grains of sand on Morecambe Bay beach).
* Most spoken language happens in the moment and is never recorded, alongside massive daily online and offline written production.

#### The Test Tube & Wine Tasting Analogies
To analyze the ocean, a marine scientist does not need to pour the entire Irish Sea into a laboratory; a single **test tube of water** tested with litmus paper reveals that the water's pH is around $8$ (slightly basic) and allows scientists to track ocean acidification over time. Similarly, in **wine tasting**, a single sip is enough to judge the quality of the whole bottle.

In corpus linguistics, **a corpus is a sample**: a small, carefully selected subset that gives us statistical power to make inferences about the wider **population** ("language in the wild").

* **Case Example — Tracking the Decline of `must` (1931–2016):**
  * Using just **five $1\text{-million-word}$ samples** of written British English ($5\text{ million}$ words total across 85 years: 1931, 1961, 1991, 2006, and 2016), we observe a steady **$55\%$ decline** in the mean frequency of the strong modal verb `must`, reflecting a cultural shift toward less direct expressions of obligation (e.g., *"You might like to do it"* rather than *"You must do it"*).
* **Corpus Size & Granularity:**
  * Corpora range from **tens of thousands** to **billions** of running words.
  * Ultimately, corpus size is a function of **granularity**: the more detailed or rare the linguistic phenomenon in your research question, the larger the sample you need.

---

### 1.2 Representativeness, Balance, and Sampling

Imagine the totality of a language as a large canvas painted with different shades of color representing genres, registers, and social contexts (dinner-table conversations, public lectures, TV shows, news articles, fiction, tweets, text messages). A corpus container moves across this canvas to sample each shade proportionally.

1. **Representativeness:** The ability of the sample (the corpus) to reflect the target population on a small scale in all crucial aspects relevant to the research questions.
2. **Balance:** Deciding which text types/registers to include and in what proportions (guided by existing corpus traditions for comparability, specific research questions, and the needs of the broader research community).
3. **Stratified Random Sampling:** Dividing the target language population into meaningful strata (e.g., regional, mass-market, and serious broadsheet newspapers) and randomly sampling texts within each stratum to avoid researcher bias.

---

### 1.3 Major Types of Corpora

| Corpus Type | Description | Example Corpus |
| :--- | :--- | :--- |
| **General Corpus** | Large reference corpus covering a wide range of spoken and written genres/registers to represent a whole language variety. | **British National Corpus 2014 (BNC 2014)** ($100\text{M}$ words: $90\%$ written, $10\%$ spoken) |
| **Specialised Corpus** | Smaller, targeted corpus focusing on a single genre, register, or situational context. | Academic English corpora (written or spoken), DIY newspaper corpora |
| **L2 / Learner Corpus** | Captures spoken or written production by second/additional language learners across proficiency levels. | **Trinity Lancaster Corpus** (L2 English); **Guangwai-Lancaster Corpus** (L2 Chinese) |
| **Historical / Diachronic Corpus** | Samples language across different historical periods to track linguistic and cultural change over time. | **The Times Corpus**, **Brown Family Corpora**, **EEBO** |
| **Parallel / Translation Corpus** | Contains original texts aligned with their translations across multiple languages for contrastive and translation studies. | Europarl, bilingual English–Russian / English–Chinese corpora |
| **Multimodal Corpus** | Synchronizes video, audio, and multi-tier transcriptions to capture gesture, gaze, and sign languages. | **British Sign Language (BSL) Corpus** |

---

## 🏗️ 2. Building Corpora: Design, Development, and Annotation

*Based on Lectures 4.3, 4.4, 4.5, 4.6, & 4.7 by Dr. Vaclav Brezina*

Lancaster University's approach to corpus building is illustrated through three flagship projects representing the three core stages of creation: **Design**, **Development**, and **Annotation**.

```
┌────────────────────────┐     ┌────────────────────────┐     ┌────────────────────────┐
│   1. CORPUS DESIGN     │ ──► │ 2. CORPUS DEVELOPMENT  │ ──► │ 3. CORPUS ANNOTATION   │
│  • Construct definition│     │  • Data collection     │     │  • Metadata headers    │
│  • Sampling frame      │     │  • Transcription (3 Cs)│     │  • POS & Semantic tags │
│  • Stratified sampling │     │  • Anonymization       │     │  • Error tagging (L2)  │
└────────────────────────┘     └────────────────────────┘     └────────────────────────┘
```

### 2.1 Corpus Design: The British National Corpus 2014 (BNC 2014)

The **BNC 2014** ($100\text{ million}$ words) is a contemporary update to the original **BNC 1994**. Its four-word title encapsulates its design operationalization:
* **British:** Sampled speakers across the UK for the spoken component and UK-based institutional/digital domains (e.g., British universities for academic prose, `.uk` discussion forums) for the written component.
* **National:** A general corpus spanning a comprehensive sampling frame of registers:
  * **Written ($90\%$):** Academic prose, newspapers (regional, mass-market, serious), magazines, fiction, e-language (forums, emails, blogs, social media), and other documents (government texts, TV scripts).
  * **Spoken ($10\%$):** $10\text{ million}$ words of informal, natural conversations.
* **Corpus:** Built via **stratified random sampling** across four primary collection channels:
  1. Web crawling
  2. Direct contributions from publishers
  3. Direct contributions from authors
  4. **Public Participation in Scientific Research (Citizen Science):** Volunteers recording their own everyday conversations and submitting them to the project.
* **2014:** Represents the mid-sampling point of the data collection window (**2010–2017**).

**Resulting Resources Extracted from the BNC 2014 Data Pool:**
1. **Spoken BNC 2014** ($10\text{M}$ words)
2. **Written BNC 2014** ($90\text{M}$ words)
3. **BNC 2014 Baby+** (A $5\text{-million-word}$ multi-genre sub-corpus designed for rapid, small-scale cross-register comparisons).

---

### 2.2 Corpus Development & Transcription: The Trinity Lancaster Corpus (TLC)

Developed jointly by **Trinity College London** (an international exam board) and **Lancaster University**, the **Trinity Lancaster Corpus** is the largest corpus of spoken L2 English, comprising over **$4\text{ million}$ running words**.

* **Data & Metadata Collection:** Every Monday, physical parcels arrived at Lancaster containing audio recordings of spoken exam tasks alongside background questionnaires capturing a strict **learner profile (metadata)**:
  * Country of origin, L2 proficiency level, gender, age, first language (L1), educational background, and length of exposure to English.
* **The Economics of Spoken Transcription:**
  * Transcribing spoken language is highly labor-intensive: **$1\text{ hour}$ of transcription work yields $\approx 1,500\text{ words}$** ($\approx 40,000\text{ words/week}$ or $1.5\text{ million words/year}$).
* **The "Three Cs" of Good Transcription Practice (Lancaster Transcription Guidelines):**
  1. **Capturing Speech Accurately:** Recording dialogic participant roles, overlapping speech, backchannels (*mm, yeah*), hesitations (*uh, um*), and short/long pauses, while fully **anonymizing** personal names and sensitive details.
  2. **Consistency:** Applying identical orthographic and markup rules across all transcribers and files.
  3. **Comparability:** Ensuring transcription conventions align with reference corpora such as the *Spoken BNC 2014*.
* **Machine-Readable XML & POS Tagging:** Final transcripts are encoded in **XML** (separating raw spoken text from color-coded speaker metadata headers) and automatically Part-of-Speech (POS) tagged.

---

### 2.3 Corpus Annotation: The Guangwai-Lancaster Corpus of L2 Chinese

The **Guangwai-Lancaster Corpus** is a $1.2\text{-million-word}$ corpus (spoken and written) of L2 Chinese produced by over **$1,400$ learners from $107$ countries** across **three proficiency levels**.

To investigate the specific developmental features and learner difficulties of L2 Chinese, the corpus is fully annotated using the **Guangwai-Lancaster Error Annotation Scheme**, which operates on two dimensions:

| Dimension 1: Linguistic Level (*Where* the error occurs) | Dimension 2: Error Type (*How* the error manifests) |
| :--- | :--- |
| • Orthography (Chinese character form)<br>• Punctuation<br>• Lexico-grammar<br>• Collocation<br>• Meaning / Semantics | • **Omission:** A required character/word is missing<br>• **Inclusion (Addition):** An extra word/character is inserted where it should not be<br>• **Irregular Construction:** Malformed grammatical structure<br>• **Word Order:** Incorrect syntactic sequence |

---

### 2.4 Five Golden Tips for Building Your Own Corpus

1. **Start with Corpus Design:** Decide early whether you need a general or specialized corpus and define the exact language variety your sample will represent.
2. **Keep Detailed Notes:** Document every inclusion/exclusion decision and sampling parameter immediately. You will need this methodological log months or years later when writing up your research.
3. **Save Texts as Separate Files:** Never dump all collected texts into one giant file. Saving each article or speaker transcript as an individual `.txt` file allows corpus tools to calculate **dispersion**, text-level frequencies, and metadata distributions.
4. **Always Check Data Accuracy:** For spoken corpora, re-listen to audio to verify transcriptions. For web-scraped written corpora, strip out stray **HTML tags** and repetitive website **boilerplate** (navigation menus, footers, ads).
5. **Select a Suitable Corpus Tool:** Choose software (such as `#LancsBox`) capable of indexing, annotating, and visualizing your specific corpus structure.

---

## 💻 3. Practical Lab 1: Building a DIY Corpus & Using the `Text` Tool in `#LancsBox`

*Based on Tutorials 4.8 & 4.9 by Dr. Vaclav Brezina*

### 3.1 How to Collect a Mini DIY Newspaper Corpus

You can build a specialized "Do-It-Yourself" (DIY) mini-corpus on any topic in five simple steps:

1. **Choose a Topic (Search Query):** e.g., `"teaching English"`, `"climate change"`, `"rugby"`, or `"healthy lifestyle"`.
2. **Select an Online Source:** e.g., *The Guardian*, *The Telegraph*, *New Zealand Herald*, or *China Daily*.
3. **Run a Site-Specific Search Engine Query:** In Google, Bing, or Baidu, use the `site:` operator to restrict results to your chosen newspaper:
   ```text
   "healthy lifestyle" site:guardian.co.uk
   ```
4. **Extract & Clean the Text:** Open 10 to 20 search results in separate browser tabs, highlight the main article text (avoiding sidebar ads and comments), copy (`Ctrl+C` / `Cmd+C`), and paste (`Ctrl+V` / `Cmd+V`) each article into a plain text editor (such as **Notepad++**).
5. **Save as UTF-8 Plain Text (`.txt`):**
   * Save each article as a separate `.txt` file.
   * Always select **UTF-8 (Unicode) encoding** so characters display properly across all operating systems and corpus tools.
   * Load the folder of `.txt` files directly into `#LancsBox` (where you can explore them with the **Text** and **Whelk** tools).

---

### 3.2 Exploring Files, Lexical Diversity, and Context in the `#LancsBox X` Text Tool

Using the **BNC 2014 v2** ($88,171$ files) as a demonstration, the **Text** tool provides both a macro file-level overview and a micro full-text reading view.

#### 1. File Overview & Lexical Diversity Metrics
When opening the **Text** tool, `#LancsBox X` displays a sortable table of every file in the corpus (sorted from largest to smallest token count by default) along with two robust measures of **lexical diversity**:
* **MATTR 50 (Moving-Average Type-Token Ratio, chunk size = 50):** Computes type-token ratio across a sliding 50-word window so lexical diversity is not distorted by text length.
* **MTLD (Measure of Textual Lexical Diversity):** Evaluates how many sequential words a text maintains above a given TTR threshold before resetting.
* **Metadata Integration:** Add metadata columns (such as `Genre`) to filter and sort files by extralinguistic variables.

#### 2. Searching Across Files & Interpreting the Visual Graph
* **File-Level Search (`technology`):** Searching for `technology` reveals that the word occurs at least once in **$5,194$ out of $88,171$ files**, adding **Frequency** and **Relative Frequency** columns to the table.
* **Graph Visualization:**
  * **Circle Size:** Proportional to file size (number of tokens).
  * **Circle Color:** Automatically mapped to the search term's **Relative Frequency** (from **Blue** = very low/zero relative frequency to **Red** = high relative frequency).
  * **Spatial Position:** Can be assigned to any column (e.g., sorting files from left to right by relative frequency).
  * *Performance Note for Large Corpora:* For corpora with tens of thousands of files, the graph defaults to plotting a **random sample of $1,000$ files** for speed. You can change the graph display setting from *Random* to **Relative Frequency Order** (Apply) to prioritize plotting the top files with the highest relative frequencies on the right side of the canvas.

#### 3. Full-Text View & Multi-Layer Annotation Inspection
* Double-clicking any file in the table or graph opens the **Full-Text View** with search hits highlighted in context, allowing you to read texts from start to finish and toggle **POS tags** and **Semantic tags** directly on the words (note: copyright-restricted texts replace restricted spans with dashes `---`).

---

## 🏷️ 4. Practical Lab 2: Semantic Annotation with the USAS Web Tagger & `PyMUSAS`

*Based on Tutorial 4.11 by Prof. Paul Rayson (Director of UCREL, Lancaster University)*

The **UCREL Semantic Analysis System (USAS)** is an automatic semantic tagger that adds a layer of semantic field annotation on top of Part-of-Speech (POS) tagging.

### 4.1 Architecture of the USAS Taxonomy

First developed for English in 1990 and continuously updated, USAS assigns every word or multi-word expression (MWE) in running text to a hierarchical semantic taxonomy:
* **21 Major Discourse Domains** (labeled with letters `A` through `Z`), subdivided into **$232$ fine-grained semantic category tags**.
* **Granularity:** More general than a thesaurus, but coarser than fine-grained dictionary word senses.
  * *Example (`bank`):* Disambiguates between **Money & Commerce** (`I1`), **Geographical terms / Mound of earth** (`W3`), and **Movement / Turning an aeroplane** (`M1`), without trying to distinguish whether a financial bank refers to the corporate institution or a high-street branch building.

| USAS Code | Top-Level Semantic Domain | USAS Code | Top-Level Semantic Domain |
| :---: | :--- | :---: | :--- |
| **A** | General and abstract terms | **M** | Movement, location, travel and transport |
| **B** | The body and the individual | **N** | Numbers and measurement |
| **C** | Arts and crafts | **O** | Substances, materials, objects and equipment |
| **E** | Emotional actions, states and processes | **P** | Education |
| **F** | Food and farming | **Q** | Language and communication |
| **G** | Government and public | **S** | Social actions, states and processes |
| **H** | Architecture, housing and the home | **T** | Time |
| **I** | Money and commerce in industry | **W** | World and environment |
| **K** | Entertainment, sports and games | **X** | Psychological actions, states and processes |
| **L** | Life and living things | **Y** | Science and technology |
| | | **Z** | Names and grammatical words |

### 4.2 Knowledge-Based Lexicons & Multi-Word Expressions (MWEs)

* **Manually Curated Lexicon (English):** Contains over **$56,000$ single words** and nearly **$19,000$ multi-word expressions (MWEs)**.
* **Why MWEs Matter:** Roughly **$16\%$ of running text** in a large English corpus consists of MWEs that must be tagged as a single semantic unit:
  * *Idioms:* `living the life of Riley`
  * *Noun phrases:* `riding boots`
  * *Phrasal verbs:* `stubbed out`
  * *Proper names:* `United States of America`
* **Hybrid Disambiguation ($\approx 91\text{–}92\%$ Accuracy):** Combines POS tagging (CLAWS), auxiliary verb detection, sense frequency ranking, and text domain promotion.
* **Multilingual Support & `PyMUSAS`:** Extended via bootstrapping and manual checking to **Finnish, Russian, Italian, Chinese, Portuguese, Dutch, French, Spanish, Indonesian, Welsh, Arabic, and Urdu**. Available as a web tagger, inside **Wmatrix**, or as an open-source `pip`-installable Python library (**`PyMUSAS`**).

### 4.3 Interpreting USAS Web Tagger Output

**Example Input Sentence:**
> *"Work is expected to start for the road next year."*

1. **Vertical Output Format:** Lists each token alongside its POS tag and ranked candidate semantic tags (most likely first):
   * `Work` $\rightarrow$ **`I3.1`** (*Work and employment*)
   * `is` $\rightarrow$ **`Z5`** (*Grammatical bin*, because it functions here as an auxiliary verb rather than a main verb `A3+` *Being*)
   * `start` $\rightarrow$ **`T2+`** (*Time: Beginning*)
   * `road` $\rightarrow$ **`M3`** (*Movement/transportation on land*)
   * `next year` $\rightarrow$ Bracketed as a 2-word MWE and tagged **`T1.1.3`** (*Time: General future*), overriding the single-word tag for `year` (`T3` *Time period*).
2. **Horizontal Output Format:** Joins only the single highest-probability semantic tag to each word with an underscore (`Work_I3.1`), ready for import into standard concordancers.
3. **XML Output Format:** Wraps POS and semantic labels inside structured XML attributes.

---

## 🎙️ 5. Expert Conversations: Multimodal, Historical, Spoken, and Computational Corpora

### 5.1 In Conversation with Dr. Kearsy Cormier: The British Sign Language (BSL) Corpus & Multimodal Data

*Based on Video 4.19 — Dr. Vaclav Brezina interviews Dr. Kearsy Cormier (Deafness, Cognition and Language Research Centre [DCAL], University College London)*

* **About British Sign Language (BSL):**
  * The preferred indigenous sign language of approximately **$50,000\text{ to }70,000$ Deaf people** in the UK.
  * Because roughly **$95\%$ of Deaf signers are born to hearing families** who do not sign, age of acquisition and early language input vary dramatically. Furthermore, regional **Deaf schools** historically fostered distinct regional "schoolects" (school-based dialects).
* **Design of the BSL Corpus:**
  * Samples **$249$ Deaf signers** across **$8$ UK regions**, balanced for age, gender, and language background (native vs. non-native signers).
  * Captures four task types: **free conversation, personal narratives, language attitude interviews, and lexical elicitation**.
* **Key Research Findings from the BSL Corpus:**
  1. **Lexical Frequency:** Annotated $25,000$ sign tokens to establish the first empirical frequency list of BSL signs.
  2. **Phonological Variation:** Tracked how citation `1`-handshape signs (e.g., `THINK`, `WHAT`, `TELL`) vary across social groups.
  3. **Lexical Variation:** Documented far more regional variation in colors, countries, numbers, and UK place names than any prior BSL dictionary (e.g., over **$20$ distinct signs for the color `purple`** across 244 signers).
* **Technical Challenges & Tools (`ELAN`):**
  * Because sign languages have no standard writing system, the entire corpus consists of **digital video** annotated in **ELAN** (free multimedia annotation software developed by the Max Planck Institute for Psycholinguistics in Nijmegen).
* **Computational Applications & Multimodality:**
  * Annotated video corpora train **automatic sign language recognition** systems and **signing avatars**, which in turn can help semi-automate future corpus annotation.
  * Highlights that face-to-face human language is inherently **multimodal**: comparing sign languages to audio-only speech makes them look radically different, whereas comparing sign languages to multimodal face-to-face spoken corpora (including co-speech gesture and gaze) reveals deep structural parallels.

---

### 5.2 In Conversation with Dr. Alistair Baron: Spelling Variation, Normalization, and VARD

*Based on Video 4.20 — Prof. Tony McEnery interviews Dr. Alistair Baron (School of Computing and Communications, Lancaster University)*

* **Why Historical and Digital Spelling Variation Matters:**
  * In Early Modern English (**1500–1700**, before standardized dictionaries in the 17th century), there was no concept of a single "correct" spelling; typesetters routinely added letters (such as a final `-e`) simply to right-justify a line of print, or swapped `v/u`, `y/i`, and `vv/w`.
  * Similarly, modern **user-generated digital texts** (Twitter/social media, blogs) intentionally vary spelling to express emotion (e.g., `pleeeeeeease`) or mix British/American conventions.
* **How Spelling Variation Distorts Corpus Analysis:**
  1. **Incomplete Concordance Searches:** Searching for `witch` misses `wych`, `wytch`, `witche`, `vvitch`, etc.
  2. **Fragmented Frequency & Keyword Lists:** A word's true frequency is split across 10–15 spelling variants, preventing it from surfacing as a statistically significant keyword and skewing diachronic studies (since spelling variation drops sharply after 1700).
  3. **Broken POS & Semantic Tagging:** Lexicon-based taggers (CLAWS, USAS) fail when encountering unrecognized historical word forms.
* **The Solution: VARD (*Variant Detector*):**
  * A pre-processing tool (`ucrel.lancs.ac.uk/vard`) that detects words absent from a modern lexicon and normalizes them using a hybrid of:
    * **Modified Soundex (Phonetic Matching):** Recognizes that initial `kn-` sounds like `n-`.
    * **Letter Replacement & Contextual Rules:** e.g., replacing `v` with `u` at the start of a word, or `y` with `i` after `h`/`w`, or stripping/adding final `-e` and Unicode characters like the **long s (`ſ`)**.
    * **Interactive Machine Learning:** An expert manually normalizes a small training sample from a specific period/genre, and VARD learns the optimal weighting of rules for that text.
  * **Preserving Original Forms via XML:** VARD never destroys historical evidence. It outputs XML tags where the normalized form is visible to POS taggers while the original spelling is preserved as an attribute (e.g., `<normalised orig="wytche">witch</normalised>`).
* **Evaluating Performance: Precision vs. Recall (on 1+ Billion Words of EEBO):**
  * **Precision:** Out of all normalizations the tool *makes*, what percentage are correct? (Typically $>98\%$ on tuned samples; $\approx 80\%$ on massive automated runs).
  * **Recall:** Out of all variant spellings *actually present in the text*, what percentage did the tool successfully find and normalize? (Typically $\approx 70\%$ on **Early English Books Online [EEBO]**, comprising over $1\text{ billion}$ words from c. 1470–1700).
  * *Worked Example:* If a 100-word text has **10** true variants, and VARD flags **5** of them and normalizes **4** correctly (Wait: if it spots 5 out of 10 = $50\%$ detection/recall, and gets 4 of those 5 right = $80\%$ precision).

---

### 5.3 In Conversation with Dr. Vaclav Brezina: DIY vs. Public Corpora, Spoken Data Ethics, and the BNC 64

*Based on Video 4.21 — Prof. Tony McEnery interviews Dr. Vaclav Brezina (CASS, Lancaster University)*

* **DIY Corpora vs. Public Corpora:**
  * **DIY Corpora:** Built rapidly for a single research question (e.g., scraping newspaper articles and **online reader comment sections** to study audience reception and the blurring of spoken/written registers online).
  * **Public Corpora ("Build for yourself with others in mind"):** Designed so future researchers can investigate questions the original compiler never anticipated. Examples built by Brezina include:
    1. **New Zealand Academic Speech Corpus:** Recorded one-to-one student–supervisor consultations across disciplines during his PhD.
    2. **The BNC 64 Corpus:** Repurposed from the $4.2\text{M}$ words of informal dinner-table conversations in the BNC spoken component—selecting **$64$ speakers** ($32\text{ male}$, $32\text{ female}$) balanced across gender, age, socioeconomic status, and UK geographic regions to test popular "Men are from Mars, Women are from Venus" myths against empirical data.
* **Challenges in Spoken Corpus Building:**
  1. **Technical & Transcription Conventions:** Deciding how to standardize hesitation fillers (`er`, `erm`, `uh`, `um`) and meaningful silences/pauses so the corpus remains comparable with other spoken corpora.
  2. **Ethics & Recruitment:** Surreptitious recording (hiding a tape recorder) is unethical and illegal; researchers must obtain informed consent. To recruit non-linguists (e.g., engineers and biologists in New Zealand), Brezina used **sociological snowball sampling** and **reciprocity (*quid pro quo*)**—participating in their lab experiments in exchange for recording their academic supervisions.
  3. **Managing Media Misinterpretation:** When Brezina & Gablasova published the **New General Service List (New GSL)**, tabloid media sensationalized minor findings; researchers can counter media spin by publishing accessible public blog posts explaining the true data.

---

### 5.4 In Conversation with Prof. Paul Rayson: CLAWS, USAS, Wmatrix, and Real-World NLP Applications

*Based on Video 4.22 — Prof. Tony McEnery interviews Prof. Paul Rayson (School of Computing and Communications, Lancaster University)*

* **The Synergy of Corpus & Computational Linguistics:**
  * Corpus linguists manually annotate training data (such as the original **9-track magnetic tape reel of the POS-tagged Brown Corpus** mailed from Brown University to Lancaster in the mid-1970s), which computer scientists use to train probabilistic and rule-based taggers:
    * **Unigram baseline** (guessing a word's most frequent tag) achieves $\approx 90\%$ accuracy.
    * Adding **tag transition probabilities** (e.g., probability of `Article` $\rightarrow$ `Adjective` vs. `Noun`) and **context rules** pushes **CLAWS** POS tagging to $\approx 97\%$ and **USAS** semantic tagging to $\approx 92\%$.
  * Using POS tags first filters out impossible semantic senses (e.g., knowing `spring` is tagged as a *verb* immediately rules out the *metal coil* and *river source* noun meanings).
  * Cross-linguistic adaptation requires language-specific modules (e.g., building a **compound-splitting engine** for **Finnish** in the late-1990s *Benedict* electronic dictionary project).
* **Four High-Impact Practical Applications of Wmatrix & USAS:**
  1. **Software Engineering & Legacy Systems:** Using **Wmatrix** (which applies **keyness statistics to semantic domains** rather than just words) to rapidly gist massive documentation for legacy air-traffic control software written in COBOL/Fortran when the original programmers have retired.
  2. **Healthcare Communication:** Identifying dominant metaphors in **end-of-life care** (with Prof. Elena Semino) by extracting key semantic domains.
  3. **Market Research & Social Science Surveys:** Automatically analyzing thousands of open-ended interview transcripts and free-text survey responses (where researchers previously only analyzed tick-box numbers and cherry-picked free text).
  4. **Online Child Protection ("Frequency Fingerprints"):** Combining word, POS, stylistic, and semantic frequency profiles in online chat rooms to detect **ghosting/masquerading** (an adult posing as a child), identifying whether a user is an adult or child and male or female with **$94\%$ accuracy** to assist law enforcement.
* **The Cyclical Research Workflow:** Distant reading via key semantic domains in Wmatrix is never a replacement for reading the text; it is an entry point in a **cyclical workflow** that guides the analyst back into close reading of relevant text passages.

---

## 📖 6. References & Resources

* **Baron, A., & Rayson, P. (2008).** *VARD 2: A tool for dealing with spelling variation in historical corpora*. Proceedings of the Postgraduate Conference in Corpus Linguistics, Aston University.
* **Brezina, V., & Gablasova, D. (2015).** *Is there a core general vocabulary? Introducing the New General Service List*. Applied Linguistics, 36(1), 1–22.
* **Cormier, K., Fenlon, J., Johnston, T., Rentelis, R., Schembri, A., Rowley, K., Adam, R., & Woll, B. (2012).** *From corpus to lexical database to online dictionary: Issues in annotation of the BSL Corpus and the development of BSL SignBank*. Proceedings of LREC.
* **Gablasova, D., Brezina, V., & McEnery, T. (2019).** *The Trinity Lancaster Corpus: Development, description and application*. International Journal of Corpus Linguistics, 24(2), 134–162.
* **Love, R., Dembry, C., Hardie, A., Brezina, V., & McEnery, T. (2017).** *The Spoken BNC2014: Designing and building a spoken corpus of everyday conversations*. International Journal of Corpus Linguistics, 22(3), 319–344.
* **Rayson, P. (2008).** *From key words to key semantic domains*. International Journal of Corpus Linguistics, 13(4), 519–549.
* **Tools & Project Links Mentioned in Week 4:**
  * **#LancsBox:** [corpora.lancs.ac.uk/lancsbox](http://corpora.lancs.ac.uk/lancsbox/)
  * **UCREL & USAS Semantic Tagger / PyMUSAS:** [ucrel.lancs.ac.uk](https://ucrel.lancs.ac.uk/)
  * **VARD (Variant Detector):** [ucrel.lancs.ac.uk/vard](https://ucrel.lancs.ac.uk/vard/)
  * **ELAN Multimedia Annotator:** [archive.mpi.nl/tla/elan](https://archive.mpi.nl/tla/elan)
  * **BSL Corpus Project:** [bslcorpusproject.org](https://bslcorpusproject.org/)
