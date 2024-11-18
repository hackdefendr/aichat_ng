# AIChat Next Gen: All-in-one LLM CLI Tool

AIChat is an all-in-one LLM CLI tool featuring Shell Assistant, Chat-REPL, RAG, AI Tools & Agents, and More. 

## Install
Coming soon

## Features
Coming soon

### Multi-Platform Support

Seamlessly integrate with over 20 leading LLM platforms via a unified interface, including OpenAI, Claude, Gemini (Google AI Studio), Ollama, Groq, Azure-OpenAI, VertexAI, Bedrock, Huggingface, Github Models, Mistral, Deepseek, AI21, XAI Grok, Cohere, Perplexity, Cloudflare, OpenRouter, Ernie, Qianwen, Moonshot,  ZhipuAI, Lingyiwanwu, Deepinfra, Fireworks, Siliconflow, Together, Jina, VoyageAI, and any OpenAI-Compatible platforms.

### Shell Assistant

Supercharge your command line experience. Simply describe your desired actions in natural language, and let AIChat translate your requests into precise shell commands. 

**OS-Aware Intelligence:** AIChat tailors commands to your specific operating system and shell environment.

### Chat-REPL

Bring a powerful Chat-REPL with features such as tab autocompletion, multi-line support, history search, configurable keybindings, and custom REPL prompt.

### Multi-Form Input

Accept various forms of input, such as stdin, local files & dirs, and remote URLs.

| Input             | Example                              |
| ----------------- | ------------------------------------ |
| CMD input         | `aichat hello`                       |
| Stdin pipe        | `cat data.txt \| aichat`             |
| Local files       | `aichat -f data.txt`                 |
| Local images      | `aichat -f image.png`                |
| Local directories | `aichat -f dir/`                     |
| Remote URLs       | `aichat -f https://example.com`      |
| Combine Inputs    | `aichat -f dir/ -f data.txt explain` |

### Role

Define custom roles to tailor LLM behaviors, enhancing interactions and boosting productivity.

> The role consists of a prompt and model configuration.

### Session

Maintain context-aware conversations through sessions, ensuring continuity in interactions.

> The left side uses a session, while the right side does not use a session.

### RAG (Chat with your documents)

Integrate external documents into your LLM conversations for more accurate and contextually relevant responses.

### Function Calling

Function calling supercharges LLMs by connecting them to external tools and data sources. This unlocks a world of possibilities, enabling LLMs to go beyond their core capabilities and tackle a wider range of tasks.

#### AI Tools

Integrate external tools to automate tasks, retrieve information, and perform actions directly within your workflow.

#### AI Agents (CLI version of OpenAI GPTs)

AI Agent = Instructions (Prompt) + Tools (Function Callings) + Documents (RAG).

### Local Server

AIChat comes with a built-in lightweight http server.

```
$ aichat --serve
Chat Completions API: http://127.0.0.1:8000/v1/chat/completions
Embeddings API:       http://127.0.0.1:8000/v1/embeddings
Rerank API:           http://127.0.0.1:8000/v1/rerank
LLM Playground:       http://127.0.0.1:8000/playground
LLM Arena:            http://127.0.0.1:8000/arena?num=2
```

#### Proxy LLM APIs

AIChat offers the ability to function as a proxy server for all LLMs. This allows you to interact with different LLMs using the familiar OpenAI API format, simplifying the process of accessing and utilizing these LLMs.

Test with curl:

```sh
curl -X POST -H "Content-Type: application/json" -d '{
  "model":"claude:claude-3-5-sonnet-20240620",
  "messages":[{"role":"user","content":"hello"}], 
  "stream":true
}' http://127.0.0.1:8000/v1/chat/completions
```

#### LLM Playground

The LLM Playground is a webapp that allows you to interact with any LLM supported by AIChat directly in your browser.

#### LLM Arena

The LLM Arena is a web-based platform where you can compare different LLMs side-by-side. 

## Custom Themes

AIChat supports custom dark and light themes, which highlight response text and code blocks.

## License

Copyright (c) 2024 HackDefendr Security Research.
