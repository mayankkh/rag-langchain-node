## Introduction

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


