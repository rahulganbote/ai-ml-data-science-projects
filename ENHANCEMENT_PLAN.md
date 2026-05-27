# 5-Day Repo Enhancement Plan
### Goal: Bring `ai-ml-data-science-projects` to industry-standard GitHub quality for employer portfolios

---

## Current State Audit

| Area | Status | Issue |
|---|---|---|
| Root `README.md` | ⚠️ Needs fix | Copy-paste errors: airline & support-ticket descriptions say "article categorization" |
| Per-project `README.md` | ❌ Placeholder | All 9 projects have only 2 lines: title + "open the notebook" |
| `.gitignore` | ❌ Missing | No Python/Jupyter gitignore — commits may include `.pyc`, checkpoints, etc. |
| `requirements.txt` | ❌ Missing | No dependency files anywhere in the repo |
| `LICENSE` | ❌ Placeholder | File exists but contains only "LICENSE info goes here" |
| `common/` utilities | ❌ Empty stubs | `utils.py` and `visualization.py` are comment-only |
| GitHub Actions CI | ❌ Missing | No automated checks on push/PR |
| GitHub PR/Issue templates | ❌ Missing | No `.github/` folder |
| Notebook "Open in Colab" badges | ❌ Missing | No quick-launch links for recruiters |
| Skills/tech matrix | ❌ Missing | No at-a-glance summary of tools used across projects |

---

## Projects in Scope

| # | Project | Domain | Key Techniques |
|---|---|---|---|
| 1 | FoodHub EDA | Data Analysis | EDA, Pandas, Seaborn, Business Insights |
| 2 | Personal Loan Purchase Prediction | ML | Decision Trees, Pruning, Missing Value Handling |
| 3 | Bank Customer Churn Prediction | Deep Learning | ANN, TensorFlow/Keras, Regularization |
| 4 | Credit Card Churn Prediction | Advanced ML | Random Forest, Boosting, SMOTE, Hyperparameter Tuning |
| 5 | COVID-19 Image Classification | Computer Vision | CNN, Image Preprocessing, Multi-class Classification |
| 6 | Airline Customer Review Sentiment | NLP | Transformers, LLMs, Sentiment Analysis |
| 7 | Article Categorization | NLP | Transformers, LLMs, Multi-class Text Classification |
| 8 | Support Ticket Categorization | NLP | NLP, Text Classification, Prompt Engineering |
| 9 | Generative AI using OpenAI | Gen AI | OpenAI API, Prompt Engineering, Text Generation |

---

## Day 1 — Foundation & Repo-Level Files

**Theme:** Fix the bones. Every recruiter who lands on the repo root should immediately see a professional, well-organized project.

### Tasks

**1.1 Fix root `README.md`**
- Correct copy-paste errors in airline sentiment and support ticket descriptions
- Add a "Skills & Tech Stack" matrix table (rows = projects, columns = domain areas)
- Add "Open in Colab" badge column to the projects table
- Add a "How to Navigate This Repo" section
- Add social/profile badges (GitHub profile, LinkedIn placeholder)
- Standardize emoji usage and section headers
- Update GitHub links to point to `main` branch (not a commit hash)

**1.2 Create `.gitignore`**
- Use the standard Python + Jupyter `.gitignore` template
- Include: `__pycache__/`, `*.pyc`, `.ipynb_checkpoints/`, `.env`, `*.egg-info/`, `dist/`, `.DS_Store`, `venv/`, `.venv/`
- Add data file exclusions: `*.csv`, `*.xlsx`, `*.zip`, `data/raw/` (with note to use DVC or link)

**1.3 Fix `LICENSE`**
- Replace placeholder with MIT License text (standard for portfolio projects)

**1.4 Create root `requirements.txt`**
- Add all libraries used across all notebooks: numpy, pandas, matplotlib, seaborn, scikit-learn, tensorflow, keras, transformers, openai, torch, Pillow, nltk, imbalanced-learn, xgboost, lightgbm, jupyter, nbformat

**1.5 Create `.github/` folder**
- `PULL_REQUEST_TEMPLATE.md` — checklist: description, notebook tested, README updated
- `ISSUE_TEMPLATE/bug_report.md` — for notebook bugs/errors
- `ISSUE_TEMPLATE/feature_request.md` — for enhancement suggestions

**Prompt to use for Day 1:**
> "Execute Day 1 of the enhancement plan in ENHANCEMENT_PLAN.md — fix root README.md, create .gitignore, fix LICENSE with MIT text, create root requirements.txt, and create .github/ templates."

