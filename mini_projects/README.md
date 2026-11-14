### Depository of Useful Links and Mini-Projects

1. OpenAI Cookbook: Learn to work with LLM APIs
openai/openai-cookbook (https://developers.openai.com/cookbook)
- Contains code examples and guides for working with the OpenAI API.
- Covers API requests, conversation handling, embeddings, structured outputs, tool calling, and the examples related to agents and retrieval.
- Needs API access to call hosted models.

2. Claude Cookbooks: Explore another model integration
Repository: anthropics/claude-cookbooks (https://github.com/anthropics/claude-cookbooks)
- Contains notebooks and recipes demonstrating ways to use Claude.
- Covers retrieval-augmented generation, basic API integration, JSON handling, and tool use. Much of the code uses Python.

3. Awesome LLM Apps: Build complete applications with RAG
Repository: Shubhamsaboo/awesome-llm-apps (https://github.com/Shubhamsaboo/awesome-llm-apps)

Difficulty: Beginner to Advanced, depending on the example

This collection contains open-source LLM applications, RAG implementations, AI agents, multi-agent projects, and MCP integrations. It is particularly useful when you want to see how individual techniques fit into working applications.

What to learn?

Start with a basic RAG application that answers questions about documents.

A typical RAG pipeline works like this:

Ingest documents and split them into chunks.

Generate embeddings and index the chunks.

Retrieve relevant passages for a user’s question.

Send the question and retrieved context to the model.

Return an answer with references to its sources.

Then investigate where retrieval fails. A model cannot give a grounded answer if the retriever returns irrelevant passages or misses the information needed to answer the question.

Prerequisites: LLM API integration, basic Python, and a general understanding of databases.

Build: Create a chat application that answers questions about your own technical documentation and links each answer to its source.

Afterward, you should understand the main components of a RAG application and be able to trace a question through ingestion, retrieval, and generation.

Important: Evaluate retrieval quality separately from answer quality. That distinction makes debugging much easier.

4. Hugging Face Agents Course: Learn tools and agent fundamentals
Repository: huggingface/agents-course (https://github.com/huggingface/agents-course)

Difficulty: Intermediate

The Hugging Face Agents Course is a structured course that progresses from agent fundamentals to agent frameworks and practical assignments. Its material covers tools and frameworks including smolagents, LangGraph, and LlamaIndex, with relevant material on integrating MCP tools.

What to learn?

Focus on the relationship between an LLM, the tools it can use, and the application controlling its execution.

For example, a customer-support agent might need to retrieve an order, check its delivery status, and draft a response. The model can choose a tool, but your application should validate its arguments and enforce permissions before performing the action.

Prerequisites: API integration, Python, and basic RAG concepts.

Build: Create a support agent with two read-only tools: search documentation and retrieve an order’s status.

Afterward, you should understand tool calling, agent execution, framework abstractions, and the importance of controlling what an agent can do.

This is also a good starting point for understanding MCP. MCP standardizes how compatible clients and servers expose tools and other context. It does not automatically make tool calls safe or give an agent permission to access everything.

5. GenAI Agents: Explore agent architectures and multi-agent systems
Repository: NirDiamant/GenAI_Agents (https://github.com/NirDiamant/GenAI_Agents)

Difficulty: Intermediate to Advanced

This repository contains tutorials and implementations covering generative AI agent techniques, from conversational bots to more complex multi-agent systems.

What to learn?

Study how agents manage state, choose tools, coordinate steps, and recover when an action fails. Then investigate multi-agent designs in which different agents handle specialized tasks.

Consider a research assistant that gathers information, extracts evidence, and prepares a report. You could implement it as a single agent first, then compare it with a design that delegates research and review to separate agents.

Prerequisites: Tool calling, Python, and a basic understanding of agent loops.

Build: Create a research workflow with a retrieval step, a drafting step, and a verification step. Compare a fixed workflow with an agent that can decide when to retrieve more information.

Afterward, you should be able to compare agent architectures and identify when orchestration adds value.

Don’t assume multiple agents will automatically improve quality. They can introduce extra model calls, latency, coordination failures, and more complicated debugging.

6. AI Project Gallery: Learn from applied AI projects
Repository: KalyanM45/AI-Project-Gallery (https://github.com/KalyanM45/AI-Project-Gallery)

Difficulty: Beginner to Intermediate

This repository catalogs projects across machine learning, deep learning, and generative AI. Its examples include prediction systems, chatbots, document-related tools, and agentic workflows. It works best as an exploration and project-selection resource. Not every catalog entry necessarily provides a complete implementation.

What to learn?

Look at how AI techniques map to application problems. Compare a conventional prediction project with a chatbot or agentic workflow, and identify the data, model, and user-interface requirements each one needs.

Prerequisites: Basic programming and familiarity with API-backed AI applications.

Build: Choose a project related to your interests and implement a small, working version. Document its inputs, outputs, failure cases, and evaluation method.


7. System Prompts Leaks: Study prompt patterns and security risks
Repository: asgeirtj/system_prompts_leaks (https://github.com/asgeirtj/system_prompts_leaks)
- This repository collects documented system prompts attributed to various AI assistants and coding tools. Treat it as a resource for examining publicly accessible examples of instruction design and considering their security implications.
- Study how instructions define an assistant’s role, describe available tools, constrain responses, and establish task-specific behavior. Also examine the risks of prompt injection, instruction disclosure, and overly broad tool permissions.
- Prerequisites: Basic prompting and an understanding of how system instructions influence an AI application.
- Build: Create a security test suite for your own assistant. Include attempts to override its instructions, request unauthorized records, and misuse available tools.
