<div align="center">
 <img src="https://github.com/soonchain/4AI-Agent-Space/blob/main/img/Agent%20Space.png" alt="4AI Agent Space" width="900"/>

</div>

## Agent Space Introduction
Agent Space is an open-source framework that automatically selects the appropriate agent based on task requirements, executes the task, evaluates the results, and returns the result.

## 4AI Agent Space Framwork

![Alt text](https://github.com/soonchain/4AI-Agent-Space/blob/main/img/Agent_Space.png)

## Component
### 🔥 Pioneer  
This is the starting point that initiates the task with tags and a specific task. It sends the task with tags { tag: 1+4, task }.

### 🚀 Root Agent
Master Agent selects the suitable agents from the Agent Cluster based on the task's needs. And evaluates the outputs to determine the final result.

### 🌐 Agent  
Cluster: The "Agent Cluster" contains multiple agents (labeled A, B, C, D, E, etc.) that are assigned tags like 1, 2, 1+2, 3, 4, and so on.

## How To Start
### 📝 Agent Registration
The content of the [tag](https://github.com/soonchain/4AI-Agent-Space/edit/main/README.md) field is manually entered. Before registration, you should carefully consider the functionality of the agent. If the tag entered does not support the corresponding function or performs poorly, it will affect the agent's rating.  
```
# agent_1 
{
  "url" : "https://4AI.agent/agent-1",
  "name" : "agent 1",
  "tag" : {1, 3, 4}
}
```

## ⚙️ Use Case Example: Task Execution Flow

This example demonstrates how 4AI Agent Space works step-by-step in an actual scenario.

1. **Task Initiation (Pioneer)**
   - The Pioneer sends a task request:
     ```json
     {
       "task": "Analyze BSC transaction trends",
       "tag": [2, "bsc"]
     }
     ```

2. **Agent Selection (Root Agent)**
   - The Root Agent analyzes the tags and selects the most suitable agents:
     - Agent A (tag: 2)
     - Agent D (tag: "bsc")

3. **Task Execution (Agents)**
   - Both agents perform their tasks independently and return their results.

4. **Evaluation (Root Agent)**
   - The Root Agent compares the results and selects the one with the highest accuracy or reliability.

5. **Result Return (Pioneer)**
   - The final processed result is returned to the Pioneer:
     ```json
     {
       "summary": "Transaction volume on BSC increased by 12% last week.",
       "confidence": 0.93
     }
     ```

> ✅ This example shows how the system dynamically selects, executes, and evaluates multiple agents to provide the best possible result automatically.


## How to Contribute
Thank you for your interest in contributing! If you would like to contribute, please follow these steps:
1. **Fork the repository**.
2. **Clone the repository** to your local machine.
3. **Commit And Push** your changes to your forked repository.
4. **Create a Pull Request (PR)** describing the changes you made.

## Thank You!
Thank you for contributing to this project! We look forward to your ideas and improvements.
