# Deepmind
📘 LangChain Agent with Tools, Memory & Tavily Search (LangChain v1)

A beginner-friendly AI Agent built using LangChain v1, OpenAI, Tavily Search, and custom tools.
Supports:

✅ Tool Calling
✅ Short-Term Memory (Chat History)
✅ Web Search using Tavily
✅ Weather Tool
✅ Datetime Tool
✅ Interactive CLI Chat
✅ Clean & simple LangChain v1 setup

🚀 Features
🔧 Built-in Tools

get_current_datetime → Returns the current system time

get_weather(city) → Weather using the free wttr.in API (no key needed)

TavilySearchResults → Web search with Tavily

🧠 Memory System

Stores up to 10 recent message pairs (20 messages total)

Maintains context across conversations

Automatically formats memory for LangChain v1

🤖 Agent System

Uses ChatOpenAI (gpt-4o-mini)

Supports structured tool calling (LangChain v1 standard)

Handles parsing errors

Verbose mode enabled for debugging

📦 Requirements

Install using your Python 3.10 environment:

pip install langchain==0.3.14
pip install langchain-openai==0.2.14
pip install langchain-core==0.3.29
pip install langchain-community==0.3.14
pip install tavily-python==0.5.0
pip install python-dotenv==1.0.1
pip install requests==2.32.3
pip install openai>=1.0.0
pip install pydantic>=2.0.0


Or, add everything inside requirements.txt and run:

pip install -r requirements.txt

🔑 Environment Variables

Create a file called .env in the same folder as your script:

OPENAI_API_KEY=your-openai-key-here
TAVILY_API_KEY=your-tavily-key-here


Both keys are required:

OPENAI_API_KEY → for the LLM

TAVILY_API_KEY → for web search

▶️ How to Run
1️⃣ Activate venv
venv\Scripts\activate

2️⃣ Run the agent
python main.py


You will see:

============================================================
LangChain Agent with Tools and Memory (v1)
============================================================
📋 Loading API keys...
🤖 Initializing agent...
✅ Agent ready!

💬 Usage (Inside the Chat)

Enter messages normally:

You: what is the time now?
🤖 Agent: The current time is...

⏱ Useful Commands
Command	Action
quit / exit / q	Stop the agent
history	Show recent chat history
clear	Clear memory
🛠 Project Structure
project/
│
├── main.py          # Your agent code
├── .env             # API keys
├── requirements.txt # Dependencies
└── README.md        # Documentation

📙 How the Agent Works
1. Loads tools
2. Loads prompt with memory placeholders
3. Uses create_tool_calling_agent() (correct v1 method)
4. Uses AgentExecutor to run
5. Stores every human/assistant message in memory
6. Trims memory to last 10 interactions
7. Responds using LLM — with tool support when needed

Done !
