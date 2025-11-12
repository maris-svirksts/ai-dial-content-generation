# Quick Start Guide

## Setup

```bash
cd <root directory> && \
source .venv/bin/activate && \
pip install -r requirements-dev.txt && \
export PYTHONPATH=<root directory>
```

## Run Tasks

```bash
# Task 1: OpenAI-style image analysis (base64 encoding)
python task/image_to_text/openai/task_openai_itt.py

# Task 2: DIAL-style image analysis (bucket storage)
python task/image_to_text/task_dial_itt.py

# Task 3: Text-to-image generation
python task/text_to_image/task_tti.py
```

## Environment Variables

The `.env` file must contain your DIAL API key:

```properties
DIAL_API_KEY=your-api-key-here
```

This is automatically loaded by `task/_utils/constants.py`.

## Troubleshooting

| Issue | Solution |
|-------|----------|
| `ModuleNotFoundError: No module named 'task'` | Set `PYTHONPATH` environment variable |
| `ModuleNotFoundError: No module named 'dotenv'` | Install `requirements-dev.txt` instead of `requirements.txt` |
| Empty API key error | Ensure `.env` file has valid `DIAL_API_KEY` |
| VPN connection error | Activate EPAM VPN before running tasks |
