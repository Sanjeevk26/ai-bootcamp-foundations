# Module 7 – Generative AI Tools and RAG
## Practical Overview of ChatGPT, Claude, Perplexity, Amazon Bedrock, and Retrieval-Augmented Generation

In this module, we move from concepts to practical usage.

We will cover:

- ChatGPT (GPT-3.5, GPT-4, DALL·E)
- Claude (Anthropic)
- Perplexity (search + AI answers)
- Amazon Bedrock (multi-model platform)
- RAG (Retrieval-Augmented Generation)
- A simple view of how RAG works end-to-end

The goal is not deep technical implementation yet.
The goal is to understand what each tool does, what it is good at, and how these tools fit together in real applications.

---

# 1) ChatGPT (OpenAI)

ChatGPT is a conversational AI system where you can type a prompt and get a response.

Common uses include:
- Writing emails
- Summarizing content
- Generating ideas
- Drafting documents
- Answering questions
- Creating images (using image models such as DALL·E)

## GPT-3.5 vs GPT-4

Think of these as different generations of models.

- GPT-3.5: older generation, typically faster and cheaper
- GPT-4: newer generation, typically stronger reasoning and better output quality (often higher cost)

The exact differences depend on the platform and configuration, but the core idea is:
newer generation usually performs better on complex tasks.

## Example Workflow: Email Drafting

Example prompt:
"Write an email to request a quote from local plumbers."

The model can generate:
- Subject line
- Email body
- Polite closing

Then you can refine it by giving additional details:
- "Revise it for a clogged toilet issue."
- "Make it urgent."
- "Make it shorter."

This iterative prompting is a common workflow with ChatGPT.

## Image Generation with DALL·E

ChatGPT can also generate images using image generation capabilities.

Example:
"Create an illustration of a clogged toilet."

This produces an image you could use as an illustrative reference.

Note: image generation is a separate capability from text generation, even though it may appear in one chat interface.

---

# 2) Claude (Anthropic)

Claude is another large language model.

Like ChatGPT, it can:
- Write drafts
- Summarize content
- Help brainstorm
- Refine writing
- Answer questions

Example:
"Write an email to a plumber for a clogged toilet and ask for a quote."

Claude can produce a clean template and request clarifications such as:
- Is it a slow drain or fully clogged?
- Is it an emergency?
- What is the preferred time window?

## Key Practical Difference Highlighted in This Module

- Claude (in the workflow shown here) focuses on text generation.
- If image creation is needed, you can take Claude’s text description and send it to an image model.

---

# 3) Amazon Bedrock

Amazon Bedrock is a platform that provides access to multiple foundation models through one interface and API layer.

High-level idea:
- You choose a model based on your task.
- You interact via UI or API.
- You can build applications on top of it.

## Why Bedrock Matters

Instead of committing to a single model provider, Bedrock allows you to:
- Experiment with multiple models
- Select the best model for your use case
- Build applications that can switch models if needed

## Text Models and Image Models

Bedrock can provide:
- Text models for writing, summarization, Q&A
- Image models for image generation (example: Stable Diffusion)

Example workflow shown:
- Use a text model to generate a description
- Use an image model to generate an image from that prompt

## Building Applications with Bedrock

Many models expose API access.

Once you can call an API, you can integrate the model into:
- A web application
- A mobile app
- An internal tool
- A customer support experience

Bedrock also offers additional capabilities (knowledge bases, agents, evaluation) which can be explored later.

---

# 4) Perplexity

Perplexity behaves like a search engine combined with an AI assistant.

Key behavior:
- You ask a question like a search query
- It returns an answer
- It cites sources and links to where it found information

Example:
"Apple Vision Pro availability" or "Apple Vision Pro features"

Perplexity:
- Retrieves information from the web
- Summarizes it into an answer
- Shows sources used

Practical guidance:
- Use Perplexity when you want answers grounded in web sources
- Use it like an upgraded search experience for research and fact-finding

---

# 5) RAG (Retrieval-Augmented Generation)

A common limitation of many large language models:
- They do not automatically know information after their training cutoff date.
- They also do not know your company’s private documents by default.

RAG addresses this by:
- Retrieving relevant external or private information at query time
- Injecting that retrieved content into the model as context
- Generating a response using both your prompt and the retrieved context

In short:
RAG helps the model answer using the right, up-to-date, or private data without retraining the model.

---

# 6) How RAG Works (High-Level Flow)

RAG typically has two phases:

## Phase A: Preparation (Indexing)

1. Collect documents (PDFs, docs, wikis, tickets, emails, etc.)
2. Chunk the documents into smaller pieces
3. Create embeddings (numeric representations) for each chunk
4. Store those embeddings in a vector database

Simple mental model:
You convert your documents into a form that computers can efficiently search by meaning, not just keywords.

## Phase B: Answering a User Query (Retrieval + Generation)

1. User asks a question (prompt)
2. The question is converted into an embedding
3. The vector database finds the most relevant document chunks
4. The system appends those chunks as context to the prompt
5. The LLM generates an answer grounded in that context

This produces a better answer because the model has:
- Your question
- The most relevant reference material

---

# Summary

In this module, we covered:

- ChatGPT as a general-purpose generative AI assistant for text and images
- Claude as a strong text-focused assistant that can be used similarly for drafting and refinement
- Perplexity as a search-oriented AI tool that provides answers with sources
- Amazon Bedrock as a platform to access multiple foundation models through one layer
- RAG as a practical technique to provide up-to-date or private context to an LLM without retraining it

---
