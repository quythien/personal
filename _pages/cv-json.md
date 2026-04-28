---
layout: archive
title: ""
permalink: /cv-json/
author_profile: true
redirect_from:
  - /resume-json
---
{% include base_path %}

<link rel="stylesheet" href="{{ base_path }}/assets/css/cv-style.css">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">

<style>
  .archive {
    width: 80%;
    margin: 0 auto;
    float: none;
    padding-right: 0;
  }

  @media (min-width: 80em) {
    .archive {
      width: 70%;
    }
  }

  .cv-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 1rem;
  }

  .cv-download-links .btn {
    margin-left: 1rem;
    white-space: nowrap;
  }
</style>

<div class="cv-header">
  <h1>Curriculum Vitae</h1>
  <div class="cv-download-links">
    <a href="{{ base_path }}/files/cv.pdf" class="btn btn--primary">Download CV as PDF</a>
  </div>
</div>

## Education

* **Ph.D. Candidate in Biostatistics**, University of Pittsburgh (Aug 2021 – Dec 2026, GPA: 3.85)
* **B.S. in Statistics & B.S. in Mathematics**, University of North Carolina at Chapel Hill (Sep 2017 – May 2021, GPA: 3.85)
  * Highest Distinction. Honors: Phi Beta Kappa, Dean's List

## Skills

* **Programming**: R, R Shiny, Python, STATA, SQL, Bash (proficient); Java, C++, SAS (familiar)
* **Statistical & ML**: Statistical inference, optimization & stochastic models, Bayesian statistics, causal inference, clinical trials, deep learning (PyTorch), classical ML (scikit-learn)
* **Research**: Biomarker detection in high-dimensional omics data, longitudinal & correlated-data analysis, generative models for multimodal data integration
* **Tools & Pipelines**: STAR, Hisat2, Scanpy, Seurat, PyTorch Geometric, AWS, high-throughput computing

## Professional Experience

* **Senior Statistician Intern**, Otsuka America Pharmaceutical (May 2025 – Aug 2025)
  - Built an internal SAS pipeline for Bayesian meta-analysis using shared-parameter models with simulation, supporting Phase 3 efficacy analysis of sibeprenlimab in IgA nephropathy
  - Evaluated urinary protein as a surrogate endpoint via mixed-effects and survival modeling
  - Conducted a systematic literature review and applied MNAR multiple imputation with sensitivity analyses for a brexpiprazole + sertraline PTSD trial

* **Graduate Research Assistant — UPMC, Multi-omics Bioinformatics & Bayesian Lab**, University of Pittsburgh (Aug 2021 – Present)
  - Hierarchical Bayesian and ML models (XGBoost, Random Forest, unsupervised clustering) for novel cross-species concordance metrics in high-dimensional omics
  - Evaluated circadian biomarkers from multi-omics data in early-phase oncology trials, assessing sex- and condition-specific effects across brain regions and tissues
  - Streamlined RNA-seq, single-cell RNA-seq, and proteomics preprocessing pipelines (STAR, Hisat2)
  - Integrated multi-modal single-cell data using deep learning (PyTorch) and probabilistic models with domain adaptation
  - Applied SmCCNet (phenotype-guided sparse multi-CCA) to integrate DNA methylation (450K/EPIC), RNA-seq, and proteomics with cis-eQTM mapping (±1 Mb) for cross-omics modules
  - Designed graph-based ML models in PyTorch Geometric to infer gene–disease causal relationships

* **Graduate Research Assistant — Department of Infectious Disease**, University of Pittsburgh (Aug 2023 – Present)
  - Mixed-effect models and GEE for clinical-trial data, deriving insights to improve HIV treatment adherence and quality of life among women industrial-zone workers
  - Longitudinal mediation models estimating short-term causal effects of dry needling, identifying pain reduction as a mediator of disability outcomes

* **Undergraduate Research Assistant**, Carolina Center for Neurostimulation, Chapel Hill, NC (Aug 2019 – Dec 2019)
  - Investigated thalamus–cortex synchrony using Python and MATLAB to advance brain-stimulation modeling

* **Research Assistant Intern**, Hill-Rom, Cary, NC (Jun 2020 – Aug 2020)
  - Conducted exploratory analyses and literature review for ML models predicting pediatric sepsis in ICU settings

## Other Projects

* **Phoneme recognition (deep learning)**: CNN/RNN models with VAEs and efficient sampling to improve audio-text alignment
* **Diffusion models**: DDIM, VAE, and EMA on ImageNet-100, exploring class-specific performance on reduced-class subsets

## Publications

<ul>
  {% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}
</ul>

## Teaching Experience

* **University of Pittsburgh — Department of Biostatistics**
  - BIOST 2086: Mixed Models (Spring 2024)
  - BIOST 2050: Longitudinal and Clustered Data Analysis (Fall 2023)
  - BIOST 2041: Introduction to Statistical Methods (Spring 2022)
  - BIOST 2038: Foundation of Statistical Theory (Fall 2021, Fall 2022)

* **University of Pittsburgh — Institute for Clinical Research Education**
  - CLRES 2020: Biostatistics (Summer 2022, Summer 2024)
  - CLRES 2005: Computational Methods for Clinical Research (Summer 2022, Summer 2024)

* **UNC–Chapel Hill — Department of Mathematics**
  - MATH 547: Linear Algebra (Fall 2019)

## Awards

* Travel Funding Award — STATGEN Conference (2025)
* Biostatistics Dean's Day Doctoral Award (2025)
* Outstanding Teaching Assistant (TA) Award (2025)
* Phi Beta Kappa, top 1%, UNC–Chapel Hill (2021)
* International Championship of Collegiate A Cappella — Semi-finalist, 2nd place (2019, 2020)
* Outstanding Student Scholarship, top 1%, Pham Ngoc Thach University of Medicine (2015, 2016)
* Excellent Student at City Level in Biology, 2nd place (2011, 2013, 2014)

## Leadership & Membership

* American Statistical Association — Pittsburgh Chapter, Member (2021–Present)
* Pittsburgh Men's Glee Club, Member (2023–Present)
* Tar Heel Voices (UNC co-ed a cappella), Fundraising Committee (2019–2021)
* Pham Ngoc Thach University of Medicine, Class President (2014–2016)
