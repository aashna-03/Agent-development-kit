# Vertex AI RAG Agent

A conversational AI agent built with [Google ADK (Agent Development Kit)](https://google.github.io/adk-docs/) that enables natural language interaction with **Vertex AI RAG (Retrieval-Augmented Generation)** corpora.

The agent can create, manage, query, and delete document corpora hosted on Google Cloud's Vertex AI platform.

---

## 🚀 How It Works

```mermaid
flowchart TD
    User["👤 User"] -->|Natural language| Agent["🤖 RAG Agent<br/>Gemini 2.5 Flash"]
    Agent -->|Tool calls| Tools["🛠️ ADK Tools"]
    Tools -->|Vertex AI SDK| VertexRAG["☁️ Vertex AI<br/>RAG Corpus"]
    VertexRAG -->|Embeddings| EmbedModel["📐 text-embedding-005"]
    VertexRAG -->|Chunked Docs| VectorStore["🗄️ Managed Vector Store<br/>Google Cloud"]

Setup & Installation
Prerequisites

Before running the project, make sure you have the following installed and configured:

Python 3.9+
A Google Cloud project with the Vertex AI API enabled
Google Cloud CLI (gcloud) installed
GCP authentication configured
1. Clone the Repository
git clone <your-repo-url>
cd adk
2. Create and Activate a Virtual Environment

Create a Python virtual environment:

python -m venv venv
Windows
venv\Scripts\activate
macOS / Linux
source venv/bin/activate
3. Install Dependencies

Install the required Python packages:

pip install -r requirements.txt
4. Configure Environment Variables

Create a .env file inside the rag_agent/ directory:

GOOGLE_CLOUD_PROJECT="your-gcp-project-id"
GOOGLE_CLOUD_LOCATION="us-central1"
GOOGLE_GENAI_USE_VERTEXAI="True"
GEMINI_API_KEY="your-api-key"


5. Authenticate with Google Cloud

Authenticate using Google Cloud Application Default Credentials:

gcloud auth application-default login


6. Launch the ADK Web UI

Start the ADK web interface:

adk web

The ADK web UI can then be used to interact with and test the RAG agent.
