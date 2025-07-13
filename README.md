# ZaQQ
ZaQQ: A Novel Automatic Arabic Essay Scoring Dataset


# ZaQQ: A Novel Automatic Arabic Essay Scoring Dataset

This repository contains the `ZaQQ` dataset, a novel resource for Automated Essay Scoring (AES) in Arabic. `ZaQQ` is designed to address the critical scarcity of labeled Arabic essay datasets, leveraging a human-AI collaboration framework to generate multidimensional assessments across seven writing criteria: Relevance, Organization, Vocabulary, Style, Development, Mechanics, and Structure.

## Dataset Overview

`ZaQQ` is an expanded dataset built upon existing Arabic essay collections, `QCAW` (It contais essays, and `QAES` the trait results for QCAW), `ZAEBUC` and QALB, by applying a systematic LLM-based annotation framework. The goal is to provide a comprehensive and high-quality resource for developing robust Arabic AES systems.

### Writing Criteria

The essays in `ZaQQ` are scored across the following seven traits, each on a scale of 1-5 (except Relevance, which is 1-2):

1.  **Relevance (REL):** How well the essay addresses the prompt/topic.
2.  **Organization (ORG):** The logical structure and coherence of the essay.
3.  **Vocabulary (VOC):** The richness, appropriateness, and accuracy of word choice.
4.  **Style (STY):** The clarity, fluency, and overall writing voice.
5.  **Development (DEV):** The depth and elaboration of ideas and arguments.
6.  **Mechanics (MEC):** Grammatical correctness, spelling, and punctuation.
7.  **Structure (GRA/STR):** Sentence structure and overall composition.

## Data Sources

The `ZaQQ` dataset is an augmentation of the following publicly available Arabic essay datasets:

### 1. QCAW/QAES

* **Description:** The QCAW (Qatari Corpus of Argumentative Writing) contains the raw essay texts. QAES refers to the trait-specific scoring results that were generated for these QCAW essays. This dataset, comprising QCAW essays and their QAES scores, is the first trait-specific Arabic dataset with multi-layer annotations and includes detailed analytical scoring rubrics.
* **Reference:**
    * Zaghouani, W.; Ahmed, A.; Zhang, X.; Rezk, L. QCAW 1.0: Building a Qatari Corpus of Student Argumentative Writing. In *Proceedings of the 2024 Joint International Conference on Computational Linguistics, Language Resources and Evaluation (LREC-COLING 2024)*; Torino, Italia, May 2024; pp. 13382–13394.
    * Bashendy, M.; Albatarni, S.; Eltanbouly, S.; Zahran, E.; Elhuseyin, H.; Elsayed, T.; Massoud, W.; Bouamor, H. QAES: First Publicly-Available Trait-Specific Annotations for Automated Scoring of Arabic Essays. In *Proceedings of ARABICNLP*; 2024.
* **QAES Link:** https://gitlab.com/bigirqu/qaes
* **QCAW Link:** https://catalog.ldc.upenn.edu/LDC2022T04

### 2. ZAEBUC

* **Description:** The ZAEBUC dataset offers a bilingual Arabic-English approach with CEFR proficiency labels and includes valuable writer metadata. It is particularly useful for cross-lingual transfer learning studies.
* **Reference:** Habash, N.; Palfreyman, D. M. ZAEBUC: An Annotated Arabic-English Bilingual Writer Corpus. In *Proceedings of the International Conference on Language Resources and Evaluation*; 2022.
* **Link:** https://sites.google.com/view/zaebuc/home

### 3. QALB Corpus

* **Description:** The second QALB Corpus (2015) primarily focuses on grammatical error correction and categorizes detailed error types. For `ZaQQ`, topics were generated for this dataset to enable trait-based assessment.
* **Note:** We removed 8 redundunt essays from 622 essays as they were too small.
* **Reference:**Rozovskaya, Alla, Houda Bouamor, Nizar Habash, Wajdi Zaghouani, Ossama Obeid, and Behrang Mohit. "The second qalb shared task on automatic text correction for Arabic." In Proceedings of the Second workshop on Arabic natural language processing, pp. 26-35. 2015.

Zaghouani, Wajdi, Nizar Habash, Houda Bouamor, Alla Rozovskaya, Behrang Mohit, Abeer Heider, and Kemal Oflazer. "Correction annotation for non-native Arabic texts: Guidelines and corpus." In Proceedings of The 9th Linguistic Annotation Workshop, pp. 129-139. 2015.
* **Link:** https://camel.abudhabi.nyu.edu/qalb-shared-task-2015/

## `ZaQQ` Dataset Content

The `ZaQQ.csv` file, provided alongside this README, contains the expanded and annotated Arabic essays. Each entry includes:

* The original essay information; metadata from the orignal datasets (ZAEBUC, QALB) so you can merge each essay from orignal dataset to its result in our dataset.
* The automatically generated scores for each of the seven writing traits.
* The generated topics for QALB essays.

The `Dataset_Sample.xlsx` file, provided alongside this README, contains sample data from the three datasets used:

* **QAES & QCAW**: publicly available  
* **QALB**: essays are from the dataset; topics and scores taken from ZaQQ  
* **ZAEBUC**: essays and topics are from the dataset; scores taken from ZaQQ

