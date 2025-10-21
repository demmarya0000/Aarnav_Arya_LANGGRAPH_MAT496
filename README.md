## **LANGGRAPH**
---

## MODULE 1

---

This repository contains a series of lessons demonstrating how to build reasoning workflows and agents using **LangChain** and **LangGraph**.

---

## LESSON 1: SIMPLE GRAPH

This project demonstrates how to use **LangChain** and **LangGraph** to build a simple reasoning workflow.

It takes a natural language instruction like "Add 3 and 4. Multiply the output by 2. Divide the output by 5." and shows how such tasks can be represented and processed step-by-step in a computational graph.

- SOURCE FILE: https://github.com/langchain-ai/langchain-academy/blob/main/module-1/simple-graph.ipynb

---

## LESSON 2: CHAIN

This project demonstrates how to use **LangGraph** with the **API** to build a simple router that processes messages and uses tools like `multiply`.

- SOURCE FILE: https://github.com/langchain-ai/langchain-academy/blob/main/module-1/chain.ipynb

---

## LESSON 3: ROUTER

### What We Learned
- **LangGraph** allows us to design structured "graphs" of actions — similar to flowcharts — for reasoning or decision-making
- Understood the difference between `HumanMessage`, `AIMessage`, and how messages pass through the model

- SOURCE FILE: https://github.com/langchain-ai/langchain-academy/blob/main/module-1/router.ipynb


---

## LESSON 4: AGENT

IN THE LESSON: 
- Three arithmetic tools (add, multiply, divide)
- A loop that allows the agent to call multiple tools sequentially

- SOURCE FILE: https://github.com/langchain-ai/langchain-academy/blob/main/module-1/agent.ipynb

---

## LESSON 5: Agent with Memory

This lesson demonstrates:
- How to use `thread_id` to maintain conversation context
- How different threads maintain separate conversation histories
- The agent can now remember previous calculations and reference them
- 
### Main Topics:-
- **MemorySaver**: In-memory checkpointer for graph state
- **thread_id**: Unique identifier for conversation threads
- **Persistence**: Automatic saving of graph state after each step

- SOURCE FILE: https://github.com/langchain-ai/langchain-academy/blob/main/module-1/agent-memory.ipynb

---

## THE STUDIO : USING THE LANGSMITH GRAPH
** THIS IS WHAT I GOT WHEN I GAVE THE PROMPT IN THE LANGGRAPH STUDIO USING THE SIMPLE GRAPH FEATURE 

<img width="1280" height="708" alt="image" src="https://github.com/user-attachments/assets/0d9dff3d-fb72-47e6-9234-0f658853310a" />

---

## MODULE 2

---

## LESSON 1: STATE SCHEMA

- What We Learned

- State Schema defines the structure and types of data that our LangGraph uses
- Explored three ways to define state: TypedDict, Dataclass, and Pydantic
- TypedDict and Dataclass provide type hints but don't enforce types at runtime
- Pydantic performs validation at runtime to ensure data conforms to specified types and constraints
- Each state key acts as a "channel" that nodes can read from and write to
- Nodes return dictionaries to update state, regardless of which schema type is used

- SOURCE FILE:https://github.com/langchain-ai/langchain-academy/blob/main/module-2/state-schema.ipynb

---

## LESSON 2: STATE REDUCERS 

- What We Learned

- Reducers specify how state updates are performed on specific keys/channels in the state schema
- By default, LangGraph overwrites state values with each node update
- Problem with branching: When nodes run in parallel (same step), both try to overwrite state, causing an InvalidUpdateError

- SOURCE FILE:https://github.com/langchain-ai/langchain-academy/blob/main/module-2/state-reducers.ipynb

---

## LESSON 3: MULTIPLE SCHEMA 

- What We Learned:

- By default, all nodes communicate with a single schema (input = output)
- LangGraph supports multiple schemas for advanced control over data flow
- Private State: Pass internal data between nodes that's not needed in final output
- Input/Output Filtering: Constrain what keys are allowed on graph boundaries

- SOURCE FILE:https://github.com/langchain-ai/langchain-academy/blob/main/module-2/multiple-schemas.ipynb

---

## LESSON 4: TRIM AND FILTERING MESSAGES 

- What We Learned:

- Message State Management: How to work with messages as graph state
- Token Management: Strategies to control token usage and latency in long conversations
- Message Filtering: Selecting specific messages to pass to the model
- Message Trimming: Restricting messages based on token limits

- SOURCE FILE:https://github.com/langchain-ai/langchain-academy/blob/main/module-2/trim-filter-messages.ipynb

---

## LESSON 5:Chatbot w/ Summarizing Messages and Memory

- What We Learned

- Message Summarization: Using LLMs to create running summaries of conversations
- Memory Persistence: LangGraph's checkpointer system for state management
- Thread Management: Organizing separate conversation contexts
- Conditional Logic: Dynamic routing based on conversation length

- SOURCE FILE:https://github.com/langchain-ai/langchain-academy/blob/main/module-2/chatbot-summarization.ipynb

---

## LESSON 6:Chatbot w/ Summarizing Messages and External Memory

-Learned how to implement external checkpointers like SQLite to save each thread’s state, allowing the chatbot to continue conversations with previous context intact and reducing token usage.

- SOUREC FILE:https://github.com/langchain-ai/langchain-academy/blob/main/module-2/chatbot-external-memory.ipynb

---



