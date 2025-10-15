## **LANGGRAPH**

This repository contains a series of lessons demonstrating how to build reasoning workflows and agents using **LangChain** and **LangGraph**.

---

## LESSON 1: SIMPLE GRAPH

This project demonstrates how to use **LangChain** and **LangGraph** to build a simple reasoning workflow.

It takes a natural language instruction like "Add 3 and 4. Multiply the output by 2. Divide the output by 5." and shows how such tasks can be represented and processed step-by-step in a computational graph.

---

## LESSON 2: CHAIN

This project demonstrates how to use **LangGraph** with the **API** to build a simple router that processes messages and uses tools like `multiply`.

---

## LESSON 3: ROUTER

### What We Learned
- **LangGraph** allows us to design structured "graphs" of actions — similar to flowcharts — for reasoning or decision-making
- Understood the difference between `HumanMessage`, `AIMessage`, and how messages pass through the model


---

## LESSON 4: AGENT

**In this lesson there is->
- Three arithmetic tools (add, multiply, divide)
- A loop that allows the agent to call multiple tools sequentially

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

---

## THE STUDIO :
** THIS IS WHAT I GOT WHEN I GAVE THE PROMPT IN THE LANGGRAPH STUDIO USING THE SIMPLE GRAPH FEATURE 

<img width="1280" height="708" alt="image" src="https://github.com/user-attachments/assets/0d9dff3d-fb72-47e6-9234-0f658853310a" />



