# Resume Evaluator

An AI-powered Resume–Job Description matching system built with **Python, Pydantic, Groq LLMs, and document parsing**.

The application takes a Job Description and one or more resumes, extracts structured information from both, and uses an LLM to evaluate how well a candidate's resume matches the requirements of the job.

---

## 🚀 Features

- 📄 Accepts resumes in **PDF and Word (.docx)** formats
- 📝 Takes any **Job Description (JD)** as text input
- 🔍 Automatically extracts clean text from resumes
- 🧩 Uses **Pydantic models** for structured data extraction
- 🤖 Uses **Groq LLM API** for intelligent Resume–JD matching
- 🎯 Generates a **match score**
- ✅ Provides a **match verdict**
- 💡 Generates reasoning behind the evaluation
- 🌡️ Uses **temperature = 0** for consistent evaluation
- 🧾 Uses **JSON mode / structured output** for reliable parsing
- 💰 Considers token usage for efficient LLM API calls

---

## 🧠 How It Works

The application follows an end-to-end AI evaluation pipeline:

```text
                Job Description
                      │
                      ▼
              JD Text Processing
                      │
                      ▼
             Pydantic Extraction
                      │
                      │
                      ▼
                ┌───────────┐
                │   LLM     │
                │  Matching │
                └───────────┘
                      ▲
                      │
             Pydantic Extraction
                      ▲
                      │
            Resume Text Extraction
                      ▲
                      │
              PDF / DOCX Resume
                      │
                      ▼
              Clean Resume Text
