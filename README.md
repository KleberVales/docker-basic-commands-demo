# Demo: Docker Basic Commands

This repository contains a simple demo to practice **basic Docker commands**.  
It is part of the topic *Microservices & Containerization*.

---

## 🚀 What is Docker?

Docker is a platform that allows developers to build, run, and manage applications inside containers.  
Containers are lightweight, portable, and faster compared to virtual machines.

---

## 📌 Docker Basic Commands

### 1. Run a Container

```bash
docker run hello-world
```

### 2. List Containers

```bash
docker ps         # shows running containers
docker ps -a      # shows all containers (including stopped ones)
```

### 3. Start / Stop Containers

```bash

docker start <container_id>
docker stop <container_id>

```

### 4. Build an Image

Inside the demo/ folder:

```bash
docker build -t myapp:1.0 .

```

### 5. Run the Image as a Container

```bash
docker run -d -p 8080:80 myapp:1.0
```

### 6. Remove Containers and Images

```bash
docker rm <container_id>
docker rmi <image_id>
```

## 📂 Demo Dockerfile

The demo/Dockerfile creates a simple container with Nginx:

```bash
# Use official Nginx image
FROM nginx:latest

# Copy custom HTML file to container
COPY index.html /usr/share/nginx/html/index.html
```

Create an index.html in the demo/ folder:

```bash
<!DOCTYPE html>
<html>
  <head>
    <title>Docker Demo</title>
  </head>
  <body>
    <h1>Hello from Docker Container 🚀</h1>
  </body>
</html>
```

## 🏃 How to Run

1. Clone this repo:
```bash
git clone https://github.com/<your-username>/docker-basic-commands-demo.git
```

2. Navigate into the demo folder:

```bash
cd docker-basic-commands-demo/demo
```

3. Build and run the container:

```bash
docker build -t myapp:1.0 .
docker run -d -p 8080:80 myapp:1.0
```

