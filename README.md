# **Dockerized Notes App**

## **Overview**
This project demonstrates how to containerize a **Notes App** using **Docker** and deploy it on an **AWS EC2 instance**. The application is built with **JavaScript** (frontend), **Django** (backend), and **Nginx** (reverse proxy). Docker enables easy deployment and scalability by packaging all dependencies into containers.

## **Why This Project is Important**
- **Containerization** ensures the application runs consistently across different environments.
- **Simplifies Deployment** by packaging dependencies into containers.
- **Scalability** as new instances can be easily deployed.
- **Microservices Architecture** with separate containers for frontend, backend, and Nginx.

## **What I Learned**
- Installing and managing **Docker** on AWS EC2.
- Writing a **Dockerfile** to containerize an application.
- Using **Docker Compose** to orchestrate multiple services.
- Configuring **Nginx** as a reverse proxy for handling requests.
- Deploying and running containers efficiently in a cloud environment.

## **Technologies Used**
- **Docker**: Containerization of the application.
- **Docker Compose**: Managing multi-container setup.
- **Nginx**: Used as a reverse proxy for serving the application.
- **Django**: Backend API for handling notes data.
- **JavaScript**: Frontend for the Notes App.
- **AWS EC2**: Hosting the application.

## **Setup and Deployment**

### **1. Install Docker on AWS EC2**
Run the following commands to install and set up Docker:
```sh
sudo apt-get update
sudo apt-get install docker.io
sudo systemctl status docker
```
Verify Docker installation:
```sh
docker ps
```
If permission is denied, add your user to the Docker group:
```sh
sudo usermod -aG docker $USER
newgrp docker
```

### **2. Build and Run the Docker Containers**
Clone the repository and navigate to the project folder:
```sh
git clone https://github.com/your-repo/notes-app.git
cd notes-app
```
Log in to Docker Hub:
```sh
docker login -u your-dockerhub-username
```
Build the Docker image:
```sh
docker build -t notes-app .
```
Run the container:
```sh
docker run -p 80:80 nginx:1.23.3-alpine
```
Alternatively, use Docker Compose to build and run all services:
```sh
docker-compose up --build
```

### **3. Verify Deployment**
Access the application by visiting your EC2 instance's public IP in a browser.

## **Credits**
A huge thanks to [this YouTube tutorial](https://www.youtube.com/watch?v=9bSbNNH4Nqw&t=13849s) for an excellent explanation that greatly helped in understanding and implementing this project.

