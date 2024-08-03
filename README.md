# Context-Search
The RAG (Retrieval-Augmented Generation) is an innovative solution designed to transform how we interact with document-based data. Leveraging advanced technologies like LangChain, prompt templates, and the PHI-3 LLM model from Ollama, this project efficiently processes PDF documents to deliver precise and well-structured responses to user queries.

### Key Components and Workflow for Simple RAG:

<ins> **1. PDF Document Ingestion:** </ins>
- The system starts by accepting PDF documents as input. These documents can be rich in information across various topics.

<ins> **2. Vector Store Creation:** </ins>
- Once the PDFs are ingested, the content is processed to create a vector store. This involves generating embeddings for different sections of the documents, allowing for efficient retrieval of relevant information.

<ins> **3. Query Handling:** </ins>
- When a user submits a query, the system searches the vector store to find the most relevant parts of the documents. The retrieved sections are then used to construct a comprehensive response.

<ins> **4. Response Generation with PHI-3:** </ins>
- The PHI3 LLM model from Ollama plays a crucial role in generating the final response. It takes the relevant document parts and integrates them into a coherent and well-structured output.


## CRAG
Corrective Retrieval-Augmented Generation (CRAG) is a major breakthrough in AI-driven information retrieval and content creation. By integrating real-time corrective feedback and continuous learning, CRAG improves the precision, relevance, and overall quality of generated content.

### Key Components and Workflow for CRAG:
<ins> **1. Text data via blogs:** </ins>
- For the text data we can use some blog posts on topics like LLM Powered Autonomous Agents, Prompt Engineering, and Adversarial Attacks on LLMs by **Lilian Weng**. These posts are a great read you can check out her other blogs as well. We will store the text in a vector store.

<ins> **2. llama3-groq-tool-use:** </ins>
- We will use llama3-groq model via ollama. It is a series of models from Groq that represent a significant advancement in open-source AI capabilities for tool use/function calling. These models have achieved remarkable results, setting new benchmarks for Large Language Models with tool-use capabilities.

<ins> **3. Tavily Search:** </ins>
- It is a search engine built for AI agents so that they can deliver accurate and factual results quickly. Firstly you will need to create an account to access the tavily API. You can integrate it into your RAG implementation using the API key. This gives AI agents the ability to access the internet for information that may be unknown or not updated.

<ins> **4. LangGraph Implementation:** </ins>
- LangGraph is used for building stateful, multi-actor applications with Large Language Models. It extends the LangChain library, allowing you to coordinate multiple chains across multiple steps of computation in a cyclic manner. In this case, the flow of the graph will be as follows: the user will ask the query then if the chunks retrieved are of all relevance agent will pass those chunks along with a prompt to llm and generate a response. But if the documents are not relevant then the agent will rewrite the query and perform a web search, the results will then be added to a prompt and passed to llm and generate an appropriate response.
