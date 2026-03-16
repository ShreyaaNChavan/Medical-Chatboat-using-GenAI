# **Medical-Chatbot-using-GenAI**

A **medical knowledge-based chatbot** using a large medical book, Pinecone vector database, and large language models (LLMs) for semantic question answering.

---


### **Workflow Steps**

1. **Document Extraction:** Extract text from the medical book.
2. **Chunking:** Divide text into smaller chunks for processing.
3. **Vectorization:** Generate embeddings to represent chunks semantically.
4. **Knowledge Base:** Store embeddings in Pinecone for semantic search.
5. **Query Handling:** User inputs a question; the system searches relevant chunks.
6. **LLM Processing:** Pass context to LLMs (OpenAI, Gemini, Gorg) to generate a response.
7. **Response:** Return the answer to the user.

---
![Medical Chatbot Architecture](https://miro.medium.com/v2/resize:fit:1400/1*J7vyY3EjY46AlduMvr9FbQ.png)

## **How to Run**

### **STEP 0 — Clone the repo**

```bash
git clone https://github.com/<your-repo>/Medical-Chatbot-using-GenAI.git
cd Medical-Chatbot-using-GenAI
```

### **STEP 1 — Create and activate a Python environment**

```bash
python -m venv llmapp
```

Activate environment:

* **Windows**

```bash
llmapp\Scripts\activate
```

* **Mac/Linux**

```bash
source llmapp/bin/activate
```

### **STEP 2 — Install dependencies**

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### **STEP 3 — Setup `.env` file**

Create a `.env` file in the project root to store API keys and configuration.
Load it in Python as needed.

### **STEP 4 — Initialize Pinecone**

Setup your Pinecone API and index to store embeddings.

### **STEP 5 — Initialize Groq / OpenAI / Gemini LLM**

Connect to the desired LLM using credentials from `.env`.

### **STEP 6 — Setup RAG (Retrieval-Augmented Generation) Chain**

* Query the vector database
* Retrieve relevant chunks
* Pass chunks to LLM for answer generation

### **STEP 7 — Query your chatbot**

Run the chatbot script or web app and enter medical queries.

### **STEP 8 — Optional: List available LLM models**

This ensures you are using the correct `model_name`.

---


