# Resume and Job Skill Matching using Hybrid NLP (Rule-Based + Transformers)

This project started as a TF-IDF matching system. It worked, but it only saw text as word counts. The updated version keeps the original idea but adds real language understanding by combining **rule-based skill extraction** with **transformer-based NER** and **RoBERTa embeddings**.

Not a new project.  
Just a smarter version of the original one.

---

## 🚀 What This Project Does

Given a resume and a set of job descriptions, the system:

1. Extracts skills using **two methods together**:  
   - A **rule-based skill dictionary / keyword matcher**  
   - A **transformer-based NER model** (HuggingFace pipeline)

2. Merges and deduplicates the extracted skills

3. Generates contextual embeddings using a **RoBERTa SentenceTransformer**

4. Computes similarity between the resume and job descriptions

5. Ranks and returns the best-matching roles

This hybrid approach mixes precision (rule-based) with intelligence (transformers).

---

## 🧩 Why Hybrid Skill Extraction?

Your code doesn't rely on a single method. It uses both because:

### Rule-based  
✔ Very accurate for known skills  
✔ Fast  
✔ Good for domain-specific terms  
➤ Weak at discovering new/hidden skills

### Transformer NER  
✔ Recognizes skills even if phrased differently  
✔ Handles synonyms and variations  
✔ Finds entities your skill list doesn’t know  
➤ Can produce noise or miss niche technical terms

### Both Together  
You get the best of both.  
High recall. High precision. No blind spots.

---

## 🔥 What’s New vs Original Version

| Original Version (TF-IDF) | Updated Version (Hybrid + Transformers) |
|---------------------------|------------------------------------------|
| TF-IDF only | Rule-based extraction + transformer NER |
| No entity recognition | Detects skills, tools, certifications |
| Bag-of-words | Semantic RoBERTa embeddings |
| Keyword overlap | Context-aware similarity |
| Limited accuracy | Stronger, more realistic matching |

---

## 🧠 Why RoBERTa?

RoBERTa is a toughened-up BERT: better training, more robust, and ideal for semantic similarity.  
SentenceTransformers gives clean embeddings ready for cosine similarity.

You chose RoBERTa because it balances accuracy and speed.

---

## 📌 Pipeline Overview

**1. Extract text from resume (PDF → text)**  
Via PyPDF2.

**2. Clean and normalize text**  
Lowercasing, regex cleanup, etc.

**3. Extract skills using TWO methods**  
- Rule-based skill dictionary  
- Transformer NER pipeline  

**4. Merge + dedupe skills**  
Your code does this explicitly.

**5. Encode resume + job descriptions using RoBERTa**  
SentenceTransformer embeddings.

**6. Compute cosine similarity**  
Compare resume embedding with each job embedding.

**7. Output ranked matches**

---
## 🧰 Tech Stack

- Python  
- PyPDF2  
- Transformers (NER)  
- SentenceTransformers (RoBERTa)  
- PyTorch  
- Pandas  
- scikit-learn  
- Google Colab/Notebook

- ## 🚧 Future Improvements

- Skill-gap detection  
- Resume rewriting suggestions  
- Job clustering / domain detection  
- Web deployment (Streamlit)  
- Fine-tuned domain-specific transformer model  

## 📊 Sample Output

