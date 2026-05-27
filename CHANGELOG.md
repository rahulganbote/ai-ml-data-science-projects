# Changelog

All notable changes to this project are documented here.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).
This project uses [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [Unreleased]

---

## [1.0.0] — 2025-05-26

First fully-polished, employer-ready release of the portfolio. All 9 projects have been
upgraded from placeholder notebooks to professional-standard GitHub repositories.

### Added

**Repo-level foundations**
- `.gitignore` — comprehensive Python + Jupyter ignore rules (bytecode, checkpoints, data files, secrets, model artifacts, OS/editor junk)
- `LICENSE` — MIT License
- `requirements.txt` — pinned root dependencies covering all 9 projects (numpy, pandas, scikit-learn, tensorflow, transformers, openai, and dev tooling)
- `CONTRIBUTING.md` — branch naming, conventional commits, local quality-check commands, notebook conventions, PR process
- `CHANGELOG.md` — this file
- `pyproject.toml` — project metadata; `black`, `isort`, and `flake8` tool configuration
- `.pre-commit-config.yaml` — `nbstripout`, `black`, `isort`, `flake8` hooks

**GitHub templates (`.github/`)**
- `PULL_REQUEST_TEMPLATE.md` — checklist-driven PR template
- `ISSUE_TEMPLATE/bug_report.md` — structured bug report with environment fields
- `ISSUE_TEMPLATE/feature_request.md` — project-scoped enhancement request

**GitHub Actions CI (`.github/workflows/`)**
- `notebook-check.yml` — validates all `.ipynb` files with `nbformat` and `nbconvert` on every push/PR to `main`
- `code-quality.yml` — runs `black`, `isort`, and `flake8` on `common/` on every push/PR to `main`

**Common utilities (`common/`)**
- `utils.py` — 7 reusable helpers: `load_and_preview`, `check_missing_values`, `encode_categoricals`, `split_data`, `evaluate_classifier`, `save_model`, `load_model`
- `visualization.py` — 6 reusable plotting helpers: `plot_class_distribution`, `plot_confusion_matrix`, `plot_feature_importance`, `plot_roc_curve`, `plot_learning_curve`, `plot_correlation_heatmap`
- `README.md` — full API docs with usage examples for every function

**Per-project READMEs (all 9 projects — added from scratch)**
- `online-foodhub-exploratory-data-analysis/README.md`
- `personal-loan-purchase-prediction/README.md`
- `bank-customer-churn_prediction/README.md`
- `credit-card-churn-prediction/README.md`
- `covid-image-classification/README.md`
- `airline-customer-review-sentiment-analysis/README.md`
- `article-categorization/README.md`
- `support-ticket-categorization/README.md`
- `generative-ai-using-openai/README.md`

Each README includes: problem statement, dataset description, methodology, model architecture, results table, key findings, business recommendations, project structure, how-to-run instructions, tech stack badges, and limitations/future work.

**Per-project `requirements.txt` (all 9 projects — added)**
- Pinned dependencies for each project's specific library needs

### Fixed

**Root `README.md`**
- Corrected copy-paste errors in two project descriptions:
  - Airline Customer Review Sentiment Analysis — was incorrectly describing the Article Categorization project
  - Support Ticket Categorization — was incorrectly describing the Article Categorization project
- Updated all 9 notebook links from a pinned commit hash to the `main` branch
- Added Open-in-Colab and View-on-GitHub badges to all 9 project entries
- Added repo structure tree, skills matrix table, portfolio stats, and Getting Started section

**`LICENSE`**
- Replaced placeholder text `"LICENSE info goes here"` with the full MIT License

---

## [0.1.0] — 2024-01-01 *(initial commit)*

- Initial repository structure with 9 project notebooks and minimal placeholder READMEs
- Projects: FoodHub EDA, Personal Loan, Bank Churn, Credit Card Churn, COVID Image Classification, Airline Sentiment, Article Categorization, Support Ticket Categorization, GenAI OpenAI Demo

---

[Unreleased]: https://github.com/rahulganbote/ai-ml-data-science-projects/compare/v1.0.0...HEAD
[1.0.0]: https://github.com/rahulganbote/ai-ml-data-science-projects/releases/tag/v1.0.0
[0.1.0]: https://github.com/rahulganbote/ai-ml-data-science-projects/releases/tag/v0.1.0
