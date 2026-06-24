# Agentic-Research-Assistant-RAG-with-LangGraph
# Agentic Research Assistant – RAG with LangGraph

## Overview

This project implements an intelligent agentic Retrieval-Augmented Generation (RAG) system using LangChain, LangGraph, and ChromaDB.

The assistant can:

* Load and chunk documents
* Generate embeddings
* Store them in a persistent vector database
* Dynamically decide when retrieval is necessary
* Skip retrieval for simple logic questions
* Enforce factual grounding using prompt engineering

---

## Discovery-to-Action Framework

### Discovery Phase

* Load AI Ethics PDF
* Chunk into 500-character segments
* Store embeddings in ChromaDB
* Create knowledge base retrieval tool

### Technical Phase

* Build stateful workflow
* Define Agent node
* Define Tool node
* Implement conditional routing

### Action Phase

* Test retrieval behavior
* Test direct response behavior
* Visualize graph execution
* Propose enterprise use case

---

## Architecture

```text
User Query
   |
   v
Agent Node
   |
   +---- Simple Query? ----> Direct Response
   |
   +---- Complex Query ----> Tool Node
                               |
                               v
                        ChromaDB Retrieval
                               |
                               v
                           Final Answer
```

---

## Business Use Case

A scalable use case for this architecture is legal contract review.

Law firms process thousands of contracts daily. Instead of manually reviewing each document, this system can:

* Retrieve relevant clauses instantly
* Flag compliance risks
* Detect missing legal obligations
* Reduce review time significantly

This lowers operational costs and improves accuracy.

---

## Technologies

* LangChain
* LangGraph
* ChromaDB
* OpenAI
* Pydantic
* Python
