# 🕵️‍♂️ Deep Research AI Agent

**An autonomous research assistant that browses the web, synthesizes data, and provides answers with inline citations.**

<img src="Resume.png" alt="App Screenshot" width="800">

## 🚀 Key Features
* **Multi-Step Reasoning:** Uses `LangGraph` to plan research steps rather than just answering blindly.
* **Live Web Access:** Integrated with **Tavily API** to fetch real-time data (not limited to training cutoff).
* **Hallucination Guardrails:** Enforces strict citation rules (`[1]`, `[2]`) linking back to source URLs.
* **Transparent UI:** Built with **Streamlit** to show the user exactly which sources were used in the sidebar.
* **Secure by Design:** API keys are entered via the UI and never stored in code, making it safe for public demos.

## 🛠️ Tech Stack
* **Orchestration:** LangGraph & LangChain
* **LLM:** Google Gemini 2.5 Flash
* **Search Engine:** Tavily AI
* **Frontend:** Streamlit

## ⚙️ How it Works
1.  **User Query:** The user asks a complex question (e.g., "Compare Llama 3 vs GPT-4").
2.  **Researcher Node:** The agent identifies key search terms and queries the web using Tavily.
3.  **Context Construction:** Search results are parsed and structured into a context block.
4.  **Writer Node:** The LLM generates an answer, citing the specific source IDs from the context.

## 📦 Setup & Installation

### Option 1: Try it Live 🟢
Check out the live demo here: **[https://insight-agent-ai.streamlit.app/](https://insight-agent-ai.streamlit.app/)**

---

### Option 2: Run Locally 💻
1.  **Clone the repo:**
    ```bash
    git clone [https://github.com/Raghav1378/deep-research-agent.git](https://github.com/Raghav1378/deep-research-agent.git)
    cd deep-research-agent
    ```
2.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
3.  **Run the app:**
    ```bash
    streamlit run app.py
    ```
4.  **Enter API Keys:** The app will launch in your browser. Enter your **Google API Key** and **Tavily API Key** in the sidebar to start researching.
