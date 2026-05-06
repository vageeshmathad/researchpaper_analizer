

"Don't read 100 papers. Understand all of them in minutes."

---

## Live Demo  
https://data-flow-hub--kapalikhushi8.replit.app  

---

## Problem Statement  
Every research cycle, hundreds of papers are published on overlapping topics. Current systems are manual and require researchers to spend weeks reading and comparing papers.

There is no widely used AI system that automatically identifies agreements and contradictions across research work.

This is important because:

- A large portion of research time is spent reading and organizing papers  
- Contradictions between studies often go unnoticed  
- Institutions lack AI-driven tools for knowledge mapping  
- Delayed insights lead to redundant or flawed research  

---

## Solution  
This project presents an AI system that analyzes multiple research papers and detects relationships between them using:

- Research PDF ingestion and text extraction  
- Semantic understanding using embeddings (SciBERT)  
- Pairwise relationship classification (AGREE / CONTRADICT / NEUTRAL)  


## Dataset  
- Total records: 460,000+  
- Datasets: MultiNLI, SciTail  

### Target Variable:
- AGREE → Same findings  
- CONTRADICT → Opposite claims  
- NEUTRAL → Independent  

### Features Used:
- Sentence pairs from research papers  
- Domain/genre (fiction, government, telephone, travel, slate)  
- Annotator confidence labels  

---

## Model  
A SciBERT Sequence Classifier is used for conflict detection.

### Configuration:
- Model: allenai/scibert_scivocab_uncased  
- Task: Sequence Classification  
- Classes: AGREE · CONTRADICT · NEUTRAL  

### Performance:
- Accuracy: ~90–95%  
- Inter-annotator agreement: 88.7%  
- Balanced precision and recall  

---

## Features  
- User-friendly web interface  
- Multi-PDF upload and processing  
- Instant conflict and consensus detection  
- Confidence scoring for every relationship  
- Citation graph visualization (support / contradict / neutral edges)  
- Interactive cross-paper Q&A  
- Key sentence highlighting for interpretability  

---

## Tech Stack  
- Python  
- PyTorch  
- HuggingFace Transformers, SciBERT  
- Scikit-learn, NetworkX  
- Next.js / React  
- FastAPI  
- MongoDB Atlas  
- Replit (deployment)  

---



## Impact  

- Helps researchers detect contradicting studies before building on flawed foundations  
- Enables faster literature review and knowledge synthesis  
- Supports institutions in mapping knowledge gaps across disciplines  
- Reduces time spent on manual paper comparison  

---

## Future Scope  

- Integration with real-time Arxiv and PubMed APIs  
- Interactive graph visualization with zoom and filters  
- LLM-powered Q&A using GPT or LLaMA  
- Automated conflict alert system for newly published papers  
- Multilingual support using multilingual BERT  

---

## Limitations  

- Depends on dataset quality  
- Complex scientific language may reduce accuracy  
- Requires manual PDF upload  
- Full system integration is still evolving  

---

## Team  
Team Stack  

Mehak Sayed  
Vageesh S M  
Khushi Kapali  
