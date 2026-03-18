# 🧠 meet2action-ai

## 🚀 Overview
This project is an **AI-powered multi-agent system** built using LangGraph that converts raw meeting notes into **structured, actionable tasks**.

The system processes unstructured text through multiple intelligent agents, applies classification, and incorporates a **Human-in-the-Loop (HIL)** step before exporting finalized tasks.

<img width="1536" height="1024" alt="ChatGPT Image Mar 18, 2026, 01_19_16 PM" src="https://github.com/user-attachments/assets/99b2ce9d-2c54-4bc8-b943-571e5a318111" />


## 🛠️ Tech Stack
- Python (3.10+ recommended)
- Jupyter Notebook
- LangGraph
- LangSmith

## 🧩 System Architecture

The system follows a **pipeline-based multi-agent workflow**:

  <img width="317" height="636" alt="Screenshot 2026-03-18 132444" src="https://github.com/user-attachments/assets/b89c383e-207f-4f10-9bcc-c053561ae5fd" />

## 🤖 Agents Description

### 1. Meeting Parser Agent
- Takes raw meeting notes as input
- Cleans and restructures them into meaningful, readable text
- Removes ambiguity and noise

### 2. Action Item Extractor
- Analyzes parsed notes
- Identifies actionable tasks
- Converts them into structured action items

### 3. Priority Classifier Agent
- Assigns:
  - **Priority** (HIGH / MEDIUM / LOW)
  - **Team Ownership** (Backend / Frontend / Platform, etc.)
- Adds additional context like descriptions if needed

## 👤 Human-in-the-Loop (HIL)

The system pauses execution before finalizing tasks.

Users can:
- Review generated tasks
- Edit titles, priorities, descriptions, or teams
- Approve or reject tasks

### Why HIL?
- Improves accuracy  
- Enables human validation  
- Prevents incorrect automation  

## 📤 Export Node

Once approved, tasks are exported into:

### ✅ Text File (`.txt`)
- Human-readable format  
- Structured output with:
  - Title  
  - Priority  
  - Team  
  - Description  

### ✅ JSON File (`.json`)
- Machine-readable format  
- Useful for:
  - APIs  
  - Jira / ticketing systems  
  - Automation pipelines  

## ⚙️ Key Features

- Multi-agent workflow using LangGraph  
- LLM-powered parsing and reasoning  
- Human-in-the-loop approval system  
- Dual export (TXT + JSON)  
- Stateful execution with checkpointing  
- Modular and extensible architecture

## 🧪 Example

### Input:
John mentioned that users are complaining about login timeout.
We should probably investigate that.

Someone also said the Kafka consumer crashes sometimes and maybe
we should add retry logic.

Also checkout page UI breaks on mobile devices.


### Output:
- Investigate login timeout issue → LOW → Backend  
- Add retry logic to Kafka consumer → MEDIUM → Platform  
- Fix mobile UI issues on checkout → HIGH → Frontend  

## 🏁 Getting Started

1. Clone the repository  
2. Create a virtual environment  
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
4. Run the Jupyter Notebook

5. Execute the LangGraph pipeline

## 📌 Future Enhancements

1. Jira / ServiceNow integration

2. Streamlit UI for task editing

3. Analytics dashboard

4. Smarter prioritization using historical data

## 💡 Notes

This is a Proof of Concept (POC) for AI-driven workflow automation

Can be extended into a production-grade task management system
