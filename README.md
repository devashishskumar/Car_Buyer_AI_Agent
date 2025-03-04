# 🚗 Smart Car Buyer AI Agent  

## 📌 Overview  

The **Smart Car Buyer AI Agent** is an **LLM-powered AI assistant** designed to help users **search, filter, and analyze car listings** efficiently. Developed as a **Proof of Concept (PoC)**, it currently supports **AutoTrader** but can be easily extended to integrate with other platforms.

## 🎯 Features  

- 🧠 **LLM-powered Decision Making** – Interacts dynamically with users to refine their preferences.  
- 🔍 **Smart Search Filters** – Automatically applies relevant filters to match user requirements.  
- 🌐 **Web Scraping & Data Retrieval** – Fetches car listings from **AutoTrader** (with potential for more).  
- 📊 **Insightful Recommendations** – Summarizes listings and provides key insights.  
- 🖥 **Interactive Gradio Interface** – User-friendly UI for easy navigation and query input.  

---

## 🏗 Architecture  

The agent follows a structured workflow:  

1. **User Need Assessment** – Understands user preferences (budget, brand, fuel type, etc.).  
2. **Filter Optimization** – Applies relevant filters dynamically.  
3. **Listing Retrieval** – Scrapes listings from the integrated platform.  
4. **Insight Generation** – Provides key information and comparative analysis.  

![Smart Product Buyer Agent Architecture](images/car_buyer_agent_langgraph.png)

---

## 🛠️ Tech Stack  

- **LangGraph & LangChain** – AI workflow orchestration  
- **OpenAI GPT (LLM)** – AI-based user interaction & recommendation  
- **Playwright & lxml** – Web scraping  
- **Gradio** – Web-based UI for user interaction  
- **DuckDuckGo Search** – Fetches additional car-related insights  

---

## 📦 Installation  

### 1️⃣ Clone the Repository  

```bash
git clone git@github.com:devashishskumar/car-buyer-agent.git
cd car-buyer-agent

2️⃣ Set Up a Virtual Environment

python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`

3️⃣ Install Dependencies

pip install -r requirements.txt

	If you’re running this inside a Jupyter Notebook, first install Jupyter:

4️⃣ Configure Environment Variables

Create a .env file in the project root and add your API keys:

OPENAI_API_KEY=your_openai_api_key
LANGCHAIN_API_KEY=your_langchain_api_key (optional)

5️⃣ Run the Notebook

Launch Jupyter Notebook and open car_buyer_agent_langgraph.ipynb:

jupyter notebook

Run all cells to initialize the Gradio interface. Once running, click the provided link to interact with the agent.

	Note: If scraping is slow on Google Colab, it is recommended to run locally (preferably on macOS/Linux or WSL for Windows users).

🖥 Running Without Gradio

For debugging and testing, you can disable the Gradio UI:
	1.	Open the notebook.
	2.	Set USE_GRADIO = False.
	3.	Run the cells manually.

🛠 Dependencies

The project requires the following Python packages:

pip install langgraph langchain langchain-openai langchain-community importnb
pip install python-dotenv patchright lxml nest_asyncio playwright duckduckgo-search gradio

🔑 Key Learnings
	•	AI-driven automation enhances the user experience in decision-making.
	•	Web scraping techniques play a crucial role in fetching and presenting relevant listings.
	•	Workflow orchestration with LangGraph enables dynamic state-based AI interactions.

🚀 Future Enhancements
	•	🔄 Multi-platform support – Expand beyond AutoTrader to integrate other car listing sites.
	•	📊 Advanced analytics – Compare price trends, reliability, and cost of ownership.
	•	🏡 Other product categories – Extend AI agent capabilities to electronics, real estate, etc.
