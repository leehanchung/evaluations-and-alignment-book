# AI Evaluation and Alignments

Companion repository for **AI Evaluation and Alignments** (Manning Seminal Papers Series).

## Chapters

### Part 1: Foundational Evaluation Metrics
| Ch | Title | Notebook |
|----|-------|----------|
| 1 | Evaluations and Alignments for AI | [ch01_intro.ipynb](notebooks/ch01_intro.ipynb) |
| 2 | The Dawn of Automatic Evaluation: BLEU and ROUGE | [ch02_bleu_rouge.ipynb](notebooks/ch02_bleu_rouge.ipynb) |
| 3 | Bridging the Semantic Gap: BERTScore and COMET | [ch03_bertscore_comet.ipynb](notebooks/ch03_bertscore_comet.ipynb) |

### Part 2: AI Native Evaluation
| Ch | Title | Notebook |
|----|-------|----------|
| 4 | LLM-as-a-Judge: The New Paradigm | [ch04_llm_as_judge.ipynb](notebooks/ch04_llm_as_judge.ipynb) |
| 5 | Detecting and Quantifying Hallucinations | [ch05_hallucinations.ipynb](notebooks/ch05_hallucinations.ipynb) |
| 6 | Evaluating Retrieval-Augmented Generation | [ch06_rag_evaluation.ipynb](notebooks/ch06_rag_evaluation.ipynb) |

### Part 3: Aligning AI
| Ch | Title | Notebook |
|----|-------|----------|
| 7 | RLHF: The Foundation | [ch07_rlhf.ipynb](notebooks/ch07_rlhf.ipynb) |
| 8 | Constitutional AI: Alignment Through Principles | [ch08_constitutional_ai.ipynb](notebooks/ch08_constitutional_ai.ipynb) |
| 9 | Red Teaming and Beyond | [ch09_red_teaming.ipynb](notebooks/ch09_red_teaming.ipynb) |
| 10 | Deliberative Alignment | [ch10_deliberative_alignment.ipynb](notebooks/ch10_deliberative_alignment.ipynb) |

### Part 4: Future Directions
| Ch | Title | Notebook |
|----|-------|----------|
| 11 | The Evolving Landscape | [ch11_evolving_landscape.ipynb](notebooks/ch11_evolving_landscape.ipynb) |

## Quick Start

```bash
# Install uv (if not already installed)
curl -LsSf https://astral.sh/uv/install.sh | sh

# Clone and setup
git clone https://github.com/yourusername/eval-align-book.git
cd eval-align-book
uv sync

# Run Jupyter
uv run jupyter notebook
```

## Requirements

- Python 3.14+
- [uv](https://docs.astral.sh/uv/) package manager

## Project Structure

```
eval-align-book/
├── notebooks/          # Chapter notebooks (ch01-ch11)
├── data/               # Datasets (gitignored)
└── docs/               # Additional documentation
```

## Key Dependencies

- **Data**: pandas, numpy, matplotlib, seaborn
- **ML**: torch, transformers, datasets, evaluate
- **APIs**: anthropic, openai
- **Dev**: jupyter, ruff

## Environment Variables

Create a `.env` file (not tracked in git):

```bash
ANTHROPIC_API_KEY=your-key-here
OPENAI_API_KEY=your-key-here
```

## License

[Add your license here]
