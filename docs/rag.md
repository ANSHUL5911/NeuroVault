\# Retrieval Augmented Generation (RAG)



\## What is RAG?



RAG combines:



\- Information Retrieval

\- Large Language Models



Instead of relying only on model training data,

the model retrieves relevant documents first.



\---



\## NeuroVault Pipeline



```text

Document

&#x20;  │

&#x20;  ▼

Chunking

&#x20;  │

&#x20;  ▼

Embedding

&#x20;  │

&#x20;  ▼

HNSW Storage

```



Query flow:



```text

Question

&#x20;  │

&#x20;  ▼

Embedding

&#x20;  │

&#x20;  ▼

HNSW Search

&#x20;  │

&#x20;  ▼

Top-K Chunks

&#x20;  │

&#x20;  ▼

llama3.2

&#x20;  │

&#x20;  ▼

Answer

```



\---



\## Example



Document:



```text

A process is a program in execution.

```



Question:



```text

What is a process?

```



Retrieved chunk:



```text

A process is a program in execution.

```



Generated answer:



```text

A process is a program currently being executed by the operating system.

```



\---



\## Advantages



\- More accurate

\- Uses custom knowledge

\- No retraining required

\- Reduces hallucinations



\---



\## Models Used



Embedding Model:



```text

nomic-embed-text

```



Generation Model:



```text

llama3.2

```

