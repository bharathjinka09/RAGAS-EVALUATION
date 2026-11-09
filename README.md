# RAG Evaluation Framework

This repository provides a comprehensive pipeline to benchmark and evaluate Retrieval-Augmented Generation (RAG) workflows using the Ragas Evaluation Framework. It enables automated checking of component performance across key parameters, including context relevance, generation consistency, and answer validity.


🛡️ Installation

Set up the project dependency structure using either uv or pip:

Option A: Using uv (Recommended)

## Bootstrap an evaluation project template directly
uvx ragas quickstart rag_eval

Option B: Using pip

## Install the core framework package
pip install ragas

📊 Core RAG Evaluation Metrics

• Faithfulness: Measures the factual consistency of the generated response against the retrieved context fragments.
• Answer Relevancy: Measures how pertinent the generated response is to the user's initial question.
• Context Precision & Recall: Benchmarks the retrieval layer to verify whether the most relevant information was fetched successfully.
• Answer Correctness: Measures the factual and semantic accuracy of the generated answer against a specified ground-truth reference.

