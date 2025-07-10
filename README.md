💻 Project Setup: LangChain-Based Experimental Environment
This document outlines the steps to set up a Python-based AI project environment using LangChain, Groq, and other tools for experimentation and later modularization.

✅ Step 1: Create a Conda Virtual Environment
bash
Copy
Edit
conda create -p venv python=3.10 -y
conda activate ./venv
✅ Step 2: Create requirements.txt
Add the following libraries to requirements.txt:

txt
Copy
Edit
langchain                # Framework to work with LLMs
langchain-openai         # Integration with OpenAI
langchain-core
langchain-community
langchain_groq           # For using Groq LLMs
langgraph                # Updated LangChain graph support
faiss-cpu                # In-memory vector store (alternative to Pinecone)
wikipedia                # Get content from Wikipedia
python-dotenv            # Load environment variables from .env
✅ Step 3: Install All Dependencies
bash
Copy
Edit
pip install -r requirements.txt
✅ Step 4: Setup Environment Variables
Go to: https://console.groq.com/keys

Create your API key.

Add it to a .env file:

env
Copy
Edit
GROQ_API_KEY=your_key_here
You can add your OpenAI key here too if needed.

✅ Step 5: Install Jupyter Kernel (for .ipynb files)
bash
Copy
Edit
pip install ipykernel
✅ Step 6: Create the Experimentation File
Create a new Jupyter notebook file:

bash
Copy
Edit
touch tax.ipynb
Use this notebook to test:

LangChain pipelines

Retrieval from Wikipedia

Output formatting

💡 Note: It's best practice to first experiment with features in a notebook before modularizing them into Python scripts.

✅ Step 7: Running the Notebook
Launch Jupyter Lab or Notebook:

bash
Copy
Edit
jupyter lab
# or
jupyter notebook
Run code cells using Shift + Enter.

🔧 Modularization (After Testing)
Once your experimentation is validated:

Move logic into Python modules (e.g., /src or /modules)

Follow a clean architecture (e.g., split into retrieval, processing, response generation, etc.)
