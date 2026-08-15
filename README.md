<div align="center">
  <h1>🦜🔗 Mastering LangChain (v1+)</h1>
  <p><i>My personal journey and comprehensive notes on mastering the updated LangChain framework.</i></p>

  <img src="https://img.shields.io/badge/LangChain-1.1.0-blue?style=for-the-badge&logo=langchain" alt="LangChain Version" />
  <img src="https://img.shields.io/badge/Python-3.13-yellow?style=for-the-badge&logo=python" alt="Python" />
  <img src="https://img.shields.io/badge/uv-Package_Manager-purple?style=for-the-badge" alt="uv Package Manager" />
</div>

---

## 🚀 About This Repository

Welcome to my LangChain learning repository! This repo serves as a structured collection of my notes, concepts, and code implementations as I dive deep into building autonomous agents and GenAI applications using **LangChain's latest v1+ framework**. 

I created this to transition from building basic LLM wrappers to developing production-ready, autonomous AI agents equipped with tools, memory, structured outputs, and critical human-in-the-loop workflows.

---

## 📚 What I've Learned

Here is a breakdown of the core concepts I have mastered in this journey:

### 1. Modern Environment Setup ⚡
Transitioned to using **`uv`**, the blazingly fast Rust-based Python package manager.
* Initializing projects (`uv init`)
* Seamless virtual environment management (`uv venv`)
* Fast dependency installation

### 2. Autonomous Agents 🤖
Moved beyond basic LLM calls to creating intelligent agents that can reason and interact with external systems.
* Implemented the **ReAct architecture**.
* Leveraged the updated `create_agent` method for streamlined agent building.

### 3. Tool Creation & Execution 🛠️
Taught LLMs how to "act" on the world.
* Building custom tools using the `@tool` decorator.
* Understanding the profound importance of **Docstrings and Type Hints** for LLM decision-making.
* Binding tools to models and mastering the **Tool Execution Loop**.

### 4. Advanced Message Structures 💬
Learned how to maintain state and instruct models effectively.
* `SystemMessage`: Giving the LLM a persona and rules.
* `HumanMessage` & `AIMessage`: Managing the back-and-forth conversation.
* `ToolMessage`: Injecting tool context back into the agent's thought process.

### 5. Enforcing Structured Outputs 📊
Ensured LLMs return predictable, parsable data instead of plain text.
* **Pydantic**: Enforcing strict runtime validation and nested data structures.
* **TypedDict**: Lightweight structuring without strict runtime validation.
* **DataClasses**: Utilizing built-in Python structures for schema enforcement.

### 6. Agent Middleware (Ultimate Control) 🛑
Learned how to securely manage agents in production by intercepting their execution.
* **`SummarizationMiddleware`**: Preventing token-limit crashes by summarizing older contexts dynamically (triggered by token counts or message lengths).
* **`HumanInTheLoopMiddleware`**: Intercepting high-stakes tool executions (like sending emails or database writes) to wait for a human to **Approve, Reject, or Edit** the action via `Command` resumes.

### 7. LCEL (LangChain Expression Language) 🔗
Embraced the modern, declarative way to compose LangChain components.
* Building pipelines with the Unix-style pipe operator (`|`).
* Leveraging `RunnablePassthrough` for dynamic data injection.
* Running tasks concurrently using `RunnableParallel`.

### 8. Performance: Streaming & Batching 🏎️
* **Streaming (`stream()`)**: Implemented progressive output generation for real-time chatbot UX.
* **Batching (`batch()`)**: Processed multiple parallel LLM requests with `max_concurrency` to save time and reduce API costs.

---

## 📖 Useful Resources in this Repo

* [**LCEL Interactive Guide**](./notebooks/07-lcel-guide.ipynb): A Jupyter Notebook containing practical LCEL examples (basic chains, data injection, parallel execution).
* [**LangChain Interview Preparation Guide**](./notebooks/langchain-revision.md): A comprehensive Q&A guide focusing on the "Why" and "When" of LangChain features—perfect for exam or interview prep!

---

<div align="center">
  <i>Built with ❤️ while learning Generative AI.</i>
</div>
