# Advanced Retrieval Strategies

Beyond simple similarity search, more sophisticated retrieval strategies can be employed to get even more relevant context.

Metadata Filtering: In addition to the vector embeddings, you can store metadata alongside your chunks of text. This could include timestamps, source documents, user IDs, or keywords. You can then filter your search based on this metadata before performing the vector similarity search. For example, you could search for information from a specific user within the last week.
Hybrid Search: This powerful technique combines traditional keyword-based search with semantic vector search. This is beneficial because some queries, like those for specific names or acronyms, are better handled by keyword matching, while broader, more conceptual queries are better suited for semantic search.
Time-Weighted Retrieval: In many conversational AI applications, recent information is more relevant. Time-weighted retrieval algorithms give a higher score to more recent memories, causing them to be surfaced more readily than older, potentially outdated information.
Re-ranking: After an initial retrieval of a larger set of potentially relevant chunks, a more sophisticated model (often a cross-encoder) can be used to re-rank these results for even better relevance to the specific query.
