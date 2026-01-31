# Contributing

Thank you for your interest in contributing to the AI Evaluation and Alignments book companion repository.

## Ways to Contribute

- **Report bugs** in notebooks or documentation
- **Suggest improvements** to explanations or code examples
- **Fix typos** or clarify confusing sections
- **Add examples** that demonstrate concepts from the chapters

## Getting Started

1. Fork the repository
2. Clone your fork:
   ```bash
   git clone https://github.com/YOUR_USERNAME/eval-align-book.git
   cd eval-align-book
   ```
3. Set up the environment:
   ```bash
   uv sync
   ```
4. Create a branch for your changes:
   ```bash
   git checkout -b your-branch-name
   ```

## Development Workflow

### Running Notebooks

```bash
uv run jupyter notebook
```

### Code Style

We use `ruff` for linting and formatting:

```bash
uv run ruff check .
uv run ruff format .
```

### Commit Messages

Use clear, descriptive commit messages:
- `fix: correct BLEU score calculation in ch02`
- `docs: clarify RAG evaluation metrics in ch06`
- `feat: add visualization for reward model training`

## Submitting Changes

1. Ensure notebooks run without errors
2. Run `uv run ruff check .` and fix any issues
3. Commit your changes
4. Push to your fork
5. Open a pull request with a clear description of your changes

## Code of Conduct

Be respectful and constructive. We're all here to learn about AI evaluation and alignment.

## Questions?

Open an issue if you have questions about contributing.
