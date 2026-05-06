AI Research Synthesizer with Conflict Mapping
Dev Delight Hack 2025 | Team Stack

"Don't read 100 papers. Understand all of them in minutes."

Live Demo
https://data-flow-hub--kapalikhushi8.replit.app
Problem Statement
Every research cycle, hundreds of papers are published on overlapping topics. Current systems are manual and respond only after researchers have spent weeks reading. There is no widely used AI-based system that automatically maps agreements and contradictions across research papers.
This is important because:

A large portion of research time is spent just reading and organizing papers
Contradictions between published studies go undetected and mislead future work
Institutions lack AI-driven tools to prioritize and connect knowledge
Delayed insight discovery leads to redundant or flawed research

Solution
This project presents an AI system that detects relationships across research papers using three key inputs:

Uploaded research PDFs (text extraction)
Semantic embeddings (SciBERT)
Pairwise relationship classification (AGREE / CONTRADICT / NEUTRAL)

Example:

Paper A: "Transformers outperform RNNs on NLI tasks" + Paper B: "LSTMs remain competitive on domain-specific NLI" → CONTRADICT (~88% confidence)
Paper A: "BERT achieves 86.7% on MultiNLI" + Paper B: "RoBERTa achieves 90.8% on MultiNLI" → AGREE (~94% confidence)

Dataset

Total records: 460,000+
Datasets: MultiNLI, SciTail
Target variable:

AGREE = papers support same finding
CONTRADICT = papers make opposing claims
NEUTRAL = papers are independent



Features used:

sentence pairs from research papers
domain genre (fiction, government, telephone, travel, slate)
annotator confidence labels

Model
A SciBERT Sequence Classifier is used for conflict detection.
Configuration:

Model: allenai/scibert_scivocab_uncased
Task: Sequence Classification
Output classes: AGREE · CONTRADICT · NEUTRAL

Performance:

Accuracy: ~90–95%
Inter-annotator agreement: 88.7%
Precision / Recall: balanced across all three classes

Features

User-friendly web interface
Multi-PDF upload and processing
Instant conflict and consensus detection
Confidence scoring for every relationship
Citation graph visualization (support / contradict / neutral edges)
Interactive cross-paper Q&A
Key sentence highlighting for interpretability

Tech Stack

Python
PyTorch
HuggingFace Transformers, SciBERT
Scikit-learn, NetworkX
Next.js, FastAPI
MongoDB Atlas
Replit (deployment)

How to Run

Clone the repository: git clone https://github.com/YOUR_USERNAME/ai-research-synthesizer.git
Install dependencies: pip install -r requirements.txt
Set environment variables: MONGO_URI and NEXT_PUBLIC_API_URL
Run backend: uvicorn main:app --reload
Run frontend: npm run dev

Impact

Helps researchers identify contradicting studies before building on flawed foundations
Supports institutions in mapping knowledge gaps across disciplines
Gives analysts the ability to understand large paper corpora in minutes
Assists journals in detecting inconsistencies across submissions

Future Scope

Integration with real-time Arxiv and PubMed APIs
Interactive graph visualization with zoom and filters
LLM-powered Q&A using GPT or Llama
Automated conflict alert system for newly published papers
Multilingual support using multilingual BERT

Limitations

Depends on dataset quality
Complex scientific language may reduce accuracy
Requires manual PDF upload
Full system integration is still evolving

Team
Team Stack

Mehak Sayed
Vageesh S M
Khushi Kapali
