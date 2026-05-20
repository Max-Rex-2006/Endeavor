# Endeavor

> A GSSOC-ready project space for a hackathon-built RAG pipeline that checks whether narrative claims are supported by long-form text sources.

## Overview

**Endeavor** is centered on a Retrieval-Augmented Generation (RAG) workflow created during **KDSH 2026**. The project explores how structured retrieval and evidence-based reasoning can be used to verify factual consistency in claims drawn from novels, historical documents, or other long-form text.

In practical terms, the workflow is designed to:

- split large source material into searchable chunks,
- embed claims and source passages for retrieval,
- fetch the most relevant evidence,
- compare each claim against retrieved passages, and
- produce machine-readable judgement output.

This repository is a strong candidate for open-source collaboration because the idea is clear, the problem statement is practical, and there is room for contributors to improve documentation, code organization, evaluation quality, and reproducibility.

## Project Goals

- Build an evidence-first claim verification pipeline
- Make the workflow easier to understand and reproduce
- Improve repository structure for open-source collaboration
- Encourage beginner-friendly contributions during **GirlScript Summer of Code (GSSOC)**

## What Contributors Can Expect

Contributors can expect a project that is:

- **practical** — focused on retrieval, verification, and structured output,
- **learning-friendly** — approachable for contributors interested in Python, RAG, NLP, or hackathon projects,
- **open for refinement** — ideal for improving documentation, code quality, usability, and evaluation flow.

If you are a new contributor, this repository is a good place to learn how a small AI workflow can be documented, organized, and gradually shaped into a more complete open-source project.

## How the Project Works

Based on the original project notes, the pipeline follows this flow:

1. Source text is chunked into overlapping token windows
2. Claims and chunks are embedded using OpenAI embeddings
3. A vector index is used to retrieve the most relevant evidence
4. Claims are checked against retrieved passages
5. Results are exported in structured formats such as JSON and CSV

## Expected Project Structure

The current repository snapshot is minimal, but the existing project description references a structure similar to the following:

```text
Projects/
├── Code.py          # Core RAG pipeline
├── Claims.json      # Input claims to verify
├── Evidence.json    # Retrieved evidence passages
├── Judgements.json  # Final verdicts per claim
├── results.csv      # Summary output
└── Readme.txt       # Original project notes
```

As the repository grows, contributors can help turn this into a clearer and more maintainable layout.

## Tech Stack

- **Python** for the core pipeline
- **Pathway** for document ingestion and vector indexing
- **OpenAI API** for embeddings
- **tiktoken** for token-aware chunking

## Getting Started

At the moment, this repository mainly provides project context rather than a fully tracked runnable codebase.

If the original project files are added or restored, the intended usage from the earlier project notes is:

```bash
export OPENAI_API_KEY=your_key_here
python Code.py
```

Until then, reviewers and contributors can use this repository to:

- understand the project idea quickly,
- review the intended workflow and outputs,
- propose improvements to documentation and structure,
- prepare the repository for broader open-source participation.

## Contributing

Contributions are welcome — especially documentation improvements, project organization updates, beginner-friendly issues, and future code cleanups.

Please read **[CONTRIBUTING.md](./CONTRIBUTING.md)** before opening an issue or pull request.

## GSSOC Contributors Welcome

This repository is being prepared with **GSSOC** in mind.

If you are a student or first-time open-source contributor, you are encouraged to participate. Good contributions can include:

- improving documentation,
- clarifying setup steps,
- organizing files and project structure,
- improving code readability when source files are available,
- suggesting or implementing beginner-friendly enhancements.

We want this repository to be welcoming, understandable, and easy to review for both maintainers and new contributors.

## Why This Project Stands Out for Reviewers

For GSSOC reviewers, Endeavor offers:

- a clear real-world use case,
- an AI/ML-flavored problem statement with practical relevance,
- room for meaningful beginner and intermediate contributions,
- a foundation that can evolve from hackathon prototype to cleaner open-source project.

## License

This repository is available under the **MIT License**. See [LICENSE](./LICENSE) for details.
