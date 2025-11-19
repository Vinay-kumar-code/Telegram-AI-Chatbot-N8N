






<img width="1690" height="786" alt="image" src="https://github.com/user-attachments/assets/197ec90b-846f-46fb-b412-e6418cc14b8a" />






n8n-based Telegram AI Chatbot 🤖
A powerful, context-aware AI chatbot for Telegram, built entirely on the n8n automation platform. This chatbot provides fun and engaging conversations, has access to real-time information from the web, and remembers the context of your conversation.



✨ Key Features
This isn't just another chatbot. It's a smart agent designed to be a helpful and interesting conversation partner.

🧠 Conversational Memory: The agent remembers the last 10 messages in the chat history, allowing for natural, context-aware follow-up questions and discussions.

🌐 Real-Time Web Access: Using the Tavily Web Scraper Tool, the chatbot can answer questions about recent events, news, and topics by searching the web, ensuring its knowledge is always up-to-date.

😄 Fun & Engaging Personality: The AI is prompted to be friendly, witty, and engaging, making interactions feel less robotic and more human-like.

🚀 Low-Code Implementation: Built on n8n, this project is easy to manage, modify, and extend, even with minimal coding knowledge.

⚙️ How It Works: The Workflow
The entire logic is contained within a single n8n workflow that orchestrates the different services.

⬇️ Receive Message: The workflow starts when the Telegram Trigger node receives a new message from a user.

💾 Store & Retrieve History: The workflow appends the new message to a stored chat history (limited to the last 10 messages) and retrieves this history for context.

🤖 Process with AI Agent: The user's message, along with the chat history, is sent to an AI Agent.

🔎 Web Search (If Needed): The AI agent determines if it needs fresh information to answer the query. If so, it activates the Tavily tool to perform a web search.

💬 Generate Response: The agent combines its base knowledge, the chat history, and any new information from the web to formulate a comprehensive and relevant response.

⬆️ Send Reply: The final generated message is sent back to the user on Telegram via the Telegram node.

🛠️ Setup & Installation
To get your own instance of this chatbot running, follow these steps.

Prerequisites
You will need the following accounts and credentials:

An active n8n instance (either on n8n.cloud or self-hosted).

A Telegram Bot Token. You can get one by talking to the BotFather on Telegram.

A Tavily API Key for the web scraping functionality.

An API key for your chosen Large Language Model (LLM) provider (e.g., OpenAI, Cohere, Anthropic). In my case openrouter api and Meta llama 4 scout llm.

Installation Steps
Download the Workflow: Grab the workflow.json file from this repository.

Import to n8n:

In your n8n canvas, click Import from File.

Select the workflow.json file you just downloaded.

Configure Credentials:

In the n8n workflow, you will see nodes that require credentials (Telegram, Tavily, and your LLM).

Click on each node and either select your existing credentials from the dropdown or create new ones by pasting in your API keys/tokens.

Activate the Workflow: Once all credentials are set up, save the workflow and activate it using the toggle at the top right of the screen.

🚀 Usage
Once the workflow is active, just open a chat with your bot on Telegram and start talking to it!

You can try asking it:

A simple question: What is the capital of Mongolia?

A recent event question: What were the main highlights from the biggest tech conference last week?

A follow-up question:

User: Who directed the movie "Inception"?

Bot: "Inception" was directed by Christopher Nolan.

User: What other movies has he directed?

🤝 Contributing
Pull requests are welcome! If you have ideas for improvements, new features, or bug fixes, please feel free to open an issue or submit a pull request.

Fork the Project

Create your Feature Branch (git checkout -b feature/AmazingFeature)

Commit your Changes (git commit -m 'Add some AmazingFeature')

Push to the Branch (git push origin feature/AmazingFeature)

Open a Pull Request

📄 License
This project is distributed under the GPL-3.0 License. See the LICENSE file for more information.
