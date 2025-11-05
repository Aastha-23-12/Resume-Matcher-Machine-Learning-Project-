# Resume-Matcher-Machine-Learning-Project-
A smart Resume Matcher app using Flask, scikit-learn, and ML to rank resumes against a job description. It extracts text, identifies skills, calculates match scores via TF-IDF and Cosine Similarity, and visualizes results with a Confusion Matrix. Supports bulk uploads and live deployment via Ngrok.

# Resume Matcher 

## Overview
This is a Flask web application that matches uploaded resumes to a job description using TF-IDF vectorization and **cosine similarity**. It also extracts a predefined list of skills from the job description and each resume and reports a confusion-matrix style breakdown (True Positives, False Positives, False Negatives) for each resume.

## Features
- Upload multiple resumes (`.pdf`, `.docx`, `.txt`) via a web form.
- Extract text from each resume (PyPDF2, docx2txt).
- Extract skills from both Job Description and Resumes using a predefined SKILL_SET.
- Compute TF-IDF vectors for job + resumes and compute cosine similarity and Eucliden distnce.
- Return matching resumes sorted by highest similarity (%).
- Display extracted skills and confusion-matrix per resume.

## Requirements
- Python 3.8+
- Install dependencies:
```bash
pip install flask PyPDF2 docx2txt scikit-learn

File Structure 
app_cosine/
├─ app.py
├─ templates/
│  └─ index.html
├─ uploads/           # created at runtime
└─ README.md

