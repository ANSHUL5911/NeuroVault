\# HNSW Explained



\## What is HNSW?



HNSW stands for:



\*\*Hierarchical Navigable Small World\*\*



It is one of the most widely used algorithms for Approximate Nearest Neighbor Search.



Used by:



\- Pinecone

\- Weaviate

\- Chroma

\- Milvus



\---



\## Problem



Given a query vector:



```text

Q = \[0.2, 0.4, 0.8]

```



Find the most similar vectors from millions of candidates.



Brute force compares against every vector.



This is expensive.



\---



\## HNSW Solution



HNSW creates multiple graph layers.



```text

Layer 3

&#x20;  ●

&#x20;  │

Layer 2

&#x20;●   ●



Layer 1

● ● ● ●



Layer 0

Dense graph

```



Upper layers:



\- Sparse

\- Fast navigation



Lower layers:



\- Dense

\- Precise search



\---



\## Search Process



1\. Start from top layer

2\. Navigate to closer nodes

3\. Move down a layer

4\. Repeat until layer 0

5\. Return nearest neighbors



\---



\## Complexity



Approximate:



```text

O(log N)

```



Compared to:



```text

Brute Force = O(N)

```



\---



\## Benefits



\- Extremely fast

\- Scalable

\- High recall

\- Industry standard



This is why most production vector databases use HNSW.

