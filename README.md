# 🚀 MCP Client with Gemini AI

[![Tutorial video](https://img.youtube.com/vi/GAPncIfnDwg/maxresdefault.jpg)](https://youtu.be/GAPncIfnDwg)

[📢 Subscribe to The AI Language!](https://youtube.com/@theailanguage?sub_confirmation=1)

Before we begin, if you enjoy learning about AI, coding, and automation, please **like this video and subscribe** to the channel. It really helps us bring more tutorials your way! Now, let’s get started!

---

## 📌 **Features**
✅ Connects to an MCP server (Python or Node.js)  
✅ Sends queries to **Google Gemini AI**  
✅ Lets **Gemini call external tools** from the MCP server  
✅ Executes MCP tool commands and **returns the results**  
✅ **Maintains conversation history**, so Gemini **remembers past queries**  

---

## 📦 **Installation**
**1️⃣ Install the required dependencies using `uv` (Universal Virtualenv):**
```bash
uv add mcp python-dotenv google-genai
```

**2️⃣ Clone this repository:**
```bash
git clone https://github.com/your-username/mcp-client-gemini.git
cd mcp-client-gemini
```

**3️⃣ Set up the project and virtual environment:**
```bash
uv init mcp-client
cd mcp-client
uv venv
```

**4️⃣ Activate the virtual environment:**
```bash
# On Windows:
.venv\Scripts\activate

# On MacOS/Linux:
source .venv/bin/activate
```

---

## 🔑 **Setting Up the API Key**
To use **Google Gemini AI**, you need an **API key**.

**1️⃣ Create a `.env` file:**
```bash
touch .env
```

**2️⃣ Add your API key inside `.env`:**
```
GEMINI_API_KEY=your_api_key_here
```

**3️⃣ Make sure `.env` is ignored in Git:**
```bash
echo ".env" >> .gitignore
```

---

## 🚀 **Running the MCP Client**
**Start the MCP client and connect it to an MCP server:**
```bash
uv run client.py path/to/server.py  # Use a Python server
uv run client.py path/to/server.js  # Use a Node.js server
```

Example (if using a **weather server**):
```bash
uv run client.py ./server/weather.py
```

---

## 🔧 **How It Works**
1️⃣ The user enters a query (e.g., `"Create a file named test.txt"`).  
2️⃣ The MCP client sends the query to **Gemini AI**.  
3️⃣ **Gemini AI checks available MCP tools** and calls the correct one.  
4️⃣ The MCP client **executes the command** and returns the result.  
5️⃣ Gemini **remembers past interactions** and adjusts responses accordingly.  

---

## 📁 **Project Structure**
```
mcp-client-gemini/
│── client.py          # MCP Client (Main script)
│── .env               # Stores API Key (ignored in Git)
│── README.md          # Documentation
│── requirements.txt   # Dependencies (optional)
│── server/            # Folder for MCP server scripts (e.g., weather.py)
│── .gitignore         # Ignores sensitive files
│── LICENSE            # License file
```

---

## 🎯 **Contributing**
Feel free to submit issues or contribute improvements via pull requests.

---