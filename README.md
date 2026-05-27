# 📚 AI & ML Data Science Projects Portfolio

> **Artificial Intelligence and Machine Learning: Business Applications**

![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-FF6F00?logo=tensorflow&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.x-F7931E?logo=scikit-learn&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)
![Notebook CI](https://github.com/rahulganbote/ai-ml-data-science-projects/actions/workflows/notebook-check.yml/badge.svg)
![Code Quality](https://github.com/rahulganbote/ai-ml-data-science-projects/actions/workflows/code-quality.yml/badge.svg)

---

## 📖 About This Repository

A curated portfolio of **9 end-to-end AI/ML and Data Science projects** spanning supervised learning, deep learning, computer vision, natural language processing, and generative AI. Each project applies industry-standard methodologies to real-world business problems and includes actionable insights and recommendations.

---

## 🗺️ How to Navigate This Repo

```
ai-ml-data-science-projects/
├── projects/                  # One folder per project (notebook + README)
│   ├── airline-customer-review-sentiment-analysis/
│   ├── article-categorization/
│   ├── bank-customer-churn_prediction/
│   ├── covid-image-classification/
│   ├── credit-card-churn-prediction/
│   ├── generative-ai-using-openai/
│   ├── online-foodhub-exploratory-data-analysis/
│   ├── personal-loan-purchase-prediction/
│   └── support-ticket-categorization/
├── common/                    # Shared utility functions (EDA, visualization, evaluation)
├── .github/                   # CI workflows, PR template, issue templates
├── requirements.txt           # All project dependencies
├── pyproject.toml             # Tool configuration (black, isort, flake8, pytest)
├── .pre-commit-config.yaml    # Pre-commit hooks (nbstripout, black, isort, flake8)
├── CONTRIBUTING.md            # Branching, commit, and PR guidelines
├── CHANGELOG.md               # Version history of repo enhancements
└── README.md                  # This file
```

Each project folder contains:
- A **Jupyter notebook** with full code, analysis, and results
- A **README.md** with problem statement, methodology, key results, and how-to-run instructions

---

## 🚀 Projects

### 🍽️ FoodHub Exploratory Data Analysis
**Course:** Python Foundations

Performed exploratory data analysis for a food aggregator company to uncover patterns in restaurant demand, cuisine preferences, and delivery times — translating findings into data-driven business recommendations.

**Skills & Tools:** Python · NumPy · Pandas · Matplotlib · Seaborn · Univariate & Bivariate Analysis

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rahulganbote/ai-ml-data-science-projects/blob/main/projects/online-foodhub-exploratory-data-analysis/RahulGanbote_FoodHub_EDA_FullCode.ipynb)
[![View on GitHub](https://img.shields.io/badge/View-Notebook-181717?logo=github)](https://github.com/rahulganbote/ai-ml-data-science-projects/blob/main/projects/online-foodhub-exploratory-data-analysis/RahulGanbote_FoodHub_EDA_FullCode.ipynb)

---

### 🏠 Personal Loan Campaign Modeling
**Course:** Machine Learning

Built a classification model to identify bank customers most likely to purchase a personal loan, enabling the marketing team to target high-conversion segments and optimize campaign spend.

**Skills & Tools:** EDA · Data Preprocessing · Decision Trees · Cost-Complexity Pruning · Handling Missing Values · Business Recommendations

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rahulganbote/ai-ml-data-science-projects/blob/main/projects/personal-loan-purchase-prediction/Personal_Loan_Purchase_Prediction.ipynb)
[![View on GitHub](https://img.shields.io/badge/View-Notebook-181717?logo=github)](https://github.com/rahulganbote/ai-ml-data-science-projects/blob/main/projects/personal-loan-purchase-prediction/Personal_Loan_Purchase_Prediction.ipynb)

---

### 💳 Credit Card Users Churn Prediction
**Course:** Advanced Machine Learning

Developed an ensemble-based predictive model to identify credit card customers at risk of churning, and surfaced the key drivers behind attrition to support targeted retention strategies.

**Skills & Tools:** EDA · SMOTE · Random Forest · Bagging · Gradient Boosting · Cross-Validation · Hyperparameter Tuning

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rahulganbote/ai-ml-data-science-projects/blob/main/projects/credit-card-churn-prediction/Rahul_AML_Credit_Card_Users_Churn_Prediction.ipynb)
[![View on GitHub](https://img.shields.io/badge/View-Notebook-181717?logo=github)](https://github.com/rahulganbote/ai-ml-data-science-projects/blob/main/projects/credit-card-churn-prediction/Rahul_AML_Credit_Card_Users_Churn_Prediction.ipynb)

---

### 🏦 Bank Customer Churn Prediction
**Course:** Introduction to Neural Networks

Built an Artificial Neural Network to predict which bank customers are likely to leave, and recommended proactive retention strategies based on the model's key predictors.

**Skills & Tools:** EDA · Data Preprocessing · TensorFlow · Keras · ANN · Dropout · Batch Normalization · Early Stopping

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rahulganbote/ai-ml-data-science-projects/blob/main/projects/bank-customer-churn_prediction/Rahul_INN_Bank_Customer_Churn_Notebook.ipynb)
[![View on GitHub](https://img.shields.io/badge/View-Notebook-181717?logo=github)](https://github.com/rahulganbote/ai-ml-data-science-projects/blob/main/projects/bank-customer-churn_prediction/Rahul_INN_Bank_Customer_Churn_Notebook.ipynb)

---

### 🩺 COVID-19 Image Classification
**Course:** Introduction to Computer Vision

Designed and trained a Convolutional Neural Network to classify chest X-ray images into three categories — COVID-19, Viral Pneumonia, and Normal — to assist radiologists in high-volume triage scenarios.

**Skills & Tools:** Image Preprocessing · Data Augmentation · CNN · Transfer Learning · TensorFlow · Keras · Model Evaluation

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rahulganbote/ai-ml-data-science-projects/blob/main/projects/covid-image-classification/COVID_Detection_using_AI.ipynb)
[![View on GitHub](https://img.shields.io/badge/View-Notebook-181717?logo=github)](https://github.com/rahulganbote/ai-ml-data-science-projects/blob/main/projects/covid-image-classification/COVID_Detection_using_AI.ipynb)

---

### 🗞️ Article Categorization using NLP
**Course:** Introduction to Natural Language Processing and LLM

Built a multi-class text classification system that automatically categorizes news articles into topics such as Sports, Business, Politics, and Technology using both traditional NLP and transformer-based models.

**Skills & Tools:** EDA · Text Preprocessing · TF-IDF · Transformers (BERT) · LLMs · Prompt Engineering · scikit-learn

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rahulganbote/ai-ml-data-science-projects/blob/main/projects/article-categorization/NLP_Article_Categorization_LLM_Notebook.ipynb)
[![View on GitHub](https://img.shields.io/badge/View-Notebook-181717?logo=github)](https://github.com/rahulganbote/ai-ml-data-science-projects/blob/main/projects/article-categorization/NLP_Article_Categorization_LLM_Notebook.ipynb)

---

### 🎫 Support Ticket Categorization using NLP
**Course:** Introduction to Natural Language Processing and LLM

Built an automated support ticket routing system that classifies incoming customer tickets into the correct support category, reducing manual triage time and improving response SLAs.

**Skills & Tools:** EDA · Text Preprocessing · NLP · Transformers · LLMs · Prompt Engineering · Zero-shot Classification

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rahulganbote/ai-ml-data-science-projects/blob/main/projects/support-ticket-categorization/support_ticket_categorization_nlp_notebook.ipynb)
[![View on GitHub](https://img.shields.io/badge/View-Notebook-181717?logo=github)](https://github.com/rahulganbote/ai-ml-data-science-projects/blob/main/projects/support-ticket-categorization/support_ticket_categorization_nlp_notebook.ipynb)

---

### ✈️ Airline Customer Review Sentiment Analysis
**Course:** Introduction to Natural Language Processing and LLM

Analyzed thousands of airline customer reviews to classify sentiment and extract key themes driving positive and negative experiences, providing the airline with targeted service improvement areas.

**Skills & Tools:** EDA · Text Preprocessing · Sentiment Analysis · Transformers · LLMs · Prompt Engineering · Hugging Face

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rahulganbote/ai-ml-data-science-projects/blob/main/projects/airline-customer-review-sentiment-analysis/airline_customer_review_sentiment_analysis_notebook.ipynb)
[![View on GitHub](https://img.shields.io/badge/View-Notebook-181717?logo=github)](https://github.com/rahulganbote/ai-ml-data-science-projects/blob/main/projects/airline-customer-review-sentiment-analysis/airline_customer_review_sentiment_analysis_notebook.ipynb)

---

### 🤖 Generative AI Demo using OpenAI API
**Course:** Introduction to Generative AI and LLM

Explored and demonstrated the capabilities of the OpenAI API for text generation, summarization, question-answering, and creative writing, with hands-on examples of prompt engineering techniques including zero-shot, few-shot, and chain-of-thought prompting.

**Skills & Tools:** OpenAI API · GPT-4 · Prompt Engineering · LLMs · Generative AI · Python

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rahulganbote/ai-ml-data-science-projects/blob/main/projects/generative-ai-using-openai/openai_api_demo.ipynb)
[![View on GitHub](https://img.shields.io/badge/View-Notebook-181717?logo=github)](https://github.com/rahulganbote/ai-ml-data-science-projects/blob/main/projects/generative-ai-using-openai/openai_api_demo.ipynb)

---

## 🧠 Skills & Technology Matrix

| Project | EDA | Classical ML | Deep Learning | NLP / LLM | Computer Vision | Gen AI |
|---|:---:|:---:|:---:|:---:|:---:|:---:|
| FoodHub EDA | ✅ | | | | | |
| Personal Loan Prediction | ✅ | ✅ | | | | |
| Credit Card Churn | ✅ | ✅ | | | | |
| Bank Customer Churn | ✅ | | ✅ | | | |
| COVID-19 Classification | | | ✅ | | ✅ | |
| Article Categorization | ✅ | ✅ | | ✅ | | |
| Support Ticket Routing | ✅ | | | ✅ | | |
| Airline Sentiment | ✅ | | | ✅ | | |
| Generative AI (OpenAI) | | | | ✅ | | ✅ |

---

## 📊 Portfolio at a Glance

| | |
|---|---|
| **Total Projects** | 9 |
| **Domains** | EDA · Classical ML · Deep Learning · NLP · Computer Vision · Generative AI |
| **Languages** | Python 3.9+ |
| **Key Libraries** | TensorFlow · Keras · scikit-learn · Hugging Face Transformers · OpenAI · Pandas · Seaborn |
| **Shared Utilities** | 13 reusable functions across `common/utils.py` and `common/visualization.py` |
| **CI / Quality Gates** | GitHub Actions: notebook validation + code quality (black · isort · flake8) |
| **Commit Hygiene** | `nbstripout` pre-commit hook strips notebook outputs before every commit |
| **Program** | PGP AI & ML — UT Austin McCombs School of Business |

---

## ⚙️ Getting Started

**1. Clone the repo:**
```bash
git clone https://github.com/rahulganbote/ai-ml-data-science-projects.git
cd ai-ml-data-science-projects
```

**2. Set up a virtual environment and install dependencies:**
```bash
python -m venv venv
source venv/bin/activate        # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

**3. Launch Jupyter:**
```bash
jupyter notebook
```
Navigate to `projects/<project-name>/` and open the `.ipynb` file.

> **Tip:** Each project folder has its own `requirements.txt` for installing only that project's dependencies.

---

## 📁 Common Utilities

The [`common/`](./common/) folder contains shared helper functions reusable across projects:

- **`utils.py`** — data loading, missing value checks, encoding helpers, train/test splitting, classifier evaluation
- **`visualization.py`** — confusion matrix, ROC curve, feature importance, learning curve, correlation heatmap

---

## 📄 License

This project is licensed under the [MIT License](./LICENSE).

---

## 🤝 Contributing

Feedback and suggestions are welcome! Please see [CONTRIBUTING.md](./CONTRIBUTING.md) for guidelines on branching, commit messages, and pull requests.

---

See [CHANGELOG.md](./CHANGELOG.md) for a full history of repository improvements.

---

*© 2026 Rahul Ganbote · All rights reserved.*
