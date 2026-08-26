# streamlit-cicd

This README summarizes the work completed today in this repository.

## Project Overview

- Small Streamlit app with a calculator backend and CI/CD-focused artifacts.

## What I did today

- **Implemented:** core calculator logic in [calculator.py](calculator.py).
- **Built:** Streamlit UI in [app.py](app.py) to expose the calculator.
- **Added:** containerization via [Dockerfile](Dockerfile).
- **Tested:** unit tests in [test_calculator.py](test_calculator.py).
- **Dependency updates:** reviewed/updated [requirements.txt](requirements.txt).
- **Local runs:** attempted to run the app locally with Streamlit (`streamlit run app.py`). The run exited with code 137 (process killed), which often indicates the process was terminated (e.g., out-of-memory); consider checking memory usage or logs.
- **Docker:** checked running containers with `docker ps` to verify container state.
- **Version control:** pushed changes to remote with `git push origin main`.

## Files changed / created today

- [app.py](app.py)
- [calculator.py](calculator.py)
- [Dockerfile](Dockerfile)
- [test_calculator.py](test_calculator.py)
- [requirements.txt](requirements.txt)

## How to run locally

1. Install dependencies (prefer a virtual environment):

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

2. Run the Streamlit app:

```bash
streamlit run app.py
```

If Streamlit exits with code 137, try closing other memory-heavy applications or run with more available memory.

## Run tests

```bash
pytest -q
```

## Docker (build & run)

```bash
docker build -t streamlit-calc .
docker run -p 8501:8501 streamlit-calc
```


