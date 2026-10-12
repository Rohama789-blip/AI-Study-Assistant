# 📚 StudySpace — AI Learning Companion

> Your personal AI tutor that helps you understand, summarize, and revise your study materials using Retrieval-Augmented Generation (RAG).

StudySpace is an AI-powered learning companion that allows students to upload PDF chapters and ask questions about their study material. It retrieves relevant information from uploaded documents and uses AI to generate clear, context-based answers.

## ✨ Features

- 📄 **PDF Upload:** Upload up to 5 PDF chapters.
- 🔍 **Semantic Search:** Retrieve relevant passages using vector embeddings.
- 🤖 **AI Question Answering:** Ask questions about your uploaded study materials.
- 🧠 **RAG Pipeline:** Generate answers using retrieved document context.
- 📝 **Study Assistance:** Summarize main ideas, explain key concepts, and create revision notes.
- 📚 **Document Library:** Manage your uploaded learning material.
- ⚡ **FastAPI Backend:** Serve application functionality through API endpoints.
- 🎨 **Interactive UI:** Clean workspace designed for a better learning experience.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Core application logic |
| FastAPI | Backend API |
| ChromaDB | Vector database |
| Sentence Transformers | Text embeddings |
| Groq | AI-powered responses |
| HTML & CSS | User interface |
| JavaScript | Frontend interactions |
| PyPDF | PDF text extraction |

## 🏗️ How It Works

StudySpace follows a Retrieval-Augmented Generation (RAG) workflow:

1. **Upload:** Upload PDF chapters through the web interface.
2. **Extract:** Extract text from the uploaded PDFs.
3. **Chunk:** Split the extracted text into smaller sections.
4. **Embed:** Convert text chunks into vector embeddings using Sentence Transformers.
5. **Index:** Store the embeddings in ChromaDB.
6. **Retrieve:** Search for relevant chunks when a user asks a question.
7. **Generate:** Use Groq to generate an answer based on the retrieved context.

## 📂 Project Structure

```text
ai_study_assistant/
├── main.py
├── backend/
│   ├── pdf_processor.py
│   └── rag.py
├── templates/
│   └── index.html
├── static/
│   ├── style.css
│   └── script.js
├── uploaded_pdfs/
├── requirements.txt
├── .env
├── .gitignore
└── README.md
```

*Note: Adjust the project structure above to match the actual files in your repository.*

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/Rohama789-blip/AI-Study-Assistant.git
cd ai_study_assistant
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables

Create a `.env` file in the project root directory.

Add your actual API credentials:

```dotenv
GROQ_API_KEY=your_groq_api_key
CHROMA_API_KEY=your_chroma_api_key
CHROMA_TENANT=your_chroma_tenant_id
CHROMA_DATABASE=study-assistant
```

Replace the placeholder values with your actual credentials. Create the Chroma Cloud database if required by your configuration.

**Security:** Never commit your `.env` file or expose API keys in your source code.

### 5. Run the Application

If your FastAPI instance is defined as `app` in `main.py`, run:

```bash
uvicorn main:app --reload
```

Open your browser:

**http://127.0.0.1:8000**

## 💡 Example Questions

After uploading your PDF chapters, try asking:

- Summarize the main ideas of this chapter.
- Explain the key concepts in simple language.
- Create revision notes from this material.
- What are the most important topics in this chapter?
- Explain a particular concept discussed in the uploaded PDF.

## 🔐 Environment Variables

| Variable | Description |
|---|---|
| `GROQ_API_KEY` | API key for Groq AI |
| `CHROMA_API_KEY` | Chroma Cloud API key |
| `CHROMA_TENANT` | Chroma Cloud tenant identifier |
| `CHROMA_DATABASE` | Chroma database name |

Keep all credentials private and configure them through environment variables.

## 🔮 Future Improvements

- Automatic flashcard generation
- Practice quizzes based on uploaded chapters
- PDF source references in AI responses
- Persistent chat history
- Improved document management
- Deployment for online access

## 🎯 Project Goal

The goal of StudySpace is to make learning more interactive and accessible by helping students understand their own study materials with the assistance of AI.

## 👩‍💻 Contributing

Contributions, suggestions, and bug reports are welcome. Feel free to open an issue or submit a pull request.

---

**Built with ❤️ using FastAPI, ChromaDB, Sentence Transformers, and Groq.**
