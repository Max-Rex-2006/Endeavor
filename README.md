# Meta Phreaks — KDSH 2026

A RAG (Retrieval-Augmented Generation) pipeline built during the **KDSH 2026 Hackathon** to verify the factual consistency of narrative claims against long-form text sources like novels or historical documents.

## What it does

Given a set of claims, the system:
- Chunks source text into overlapping token windows for accurate retrieval
- Embeds both documents and queries using OpenAI's `text-embedding-3-small`
- Retrieves the top-K most relevant passages via a vector index (Pathway)
- Evaluates whether each claim is **consistent** or **contradicted** by the evidence
- Outputs structured, machine-readable verdicts in JSON format

## Tech Stack

- **Python** — core pipeline
- **Pathway** — real-time document ingestion and vector indexing
- **OpenAI API** — embeddings
- **tiktoken** — token-based chunking with overlap

## Project Structure

```
Projects/
├── Code.py          # RAG pipeline (ingestion, chunking, retrieval)
├── Claims.json      # Input claims to verify
├── Evidence.json    # Retrieved evidence passages
├── Judgements.json  # Verdict output per claim
├── results.csv      # Summary results
└── Readme.txt       # Original problem overview
```

## How to run

```bash
export OPENAI_API_KEY=your_key_here
python Code.py
```

## Team

**Meta Phreaks** — SOA University, KDSH 2026

---

> Built under hackathon time constraints. Focus was on reproducibility and structured reasoning over end-to-end generation.
