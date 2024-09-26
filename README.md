<p align="center">
    <img alt="logo" src="img/agentic_patterns.png" width=600 />
    <h1 align="center">Agentic Patterns</h1>
    <h3 align="center">Implementing the agentic patterns using Groq</h3>
</p>


> No LangChain, no LangGraph, no LlamaIndex, no CrewAI. Pure and simple API calls to Groq.


## Introduction

This repository contains an implementation of the 4 agentic
patterns defined by Deeplearning.ai using Groq.

<p align="center">
    <img alt="logo" src="img/groq.png" width=200 />
</p>


Below, you have a description of the 4 patterns we are going to be implementing.

## The 4 Agentic patterns

### Reflection Pattern 🤔

<p align="center">
    <img alt="logo" src="img/reflection_pattern.png" width=500 />
</p>

A very basic pattern but, despite its simplicity, it provides
surprising performance gains for the LLM response.

It allows the LLM to **reflect on its results**, suggesting
modifications, additions, improvements in the writing style, etc.

Want to see this pattern in action?

- Check the [notebook](notebooks/reflection_pattern.ipynb) for a step by step explanation
- Check the [`ReflectionAgent`](src/agentic_patterns/reflection_pattern/reflection_agent.py) for a complete Python implementation

---

### Tool Pattern  🛠

<p align="center">
    <img alt="logo" src="img/tool_pattern.png" width=600 />
</p>

The information stored in the LLM weights is (usually) **not enough** to give accurate and insightful answers to our questions

That's why we need to provide the LLM with ways to access the outside world 🌍

In practice, you can build tools for whatever you want (at the end of the day they are just functions the LLM can use), from a tool that let's you access Wikipedia, another to analyse the content of YouTube videos or calculate difficult integrals in Wolfram Alpha.

**Tools** are the **secret sauce of agentic applications** and the possibilities are endless! 🥫

Want to see this pattern in action?

- Check the [notebook](notebooks/tool_pattern.ipynb) for a step by step explanation
- Check the [`ToolAgent`](src/agentic_patterns/tool_pattern/tool_agent.py) for a complete Python implementation
- Check the [`Tool`](src/agentic_patterns/tool_pattern/tool.py) for understanding how Tools work under the hood.


---

### Planning Pattern 🧠

<p align="center">
    <img alt="logo" src="img/planning_pattern.png" width=500 />
</p>

So, we've seen agents capable of reflecting and using tools to access the outside world. But ... **what about planning**,
i.e. deciding what sequence of steps to follow to accomplish a large task?

That is exactly what the Plannin Pattern provided; ways for the LLM to break a task into **smaller, more easily accomplished subgoals** without losing track of the end goal.

The most paradigmatic example of the planning pattern is the **ReAct** technique, displayed in the diagram above.

Want to see this pattern in action?

TBD 

---

### Multiagent Pattern 🧑🏽‍🤝‍🧑🏻

<p align="center">
    <img alt="logo" src="img/multiagent_pattern.png" width=500 />
</p>

You may have heard about frameworks like crewAI or AutoGen, which allow you to create multi-agent applications.

These frameworks implement different variations of the multi-agent pattern, in which tasks are divided into **smaller subtasks executed by different roles** (e.g. one agent can be a software engineer, another a project manager, etc.)

Want to see this pattern in action?

TBD

---

