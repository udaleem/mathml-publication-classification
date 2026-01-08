# CNN-Based Classification of Mathematical Publications from MathML

Applied Machine Learning · Structured Data · Deep Learning · Reproducible Pipelines

This project implements an **end-to-end machine learning pipeline** for classifying mathematical research publications **based solely on their MathML formulas**, without using natural language text.

The work focuses on **structured scientific data**, where input is hierarchical XML rather than plain text, a setting common in scientific, technical, and biomedical domains.

🔒 **Source code is private and available upon request.**

---

## Problem Statement
Mathematical publications often contain rich semantic information embedded in **MathML formulas**.  
The goal of this project is to **automatically classify publications into subject categories** using only their formula content.

Key challenges:
- Hierarchical XML structure
- Long and variable-length formula sequences
- Large and sparse vocabularies
- Need for reproducible training and inference

---

## Approach

### Data Processing
- Parsed MathML formulas using XML traversal
- Converted hierarchical MathML into linear token sequences
- Built a frequency-controlled vocabulary (up to 32k tokens)
- Padded and truncated sequences for batch training

### Model Architecture
A **CNN-based sequence classifier** was used after empirical comparison with recurrent models:


### Why CNN?
- Better performance than BiLSTM on long sequences
- Lower computational cost
- Strong local pattern detection in structured formula tokens

### Training & Evaluation
- Implemented full training + inference workflow
- Used categorical cross-entropy and accuracy metrics
- Fixed random seeds for reproducibility
- Achieved ~60–62% accuracy on held-out evaluation data

---

## Key Skills Demonstrated
- Applied deep learning with **TensorFlow / Keras**
- Structured data tokenization (XML / MathML)
- CNN-based sequence modeling
- Reproducible ML pipelines
- Large-scale vocabulary handling

---

## Use Cases
- Scientific document classification
- Mathematical knowledge management
- Structured technical content analysis
- Research analytics and indexing systems
