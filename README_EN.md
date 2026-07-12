# Pharmacogenetics Health Education Analysis
![UFMG](https://img.shields.io/badge/INSTITUTION-UFMG-B20000?style=for-the-badge&logo=school)
![Focus](https://img.shields.io/badge/FOCUS-PHARMACOGENETICS-blue?style=for-the-badge&logo=dna)
![Status](https://img.shields.io/badge/STATUS-ACTIVE%20RESEARCH%20PROJECT-orange?style=for-the-badge)

> **Data-driven analysis of pharmacogenetics education impact. | Projeto de análise de dados e impacto educacional em farmacogenética para estudantes da área da saúde (UFMG).**

🇧🇷 *[Leia em Português](README.md)*

---

## ⌛ Project Status
> **Nursing (2026/1) ✅**
> *Pre-intervention survey, Discussion Group (DG), post-intervention data collection, and comparative analysis successfully completed.*
>
> **Biomedicine (2026/1) ✅**
> *Pre and post-intervention data collection completed. The intervention consisted solely of an Expository Lecture (no DG), serving as a methodological control group for the other cohorts.*
>
> **Pharmacy (2026/1) 🔍**
> *Baseline data collection and diagnostic analysis completed. The results demonstrated the need for the intervention, and the full implementation (Lecture + DG) with a new cohort has been scheduled for the 2026/2 cycle.*

---

This project aims to evaluate health sciences students' knowledge of pharmacogenetics and measure the impact of educational interventions based on clinical data, utilizing a structured approach to data analysis and descriptive statistics.

## 📌 Objective
To identify and analyze data-driven gaps in academic education regarding genetics and pharmacogenetics, quantitatively assessing whether an educational intervention improves students' understanding of patient safety and clinical decision-making.

## ⚠️ The Problem (Literature-Based)
Recent studies indicate that the gap in precision medicine education is not an isolated issue, but a systemic flaw in the training of the entire multidisciplinary healthcare team. Nurses, pharmacists, and other professionals show low confidence when interpreting genetic tests and applying pharmacogenetics in clinical practice. Traditional academic curricula still offer limited preparation for handling this information, directly impacting the prevention of adverse drug reactions and patient safety.

> *Source: Bibliographic review of 17 scientific articles ([see /docs folder](./docs)).*

## 🏆 Key Findings (Data Insights - Phase 1: Nursing)
Data extraction and analysis following the full educational intervention (Lecture + DG) revealed a clear breakdown of common misconceptions and high retention of patient safety practices:

* **Debunking the Package Insert Myth:** Full agreement that "strictly following the package insert prevents intoxication" dropped drastically, shifting to **48.3%** disagreement post-intervention.
![Package Insert Myth](./plots/enfermagem/pos/01_mito_bula.png)

* **Paradigm Shift (Allergy vs. Metabolism):** The initial assumption that severe reactions upon the first dose are always "allergies" was reversed, with the majority of the class disagreeing with this premise after the educational intervention.
![Allergy vs. Metabolism](./plots/enfermagem/pos/04_alergia_ou_metabolismo.png)

* **Practical Clinical Retention:** **100%** of students correctly identified the fatal risk of overdose in the practical case of Codeine ultrarapid metabolism (CYP2D6), and **93.1%** chose the correct clinical action of drastically reducing the dose in the TPMT case.
<p>
  <img src="./plots/enfermagem/pos/07_pos_caso_codeina.png" width="45%" />
  <img src="./plots/enfermagem/pos/08_pos_caso_tpmt.png" width="45%" />
</p>

## 🏆 Key Findings (Data Insights - Phase 2: Biomedicine)
For the biomedicine cohort, the intervention was delivered exclusively through a **Theoretical Lecture** on pharmacogenetics, without the practical Discussion Group (DG). The data showed that the lecture alone had a massive statistical impact on correcting conceptual errors:

* **The End of the "Fence-Sitting" Wall:** At baseline, **38.9%** of the Biomedicine class chose "Neutral" when asked if intoxications were always allergies. Following the lecture, indecision plummeted to **0%**, with the vast majority (**70.6%**) shifting to total disagreement.
 ![Allergy vs. Metabolism](./plots/biomedicina/pos/04_alergia_ou_metabolismo.png)

* **Eradicating the Package Insert Myth:** Reliance on the common belief that the "standard dose is safe for everyone" was eliminated. The cohort shifted from scattered responses to a solid **82.4%** block of total disagreement post-intervention.
  ![Package Insert Myth](./plots/biomedicina/pos/01_mito_bula.png)
  
* **Professional Empowerment:** Total disagreement that genetic risks are the "exclusive responsibility of the medical team" jumped from **72.2%** to **94.1%**, solidifying the biomedical scientists' understanding of their technical responsibility in laboratory reporting.
   ![Biomedic Role](./plots/biomedicina/pos/02_responsabilidade_biomedicina.png)

### 📊 Diagnosis & Baseline (Pharmacy)
The initial analysis of the Pharmacy cohort served as an essential diagnostic tool for our project. The data highlighted a curious finding: while students perform exceptionally well in basic theory (100% accuracy on the definition of pharmacogenetics), the class remains divided when applying this clinical reasoning to an "Allergy vs. Metabolism" scenario.

Furthermore, **65.2%** of the students relied heavily on common assumptions regarding the "Package Insert Myth" before receiving any intervention. This result provides practical proof of the need to expand lectures and discussion groups for future pharmacists in upcoming semesters.
<p>
  <img src="./plots/farmacia/pre/q6_conceito_farmacogenetica_PRE.png" width="45%" />
  <img src="./plots/farmacia/pre/q4_alergia_metabolismo_PRE.png" width="45%" />
</p>

## 🛠️ Tech Stack & Tools
This project relies on data-driven statistical programming to extract insights directly from the surveys:
* **Data Collection:** Google Forms (Structured questionnaires using Likert scales).
* **Core Language:** `R`
* **Data Cleaning & Manipulation:** `dplyr` / `tidyr` (`tidyverse` package ecosystem for dataset merging, variable renaming, and factor labeling).
* **Data Visualization:** `ggplot2` (Generation of static comparative charts focused on healthcare storytelling, with automated exporting via `ggsave` at 300 DPI).

## 📕 Methodology
The project follows an educational data analysis workflow composed of the following stages:
1. **Literature Review:** Analysis of scientific literature to identify knowledge gaps in genetics and pharmacogenetics among healthcare students and professionals.
2. **Baseline Data Collection:** A structured survey administered prior to the intervention to map students' prior knowledge.
3. **Educational Intervention (Lecture + DG):** An expository lecture delivered by the lead professor covering the fundamentals of pharmacogenetics. For the Nursing cohort, the lecture was followed by a Discussion Group (DG) focused on solving real clinical cases. The Biomedicine cohort received only the theoretical lecture (control group), and the Pharmacy cohort participated in the initial diagnostic phase of the research.
4. **Post-Intervention Collection:** A follow-up survey for response pairing, administered after the educational intervention was completed.
5. **Impact Analysis:** Execution of a unified R script to clean, cross-reference, and generate visualizations to evaluate shifts in the cohorts' clinical reasoning.

## 🧱 Repository Structure
* [**`/docs`**](./docs): Literature review, article excerpts, and intervention planning documents.
* [**`/data`**](./data): Anonymized `.csv` datasets categorized by academic major.
* [**`/scripts`**](./scripts): Full `R` code containing the unified ETL pipeline and chart generation scripts.
* [**`/plots`**](./plots): High-resolution exported graphics organized by research phase.

## 🚀 Next Steps

1. Refine and improve the questionnaire based on the insights and challenges identified during this first cycle.
2. Implement the full educational intervention (Lecture + DG) with a new Pharmacy cohort.
3. Run the R script to analyze pre- and post-intervention data for Pharmacy, evaluating the cohort's progress.
4. Cross-reference results across all three majors to evaluate how the Discussion Group impacts learning compared to the theoretical lecture alone.
5. Collect data from new Nursing and Biomedicine cohorts using the same intervention methodology.

## ▶️ How to Run the Analysis (Total Portability)
This project was developed to be completely automated and structured. To ensure relative file paths work on your local machine without altering a single line of code, follow standard professional practices for R projects:

### 1. Download the Full Project
Instead of downloading individual files, download the entire repository structure to keep the pipeline intact:
* Click the green **Code** button at the top of this page and select **Download ZIP** (then extract the folder on your computer).

### 2. Open the Project in RStudio
Open RStudio. In the top menu, go to File > New Project > Existing Directory.
Click Browse, navigate to the extracted project folder, and click Create Project.

### 3. Run the Script Automatically
In the RStudio files pane, open the `/scripts` folder and select the script corresponding to the course you want to analyze (e.g., `05_pre_biomedicina.R`).
Ensure the corresponding `.csv` dataset is located inside the `/data` folder.

Press Ctrl + A (Cmd + A on Mac) to select the entire code and click Run (or use the shortcut Ctrl + Enter).
The pipeline will autonomously execute the entire workflow:

- Import and cleaning of raw data (ETL);
- Variable standardization and Likert scale factoring;
- Automated exporting of high-resolution charts via `ggsave()`.

### Notes on Reproducibility & Scalability
- Consistent Framework: The scripts maintain the exact same statistical logic, altering only specific titles and phrasing tailored to the competencies of each professional field.
- Zero Code Alteration Required: If new cohorts or datasets are added to the project, you do not need to modify the core code logic. Simply replace the old file in the `/data` folder with a new `.csv` file bearing the exact same name and re-run the script. The entire downstream pipeline will execute seamlessly.
  
---
*Extension Project - UFMG 2025/26*

---

**By Inácio Vieira** *Nursing Student at Federal University of Minas Gerais (UFMG) | Entering Healthcare Data Analytics* [LinkedIn](https://www.linkedin.com/in/inaciosantosvieira/)
**Faculty Advisor:** Prof. Marcelo Rizzatti Luizon [Lattes](http://lattes.cnpq.br/1264026443614775)
