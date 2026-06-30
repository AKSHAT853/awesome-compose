Cloud Intern Assignment
Deploying a Python Flask Application Using Docker

Candidate: Akshat Shukla

1. Objective

Deploy a Python Flask application using Docker by building and running the application locally and verifying it through a web browser.

2. Repository

Original Repository:

https://github.com/docker/awesome-compose

Forked Repository:

https://github.com/AKSHAT853/awesome-compose

Application Folder:

awesome-compose/flask/app
3. Technologies Used
Python 3.11
Flask
Docker Desktop
Git
GitHub
Visual Studio Code
Windows 10
4. Commands Used
git clone https://github.com/AKSHAT853/awesome-compose.git

cd awesome-compose/flask/app

docker build -t flask-app .

docker run -d -p 8000:8000 --name flask-container flask-app

docker ps
5. Dockerfile
FROM python:3.11-slim

WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 8000

CMD ["python", "app.py"]
6. Verification

Application URL

http://localhost:8000

Expected Output

Hello World!

The application was successfully accessed through the browser after running the Docker container.

7. Problems Faced
Problem 1

Issue

Docker Desktop was not running.

Resolution

Started Docker Desktop and verified the installation using:

docker run hello-world
Problem 2

Issue

The original repository contained an advanced Dockerfile intended for development environments.

Resolution

Replaced it with a simplified Dockerfile suitable for deploying the Flask application.

8. Result

The Python Flask application was successfully containerized using Docker. The Docker image was built successfully, the container ran without errors, and the application was verified by accessing http://localhost:8000 in a web browser.

9. GitHub Repository
https://github.com/AKSHAT853/awesome-compose
