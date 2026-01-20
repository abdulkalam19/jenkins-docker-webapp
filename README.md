🚀 Jenkins + Docker Web Application Deployment
📌 Project Overview

This project demonstrates how to automate the build and deployment of a Dockerized web application using Jenkins.
A static HTML website is containerized using Docker (NGINX) and automatically built and deployed through a Jenkins Freestyle job on Windows.

🛠️ Tools & Technologies

Jenkins (Freestyle Job)

Docker & Docker Desktop

NGINX

Git & GitHub

HTML

Windows OS

📂 Project Structure
jenkins-docker-webapp/
├── Dockerfile
├── index.html
└── README.md

⚙️ How the Project Works

Jenkins job is triggered manually.

Jenkins executes Windows batch commands.

Docker builds an image using the Dockerfile.

Docker runs a container from the image.

The application is exposed via port mapping.

Web application is accessed through the browser.

🐳 Dockerfile
FROM nginx:latest
COPY index.html /usr/share/nginx/html/index.html

▶️ Jenkins Build Commands
cd C:\Users\kalam\Documents\jenkins-docker-webapp
docker rm -f jenkins-webapp-container
docker build -t jenkins-webapp .
docker run -d -p 8085:80 --name jenkins-webapp-container jenkins-webapp

🌐 Application Access

After successful Jenkins build, open:

http://localhost:8085

✅ Output

The browser displays:

Jenkins + Docker Working Successfully!
Built and deployed by Jenkins.

📘 Learning Outcomes

Understood Docker image and container lifecycle

Learned Jenkins Freestyle job configuration

Integrated Jenkins with Docker on Windows

Gained hands-on experience in CI/CD fundamentals

Learned troubleshooting of Windows, WSL, and Docker integration issues
