# RAGAS Evaluation Notebook

This project contains a Jupyter notebook demonstrating a small retrieval-augmented generation (RAG) pipeline and its evaluation with Ragas. It creates embeddings for example documents, retrieves relevant context with FAISS, generates answers with OpenAI, and evaluates the results with Ragas metrics.

## Requirements

- Python 3.10 or 3.11
- An OpenAI API key with access to the models used in the notebook (`text-embedding-3-small` and `gpt-4o`)

## Installation

Open a terminal in the project directory and create a virtual environment:

```powershell
py -3.11 -m venv .venv
.\.venv\Scripts\Activate.ps1
```

On macOS or Linux, use:

```bash
python3.11 -m venv .venv
source .venv/bin/activate
```

Install the notebook dependencies:

```bash
python -m pip install --upgrade pip
python -m pip install "ragas==0.1.21" faiss-cpu openai python-dotenv jupyter
```

Ragas 0.1.21 is pinned because the notebook uses its `evaluate` and `ragas.metrics` APIs.

## Configure your API key

Create a file named `.env` in the project directory and add your key:

```dotenv
OPENAI_API_KEY=your_openai_api_key
```

The notebook loads this value with `python-dotenv`. Do not commit or share your `.env` file.

## Run the notebook

Start Jupyter:

```bash
jupyter notebook
```

Open `ragas.ipynb` in the browser, select the kernel from the virtual environment, and run the cells from top to bottom. The notebook makes paid OpenAI API calls for embeddings, answer generation, and evaluation; usage charges may apply.
