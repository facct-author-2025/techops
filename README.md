# Techops

This is the template for documentation of the AI Act, accompanying the FaCCT 2025 submission.

# Documentation Website

## Locally Develop and Render Documentation Site
Templates can be viewed locally by installing all dev requirements:

```bash
pip install ".[dev]"
```

and install pre-commit hooks:
```bash
pre-commit install -t pre-commit -t pre-push
```

When ready to render templates, start an mkdocs server:
```bash
mkdocs serve
```
