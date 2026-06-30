# Cloud Intern Assignment

## Candidate
Akshat Shukla

## Objective
Deploy a Python Flask application using Docker.

## Repository
Forked from:
https://github.com/docker/awesome-compose

## Commands Used

git clone https://github.com/AKSHAT853/awesome-compose.git

cd awesome-compose/flask/app

docker build -t flask-app .

docker run -d -p 8000:8000 --name flask-container flask-app

docker ps

## Dockerfile

FROM python:3.11-slim

WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 8000

CMD ["python", "app.py"]

## Verification

Application URL:
http://localhost:8000

Output:
Hello World!

## Problems Faced

1. Docker Desktop was not running.
   Solution: Started Docker Desktop and verified it using docker run hello-world.

2. The original repository contained an advanced Dockerfile.
   Solution: Replaced it with a simplified Dockerfile suitable for deployment.

## Result

Successfully containerized the Flask application, built the Docker image, ran the container, and verified the application in the browser.