# -Built-a-RAG-Based-Generative-AI-PDF-Assistant-with-Persistent-Memory
ecently developed a Retrieval-Augmented Generation (RAG) based AI Assistant that can intelligently answer questions from a PDF using semantic search and LLM reasoning.  This project demonstrates how to combine Vector Databases + LLMs + Persistent Memory to build a real-world conversational AI system.

I recently built a Retrieval-Augmented Generation (RAG) based Generative AI PDF Assistant that can intelligently answer questions from a document using semantic search and large language models. Instead of manually searching through a PDF, the system allows users to ask natural language questions and receive accurate, context-aware responses in real time.

The assistant works by converting the PDF into embeddings and storing them in a vector database using pgvector integrated with PostgreSQL. When a user submits a query, the system performs semantic similarity search to retrieve the most relevant chunks from the document. This retrieved context is then sent to a large language model powered by Groq, which delivers ultra-fast inference using its LPU (Language Processing Unit) architecture. The LPU-based acceleration enables significantly faster response generation compared to traditional GPU-based inference systems.

To ensure portability and reproducibility, I containerized the entire setup using Docker Desktop. This allows seamless deployment of PostgreSQL with pgvector, the assistant framework, and the application environment in an isolated and scalable setup. Docker-based orchestration makes the system production-ready and easy to deploy across different machines.

In addition to retrieval and generation, the assistant maintains persistent conversational memory by storing chat history in PostgreSQL. This enables multi-turn conversations where the system remembers previous interactions and provides more contextually relevant responses.

Through this project, I gained hands-on experience in building end-to-end RAG pipelines, integrating vector databases with LLM APIs, working with high-speed LPU-powered inference, and deploying AI systems using containerized infrastructure. This architecture reflects how modern enterprise AI systems combine retrieval, memory, fast inference hardware, and scalable deployment practices to build intelligent and reliable knowledge assistants.

I am excited to continue exploring advanced RAG systems, high-performance LLM deployments, and Agentic AI architectures to design more autonomous and scalable AI solutions.


respose: 

INFO     Creating collection
INFO     Loading knowledge base
Continuing Run: ae325bce-d8ea-4395-98e0-ba06b52ebc61

 😎 User : list out all the dishes availabe       

 
╭──────────┬────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────╮
│ Message  │ list out all the dishes availabe                                                                                                                   │
├──────────┼────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│ Response │ I'm not able to provide a list of dishes available as I don't have access to real-time information about specific restaurants or menus. However, I │
│ (3.1s)   │ can suggest some ways for you to find the information you're looking for.                                                                          │
│          │                                                                                                                                                    │
│          │ To get a list of dishes available, you can try the following options:                                                                              │
│          │                                                                                                                                                    │
│          │ Option 1: Check the Restaurant's Website                                                                                                           │
│          │                                                                                                                                                    │
│          │ You can visit the website of the restaurant you're interested in and look for their menu section. Most restaurants post their menus online,        │
│          │ including descriptions of each dish and prices.                                                                                                    │
│          │                                                                                                                                                    │
│          │ Option 2: Use Online Food Delivery Platforms                                                                                                       │
│          │                                                                                                                                                    │
│          │ If you're looking for dishes available from restaurants that deliver, you can check online food delivery platforms such as Grubhub, Uber Eats, or  │
│          │ DoorDash. These platforms often have menus from multiple restaurants and allow you to filter by cuisine, price, and more.                          │
│          │                                                                                                                                                    │
│          │ Option 3: Search for Menus on Review Websites                                                                                                      │
│          │                                                                                                                                                    │
│          │ Websites like Yelp or TripAdvisor often have menus posted by users or the restaurants themselves. You can search for the restaurant you're         │
│          │ interested in and see if anyone has posted their menu.                                                                                             │
│          │                                                                                                                                                    │
│          │ Option 4: Call the Restaurant                                                                                                                      │
│          │                                                                                                                                                    │
│          │ If you're unable to find the menu online, you can try calling the restaurant directly and asking about their available dishes. This is a good      │
│          │ option if you have specific dietary restrictions or preferences and want to confirm that the restaurant can accommodate you.                       │
│          │                                                                                                                                                    │
│          │  • Running: search_knowledge_base(query=popular dishes)                                                                                            │
│          │                                                                                                                                                    │
│          │ There are numerous dishes available from various cuisines around the world. Here are some examples:                                                │
│          │                                                                                                                                                    │
│          │ Appetizers                                                                                                                                         │
│          │                                                                                                                                                    │
│          │  • Bruschetta                                                                                                                                      │
│          │  • Spinach and artichoke dip                                                                                                                       │
│          │  • Potato skins                                                                                                                                    │
│          │  • Chicken wings                                                                                                                                   │
│          │  • Onion rings                                                                                                                                     │
│          │                                                                                                                                                    │
│          │ Main Courses                                                                                                                                       │
│          │                                                                                                                                                    │
│          │  • Pizza                                                                                                                                           │
│          │  • Burgers                                                                                                                                         │
│          │  • Tacos                                                                                                                                           │
│          │  • Sushi                                                                                                                                           │
│          │  • Steak                                                                                                                                           │
│          │  • Fish and chips                                                                                                                                  │
│          │  • Chicken parmesan                                                                                                                                │
│          │  • Vegetarian lasagna                                                                                                                              │
│          │                                                                                                                                                    │
│          │ Desserts                                                                                                                                           │
│          │                                                                                                                                                    │
│          │  • Ice cream                                                                                                                                       │
│          │  • Brownies                                                                                                                                        │
│          │  • Cheesecake                                                                                                                                      │
│          │  • Chocolate cake                                                                                                                                  │
│          │  • Fruit salad                                                                                                                                     │
│          │  • Tiramisu                                                                                                                                        │
│          │                                                                                                                                                    │
│          │ International Dishes                                                                                                                               │
│          │                                                                                                                                                    │
│          │  • Chinese: Kung pao chicken, beef with broccoli, fried rice                                                                                       │
│          │  • Italian: Spaghetti bolognese, fettuccine alfredo, chicken parmesan                                                                              │
│          │  • Mexican: Tacos, burritos, quesadillas                                                                                                           │
│          │  • Indian: Chicken tikka masala, palak paneer, naan bread                                                                                          │
│          │  • Japanese: Sushi, ramen, tempura                                                                                                                 │
│          │  • Korean: Bibimbap, bulgogi, kimchi stew                                                                                                          │
│          │                                                                                                                                                    │
│          │ This is not an exhaustive list, and there are many more dishes available from different cuisines and cultures.                                     │
╰──────────┴────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────╯
