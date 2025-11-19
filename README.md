






<img width="1690" height="786" alt="image" src="https://github.com/user-attachments/assets/197ec90b-846f-46fb-b412-e6418cc14b8a" />




🤖 n8n Context-Aware Telegram AI Chatbot

A powerful, intelligent chatbot built entirely on the n8n automation platform. Unlike standard bots, this agent possesses conversational memory, access to real-time internet data, and a distinct personality.

It leverages Meta Llama 4 Scout (via OpenRouter) for reasoning and Tavily for web searching, making it a truly capable assistant.

✨ Key Features

🧠 Conversational Memory The bot remembers the last 10 messages in the chat history. It understands context, allowing for natural follow-up questions without needing to repeat details.

🌐 Real-Time Web Access Powered by the Tavily Web Scraper Tool, the agent detects when it needs to search the internet to answer questions about current events, news, or specific data points.

💬 Engaging Personality Prompted to be friendly, witty, and human-like, moving away from robotic "I am an AI" responses.

🚀 Low-Code Architecture Built on n8n, making the workflow visual, easy to debug, and simple to extend without complex coding.

⚙️ How It Works

The entire logic is contained within a single n8n workflow that orchestrates the services.

⬇️ Receive Message: The Telegram Trigger node detects a new incoming message.

💾 Context Retrieval: The workflow retrieves the last 10 messages associated with that specific user ID.

🤖 AI Processing: The message and history are sent to the AI Agent (Llama 4 Scout).

🔎 Web Search (Auto-Tool): If the AI determines the query requires external data (e.g., "What is the stock price of Apple right now?"), it triggers the Tavily tool.

📝 Response Generation: The agent synthesizes its training data, chat history, and web results into a cohesive answer.

⬆️ Send Reply: The response is sent back to the user via the Telegram API.

💾 Storage Update: The new interaction is appended to the chat history for future context.

🛠️ Tech Stack

Orchestration: n8n (Cloud or Self-Hosted)

Messaging: Telegram Bot API

LLM Provider: OpenRouter API

Model: Meta Llama 4 Scout

Web Search: Tavily API

🚀 Getting Started

Prerequisites

Before importing the workflow, ensure you have the following:

n8n Instance: An active account on n8n.cloud or a self-hosted instance.

Telegram Bot Token: Create a bot via @BotFather on Telegram.

Tavily API Key: Sign up at Tavily for web search capabilities.

OpenRouter API Key: Sign up at OpenRouter to access the Llama 4 Scout model.

Installation

Download the Workflow:

Download the workflow.json file from this repository.

Import to n8n:

Open your n8n canvas.

Click the menu (top right) -> Import from File.

Select the workflow.json file.

Configure Credentials:

Telegram Node: Create a new credential type "Telegram API" and paste your Bot Token.

Tavily Node: Create a new credential type "Tavily API" and paste your key.

OpenRouter/LLM Node: In the AI Model node, select "OpenAI-compatible" (or the specific OpenRouter node if you have the community node installed) and input your API key and Base URL.

Activate:

Click Save.

Toggle the Active switch to On (top right corner).

💡 Usage Examples

Once the workflow is active, open your bot in Telegram and start chatting.

1. General Knowledge

User: Who directed the movie "Inception"?
Bot: "Inception" was directed by Christopher Nolan.

2. Contextual Follow-up (Memory Test)

User: What other movies has he directed?
Bot: Christopher Nolan has also directed "The Dark Knight Trilogy", "Interstellar", "Dunkirk", "Tenet", and "Oppenheimer".

3. Real-Time Information (Tavily Search)

User: What were the main highlights from the biggest tech conference last week?
Bot: [Bot searches the web] Last week at [Conference Name], the biggest highlights were the release of [Product X] and the announcement regarding [Topic Y]...

🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are greatly appreciated.

Fork the Project

Create your Feature Branch (git checkout -b feature/AmazingFeature)

Commit your Changes (git commit -m 'Add some AmazingFeature')

Push to the Branch (git push origin feature/AmazingFeature)

Open a Pull Request

📄 License

Distributed under the GPL-3.0 License. See LICENSE for more information.
