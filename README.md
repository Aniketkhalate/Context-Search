# Context-Search
The RAG (Retrieval-Augmented Generation) is an innovative solution designed to transform how we interact with document-based data. Leveraging advanced technologies like LangChain, prompt templates, and the PHI-3 LLM model from Ollama, this project efficiently processes PDF documents to deliver precise and well-structured responses to user queries.

### Key Components and Workflow:

<ins> **1. PDF Document Ingestion:** </ins>
- The system starts by accepting PDF documents as input. These documents can be rich in information across various topics.

<ins> **2. Vector Store Creation:** </ins>
- Once the PDFs are ingested, the content is processed to create a vector store. This involves generating embeddings for different sections of the documents, allowing for efficient retrieval of relevant information.

<ins> **3. Query Handling:** </ins>
- When a user submits a query, the system searches the vector store to find the most relevant parts of the documents. The retrieved sections are then used to construct a comprehensive response.

<ins> **4. Response Generation with PHI-3:** </ins>
- The PHI3 LLM model from Ollama plays a crucial role in generating the final response. It takes the relevant document parts and integrates them into a coherent and well-structured output.
