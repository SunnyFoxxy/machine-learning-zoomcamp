# Homework 5: Deploying ML Models


## Q1. uv version
`uv --version` → <твоя версия>


## Q2. Scikit-Learn version in uv.lock
**1.7.2**


## Q3. Load the model
Script: `q3_predict.py`
```bash
uv run python q3_predict.py
```
Probability of conversion: **0.533**


## Q4. Serve the model
```bash
uv run uvicorn predict:app --host 0.0.0.0 --port 9696
```
conversion_probability: **0.770**


## Q5. Base image in Dockerfile
**python:3.11.15-slim-bookworm**


## Q6. Run the container
```bash
docker build -t zoomcamp-model:2026-hw5 .
docker run --rm -p 9696:9696 zoomcamp-model:2026-hw5
python q6_test.py
```
conversion_probability: **0.770** (same as Q4)
