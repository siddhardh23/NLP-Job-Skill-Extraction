# Resume and Job Skill Matching using Transformers

This project began as a simple TF-IDF based resume–job description matcher. It worked, but it treated text like a pile of disconnected words. Now it uses modern NLP: RoBERTa embeddings and transformer-based NER. Same project, smarter engine.

The goal is still the same: extract skills, understand resumes, understand job descriptions and match them in a meaningful, context-aware way.

---

## 🚀 What This Project Does

Given a resume and a set of job descriptions, the system:

1. Extracts skills, tools, and key entities using a transformer-based NER model  
2. Generates contextual embeddings using a RoBERTa SentenceTransformer model  
3. Computes semantic similarity between the resume and each job description  
4. Ranks and returns the best-fit roles  

The result is a job-matching pipeline that actually understands the text instead of counting keywords.

---

## 🔁 What’s New (Updated, Not Replaced)

| Old Approach (TF-IDF) | Updated Approach (Transformers) |
|------------------------|---------------------------------|
| Word frequency only | Full semantic meaning |
| No entity awareness | NER-based skill extraction |
| Basic cosine similarity | Embedding-level similarity |
| Keyword overlap | Contextual understanding |
| Limited accuracy | More realistic job-fit scoring |

The project keeps its original workflow and purpose but upgrades the intelligence behind it.

---

## 🧠 Why RoBERTa?

RoBERTa is a better-trained, more stable sibling of BERT.  
It handles semantic similarity very well and balances speed with accuracy.  
Perfect for resume–job understanding without the overhead of huge LLMs.

---

## 🧩 Why NER?

Resumes and job descriptions hide their most important info in long text blocks.  
NER pulls out real entities:

- Skills  
- Tools / frameworks  
- Roles  
- Certifications  
- Technologies  

This makes matches more grounded and intentional.

---

## 📌 Pipeline Overview

**1. Parse Resume**  
PDF text extraction with PyPDF2.

**2. Clean + Normalize Text**  
Lowercasing, special-character cleanup.

**3. Extract Skills using NER**  
Transformer-based token-classification pipeline.

**4. Generate Embeddings**  
RoBERTa SentenceTransformer produces contextual vectors.

**5. Compute Similarity**  
Cosine similarity between resume embedding and job embeddings.

**6. Rank Matches**  
Return highest scoring job descriptions.

---


These scores are now meaning-based, not keyword-based.

---

## 🧰 Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core language |
| PyPDF2 | Resume PDF parsing |
| Transformers | NER + embeddings |
| SentenceTransformers | RoBERTa model |
| PyTorch | Backend |
| Pandas | Data manipulation |
| scikit-learn | Cosine similarity |
| Google Colab | Development environment |

---

## 🚧 Future Improvements

- Skill-gap analysis  
- Auto-rewriting resume sections  
- Cluster jobs by domain  
- Deploy with a Streamlit UI  
- Fine-tune a domain-specific model  



