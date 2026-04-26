# 🐳 Docker   

<p align="center">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" width="170px">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Docker-Containerization-2496ED?logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/DevOps-Automation-orange" />
  <img src="https://img.shields.io/badge/Docker--Compose-Multi--Container-1abc9c?logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/License-MIT-yellow" />
</p>

A complete hands-on guide to mastering Docker — from fundamentals to real-world multi-container workflows.  
Designed for developers and DevOps engineers building production-ready containerized applications.

---

## 🚀 Features

- ✅ Docker fundamentals (images, containers, volumes, networks)  
- ✅ Writing and optimizing Dockerfiles  
- ✅ Multi-container setup using Docker Compose  
- ✅ Real-world development workflows  
- ✅ Clean, structured, and beginner-friendly repository  



---

## ⚙️ Installation & Setup

### 🐧 Install Docker (Linux - Ubuntu)

```bash
# Update packages
sudo apt update

# Install Docker
sudo apt install docker.io -y

# Start and enable Docker
sudo systemctl start docker
sudo systemctl enable docker
```

### ✅ Verify Installation

```bash
docker --version
docker run hello-world
```

---

## 🐳 Docker Commands

```bash
# Run a container
docker run nginx

# List running containers
docker ps

# List all images
docker images

# Build image from Dockerfile
docker build -t myapp .

# Stop a container
docker stop <container_id>

# Remove a container
docker rm <container_id>
```

---

## 🧱 Dockerfile Example

```dockerfile
# Use official Python image
FROM python:3.10-slim

# Set working directory
WORKDIR /app

# Copy project files into container
COPY . .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Expose application port
EXPOSE 5000

# Command to run the application
CMD ["python", "app.py"]
```


```bash
docker-compose up --build
```

---

## 🔄 Workflow (How Docker Works)

```
1️⃣ Write Code
        ↓
2️⃣ Create Dockerfile
        ↓
3️⃣ Build Docker Image
        ↓
4️⃣ Run Container from Image
        ↓
5️⃣ Deploy Anywhere
```

📦 Code → 🏗 Image → 🐳 Container

---

## 📌 Use Cases

- 🚀 Development environments  
- 🌍 Application deployment  
- 🧩 Microservices architecture  
- ⚙️ CI/CD pipelines  
- ☁️ Cloud-native applications  

---

## 👨‍💻 Author

Krishna Prajapat    
GitHub: https://github.com/krishnaa-21  

---

⭐ If this repository helped you learn Docker, consider giving it a star!