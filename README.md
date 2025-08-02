# 📄 Resume-to-Job Matching using NLP

An end-to-end NLP project that compares a candidate’s resume with job descriptions to compute a **similarity score** and recommend the best-fit roles.

## 🚀 Project Highlights

- 🔍 Reads and processes **PDF resumes** using `PyPDF2`
- 🧹 Cleans text using custom preprocessing with stopword removal
- 🧠 Uses **TF-IDF + Cosine Similarity** to match resumes with job listings
- 📊 Ranks job descriptions based on relevance to your resume
- 📂 Built in **Google Colab** for easy use and reproducibility

## 🧰 Tech Stack

| Tool | Purpose |
|------|---------|
| `Python` | Core language |
| `Pandas` | Data handling |
| `scikit-learn` | TF-IDF + similarity |
| `PyPDF2` | PDF resume parsing |
| `Colab` | Interactive execution |
| `regex` | Text cleaning |

## 📁 File Structure

```
├── NLP_project.ipynb              # Original notebook
├── clean_jobs.csv                 # Preprocessed job descriptions
├── Siddhardha_Naidu_Gorja_Resume.pdf # Input resume file
├── README.md                      # This file
```

## 📌 How It Works

1. **Upload your resume** as a PDF in Colab.
2. **Upload the cleaned job data** CSV.
3. The notebook:
   - Cleans and tokenizes both texts
   - Converts them into TF-IDF vectors
   - Scores each job using **cosine similarity**
4. Outputs the **top job matches** along with match scores.

## 📊 Sample Output

```
| Job Title                         | Similarity Score |
|----------------------------------|------------------|
| Data Analyst                     | 0.159            |
| Data Scientist                   | 0.157            |
| ICICI Securities - Data Analyst | 0.155            |
```

## ✅ Use Cases

- Tailor your resume based on job fit
- Identify **high-fit roles** to apply for
- Use as a **resume booster project** on your portfolio or LinkedIn

## 💡 Future Work

- [ ] Add skill gap detection
- [ ] Auto-generate custom cover letters
- [ ] Deploy with Streamlit for web interface
- [ ] Add resume section parsing with NLP

## 👨‍💻 Author

**Siddhardha Naidu Gorja**  
📍 Koblenz, Germany  
🔗 [LinkedIn](https://linkedin.com/in/siddhardha23g)  
💻 [GitHub](https://github.com/siddhardh23)

## 🧠 Bonus Tip for Recruiters

This project isn't just a demo — it's how I **tailor my applications** using NLP. Let’s talk data.
