# Svelte Chat Langchain (mini version)

This is a (mini) version of Chat Langchain (https://github.com/langchain-ai/chat-langchain) implemented in SvelteKit!

This repo can be a source of inspiration and starting point for developers looking to try their hand on a QA chatbot over Documents.
It is held purposefully simple and easy to understand while still holding some complexity to be a good example.

This app features:

- Ingestion
  - Document Loading (from Langchain JS docs https://js.langchain.com/docs/get_started/introduction)
  - Document Splitting
  - Setting up and using VercelPostgres as VectorDb
- Retrieval
- Complex & Conditional Chaining with Langchain Expression Language
- Streaming (simplified with Vercel AI SDK - for advanced streaming manipulation see the original Chat Langchain repo)

I call it a mini version because it does however not include some of the more advanced features of the original Chat Langchain, such as Indexing / Record Management, user feedback and stream parsing to display sources.

This repository is fully inspired by the original Chat Langchain repository:

Langchain Chat Website:
https://chat.langchain.com/

Langchain Chat Github:
https://github.com/langchain-ai/chat-langchain

Langchain Blog:
https://blog.langchain.dev/building-chat-langchain-2/

## Setup

IMPORTANT!
Set environment variables in a .env file (see .env.example for reference).

In the current configuration you need to have a OpenAI API Key, a Vercel account and a Vercel Postgres database instance to run the app (https://vercel.com/).
Optionally (but highly encouraged) you can add a Langsmith API Key (https://docs.smith.langchain.com/) for debugging and testing chains.

Install dependencies.

```sh
pnpm i
```

Run the development server at http://localhost:5173/.

```sh
pnpm run dev
```

## Important note

If you build your own example, note that this repos uses a modified vite.config.ts which is necessary to use the environment variables in local development without explicitly declaring them in the code. This is not necessary in production.
