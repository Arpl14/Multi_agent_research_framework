# Deep Research AI Multi-Agent System with LlamaIndex

A multi-agent research system built with LlamaIndex that orchestrates multiple AI agents to conduct deep research on any topic. This project explores agentic workflows, tool integration, and collaborative AI systems.

## What This Project Does

This system implements a research pipeline where multiple specialized agents work together:
- **Research Agent**: Searches the web and gathers information
- **Writing Agent**: Synthesizes findings into structured reports  
- **Review Agent**: Provides feedback and quality checks

The agents communicate through shared context, can hand off tasks to each other, and maintain state across interactions. The system supports both simple single-agent workflows and complex multi-agent orchestration.

## Technical Approach

Built using LlamaIndex's workflow abstractions:
- **AgentWorkflow**: For quick agent setup with tools and state management
- **Custom Workflows**: Fine-grained control over agent interactions and data flow
- **Event-driven architecture**: Steps communicate via typed events
- **Context management**: Shared state accessible across agents and tools

## Key Capabilities

- **Tool Integration**: Agents can use external APIs (like Tavily for web search)
- **Stateful Conversations**: Maintains context across multiple interactions
- **Event Streaming**: Real-time visibility into agent operations
- **Human-in-the-Loop**: Optional checkpoints for critical decisions
- **Parallel Processing**: Multiple agents can work concurrently
- **Custom Control Flow**: Looping, branching, and conditional execution

## Tech Stack

- **LlamaIndex**: Core framework for agent orchestration
- **OpenAI GPT-4.1-mini**: LLM for agent reasoning
- **Tavily AI**: Web search capabilities
- **Python 3.8+**: Implementation language with async support

## Project Structure

The implementation is organized in a Jupyter notebook (`solution.ipynb`) that progressively builds from:
1. Single agent with basic tool usage
2. Multi-agent collaboration with AgentWorkflow
3. Custom workflow implementation
4. Advanced deep research system

## Getting Started

1. Install dependencies:
```bash
pip install llama-index llama-index-llms-openai llama-index-utils-workflow
```

2. Set up API keys for OpenAI and Tavily

3. Run the notebook cells sequentially to explore each workflow pattern

## What I Learned

This project was an exploration of building production-ready agentic systems. The workflow abstraction in LlamaIndex provides a clean way to orchestrate complex multi-step processes involving LLMs, tools, and state management. The event-driven approach makes it intuitive to define dependencies and control flow, while the context system enables seamless information sharing between agents.

The most interesting challenge was designing the multi-agent handoff logic and ensuring each agent had access to the right information at the right time. The custom workflow implementation gave fine-grained control over parallelization and data flow that wasn't possible with simpler approaches.
