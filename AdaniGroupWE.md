
## 💼 Adani Group, Gurgaon | Ahmedabad
**Role:** Assistant Manager - Technology\
**Duration:** Oct 2023 – Present

---


# Detailed Project Summary

### 🏥 (Healthcare Module) Intelligent Automation in Healthcare Systems

Integrated a new line of business into the enterprise EHR application, enabling seamless onboarding of clinical workflows. Leveraged **Google Speech-to-Text** and **custom NLP pipelines** to automate doctor-patient interactions, converting spoken consultations into structured medical notes.

To further enhance clinical productivity, developed a **LangChain + GPT-4 powered clinical assistant chatbot** capable of:
- Summarizing patient history from EHR records.
- Generating draft prescriptions based on symptoms and prior diagnoses.
- Interacting in real-time with doctors using natural language.

**Why**  
To reduce the administrative burden on healthcare professionals and improve clinical accuracy through intelligent, autonomous agents.

**Impact:**  
✅ Reduced documentation time by **70%**  
✅ Improved prescription accuracy by **85%**  
✅ Scaled to support **1,000+ daily interactions**

---

### 👥(Employee Attendance Data Management Tool) Scalable Employee Attendance Data Management

Led the end-to-end development of a centralized attendance data platform for **50,000+ employees**. Unified disparate data sources into a **single SQL-based data lake** using Python ETL pipelines. Built robust backend microservices in **Node.js** and **Python**, supporting a React-based frontend for HR operations.

Integrated **agentic AI** in two key areas:
- A **predictive analytics agent** that detects anomalies in attendance patterns using historical trends.
- A **RAG-based HR chatbot** that answers employee queries on attendance and leave policies by retrieving relevant data and generating responses using OpenAI.

**Why**  
To enable real-time, conversational access to HR data and automate insights for proactive workforce management.

**Impact:**  
✅ Reduced data retrieval time by **80%**  
✅ Enhanced decision-making accuracy by **90%**

---

### 📊 (Talent Acquisition Dashboard) AI-Powered Talent Acquisition Dashboard & Data Lake Development

Built a comprehensive **talent acquisition dashboard** and centralized **data lake** by integrating data from **Oracle Fusion, HRMS, and Tydy** using APIs and SQL. Ensured **97% data accuracy** and implemented an **admin portal** for secure access control.

Deployed a suite of **agentic AI capabilities** to automate and optimize recruitment:
  - **Recruiter Assistant Chatbot**: Built with **LangChain Agents + OpenAI**, enabling recruiters to:
  - Retrieve real-time hiring metrics (e.g., open requisitions, pipeline status).
  - Summarize candidate profiles and interview feedback.

**Why**  
To reduce manual effort, improve candidate-job fit, and empower recruiters with intelligent, conversational tools.

**Impact:**  
✅ 90% improvement in reporting efficiency  
✅ 97% enhancement in data security and accuracy  
✅ Significant boost in recruiter productivity and hiring quality

---

### 🔊 **Google Speech-to-Text Integration**
You integrated Google’s Speech-to-Text API to transcribe real-time doctor-patient conversations into structured text. This was achieved by:
- Capturing audio streams from consultation sessions.
- Using Google’s API to convert speech into text with medical vocabulary support.
- Feeding the transcribed text into downstream NLP pipelines for further processing.

**Why this was done:**  
To eliminate the need for manual note-taking during consultations and ensure accurate, real-time capture of clinical interactions.

---

### 🧠 **Custom NLP Pipelines**
You built custom NLP pipelines to extract and structure clinical information from the transcribed text. This included:
- **Named Entity Recognition (NER)** to identify symptoms, medications, and diagnoses.
- **Intent classification** to detect the purpose of the conversation (e.g., diagnosis, follow-up).
- **Section segmentation** to organize the conversation into SOAP format (Subjective, Objective, Assessment, Plan).
- **Custom APIs** were developed using Python (FastAPI/Flask) to expose these NLP services, which were then consumed by the LangChain-based clinical assistant.

**Why this was done**  
To transform unstructured conversation data into structured clinical summaries and enable the GPT-4 assistant to generate accurate draft prescriptions and patient notes.

---

## 🏥 **Healthcare Module – Deep Dive**

### 🔧 **1. Problem Statement**
Doctors were spending too much time on documentation and manual prescription writing. The goal was to:
- Automate doctor-patient interactions.
- Summarize patient history.
- Generate prescriptions using AI.
- Integrate this into the existing EHR (Electronic Health Record) system.

---

### 🧠 **2. Architecture Overview**

#### 🗣️ **Step 1: Voice-to-Text Conversion**
- **Tool Used**: Google Speech-to-Text API
- **Purpose**: Convert real-time doctor-patient conversations into text.
- **How**: 
  - Audio stream captured via a web or mobile interface.
  - Sent to Google API for transcription.
  - Output: Cleaned and timestamped text.

#### 🧾 **Step 2: NLP Pipeline for Preprocessing**
- **Custom NLP Pipeline**:
  - **Text Cleaning**: Remove filler words, noise.
  - **Entity Recognition**: Identify symptoms, medications, patient details.
  - **Intent Detection**: Understand what the doctor is trying to do (e.g., diagnose, prescribe).

---

### 🤖 **3. LangChain + GPT-4 Integration**

#### 🧩 **LangChain Role**
LangChain acts as the **orchestration layer** between your tools and the LLM (GPT-4). It helps:
- Manage **memory** (e.g., patient history).
- Route tasks to the right **tools or agents**.
- Handle **multi-step reasoning**.

#### 🧠 **GPT-4 Role**
- Summarizes patient history.
- Suggests possible diagnoses.
- Generates prescription drafts.
- Responds to doctor queries in real time.

---

### 🧑‍💼 **4. Agents in LangChain**

#### What is an Agent?
An **agent** is an intelligent component that:
- Decides **which tool to use** based on the user’s input.
- Can **reason step-by-step** using the LLM.
- Example: If a doctor says, “Summarize last 3 visits,” the agent:
  - Fetches data from EHR.
  - Sends it to GPT-4 for summarization.
  - Returns a concise summary.

#### Tools Used by Agents:
- **EHR API**: To fetch patient data.
- **Prescription Generator**: A custom tool to format prescriptions.
- **Knowledge Base**: For medical guidelines (possibly using RAG – Retrieval-Augmented Generation).

---

### 📊 **5. Impact Metrics**
- **70% reduction** in documentation time.
- **85% improvement** in prescription accuracy.
- **1,000+ daily interactions** handled smoothly.

---

### 🧰 **6. Tech Stack Summary**
| Component | Tool/Tech |
|----------|-----------|
| Voice Input | Google Speech-to-Text |
| NLP | Custom Python pipeline (spaCy, NLTK, etc.) |
| LLM | GPT-4 via OpenAI API |
| Orchestration | LangChain |
| Backend | Python (FastAPI/Flask), Node.js |
| Frontend | React.js |
| Integration | REST APIs with EHR |
| Deployment | Azure, Docker |

---
