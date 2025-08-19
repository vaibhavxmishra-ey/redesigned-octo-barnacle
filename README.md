# redesigned-octo-barnacle

This repository contains a simple FastAPI application that can be containerized and deployed on Kubernetes.
The API provides a root greeting and a `/health` endpoint for basic health checks.

## Development

Install dependencies and run the tests:

```bash
pip install -r requirements.txt
pytest
```

Run the application locally:

```bash
uvicorn app.main:app --reload
```

## Docker

Build the Docker image:

```bash
docker build -t my-api-image .
```

## Kubernetes

Apply the deployment and service manifests:

```bash
kubectl apply -f k8s/deployment.yaml
```

Update `k8s/deployment.yaml` with the correct image name before deploying.
