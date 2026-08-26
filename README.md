# batchask

Feed a thousand prompts, get a thousand answers

## Installation

```bash
pip install -r requirements.txt
export OPENAI_API_KEY=sk-...
```

## How to use

```bash
python batch.py prompts.jsonl -o answers.jsonl --workers 4
```

## Features

- JSONL in, JSONL out: stream-safe for huge inputs
- Concurrent workers with a rate ceiling
- Idempotent: skips ids already present in the output
- Retries failed items with backoff, logs them aside

## Project structure

```text
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   └── bug_report.md
│   └── pull_request_template.md
├── docs/
│   └── faq.md
├── examples/
│   └── quickstart.md
├── .editorconfig
├── .gitattributes
├── .gitignore
├── CHANGELOG.md
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── LICENSE
├── SECURITY.md
├── batch.py
├── prompts.sample.jsonl
└── requirements.txt
```

## License

MIT. Do whatever you want.
