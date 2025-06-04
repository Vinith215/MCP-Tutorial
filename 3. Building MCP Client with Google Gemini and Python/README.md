**🚀 MCP Client with Gemini AI**

This is an MCP (Model Context Protocol) client that connects to an MCP server and integrates with Google’s Gemini AI.
The client sends user queries to Gemini, allows Gemini to call external tools from the MCP server, executes them, and keeps track of the conversation history.
🔹 MCP (Model Context Protocol) allows AI models to interact with external tools and fetch information dynamically.
🔹 Google’s Gemini AI processes user queries and calls MCP tools when needed.
🔹 This client keeps a history of interactions so Gemini can remember past commands.

**📌 Features**

✅ Connects to an MCP server (Python or Node.js)
✅ Sends queries to Google Gemini AI
✅ Lets Gemini call external tools from the MCP server
✅ Executes MCP tool commands and returns the results
✅ Maintains conversation history, so Gemini remembers past queries

**📦 Installation**

1️⃣ Install the required dependencies using uv (Universal Virtualenv):
uv add mcp python-dotenv google-genai
2️⃣ Clone the repository:
git clone https://github.com/your-username/mcp-...
cd mcp-client-gemini
3️⃣ Set up the project and virtual environment:
- uv init mcp-client
- cd mcp-client
- uv venv
4️⃣ Activate the virtual environment:
On Windows:
- .venv\Scripts\activate  

**To use Google Gemini AI, you need an API key.**

1️⃣ Create a .env file:
type nul > .env
2️⃣ Add your API key inside .env:
echo API_KEY=your_api_key_here > .env
3️⃣ Make sure .env is ignored in Git:
echo .env > .gitignore

**🚀 Running the MCP Client**

- Start the MCP client and connect it to an MCP server:
- uv run client.py path/to/server.py  # Use a Python server  
- uv run client.py path/to/server.js  # Use a Node.js server  
- Example (if using a weather server):
- uv run client.py ./server/weather.py  


**🔧 How It Works**

1️⃣ The user enters a query (e.g., "Create a file named test.txt").
2️⃣ The MCP client sends the query to Gemini AI.
3️⃣ Gemini AI checks available MCP tools and calls the correct one.
4️⃣ The MCP client executes the command and returns the result.
5️⃣ Gemini remembers past interactions and adjusts responses accordingly.

**📁 Project Structure**

mcp-client-gemini/  
│── client.py          # MCP Client (Main script)  
│── .env               # Stores API Key (ignored in Git)  
│── README.md          # Documentation  
│── requirements.txt   # Dependencies (optional)  
│── server/            # Folder for MCP server scripts (e.g., weather.py)  
│── .gitignore         # Ignores sensitive files  
