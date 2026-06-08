\# NeuroVault Architecture



\## Overview



NeuroVault is a vector database built from scratch in C++.



It demonstrates how modern AI search systems work internally by combining:



\- Vector Embeddings

\- Approximate Nearest Neighbor Search

\- Document Retrieval

\- Retrieval-Augmented Generation (RAG)



\---



\## High Level Flow



```text

User Query

&#x20;    │

&#x20;    ▼

Embedding Model

(nomic-embed-text)

&#x20;    │

&#x20;    ▼

Vector Representation

&#x20;    │

&#x20;    ▼

HNSW Index

&#x20;    │

&#x20;    ▼

Top-K Similar Documents

&#x20;    │

&#x20;    ▼

LLM Context Injection

&#x20;    │

&#x20;    ▼

Generated Response

```



\---



\## Components



\### Backend



\- C++17

\- cpp-httplib

\- REST API



\### Search Layer



\- HNSW

\- KD-Tree

\- Brute Force



\### AI Layer



\- Ollama

\- nomic-embed-text

\- llama3.2



\### Frontend



\- HTML

\- CSS

\- JavaScript

\- Canvas Visualization



\---



\## Why HNSW?



Brute force search becomes expensive as data grows.



```text

Brute Force = O(N)



HNSW = O(log N)

```



This makes HNSW suitable for large-scale vector retrieval.

