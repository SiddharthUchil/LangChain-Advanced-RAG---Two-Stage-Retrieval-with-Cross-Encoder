# LangChain Advanced RAG - Two-Stage Retrieval with Cross Encoder (BERT)

### Vector Databases: These are databases that store data in a vector format. They are particularly useful for handling high-dimensional data, such as images or text, which can be represented as vectors in a multi-dimensional space.

### Query Expansion: This is a technique used to improve the effectiveness of information retrieval. It involves expanding the original query by adding synonyms, related words, or other relevant terms`. For example, if you search for “dog”, query expansion might also search for “puppy”, “canine”, and “pet”.

### Two-Stage Retrieval with a Cross Encoder: This is an advanced retrieval technique that involves two stages. In the first stage, a large number of candidate documents are retrieved using a fast and efficient method. In the second stage, a more computationally expensive method (the Cross Encoder) is used to re-rank these candidates to find the most relevant documents. The Cross Encoder is typically a transformer model like BERT, which can understand the semantic meaning of text.

### A reranker is used in the context of two-stage retrieval systems. In these systems, a first-stage model (an embedding model/retriever) retrieves a set of relevant documents from a larger dataset. Then, a second-stage model (the reranker) is used to rerank those documents retrieved by the first-stage model. This is particularly useful if the retriever has a high recall but is bad at sorting the documents by relevance.

### To mitigate the “Lost in the Middle” problem, rerankers can be used to reorder the retrieved documents, pushing the most relevant information closer to the start of the input context. This enhances the LLM’s ability to access and utilize information effectively

### To mitigate this issue, a technique called LongContextReorder has been proposed. Instead of feeding the documents to the model in their original order, this technique places the most similar documents at the top, the next set at the bottom, and the least similar ones right in the middle. This way, even if the model overlooks the middle documents, it still has a high chance of seeing the most relevant documents and giving the correct answer





