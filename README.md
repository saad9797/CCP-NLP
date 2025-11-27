# **RAG-Based n8n Chatbot for Educational Institutions**

This project provides **ready-to-use n8n workflows** that allow anyone to build a hybrid SQL + Vector (RAG) chatbot. The workflows can be copied directly from this repository and pasted into n8n — no cloning or installation required.

The chatbot integrates:

* PostgreSQL (for structured queries)
* Supabase pgvector (for semantic search)
* Google Drive (for document ingestion)
* Gemini API (for answer synthesis)

Just paste the workflow JSON into n8n and enter your credentials.

---

## 🚀 **How to Use This Project**

You don't need Git commands or cloning.

### **Step 1 — Open any workflow JSON file in this repo**

Go to `/workflows/workflow_1.json` or `/workflows/workflow_2.json`.

### **Step 2 — Copy the entire JSON content**

Select all → Copy.

### **Step 3 — Paste into n8n**

Open n8n →
Workflows →
**Add Workflow** →
⋮ menu (top-right) →
**Import from Clipboard** →
Paste JSON → Save.

Your workflow will load instantly.

---

## 🔑 Add Your Credentials in n8n

Once imported, the workflow will ask for four types of credentials.
Add them in:

**Settings → Credentials → Create New**

### **1. PostgreSQL**

Used for SQL-based questions.

```
Host
Port
Database
Username
Password
```

### **2. Supabase**

Required for vector embeddings and semantic search.

```
SUPABASE_URL
SUPABASE_API_KEY
```

### **3. Google Drive**

Used to fetch uploaded documents for embedding.

```
Client ID
Client Secret
Refresh Token
```

### **4. Gemini API**

Used to combine SQL + vector results into a final answer.

```
GEMINI_API_KEY
```

Once all credentials are linked to the nodes, the workflow becomes fully functional.

---

## 🧠 **How the Chatbot Works**

1. User enters a question
2. Workflow checks whether the question is SQL-related
3. SQL query → sent to PostgreSQL
4. Context question → embeddings fetched from Supabase
5. Gemini synthesizes final answer
6. n8n returns response to user

---

## 📁 **Included Workflows**

### **Workflow 1 – Hybrid RAG Query Engine**

Handles:

* Query input
* SQL classifier
* PostgreSQL execution
* Supabase vector semantic search
* Response formatting

### **Workflow 2 – Document Embedding Pipeline**

Handles:

* Reading files from Google Drive
* Generating embeddings
* Storing vectors in Supabase

Copy → paste → add credentials → run.

---

## ⚙️ Prerequisites (minimal)

* n8n (cloud or local)
* PostgreSQL database
* Supabase project with pgvector enabled
* Google Drive API enabled
* Gemini API key

---

## 🎯 Purpose of This Repository

To provide **plug-and-play n8n workflows** that allow anyone to build:

* A database assistant
* Document-based educational chatbot
* Hybrid RAG system
* Institutional Q&A engine

All without any coding.
