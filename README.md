# SmolAgents Examples Notebook

This project contains a Jupyter notebook (`smlag.ipynb`) demonstrating various features and use cases of the `smolagents` library. Examples include basic search, integrating different language models (Hugging Face, LiteLLM for Gemini, Ollama), creating multi-agent systems, and implementing an Agentic RAG system.

## Setup Instructions

Follow these steps to set up your environment and run the notebook.

### 1. Create a Virtual Environment

It is recommended to use a virtual environment to manage dependencies.

```bash
python -m venv env
source env/bin/activate  # On Windows use `env\Scripts\activate`
```

### 2. Install Dependencies

Install the required Python packages using pip:

```bash
pip install smolagents duckduckgo-search 'smolagents[litellm]' pandas langchain langchain-community sentence-transformers datasets python-dotenv rank_bm25 requests --upgrade
```

### 3. Hugging Face Login (Optional)

If you plan to use models from the Hugging Face Hub that require authentication, log in using the Hugging Face CLI:

```bash
huggingface-cli login
```
Follow the prompts to enter your Hugging Face token.

### 4. Set Up Environment Variables

Some examples in the notebook, particularly those using the Gemini API, require an API key. Create a `.env` file in the root of the project directory:

```
touch .env
```

Open the `.env` file and add your Gemini API key:

```env
GEMINI_API_KEY="YOUR_GEMINI_API_KEY"
```

Replace `"YOUR_GEMINI_API_KEY"` with your actual Gemini API key.

## Running the Notebook

Once the setup is complete, you can launch Jupyter Lab or Jupyter Notebook and open `smlag.ipynb`:

```bash
jupyter lab
```
or
```bash
jupyter notebook
```

You can then run the cells in the notebook to explore the examples.

