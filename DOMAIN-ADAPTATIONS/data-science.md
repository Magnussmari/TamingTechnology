# Data Science / Machine Learning Adaptation

Adapting the AI Learning Orchestration system for Data Science and Machine Learning workflows.

---

## 🎯 Overview

The core orchestration principles apply perfectly to Data Science, but the tools, workflows, and deliverables differ from web development. This guide shows you how to adapt the three core prompts and AI orchestration patterns for DS/ML work.

**Key Differences:**
- Jupyter notebooks instead of IDE files
- Experiment tracking instead of version control focus
- Model training pipelines instead of web apps
- Data exploration vs. UI development

---

## 📝 Prompt 1 Modifications (Learning Roadmap)

### Changes to Context Section

Replace IDE setup with:

```markdown
**What I need help with:**

- **[INSERT: YES/NO]** - Jupyter/Colab environment setup
- **[INSERT: YES/NO]** - Git + DVC for notebook version control
- **[INSERT: YES/NO]** - Python data science stack (NumPy, Pandas, Matplotlib)
- **[INSERT: YES/NO]** - ML frameworks (scikit-learn, PyTorch, TensorFlow)
- **[INSERT: YES/NO]** - Experiment tracking (W&B, MLflow, Neptune)
- **[INSERT: YES/NO]** - Model deployment (FastAPI, Streamlit, Docker)
```

### Modify Goals Section

Replace with DS-specific goals:

```markdown
**My goals for this learning journey:**

Examples:
- "Build and deploy a classification model for [use case]"
- "Create a data pipeline from raw data to insights"
- "Train a neural network and track experiments systematically"
- "Deploy an ML API that other services can consume"
```

---

## 🔬 Prompt 2 Modifications (Tech Stack Analysis)

### Project Information

```markdown
**Project Information:**
- **Project name/type**: **[INSERT: e.g., "Customer churn prediction," "Image classifier," "Time series forecasting"]**
- **Main framework/library**: **[INSERT: e.g., "scikit-learn," "PyTorch," "TensorFlow," "XGBoost"]**
- **Environment file**: **[INSERT: requirements.txt, environment.yml, pyproject.toml]**
```

### Focus Areas

Modify the TASK section to analyze:

1. **Data Pipeline**: Raw data → Cleaned data → Features → Model inputs
2. **ML Stack**:
   - Data manipulation: Pandas, NumPy, Polars
   - Visualization: Matplotlib, Seaborn, Plotly
   - ML libraries: scikit-learn, XGBoost, LightGBM
   - Deep learning: PyTorch, TensorFlow, Keras
   - Experiment tracking: W&B, MLflow, Neptune
3. **Deployment Stack**: FastAPI, Flask, Streamlit, Docker, cloud services

---

## 🤖 Prompt 3 Modifications (Senior-Junior Pattern)

### Senior AI Specialization

The Senior AI (Claude Chat) focuses on:
- Algorithm selection (which model for this problem?)
- Feature engineering strategies
- Hyperparameter tuning approaches
- Model evaluation metrics selection
- Deployment architecture

### Junior AI Specialization

The Junior AI (Cursor/Claude Code) focuses on:
- Writing data preprocessing code
- Implementing model training loops
- Creating visualization code
- Building evaluation pipelines
- Debugging training errors

### Modified Report Template

```markdown
# 🔷 JUNIOR DEVELOPER REPORT (Data Science)

## 📋 Task Summary
[What experiment/model I was trying to build]

## ✅ What I Completed
- [Data preprocessing steps]
- [EDA visualizations created]
- [Models trained]
- [Evaluation metrics computed]

## ❌ Problems Encountered
**Issue 1**: [Describe the problem]
- What I tried: [Solutions attempted]
- Current performance: [Metrics: accuracy, loss, etc.]
- Error messages / Warnings: [If applicable]

## 📊 Current Results
- **Baseline performance**: [metric: value]
- **Current best performance**: [metric: value]
- **Training issues**: [Overfitting? Underfitting? NaN loss?]

## ❓ Questions for Senior Developer
1. [Which algorithm should I try next?]
2. [How to handle [specific data issue]?]
3. [Is this performance good enough for [use case]?]

## 💭 My Current Understanding
[What I think is causing the issue and why]

## 🎯 What I Need
[Specific guidance requested - e.g., "feature engineering ideas," "algorithm selection," "hyperparameter strategy"]

## 📎 Context
- Project: [Project name/type]
- Dataset: [Size, features, target]
- Current model: [Algorithm, parameters]
- Best metric so far: [value]
```

---

## 🔧 AI Tool Specialization for Data Science

| AI Tool | DS/ML Use Case |
|---------|----------------|
| **🔴 Perplexity** | Latest ML papers, SOTA models, finding datasets, research new techniques |
| **🔵 Claude Chat** | Algorithm selection, experimental design, architecture decisions, debugging logic |
| **🟢 Claude Code** | Refactor notebooks → production code, analyze existing pipelines, code review |
| **⚙️ Cursor** | Write data preprocessing, model training loops, visualization code |
| **🟡 ChatGPT** | Explain statistical concepts, brainstorm feature ideas, generate synthetic data |
| **🟠 Gemini** | Analyze data visualizations, extract info from images/PDFs, Google Colab integration |

