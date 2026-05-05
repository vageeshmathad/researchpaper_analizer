# AI Research Synthesizer with Conflict Mapping

## Overview
This project presents an AI-based system designed to analyze multiple research papers and identify relationships between them. It focuses on detecting agreement, contradiction, and neutrality across research findings, enabling faster and more structured understanding of academic content.

The system uses natural language processing and transformer-based models to perform semantic comparison between research texts.

---

## Problem Statement
Analyzing multiple research papers is time-consuming and complex. Researchers often struggle to:
- Compare findings across papers
- Identify agreements and contradictions
- Extract meaningful insights efficiently

This results in increased effort, redundancy, and missed knowledge.

---

## Proposed Solution
We propose an AI-driven system that:
- Processes research papers (text/PDF)
- Understands semantic meaning using embeddings
- Detects relationships between papers (agreement, contradiction, neutral)
- Generates structured insights for easier analysis

---

## Core Concept
Text → NLP → Embedding → Comparison → Insight Extraction

---

## Key Features
- Multi-paper analysis
- Conflict detection (AGREE / CONTRADICT / NEUTRAL)
- Semantic understanding using embeddings
- Scalable AI-based pipeline
- Notebook-based interactive demonstration

---

## Methodology

### 1. Data Processing
- Input research text is cleaned and preprocessed
- Text is prepared for model input

### 2. Embedding Generation
- Text is converted into vector representations
- Captures semantic meaning instead of keyword matching

### 3. Conflict Detection
- A transformer-based model (SciBERT) is used
- Classifies relationships into:
  - AGREE
  - CONTRADICT
  - NEUTRAL

### 4. Output Generation
- Results are presented as structured insights
- Enables comparison across papers

---

## Technologies Used
- Python
- PyTorch
- HuggingFace Transformers
- SciBERT (allenai/scibert_scivocab_uncased)
- HuggingFace Datasets
- Scikit-learn
- Pandas / NumPy

---

## Dataset
The model is trained using:

### MultiNLI
- Natural Language Inference dataset
- Provides general understanding of sentence relationships

### SciTail
- Scientific textual inference dataset
- Improves performance on research-oriented content

Note: These datasets are used specifically for training the conflict detection module.

---

## Model Details
- Model: SciBERT
- Task: Sequence Classification
- Classes:
  - AGREE
  - CONTRADICT
  - NEUTRAL

---

## Performance
- Conflict Detection Accuracy: approximately 90–95%
- Performance improves with larger datasets and GPU training
- Balanced dataset ensures better generalization

---

## Example

Input:
Paper 1: Transformer models achieve high accuracy  
Paper 2: BERT performs well on NLP tasks  

Output:
AGREE

---

## Project Structure
