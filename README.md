# Demo CI/CD App

A simple Node.js app with CI/CD using GitHub Actions and Docker.

## Run locally

```bash
cd app
npm install
npm start
```

Visit: http://localhost:3000

## Run tests

```bash
npm test --prefix app
```

## Docker

```bash
docker build -t demo-app:local .
docker run -p 3000:3000 demo-app:local
```

## Docker Compose

```bash
docker-compose up --build
```

## GitHub Actions

- On push to `main`, workflow will:
  - Run tests
  - Build Docker image
  - Push to Docker Hub (requires repo secrets)