---

## 📊 Data Science Workflow Patterns

### Pattern 1: EDA → Model → Deploy

```
1. Perplexity: "Latest best practices for [problem type] in 2025"
   → Get: Current SOTA approaches, common pitfalls

2. Claude Code: Analyze existing notebook/codebase
   → Understand: Data structure, existing preprocessing

3. Cursor: Implement data cleaning and EDA
   → Build: Preprocessing pipeline, visualizations

4. Claude Chat: "Given this EDA: [summary], which models should I try?"
   → Get: Algorithm recommendations, feature engineering ideas

5. Cursor: Implement model training pipeline
   → Train: Multiple models, track experiments

6. Claude Chat: "Review these results: [metrics]. Next steps?"
   → Get: Evaluation, next experiments to run

7. Claude Code: Refactor notebook → production code
   → Build: Clean pipeline for deployment
```

### Pattern 2: Debug ML Model

```
Problem: Model not learning (loss not decreasing)

1. Cursor: Try basic fixes (learning rate, batch size)
   → Still not working after 2-3 tries

2. Generate DS Report with current metrics

3. Claude Chat: [Paste report with learning curves]
   Analysis:
   - "Your loss plateaus immediately - likely data issue"
   - "Check: data scaling, NaN values, label distribution"
   Recommendations:
   - Normalize features
   - Check for data leakage
   - Verify labels are correct

4. Cursor: Implement data validation and scaling
   → Works! Model learns correctly
```

### Pattern 3: Notebook → Production

```
1. Claude Code: Analyze existing Jupyter notebook
   → Identify: Code to extract, dependencies, data flows

2. Claude Chat: "Best practices for converting notebook to production API"
   → Get: Architecture guidance, folder structure

3. Cursor: Implement production structure
   src/
   ├── data/          # Data loading
   ├── features/      # Feature engineering
   ├── models/        # Model definitions
   ├── training/      # Training logic
   └── api/           # FastAPI endpoints

4. Claude Code: Review for production readiness
   → Check: Error handling, logging, configuration
```

---

## 📚 Example Journey: Sarah's DS Transition

**Background:** Sarah used AutoML tools but wants to understand what's happening under the hood.

### Week 1-2: Foundation
- **Prompt 1** → Roadmap: Jupyter setup, Python basics, NumPy/Pandas
- **Prompt 2** → Analyzed AutoML-generated code to understand structure
- **Simple projects**: Data cleaning, basic visualizations

### Week 3-4: First Models
- **Cursor**: Implemented scikit-learn classifiers
- **Stuck**: Model accuracy terrible
- **Claude Chat**: "Your features aren't scaled - models sensitive to this"
- **Fixed**: Added StandardScaler, accuracy improved

### Week 5-6: Deep Learning
- **Perplexity**: Researched PyTorch vs TensorFlow
- **Claude Chat**: Recommended PyTorch for flexibility
- **Cursor**: Built first neural network
- **Claude Code**: Refactored messy notebook into clean modules

### Week 7-8: Production
- **Claude Chat**: Designed deployment architecture
- **Cursor**: Built FastAPI serving endpoint
- **Deployed**: First ML model in production!

---

## 🎯 Domain-Specific Resources

### Learning Paths
- **Perplexity searches:**
  - "Best Python data science tutorials 2025"
  - "Latest PyTorch best practices"
  - "How to deploy ML models 2025"

### Communities
- Kaggle (competitions, notebooks, datasets)
- Papers with Code (SOTA models)
- Reddit r/MachineLearning, r/datascience
- Hugging Face Community

### Tools to Add
- **Experiment Tracking**: Weights & Biases, MLflow, Neptune
- **Data Version Control**: DVC, Pachyderm
- **Deployment**: FastAPI, Streamlit, Gradio, Docker
- **Cloud**: Google Colab, Kaggle Notebooks, AWS SageMaker

---

## 💡 DS-Specific Tips

### 1. Notebook Discipline
Keep notebooks organized:
```
01_data_exploration.ipynb
02_preprocessing.ipynb
03_baseline_models.ipynb
04_advanced_models.ipynb
05_evaluation.ipynb
```

### 2. Track Everything
Use experiment tracking from Day 1:
- Hyperparameters
- Metrics
- Model versions
- Data versions

### 3. Start Simple
Always train a simple baseline first:
- Logistic Regression before Neural Networks
- Decision Trees before XGBoost
- Linear model before Deep Learning

### 4. Use AI for Math
Claude Chat excels at explaining:
- Statistical concepts
- Loss functions
- Optimization algorithms
- Model architectures

---

## 🔗 Related Resources

- [Complete Guide](../COMPLETE-GUIDE.md)
- [Prompt 1: Learning Roadmap](../PROMPTS/prompt-1-roadmap.md)
- [Prompt 2: Tech Stack Analysis](../PROMPTS/prompt-2-stack-analysis.md)
- [Prompt 3: Senior-Junior Pattern](../PROMPTS/prompt-3-senior-junior.md)

---

**Ready to orchestrate AI for Data Science? Start with Prompt 1 adapted for DS!** 🔬📊🤖
