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

## 🌐 **Workflow Diagram**

Below is the visual representation of the **LangGraph workflow**:

```mermaid
flowchart TD
    Start[Start] --> Agent[Agent Node: Process Input via LLM]
    Agent -->|Tool Call Detected| Tools[Tools Node: Tavily Search]
    Tools --> Agent
    Agent -->|No Tool Needed| End(End)

# Chatbot with LangGraph and Streamlit

## 📸 Screenshots
**Chatbot UI (Streamlit)**

**Example Response:**
- **User Input:** "Who is the current prime minister of the USA?"
- **Bot Response:** "I could not find any official Prime Minister as the USA has a President. The current President is Joe Biden."

**LangGraph State Transition**

---

## 🛠️ Setup and Installation
Follow these steps to set up the project locally:

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/chatbot-langgraph.git
cd chatbot-langgraph
```

### 2. Install Dependencies
Ensure you have Python 3.8+ installed. Install all necessary libraries using pip:
```bash
pip install -r requirements.txt
```

### 3. Set Environment Variables
Create a `.env` file to securely store API keys:
```plaintext
TAVILY_API_KEY=your_tavily_api_key
GROQ_API_KEY=your_groq_api_key
```

### 4. Run the Streamlit App
Execute the `app.py` file to start the chatbot UI:
```bash
streamlit run app.py
```

---

## 🎯 How It Works

### Input:
The user enters a question in the Streamlit app.

### Agent Processing:
- The question is passed to the LangGraph workflow.
- The ChatGroq LLM processes the message to identify intent.

### Tool Invocation:
- If external search is required, the TavilySearch API fetches relevant data.
- Results are passed back to the LLM for a complete response.

### Output:
The final response is displayed on the Streamlit UI.

---

## 🧩 Code Walkthrough

### `bot.py` - Chatbot Logic

#### Model Initialization:
- The ChatGroq model `Gemma2-9b-It` is loaded.

#### Tool Integration:
- **TavilySearch** is bound to the LLM using LangChain tools.
- Tools are managed via the `ToolNode`.

#### LangGraph Workflow:
- **Nodes:** agent and tools
- **State Transitions:**
  - `Start → Agent`
  - **Conditional Transition:** tools if tool calls are detected.

### `app.py` - Streamlit UI
- Provides a clean user interface for input and output.
- Connects the LangGraph workflow to the frontend.

---

## 📊 Visual Insights

### 1. Architecture Overview
```plaintext
User Input --> Streamlit UI --> LangGraph Workflow --> ChatGroq LLM --> Response
                            ↘ Tools Node (TavilySearch) ↙
```

### 2. Tool-Usage Graph
Tracks the number of tool calls made during execution.

---

## ✅ Why This Project Stands Out
- **Real-Time Data:** Integrates web search seamlessly.
- **Dynamic Workflow:** Uses LangGraph for flexible conversation handling.
- **Clear and Scalable Code:** Structured into reusable components.
- **Interactive UI:** Simple yet powerful frontend for user interaction.

---

## 🧪 Testing
To test the chatbot, you can input the following queries:
- **Basic LLM Query:** "What is LangChain?"
- **Tool Invocation Query:** "Who won the FIFA World Cup 2022?"

---

## 🚀 Future Enhancements
- Add support for more tools like Wikipedia Search or Google Search API.
- Implement session memory to handle multi-turn conversations.
- Integrate additional LLM models for enhanced performance.

---

## 👨‍💻 Contributing
Contributions are welcome! Feel free to open issues or submit pull requests.

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature-xyz
   ```
3. Commit your changes.
4. Push to the branch and open a PR.

---

## 📄 License
This project is licensed under the MIT License. See the LICENSE file for details.

---

## 🎥 Demo Video
[Link to Demo Video on YouTube or GitHub]
*"A 5-minute walkthrough of the chatbot in action!"*

---

## 📞 Contact
If you have any questions, reach out at:
- **Email:** [your-email@example.com]
- **LinkedIn:** [Your LinkedIn Profile](https://linkedin.com/yourprofile)

---

## 🔗 Repository Link
[GitHub Repo](https://github.com/yourusername/chatbot-langgraph)
