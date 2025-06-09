# Standard RAG

## Description
Retrieval-Augmented Generation (RAG) is an AI framework for retrieving facts from an external knowledge base to ground large language models (LLMs) on the most accurate, up-to-date information and to give users insight into LLMs' generative process.
It involves two main phases:
1.  **Retrieval:** Algorithms search for and retrieve snippets of information relevant to the user’s prompt or question. In an open-domain, consumer setting, these facts can come from indexed documents on the internet. In a closed-domain, enterprise setting, a narrower set of sources are typically used for added security and reliability.
2.  **Content Generation:** This assortment of external knowledge is appended to the user’s prompt and passed to the language model. The LLM then draws from the augmented prompt and its internal representation of its training data to synthesize an engaging answer tailored to the user.

## Studies
The concept of RAG was introduced in a 2020 paper by Meta (then Facebook) to give LLMs access to information beyond their training data.
- Meta, 2020: [Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks](https://arxiv.org/abs/2005.11401v4)

## Providers
Many cloud providers and AI companies offer RAG capabilities as part of their LLM platforms and services. Some prominent examples include:
- IBM (e.g., watsonx.ai)
- Amazon Web Services (AWS)
- Google Cloud (Vertex AI)
- Microsoft Azure (Azure AI Search)
- Various other specialized LLM and vector database providers.

## Pros
- **Access to Current Information:** Ensures the model utilizes the most up-to-date and reliable facts.
- **Verifiability:** Allows users to check the model's sources, enhancing trust and accuracy.
- **Reduced Hallucinations:** Grounding on external, verifiable facts minimizes the chances of the LLM generating incorrect or misleading information.
- **Reduced Need for Retraining:** Lessens the frequency and necessity of retraining the model with new data, as knowledge can be updated externally.
- **Cost-Effective:** Can lower computational and financial costs associated with running LLM applications, especially in enterprise settings.
- **Personalization:** Enables LLMs to provide more personalized responses without requiring extensive manual scripting for different scenarios.
- **Dynamic Knowledge Updates:** New information (e.g., updated policies, documents) can be made available to the model by simply updating the external knowledge source.

## Cons
- **Imperfect Process:** RAG is not a flawless solution, and challenges exist in optimizing its components.
- **Retrieval Quality Dependent:** The overall effectiveness heavily relies on the ability to find and fetch the most relevant information for the given prompt. Irrelevant or poorly ranked retrieved documents can lead to suboptimal responses.
- **Generation Quality Dependent:** The way retrieved information is structured and presented to the LLM can significantly impact the quality of the generated response.
- **Handling Unanswerable Questions:** LLMs need to be effectively trained or designed to recognize when they cannot answer a question based on the retrieved context, to avoid generating speculative or incorrect answers.
- **Complexity in Fine-Tuning:** Training models to identify unanswerable questions or to ask clarifying questions can require substantial effort and data.
- **Knowledge Gaps:** If the external knowledge source itself is incomplete or contains errors, the RAG system will inherit these limitations.
