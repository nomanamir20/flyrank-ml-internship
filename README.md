# FlyRank ML Internship — Applied Search Intelligence

**Content Decline Prioritization and Search Discoverability**

This repository contains my work for the FlyRank ML Internship. The project explores how machine learning can be used as a **decision-support tool for prioritizing content that may require human review**.

The work focuses on identifying keyword-article rows associated with declining performance, ranking them by a model-derived decline score, and converting those rankings into a practical content action playbook.

The project is intentionally **non-production**. Model scores are used to prioritize human investigation; they do not automatically change, publish, delete, redirect, or optimize content.

---

## Project Overview

### Problem

Content teams may have many pages or keyword-article combinations that could potentially require attention. Reviewing every item with the same priority is inefficient.

The goal of this project is to build a ranking workflow that answers:

> **Which keyword-article rows should a human review first based on observed data patterns associated with decline?**

The output is not an automated content optimizer.

Instead, it is a **ranked decision-support queue** that helps a human reviewer decide where to investigate first.

---

## Intended Users

The workflow is intended for:

- SEO analysts
- Content strategists
- Search intelligence teams
- Data analysts
- ML practitioners evaluating content-performance signals

The ranking can help a reviewer prioritize investigation, while the final content decision remains human-controlled.

---

## What the System Does

The workflow follows this general process:

```text
Anonymized content-performance data
                |
                v
        Data preparation
                |
                v
       Feature construction
                |
                v
        Leakage checks
                |
                v
       Baseline comparison
                |
                v
      Logistic regression
                |
                v
   Client-grouped validation
                |
                v
       Decline scoring
                |
                v
      Ranked action queue
                |
                v
       Human investigation
                |
                v
       Manual content decision




flyrank-ml-internship/
│
├── data/
│   └── raw/
│       └── content_refresh_anonymized.csv
│
├── notebooks/
│   └── First-win notebooks
│
├── work/
│   ├── notebooks/
│   │   ├── w01_research_question.ipynb
│   │   ├── w02_ml_task_framing.ipynb
│   │   ├── w03_data_contract.ipynb
│   │   ├── w03_feature_leakage_check.ipynb
│   │   ├── w04_signal_audit.ipynb
│   │   ├── w04_baseline_score.ipynb
│   │   ├── w05_model.ipynb
│   │   ├── w06_validation_audit.ipynb
│   │   ├── w07_action_playbook.ipynb
│   │   └── capstone.ipynb
│   │
│   ├── outputs/
│   │   └── w07_ranked_action_queue.csv
│   │
│   └── figures/
│
├── docs/
│   ├── data-dictionary.md
│   ├── ml-core-foundation-framework.md
│   ├── ml-intern-dataset-and-lane-guide.md
│   └── intern-free-tooling-guide.md
│
├── scripts/
│   ├── 01_prepare_features.py
│   ├── 02_baseline_score.py
│   ├── 03_train_model.py
│   ├── 04_evaluate_and_export.py
│   ├── 05_build_pdf_report.py
│   └── run_all.py
│
├── DATA_USE.md
├── GUIDE.md
├── SETUP.md
├── requirements.txt
└── README.md
