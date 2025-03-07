## Introduction

Retrieval-Augmented Generation (RAG) is a technique used to enhance the capabilities of large language models (LLMs) by integrating them with external knowledge bases. This approach combines the generative power of LLMs with the precision of specialized data search mechanisms, allowing for more accurate and relevant responses to user queries.

Key Components of RAG:

- Indexing: The data to be referenced is converted into numerical representations (embeddings) and stored in a vector database for efficient retrieval1.

- Retrieval: Given a user query, a document retriever selects the most relevant documents from the indexed data1.

- Augmentation: The retrieved information is incorporated into the LLM via prompt engineering to enhance the query1.

- Generation: The LLM generates output based on both the query and the retrieved documents1.

This project demonstrates how to implement a RAG using Langchain in node.js. The RAG system enhances text generation models by incorporating relevant information retrieved from external knowledge sources like a PDF document. It uses the information to augment the responses genereated by the language model.

## Requirements

- Node.js
- yarn
- OpenAI API Key (for text generation and embedding)
- Vector Database (Pinecone)

## Installation

1. Install Dependencies:

```
yarn install
```

2. Set Up Environment Variables:

Create a .env file in the root directory and add your environment variables:

```
OPENAI_API_KEY=your_openai_api_key
PINECONE_API_KEY=your_pinecone_api_key
```

## Usage

Run `node .`

- It will create index if not exists
- It will process sample PDF for the first time
- It will use OpenAI text-embedding-3-large model and storing embedding in the Pinecone Vector DB.
- Then you can accept queries from the terminal and generate answers from information in the PDF. 


