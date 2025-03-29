# 🚀 MCP Client with Gemini AI

You now have **two different MCP client implementations** in this repo:

### ➔ Option 1: Legacy Client (with Gemini but without LangChain)
```bash
uv run client.py path/to/server.py
```

### ➔ Option 2: New LangChain Client (with Gemini + React Agent)
```bash
uv run langchain_mcp_client.py path/to/server.py
```



[![Tutorial video](https://img.youtube.com/vi/GAPncIfnDwg/maxresdefault.jpg)](https://youtu.be/GAPncIfnDwg)  
[![New LangChain Client Video](https://img.youtube.com/vi/hccNm88bk6w/maxresdefault.jpg)](https://youtu.be/hccNm88bk6w)

[📢 Subscribe to The AI Language!](https://youtube.com/@theailanguage?sub_confirmation=1)

Before we begin, if you enjoy learning about AI, coding, and automation, please **like this video and subscribe** to the channel. Now, let’s get started!

---

## 📌 **Features**
✅ Connects to an MCP server (Python or Node.js)  
✅ Sends queries to **Google Gemini AI**  
✅ Lets **Gemini call external tools** from the MCP server  
✅ Executes MCP tool commands and **returns the results**  
✅ **Maintains conversation history**, so Gemini **remembers past queries**

---

## 📦 **Installation**

**1⃣ Install the required dependencies using `uv` (Universal Virtualenv):**
```bash
uv add mcp python-dotenv google-genai
```

**2⃣ Clone this repository:**
```bash
cd mcp-client-gemini
```

**3⃣ Set up the project and virtual environment:**
```bash
uv init mcp-client
cd mcp-client
uv venv
```

**4⃣ Activate the virtual environment:**
```bash
# On Windows:
.venv\Scripts\activate

# On MacOS/Linux:
source .venv/bin/activate
```

---

## 🔑 **Setting Up the API Key**

To use **Google Gemini AI**, you need an **API key**. Please got to [Google AI Studio](https://aistudio.google.com/prompts/new_chat). Please read their terms and conditions and other policies before obtaining and using the key

**1⃣ Create a `.env` file:**
```bash
touch .env
```

**2⃣ Add your API key inside `.env`:**
```
GEMINI_API_KEY=your_api_key_here
```

**3⃣ Make sure `.env` is ignored in Git:**
```bash
echo ".env" >> .gitignore
```

*Note:* If you're using the new LangChain client, you can also name the key `GOOGLE_API_KEY`. The client will automatically load it using `dotenv`.

---

## 🚀 **Running the MCP Client**

You now have **two different MCP client implementations** in this repo:

### ➔ Option 1: Legacy Client (Without LangChain)
```bash
uv run client.py path/to/server.py
```

### ➔ Option 2: New LangChain Client (with Gemini + React Agent)
```bash
uv run langchain_mcp_client.py path/to/server.py
```

Watch the LangChain tutorial video 👉 [https://youtu.be/hccNm88bk6w](https://youtu.be/hccNm88bk6w)

---

## 🔧 **How It Works**

1⃣ You enter a query like:  
`Create a file named test.txt`

2⃣ The MCP client sends this to **Google Gemini AI**

3⃣ Gemini sees available MCP tools and calls the correct one (e.g. `run_command`)

4⃣ The MCP client executes the command via the server and returns the result

5⃣ Gemini responds with context-aware output and remembers previous interactions

---

## 📁 **Project Structure**
```
mcp-client-gemini/
│— client.py                 # Legacy MCP Client (without LangChain)
│— langchain_mcp_client.py   # New MCP Client using LangChain & Gemini
│— .env                      # Stores your Google Gemini API key
│— README.md                 # This documentation
│— requirements.txt          # Optional dependency list
│— server/                   # Folder for MCP servers (e.g., terminal_server.py)
│— .gitignore                # To ignore .env and other files
│— LICENSE                   # License file
```

---

## 🎯 **Example**

Run with a terminal server:
```bash
uv run langchain_mcp_client.py ../servers/terminal_server/terminal_server.py
```

Query:
```
create file notes.txt and write hello inside
```

Output:
```json
{
  "messages": [
    {
      "type": "HumanMessage",
      "content": "create file notes.txt and write hello inside"
    },
    {
      "type": "AIMessage",
      "content": "Sure! I will create notes.txt and add 'hello' inside it."
    }
  ]
}
```

---

## 🌟 **Contributing**

Want to help improve this project?  
✅ Add more MCP tools  
✅ Submit bug fixes or ideas  
✅ Help improve documentation

Just fork this repo and submit a pull request.

---

## 📺 **Tutorial Videos**

🎥 Legacy MCP Client Tutorial  
👉 [https://youtu.be/GAPncIfnDwg](https://youtu.be/GAPncIfnDwg)

🎥 LangChain + Gemini MCP Client  
👉 [https://youtu.be/hccNm88bk6w](https://youtu.be/hccNm88bk6w)

---

Happy building, and don’t forget to subscribe!  
👉 [https://youtube.com/@theailanguage?sub_confirmation=1](https://youtube.com/@theailanguage?sub_confirmation=1)

