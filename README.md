# 🩺 DiabeCare AI – Smart Diabetes Management & Insulin Dose Calculator

DiabeCare AI is an intelligent healthcare platform designed to help diabetic patients manage their condition more effectively. The system combines insulin dose calculation, AI-powered diabetes assistance, medical report analysis, and personalized dietary recommendations into a single application.

Built using **React, TypeScript, FastAPI, LangChain, LangGraph, Groq LLM, ChromaDB, Supabase, and Retrieval-Augmented Generation (RAG)**, the platform delivers secure and personalized diabetes support.

---

# ⭐ Features

## 🧮 Smart Insulin Dose Calculator

* Calculates insulin dosage based on:

  * Carbohydrate intake
  * Insulin-to-Carb Ratio (I:C)
  * Total Daily Dose (TDD)
  * Correction Factor
  * Target Blood Glucose
* Supports Indian and International food items.
* Provides quick and accurate insulin recommendations.

---

## 🤖 AI Diabetes Health Coach

* AI-powered conversational assistant.
* Answers diabetes-related queries.
* Provides personalized diabetic-friendly food suggestions.
* Recommends low Glycemic Index (GI) meals.
* Supports Indian dietary habits.

Examples:

* Best breakfast for diabetes
* Foods to avoid with high HbA1c
* Daily meal planning
* Blood sugar management tips

---

## 📄 Medical Report Analysis

* Upload pathology reports in PDF format.
* Automatically extracts important medical information.
* Analyzes:

  * HbA1c
  * Fasting Blood Sugar
  * Postprandial Blood Sugar
  * Glucose Trends
* Generates simplified patient-friendly explanations.

---

## 🔍 Retrieval-Augmented Generation (RAG)

* Converts uploaded reports into vector embeddings.
* Stores report chunks in ChromaDB.
* Retrieves relevant medical information before generating responses.
* Enables context-aware report discussions.

---

## 🌐 Real-Time Web Search

* Uses Tavily Search integration.
* Retrieves current diabetes-related information.
* Provides updated healthcare insights and recommendations.

---

## 👤 User Management

* Secure authentication.
* Personalized user sessions.
* Medical data tracking.
* Future-ready for patient history management.

---

# 🔐 Security Features

## Authentication & Privacy

* Secure user login system
* Session-based interactions
* Protected patient information
* No exposure of API secrets

## Data Protection

* Environment variable based secret management
* Secure backend communication
* Report processing on server-side
* HTTPS-ready architecture

---

# 🏗️ System Architecture

```text
User
  │
  ▼
React Frontend
  │
  ▼
FastAPI Backend
  │
  ├── Groq LLM
  ├── Tavily Search
  ├── ChromaDB Vector Store
  ├── HuggingFace Embeddings
  └── PDF Report Processing
           │
           ▼
      AI Response
```

---

# 🧰 Technology Stack

## Frontend

* React.js
* TypeScript
* Vite
* Tailwind CSS
* ShadCN UI
* Radix UI
* React Hook Form
* Zod
* TanStack Query

## Backend

* FastAPI
* Python
* LangChain
* LangGraph
* ChromaDB
* Pydantic

## AI & Machine Learning

* Groq (Llama 3.3 70B)
* HuggingFace Embeddings
* RAG Pipeline
* Vector Search

## Search

* Tavily Search API

## Database & Storage

* Chroma Vector Database
* Session-Based Memory

---

# 📦 Getting Started

## Prerequisites

* Node.js 18+
* Python 3.10+
* Git
* Groq API Key
* Tavily API Key

---

# 🌍 Environment Variables

## Backend (.env)

```env
GROQ_API_KEY=your_groq_api_key

TAVILY_API_KEY=your_tavily_api_key
```

---

# ⚙️ Installation

## Clone Repository

```bash
git clone https://github.com/your-username/DiabeCare-AI.git

cd DiabeCare-AI
```

---

## Frontend Setup

```bash
npm install

npm run dev
```

Frontend runs on:

```text
http://localhost:5173
```

---

## Backend Setup

Create virtual environment:

```bash
python -m venv venv
```

Activate environment:

### Windows

```bash
venv\Scripts\activate
```

### Linux/Mac

```bash
source venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Start API server:

```bash
uvicorn api:app --reload
```

Backend runs on:

```text
http://localhost:8000
```

---

# 📁 Project Structure

```text
DiabeCare-AI/
│
├── src/
│   ├── components/
│   ├── pages/
│   ├── hooks/
│   ├── services/
│   └── utils/
│
├── api.py
│
├── temp_uploads/
│
├── vector_store/
│
├── public/
│
├── .env
│
└── README.md
```

---

# 🧪 Usage

## Step 1: Open Application

Launch frontend and backend servers.

---

## Step 2: Calculate Insulin Dose

Enter:

* Food item
* Quantity
* Blood glucose values
* Personal insulin settings

Receive:

* Carb-based insulin
* Correction insulin
* Total recommended dose

---

## Step 3: Upload Medical Report

Upload PDF report.

The system will:

* Extract report contents
* Generate embeddings
* Store in vector database

---

## Step 4: Chat with AI

Ask questions such as:

* What does my HbA1c mean?
* Is my blood sugar normal?
* Suggest a diabetic meal plan.
* Explain my medical report.

---

# 📈 Future Enhancements

* 📸 AI Food Recognition using Camera
* 📱 Android & iOS Application
* 🩺 Doctor Dashboard
* ⌚ Smart Glucometer Integration
* 📊 Blood Sugar Trend Analytics
* 🔔 Medicine & Meal Reminders
* 🌍 Multi-Language Support
* 🤖 Predictive Diabetes Risk Analysis

---

# 🛡️ Disclaimer

DiabeCare AI is intended for educational and supportive purposes only.

The insulin recommendations and medical insights generated by the system should not replace professional medical advice, diagnosis, or treatment.

Always consult a qualified healthcare professional before making medical decisions.

---

# 👩‍💻 Author

**Srushti Dhanawade**

Final Year Computer Engineering Student

Passionate about AI, Healthcare Technology, Full-Stack Development, and Data-Driven Solutions.

---

# 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push the branch
5. Open a Pull Request

Contributions are always welcome!

