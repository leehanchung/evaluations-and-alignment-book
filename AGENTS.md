# AGENTS.md

Instructions for AI coding agents (Claude Code, Cursor, Copilot, etc.) working in this repository.

## Project Overview

Companion repository for **AI Evaluation and Alignments** (Manning Seminal Papers Series).

### Chapters (Available)

**Part 1: Foundational Evaluation Metrics**
- Ch 1: Evaluations and Alignments for AI
- Ch 2: BLEU and ROUGE
- Ch 3: BERTScore and COMET

**Part 2: AI Native Evaluation**
- Ch 4: LLM-as-a-Judge

## Environment

- **Python**: 3.14+
- **Package Manager**: uv (not pip)
- **Virtual Environment**: `.venv/`

## Commands

```bash
# Run Python
uv run python script.py

# Run Jupyter
uv run jupyter notebook

# Lint and format
uv run ruff check .
uv run ruff format .

# Add dependencies
uv add package-name
uv add --dev package-name
```

## Project Structure

```
notebooks/
├── ch01_intro.ipynb
├── ch02_bleu_rouge.ipynb
├── ch03_bertscore_comet.ipynb
└── ch04_llm_as_judge.ipynb

data/              # Data files (gitignored)
docs/              # Additional documentation
```

## Key Dependencies

| Package | Purpose | Import |
|---------|---------|--------|
| pandas | DataFrames | `import pandas as pd` |
| numpy | Arrays | `import numpy as np` |
| torch | Deep learning | `import torch` |
| transformers | LLMs | `from transformers import ...` |
| datasets | HF datasets | `from datasets import load_dataset` |
| evaluate | Metrics | `import evaluate` |
| anthropic | Claude API | `from anthropic import Anthropic` |
| openai | OpenAI API | `from openai import OpenAI` |

## Coding Standards

### Style
- Use `ruff` for linting and formatting
- Follow PEP 8
- Use type hints for function signatures

### Imports
```python
# Standard library
import os
from pathlib import Path

# Third-party
import numpy as np
import pandas as pd
import torch
from transformers import AutoModel
```

## Common Patterns

### Loading Evaluation Metrics
```python
import evaluate

bleu = evaluate.load("bleu")
rouge = evaluate.load("rouge")
bertscore = evaluate.load("bertscore")
```

### Using Claude API
```python
from anthropic import Anthropic

client = Anthropic()  # Uses ANTHROPIC_API_KEY env var
response = client.messages.create(
    model="claude-sonnet-4-20250514",
    max_tokens=1024,
    messages=[{"role": "user", "content": "Hello"}]
)
```

### Using OpenAI API
```python
from openai import OpenAI

client = OpenAI()  # Uses OPENAI_API_KEY env var
response = client.chat.completions.create(
    model="gpt-4",
    messages=[{"role": "user", "content": "Hello"}]
)
```

### Loading Models
```python
from transformers import AutoModelForCausalLM, AutoTokenizer

tokenizer = AutoTokenizer.from_pretrained("model-name")
model = AutoModelForCausalLM.from_pretrained("model-name")
```

## Do Not

- Do not use `pip` directly; use `uv add` or `uv run pip`
- Do not commit `.env` files or API keys
- Do not commit large model weights or datasets
- Do not modify `uv.lock` manually

## File Locations

- API keys: `.env` (create locally, gitignored)
- Project config: `pyproject.toml`
- Lock file: `uv.lock`
- Python version: `.python-version`

## Documentation

- `README.md` - User documentation and setup
