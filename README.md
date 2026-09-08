# chatproxy-api

Small LLM proxy: cache, health check, latency logging

## Installation

```bash
pip install -r requirements.txt
uvicorn main:app --reload
```

## What it does

- SHA-256 keyed in-memory response cache
- Latency measured and returned per request
- POST /v1/chat with prompt/model/max_tokens
- Provider SDK plugs into one function

## Usage

```bash
curl localhost:8000/v1/chat \
  -H 'content-type: application/json' \
  -d '{"prompt": "hello", "model": "gpt-4o-mini"}'
```

## Project structure

```text
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   └── bug_report.md
│   └── workflows/
│       └── ci.yml
├── docs/
│   ├── configuration.md
│   ├── development.md
│   └── usage.md
├── examples/
│   └── quickstart.md
├── .gitignore
├── CHANGELOG.md
├── CONTRIBUTING.md
├── main.py
└── requirements.txt
```

## Development

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
```