---

## Day 2 — Per-Project READMEs: ML Projects (4 projects)

**Theme:** Give each ML project a proper README that tells the story: problem → data → approach → results → how to run.

### Projects covered
- FoodHub EDA
- Personal Loan Purchase Prediction
- Bank Customer Churn Prediction
- Credit Card Churn Prediction

### README template for each project

Each README should include these sections:
1. **Title + badge strip** (Colab badge, Python version badge, license badge)
2. **Problem Statement** — what business problem is being solved
3. **Dataset** — source, shape, key features, target variable
4. **Approach / Methodology** — step-by-step: EDA → preprocessing → modeling → evaluation
5. **Key Results** — model performance metrics (accuracy, F1, AUC-ROC, etc.)
6. **Business Recommendations** — top 3 actionable insights
7. **Project Structure** — file/folder tree
8. **How to Run** — step-by-step: clone → install deps → open notebook
9. **Tech Stack** — badges for Python, pandas, scikit-learn, etc.
10. **Per-project `requirements.txt`** — pinned dependencies for reproducibility

**Prompt to use for Day 2:**
> "Execute Day 2 of the enhancement plan in ENHANCEMENT_PLAN.md. Write rich, employer-ready README.md files for these 4 projects: online-foodhub-exploratory-data-analysis, personal-loan-purchase-prediction, bank-customer-churn_prediction, credit-card-churn-prediction. Follow the README template in the plan. Also create a requirements.txt in each project folder."

---

## Day 3 — Per-Project READMEs: NLP, CV & GenAI Projects (5 projects)

**Theme:** Same README overhaul for the remaining 5 projects, which lean heavily on modern ML (transformers, CNNs, LLMs).

### Projects covered
- COVID-19 Image Classification
- Airline Customer Review Sentiment Analysis
- Article Categorization
- Support Ticket Categorization
- Generative AI using OpenAI

### Additional sections for NLP/CV/GenAI projects
- **Model Architecture** — describe the neural network / transformer model used
- **Training Details** — epochs, optimizer, loss function, hardware (CPU/GPU)
- **Sample Predictions** — show 2-3 example inputs and their predicted outputs
- **Limitations & Future Work** — honest assessment + next steps

**Prompt to use for Day 3:**
> "Execute Day 3 of the enhancement plan in ENHANCEMENT_PLAN.md. Write rich, employer-ready README.md files for these 5 projects: covid-image-classification, airline-customer-review-sentiment-analysis, article-categorization, support-ticket-categorization, generative-ai-using-openai. Follow the README template in the plan, include model architecture and sample predictions sections. Also create a requirements.txt in each project folder."

---

## Day 4 — GitHub Actions CI + Common Utilities Module

**Theme:** Show automated quality gates and reusable code — both hallmarks of professional engineering.

### Tasks

**4.1 GitHub Actions Workflow: Notebook Linter**
- File: `.github/workflows/notebook-check.yml`
- Trigger: on push and pull_request to `main`
- Steps:
  1. Set up Python 3.10
  2. Install `nbformat` and `nbconvert`
  3. Run `jupyter nbconvert --to script` on all notebooks (validates they parse)
  4. Run `nbformat.validate` to check notebook format version
- Purpose: Catches broken notebooks before they hit the main branch

**4.2 GitHub Actions Workflow: Code Quality**
- File: `.github/workflows/code-quality.yml`
- Trigger: on push and pull_request to `main`
- Steps:
  1. Install `flake8`, `black`, `isort`
  2. Run `black --check` on all `.py` files in `common/`
  3. Run `flake8` on `common/`
- Purpose: Enforces consistent code style in shared utilities

**4.3 Fill in `common/utils.py`**
- `load_and_preview(filepath, n=5)` — loads CSV/Excel, prints shape + head
- `check_missing_values(df)` — returns a DataFrame of missing % per column
- `encode_categoricals(df, columns)` — label + one-hot encoding helper
- `split_data(df, target, test_size=0.2, stratify=True)` — train/test split with stratification
- `evaluate_classifier(y_true, y_pred, y_proba=None)` — prints accuracy, precision, recall, F1, AUC-ROC, confusion matrix
- `save_model(model, path)` / `load_model(path)` — pickle-based model persistence

