# FlyRank Internship — Final Submission Index

## Muhammad Noman Amir

Computer Science Student | COMSATS University Islamabad, Wah Campus

---

## 1. Project Overview

This repository contains my work completed during the FlyRank internship, including the applied machine learning workflow, validation, content-action recommendations, documentation, and final project materials.

The project focuses on using machine learning as decision-support for prioritizing keyword-article content for human review.

---

## 2. Machine Learning Track

### Week 1 — Research Question

Notebook:

`work/notebooks/w01_research_question.ipynb`

Focus:
- Research question
- Problem framing
- Initial investigation

---

### Week 2 — ML Task Framing

Notebook:

`work/notebooks/w02_ml_task_framing.ipynb`

Focus:
- ML problem definition
- Target definition
- Task framing

---

### Week 3 — Data Contract

Notebook:

`work/notebooks/w03_data_contract.ipynb`

Focus:
- Dataset structure
- Feature definitions
- Data assumptions
- Data-use boundaries

---

### Week 3 — Feature Leakage Check

Notebook:

`work/notebooks/w03_feature_leakage_check.ipynb`

Focus:
- Leakage investigation
- Feature exclusions
- Validation safety

---

### Week 4 — Signal Audit

Notebook:

`work/notebooks/w04_signal_audit.ipynb`

Focus:
- Signal investigation
- Feature relationships
- Observed patterns

---

### Week 4 — Baseline Score

Notebook:

`work/notebooks/w04_baseline_score.ipynb`

Focus:
- Baseline ranking
- Baseline evaluation
- Comparison framework

---

### Week 5 — Model

Notebook:

`work/notebooks/w05_model.ipynb`

Focus:
- Logistic Regression
- Model training
- Ranked predictions
- Evaluation

---

### Week 6 — Validation Audit

Notebook:

`work/notebooks/w06_validation_audit.ipynb`

Focus:
- Client-grouped validation
- Holdout evaluation
- Leakage prevention
- Model validation

Key validated results:

- Precision@20: 0.9500
- Precision@50: 0.9600
- Precision@100: 0.9600
- ROC-AUC: 0.6696
- Average Precision: 0.8568

Validation rows: 2,789

Validation clients: 5

Client overlap: 0

---

### Week 7 — Content Action Playbook

Notebook:

`work/notebooks/w07_action_playbook.ipynb`

Focus:
- Ranked content actions
- Reason codes
- Intended use
- Human-review rules
- No-go cases
- Monitoring triggers
- Retraining considerations
- Paper-ready export

Export:

`work/outputs/w07_ranked_action_queue.csv`

The ranked queue contains 2,789 candidates.

Reason-code distribution:

- HIGH_DECLINE_PRIORITY: 20
- MEDIUM_DECLINE_PRIORITY: 80
- LOW_DECLINE_PRIORITY: 2,689

The export was verified for:

- Sequential ranking
- Descending decline scores
- Valid reason codes
- Consistency with the Section 1 ranked queue

---

## 3. Model Intended Use

The model is used as a decision-support ranking system for prioritizing keyword-article rows for human review.

The model score does not automatically trigger content changes.

The intended workflow is:

Model ranking  
→ Human inspection  
→ Contextual checks  
→ Decision  
→ Manual action

---

## 4. Human Review Requirements

Before taking action, a reviewer should check:

1. Whether the observed trend supports the model signal.
2. Whether enough recent data is available.
3. Current search intent and SERP context.
4. Content freshness and missing information.
5. Competitors and major search-result changes.
6. Seasonality or other external explanations.
7. Whether the proposed change could remove useful content.

---

## 5. No-Go Cases

The system should NOT automatically perform:

- Publishing
- Article rewriting
- Content deletion
- URL redirects
- Search-intent changes
- SEO metadata changes
- Business-critical decisions
- Production changes

The model score should not be treated as causal evidence.

Human review remains required.

---

## 6. Monitoring and Retraining

Review should be triggered by:

- Material or sustained decline in Precision@20.
- Material or sustained decline in Precision@50 or Precision@100.
- Material decline in Average Precision.
- Substantial change in observed decline rate.
- Substantial change in feature or content distributions.
- New client or content patterns not represented in validation data.
- Repeated human-review feedback that high-ranked recommendations are not useful.

Monitoring changes should be investigated before retraining.

Retraining remains a human decision.

---

## 7. General AI Fluency Track

### FL-09 — Documentation and Demo

Status: Submitted

Deliverables:

- Updated README
- Live demonstration video
- Documentation of setup and usage
- Evaluation results
- Limitations
- AI-use transparency statement

README:

[Add README link]

Demo:

[Add demo video link]

---

## 8. Final Retrospective

Final retrospective:

[Add retrospective link]

The retrospective describes:

- What I set out to build
- How the project changed
- What I learned
- What I would build next
- Three transferable lessons

---

## 9. Personal Portfolio

Portfolio:

[Add live portfolio URL]

The portfolio contains:

- About
- Projects
- Skills
- Contact
- Resume/CV
- Technical work

---

## 10. Build-in-Public Post

Post:

[Add post URL]

The post explains:

- One real project decision
- One real limitation
- What I learned from building the project

---

## 11. Final Review

Final human review/sign-off:

[Add review or sign-off evidence]

Status:

Pending final review

---

## 12. AI Transparency

AI tools were used as development and thinking assistants during the internship.

I used AI to help with tasks such as:

- Explaining technical concepts
- Debugging and improving code
- Structuring documentation
- Reviewing wording and presentation
- Supporting analysis and interpretation

I personally ran, checked, validated, and reviewed the project outputs rather than treating AI-generated content as automatically correct.

---

## 13. Final Status

Machine Learning Track: Completed

General AI Fluency FL-09: Submitted

Final Package: In progress

Retrospective: Pending

Hours Log: Pending

Portfolio/Build-in-Public: Pending

Final Human Review: Pending

---

## Repository

GitHub:

https://github.com/nomanamir20/flyrank-ml-internship
