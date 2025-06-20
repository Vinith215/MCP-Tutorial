"""
langchain_mcp_client.py
This file implements an MCP client that:
  - Connects to an MCP server via a stdio connection.
  - Loads the available MCP tools using the adapter function load_mcp_tools.
  - Instantiates the ChatGoogleGenerativeAI model (Google Gemini) using your GOOGLE_API_KEY.
  - Creates a React agent using LangGraph’s prebuilt agent (create_react_agent) with the LLM and tools.
  - Runs an interactive asynchronous chat loop for processing user queries.

Detailed explanations:
  - Retries (max_retries=2): If an API call fails due to transient errors (e.g., network issues),
    the call will automatically be retried up to 2 times. Increase this if you experience temporary failures.
  - Temperature (set to 0): Controls randomness. A temperature of 0 yields deterministic responses.
    Higher values (e.g., 0.7) yield more creative, varied responses.
  - GOOGLE_API_KEY: Required for authentication with Google’s generative AI service.
  
Responses are printed as JSON using a custom encoder to handle non-serializable objects.
"""