**4.4 Fill in `common/visualization.py`**
- `plot_class_distribution(y, title)` — bar chart of class counts
- `plot_confusion_matrix(y_true, y_pred, labels)` — styled heatmap
- `plot_feature_importance(model, feature_names, top_n=15)` — horizontal bar chart
- `plot_roc_curve(y_true, y_proba)` — ROC with AUC annotation
- `plot_learning_curve(history)` — for Keras training history (loss + accuracy)
- `plot_correlation_heatmap(df)` — masked upper-triangle correlation matrix

**4.5 Update `common/README.md`**
- Document each function with parameters, return values, and usage examples

**Prompt to use for Day 4:**
> "Execute Day 4 of the enhancement plan in ENHANCEMENT_PLAN.md. Create .github/workflows/notebook-check.yml and code-quality.yml GitHub Actions workflows. Fill in common/utils.py and common/visualization.py with the documented helper functions. Update common/README.md with usage examples."

---

## Day 5 — Polish, Badges & Final Consistency Pass

**Theme:** The finishing touches that separate a "good" portfolio from a "great" one.

### Tasks

**5.1 Add `CONTRIBUTING.md`**
- How to fork and clone
- Branch naming convention: `feature/`, `fix/`, `docs/`
- Commit message format (conventional commits: `feat:`, `fix:`, `docs:`, `refactor:`)
- How to run the CI checks locally before pushing
- Code review expectations

**5.2 Add `CHANGELOG.md`**
- Start with `[Unreleased]` section
- Document the Day 1–5 enhancements under `[1.0.0]`
- Follow Keep a Changelog format: `### Added`, `### Fixed`, `### Changed`

**5.3 Add `pyproject.toml`**
- Define project metadata: name, version, authors, Python version
- Configure `black` formatting rules (line-length = 88)
- Configure `isort` profile = black
- Configure `flake8` max-line-length = 88, ignore E203, W503

**5.4 Add "Open in Colab" and "nbviewer" badges to every project README**
- Template: `[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](NOTEBOOK_URL)`
- Template: `[![View in nbviewer](https://raw.githubusercontent.com/jupyter/design/master/logos/Badges/nbviewer_badge.svg)](NBVIEWER_URL)`

**5.5 Add `nbstripout` pre-commit hook config**
- Add `.pre-commit-config.yaml` with `nbstripout` hook
- This strips notebook outputs before commits (keeps git history clean, avoids huge diffs)
- Also add `nbstripout` to root `requirements.txt`

**5.6 Final consistency pass on root README**
- Ensure all 9 project links point to correct notebooks on `main` branch
- Verify project descriptions are accurate and unique (no copy-paste errors remain)
- Add a "Portfolio Stats" section: total projects, domains covered, key algorithms
- Add contact/profile section at bottom

**5.7 Save memory notes**
- After Day 5, ask Claude to save a memory about this repo's structure and enhancement goals

**Prompt to use for Day 5:**
> "Execute Day 5 of the enhancement plan in ENHANCEMENT_PLAN.md. Create CONTRIBUTING.md, CHANGELOG.md, and pyproject.toml. Add Open-in-Colab badges to all 9 project READMEs. Add .pre-commit-config.yaml with nbstripout. Do a final consistency pass on the root README — fix all links to point to main branch, verify no copy-paste errors, add Portfolio Stats section."

---

## Summary: What Employers Will See After Day 5

| Before | After |
|---|---|
| 2-line placeholder READMEs | Rich READMEs with problem, data, methodology, results, how-to-run |
| No `.gitignore` | Professional Python + Jupyter `.gitignore` |
| Placeholder `LICENSE` | MIT License |
| No CI | GitHub Actions: notebook validation + code quality |
| No shared utilities | `common/` module with 10+ reusable ML helper functions |
| No dependency files | Root + per-project `requirements.txt`, `pyproject.toml` |
| Copy-paste errors in root README | Clean, accurate descriptions with skills matrix |
| No GitHub templates | PR template + bug/feature issue templates |
| No commit hygiene | `nbstripout` pre-commit hook, conventional commit guide |
| No Colab access | One-click "Open in Colab" on every notebook |

---

## Tips for Staying Under Token Limits

- Run one day's prompt per session — each day is self-contained
- If a day feels large, split it: e.g., Day 2 can be run as "Day 2a: FoodHub + Personal Loan" and "Day 2b: Bank Churn + Credit Card Churn"
- Always start a session by telling Claude: "We are working on Day X of the plan in ENHANCEMENT_PLAN.md"
- Claude will re-read this file at the start of each session for context

---

*Plan created: 2026-05-26*
