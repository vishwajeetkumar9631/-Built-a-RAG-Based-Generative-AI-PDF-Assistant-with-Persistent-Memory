# -Built-a-RAG-Based-Generative-AI-PDF-Assistant-with-Persistent-Memory
ecently developed a Retrieval-Augmented Generation (RAG) based AI Assistant that can intelligently answer questions from a PDF using semantic search and LLM reasoning.  This project demonstrates how to combine Vector Databases + LLMs + Persistent Memory to build a real-world conversational AI system.

I recently built a Retrieval-Augmented Generation (RAG) based Generative AI PDF Assistant that can intelligently answer questions from a document using semantic search and large language models. Instead of manually searching through a PDF, the system allows users to ask natural language questions and receive accurate, context-aware responses in real time.

The assistant works by converting the PDF into embeddings and storing them in a vector database using pgvector integrated with PostgreSQL. When a user submits a query, the system performs semantic similarity search to retrieve the most relevant chunks from the document. This retrieved context is then sent to a large language model powered by Groq, which delivers ultra-fast inference using its LPU (Language Processing Unit) architecture. The LPU-based acceleration enables significantly faster response generation compared to traditional GPU-based inference systems.

To ensure portability and reproducibility, I containerized the entire setup using Docker Desktop. This allows seamless deployment of PostgreSQL with pgvector, the assistant framework, and the application environment in an isolated and scalable setup. Docker-based orchestration makes the system production-ready and easy to deploy across different machines.

In addition to retrieval and generation, the assistant maintains persistent conversational memory by storing chat history in PostgreSQL. This enables multi-turn conversations where the system remembers previous interactions and provides more contextually relevant responses.

Through this project, I gained hands-on experience in building end-to-end RAG pipelines, integrating vector databases with LLM APIs, working with high-speed LPU-powered inference, and deploying AI systems using containerized infrastructure. This architecture reflects how modern enterprise AI systems combine retrieval, memory, fast inference hardware, and scalable deployment practices to build intelligent and reliable knowledge assistants.

I am excited to continue exploring advanced RAG systems, high-performance LLM deployments, and Agentic AI architectures to design more autonomous and scalable AI solutions.
