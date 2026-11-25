# Platform Demo API

![CI](https://github.com/Ali-Asadollahi2001/platform-demo-api/actions/workflows/ci.yml/badge.svg)

A minimal REST API built with FastAPI, containerized with Docker, and tested automatically with GitHub Actions.

## Features

- `GET /health` health check endpoint for monitoring
- `GET /hello/{name}` simple example endpoint
- Automated tests with pytest
- CI pipeline: install dependencies, run tests, build Docker image on every push

## Tech stack

Python, FastAPI, Uvicorn, Docker, pytest, GitHub Actions

## Run locally

```bash
python -m venv .venv
.venv\Scripts\activate      # Linux/macOS: source .venv/bin/activate
pip install -r requirements.txt
uvicorn main:app --reload
```

Interactive API docs: http://127.0.0.1:8000/docs

## Run with Docker

```bash
docker build -t platform-demo-api .
docker run -p 8000:8000 platform-demo-api
```

## Run tests

```bash
pytest
```

## CI

The workflow in `.github/workflows/ci.yml` runs on every push and pull request. It installs dependencies, runs the tests, and verifies that the Docker image builds.