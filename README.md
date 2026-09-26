# eval-template-library

**Cookiecutter Templates for Instant Eval Infra**

New evaluation infrastructure in 2 minutes via `cookiecutter gh:David899b/eval-template-library`.

## Templates Included

| Template | Use Case | Features |
|----------|----------|----------|
| `classification-eval` | Text classification | Golden set schema, harness, CI/CD gates, judge, drift |
| `extraction-eval` | Structured extraction | Schema-enforced prompts, Instructor, judge, compliance |
| `rag-eval` | RAG systems | Retrieval metrics, faithfulness, answer relevance, drift |
| `compliance-presets` | Regulatory compliance | Ley 25.326, GDPR, EU AI Act test suites |

## Quick Start
```bash
# Install cookiecutter
pip install cookiecutter

# Generate new eval project
cookiecutter gh:David899b/eval-template-library

# Follow prompts: project_name, use_case, model_provider, etc.
cd my-eval-project
pip install -e .
auto-eval evaluate --split test
streamlit run dashboard/app.py
```

## Template Structure
```
{{cookiecutter.project_slug}}/
├── configs/           # Configuration (gitignored secrets)
├── data/              # Golden sets (versioned, frozen)
├── src/               # Custom evaluators, judges
├── tests/             # Regression + compliance tests
├── dashboard/         # Streamlit dashboard
├── .github/workflows/ # CI/CD gates
└── pyproject.toml     # Dependencies + entry points
```

## Compliance Presets
- **Ley 25.326** (Argentina) — PII, data residency, audit trails
- **GDPR** (EU) — Data subject rights, DPIA, breach notification
- **EU AI Act** — High-risk AI system requirements, conformity assessment

## License
MIT License — Copyright (c) 2026 David Bautista
