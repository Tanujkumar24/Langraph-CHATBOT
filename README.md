# 🚀 **ChatBot with LangGraph and Streamlit**

![LangGraph ChatBot](https://github.com/Tanujkumar24/Langraph-CHATBOT/blob/main/LANGGRAPH-CHATBOT.png)  
> *A powerful AI chatbot workflow using LangChain, LangGraph, Groq, and Streamlit for an interactive and tool-augmented chatbot.*

---

## 📌 **Project Overview**

This project implements an AI chatbot that combines **LangChain**'s capabilities with **LangGraph**'s state-based workflows. It is enhanced with tool usage, like **TavilySearch** for web search, and is accessible through a simple **Streamlit UI**.

This chatbot can answer questions, search the web for real-time data, and demonstrate a dynamic workflow using **LLMs (Large Language Models)**.

---

## ⚙️ **Tech Stack**

| **Technology**            | **Purpose**                                 |
|----------------------------|---------------------------------------------|
| **LangChain**             | LLM chaining, tool binding, and integration |
| **LangGraph**             | StateGraph for defining workflows           |
| **ChatGroq**              | Model serving for `Gemma2-9b-It` LLM        |
| **Tavily Search**         | External search tool for real-time results  |
| **Streamlit**             | Front-end UI for chatbot interaction        |
| **Transformers**          | Additional NLP pipeline setup               |

---

## 🧠 **Key Features**

1. **State Management with LangGraph**  
   The chatbot workflow is created using **LangGraph**, enabling dynamic node-based transitions:
   - **Agent Node:** Processes user input through an LLM.  
   - **Tools Node:** Executes real-time web searches using `TavilySearch`.  

2. **Tool-Augmented Chat**  
   When the LLM identifies the need for external tools, the **TavilySearch** API is invoked seamlessly to fetch up-to-date information.

3. **Interactive Front-End**  
   Built with **Streamlit**, this chatbot allows users to input questions and get AI-powered responses instantly.

---

## 📸 **Screenshots**

### Chatbot UI (Streamlit)
![Chatbot UI](https://via.placeholder.com/800x400?text=Streamlit+ChatBot+UI)

### Example Response:
**User Input:** "Who is the current prime minister of the USA?"  
**Bot Response:** *"I could not find any official Prime Minister as the USA has a President. The current President is Joe Biden."*

### LangGraph State Transition
![LangGraph Workflow](https://via.placeholder.com/800x400?text=LangGraph+State+Graph)

---

## 🛠️ **Setup and Installation**

Follow these steps to set up the project locally:

### 1. **Clone the Repository**
```bash
git clone https://github.com/yourusername/chatbot-langgraph.git
cd chatbot-langgraph
