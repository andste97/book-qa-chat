Improving RAG Retrieval with FAISS
If your FAISS-based RAG system isn't retrieving relevant documents, here are several areas to investigate:

Embedding Quality
Try different embedding models (OpenAI, Cohere, Instructor, BGE, etc.)
Use domain-specific embeddings if your content is specialized
Consider fine-tuning embeddings on your specific corpus
Document Chunking
Experiment with different chunk sizes (smaller for precise matching, larger for context)
Use semantic chunking instead of arbitrary length-based chunking
Try overlapping chunks to avoid breaking semantic units
Query Processing
Implement query expansion to include synonyms and related terms
Add query rewriting using an LLM to transform user queries
Use hybrid search (combine semantic and keyword search)
FAISS Configuration
Try different similarity metrics (cosine, dot product, L2)
Adjust index parameters (nlist, nprobe) for better recall vs. speed tradeoff
Use hierarchical indices for large document collections
Evaluation
Create a test set with queries and expected documents
Measure retrieval metrics (precision, recall, NDCG) systematically
Run qualitative analysis on failed retrievals to identify patterns
Post-Processing
Implement re-ranking of initial search results
Filter results based on metadata or additional criteria
Apply maximum marginal relevance (MMR) to increase result diversity
What's your current chunking strategy and embedding model? That's often the best place to start optimizing.