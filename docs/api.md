\# REST API Documentation



Base URL



```text

http://localhost:8080

```



\---



\# Search



\## GET /search



Performs K-NN search.



\### Parameters



| Parameter | Description |

|------------|------------|

| v | Query vector |

| k | Number of results |

| metric | cosine/euclidean/manhattan |

| algo | hnsw/kdtree/bruteforce |



\### Example



```http

GET /search?v=0.1,0.2,0.3\&k=5\&metric=cosine\&algo=hnsw

```



\---



\# Insert Vector



\## POST /insert



Insert a new vector.



\---



\# Delete Vector



\## DELETE /delete/:id



Delete vector by ID.



\---



\# List Vectors



\## GET /items



Returns all stored vectors.



\---



\# Benchmark



\## GET /benchmark



Compare:



\- HNSW

\- KD-Tree

\- Brute Force



Performance side by side.



\---



\# HNSW Information



\## GET /hnsw-info



Returns:



\- Layer count

\- Graph statistics

\- Connectivity information



\---



\# Statistics



\## GET /stats



Database metrics.



\---



\# Insert Document



\## POST /doc/insert



Request:



```json

{

&#x20; "title": "Operating Systems",

&#x20; "text": "..."

}

```



\---



\# Ask AI



\## POST /doc/ask



Request:



```json

{

&#x20; "question": "What is a process?",

&#x20; "k": 3

}

```



Returns an answer generated using retrieved context.



\---



\# Status



\## GET /status



Checks:



\- Ollama availability

\- Loaded models

\- System health

