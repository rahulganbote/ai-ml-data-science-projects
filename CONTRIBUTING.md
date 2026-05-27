# Contributing to AI & ML Data Science Projects

Thank you for taking the time to contribute! This document covers everything you need to know to open a pull request, report a bug, or suggest an improvement.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Branch Naming](#branch-naming)
3. [Commit Messages](#commit-messages)
4. [Running Quality Checks Locally](#running-quality-checks-locally)
5. [Pull Request Process](#pull-request-process)
6. [Code Style](#code-style)
7. [Notebook Conventions](#notebook-conventions)
8. [Reporting Bugs](#reporting-bugs)

---

## Getting Started

```bash
# 1. Fork the repo, then clone your fork
git clone https://github.com/<your-username>/ai-ml-data-science-projects.git
cd ai-ml-data-science-projects

# 2. Create a virtual environment
python -m venv venv
source venv/bin/activate          # macOS / Linux
venv\Scripts\activate             # Windows

# 3. Install all dependencies (including dev tools)
pip install -r requirements.txt

# 4. Install pre-commit hooks (strips notebook outputs before every commit)
pip install pre-commit
pre-commit install
```

---

## Branch Naming

Use a short, descriptive prefix followed by a kebab-case slug:

| Prefix | Use for |
|---|---|
| `feature/` | New project, new analysis, or new utility function |
| `fix/` | Bug fix in a notebook or utility |
| `docs/` | README, CHANGELOG, or docstring update |
| `refactor/` | Code cleanup with no functional change |
| `ci/` | Changes to GitHub Actions workflows |

**Examples:**
```
feature/add-lstm-sentiment-model
fix/foodhub-revenue-calculation
docs/update-bank-churn-readme
refactor/common-utils-type-hints
ci/add-python-3-11-matrix
```

---

## Commit Messages

This project follows the **Conventional Commits** specification. Each commit message has the form:

```
<type>(<optional scope>): <short summary in present tense>

[optional body — explain *why*, not *what*]
[optional footer — references, breaking changes]
```

### Types

| Type | When to use |
|---|---|
| `feat` | New feature, project, or analysis |
| `fix` | Bug fix |
| `docs` | Documentation only |
| `refactor` | Code restructuring — no behaviour change |
| `test` | Adding or fixing tests |
| `ci` | CI/CD pipeline changes |
| `chore` | Dependency bumps, tooling config |
| `perf` | Performance improvement |

### Examples

```
feat(credit-card-churn): add SHAP feature importance plot

fix(utils): handle empty DataFrame in check_missing_values

docs(bank-churn): add model architecture diagram to README

refactor(common): extract evaluate_classifier into utils.py

ci: pin actions/checkout to v4
```

**Rules:**
- Summary line ≤ 72 characters
- Use present tense ("add", not "added")
- No period at the end of the summary line
- Reference issues with `Closes #<issue-number>` in the footer

---

## Running Quality Checks Locally

Run these before pushing — they mirror exactly what the CI workflows check.

### 1. Notebook validation

```bash
# Validate all notebooks parse correctly
python -c "
import os, nbformat
for root, _, files in os.walk('projects'):
    for f in files:
        if f.endswith('.ipynb'):
            path = os.path.join(root, f)
            nb = nbformat.read(open(path), as_version=4)
            nbformat.validate(nb)
            print(f'  OK: {path}')
"
```

### 2. Code formatting and linting (`common/`)

```bash
# Auto-format with black (modifies files in place)
black common/

# Auto-sort imports
isort common/

# Style check
flake8 common/ --max-line-length=88 --extend-ignore=E203,W503

# Or run all three via pre-commit
pre-commit run --all-files
```

### 3. Strip notebook outputs before committing

The `nbstripout` pre-commit hook handles this automatically. To run manually:

```bash
nbstripout projects/**/*.ipynb
```

---

## Pull Request Process

1. **Create a branch** from `main` following the naming convention above.
2. **Make your changes** — keep PRs focused; one logical change per PR.
3. **Run quality checks** locally (see above).
4. **Open a PR** against `main` using the PR template.
5. **Fill in the checklist** in the PR template completely.
6. **Wait for CI** — both the notebook-check and code-quality workflows must pass.
7. **Address review comments** — push additional commits to the same branch.
8. **Squash or rebase** before merge if the commit history is noisy.

### What makes a good PR

- **Small and focused** — reviewers can understand it in one read.
- **Self-contained** — includes both the code change and its README/docs update.
- **Tested** — notebook runs end-to-end (Kernel → Restart & Run All without errors).
- **Clean history** — no debug commits, no "fix typo" chains; squash them.

---

## Code Style

All Python files in `common/` must pass:

| Tool | Config location | Rule |
|---|---|---|
| `black` | `pyproject.toml` | Line length 88, opinionated formatting |
| `isort` | `pyproject.toml` | Profile = black |
| `flake8` | CI args | Max line 88, ignore E203, W503 |

**Type hints** are encouraged on all public functions. Follow the patterns in `common/utils.py`.

**Docstrings** must follow NumPy style with `Parameters`, `Returns`, and `Examples` sections.

---

## Notebook Conventions

- **No hardcoded file paths** — use relative paths or environment variables.
- **No committed outputs** — the `nbstripout` pre-commit hook strips cell outputs automatically. This keeps diffs small and avoids committing large binary blobs.
- **No API keys in notebooks** — use `os.environ["API_KEY"]` or `python-dotenv`.
- **Section headers** — use Markdown cells to divide the notebook into clearly named sections (Data Overview, EDA, Model Building, Evaluation, Recommendations).
- **Kernel restart test** — before pushing, run Kernel → Restart & Run All to confirm the notebook executes cleanly from scratch.

---

## Reporting Bugs

Use the [Bug Report issue template](.github/ISSUE_TEMPLATE/bug_report.md). Include:

- Which notebook and cell number the error occurs in
- The full error traceback
- Your OS, Python version, and key package versions
- Steps to reproduce

---

*Thank you for contributing!*
