```markdown
# 🐳 Docker 

<p align="center">
  <img src="https://www.docker.com/wp-content/uploads/2022/03/vertical-logo-monochromatic.png" alt="Docker Logo" width="160px"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker%20Compose-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/DevOps-FF6C37?style=for-the-badge&logo=azuredevops&logoColor=white"/>
  <img src="https://img.shields.io/badge/License-MIT-brightgreen?style=for-the-badge"/>
</p>

---

<p align="center">
  A structured, hands-on repository to master <strong>Docker</strong> from fundamentals to real-world container workflows. 🚀<br/>
  Covers images, containers, volumes, networks, Dockerfile, and Docker Compose — all in one place.
</p>

---

## 🚀 Features

- 🐳 **Docker Fundamentals** — images, containers, volumes, and networks explained clearly
- 📄 **Dockerfile Mastery** — write optimized, production-ready Dockerfiles
- 🔗 **Docker Compose** — multi-service orchestration made simple
- 🌍 **Real-World Workflows** — container lifecycle from dev to deployment
- 🧩 **Modular Structure** — clean, topic-wise folder organization
- 🎓 **Beginner to Advanced** — structured for all learning levels

---

## ⚙️ Installation & Setup

**1. Install Docker on Linux**
```bash
sudo apt-get update
sudo apt-get install -y ca-certificates curl gnupg
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
```

**2. Add user to Docker group (no sudo required)**
```bash
sudo usermod -aG docker $USER
newgrp docker
```

**3. Verify Docker Installation**
```bash
docker --version
docker info
```

**4. Install Docker Compose**
```bash
sudo apt-get install -y docker-compose-plugin
docker compose version
```

> ✅ Docker is ready to use!

---

## 🐳 Docker Commands

### 📦 Container Management

```bash
# Run a container
docker run -d -p 8080:80 --name my-container nginx

# List running containers
docker ps

# List all containers (including stopped)
docker ps -a

# Stop a container
docker stop my-container

# Remove a container
docker rm my-container

# Run interactively
docker run -it ubuntu bash
```

### 🖼️ Image Management

```bash
# List all images
docker images

# Pull an image
docker pull python:3.11-slim

# Build an image from Dockerfile
docker build -t my-app:v1 .

# Remove an image
docker rmi my-app:v1

# Tag an image
docker tag my-app:v1 yourusername/my-app:latest
```

### 📋 Logs & Inspect

```bash
# View container logs
docker logs my-container

# Inspect container details
docker inspect my-container

# Execute command inside running container
docker exec -it my-container bash
```

---

## 🧱 Dockerfile Example

```dockerfile
# ────────────────────────────────────────
# 🐳 Dockerfile — Flask Application
# ────────────────────────────────────────

# Step 1: Use official lightweight Python image
FROM python:3.11-slim

# Step 2: Set working directory inside container
WORKDIR /app

# Step 3: Copy dependency file first (layer caching)
COPY requirements.txt .

# Step 4: Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Step 5: Copy the rest of the application code
COPY . .

# Step 6: Expose the port the app runs on
EXPOSE 5000

# Step 7: Define environment variable
ENV FLASK_ENV=production

# Step 8: Command to run the application
CMD ["python", "app.py"]
```

**Build & Run:**
```bash
docker build -t flask-app:v1 .
docker run -d -p 5000:5000 --name flask-app flask-app:v1
```

---

## 🔗 Docker Compose Example

```yaml
# ────────────────────────────────────────
# 🔗 docker-compose.yml — App + Database
# ────────────────────────────────────────

version: "3.9"



**Run with Docker Compose:**
```bash
# Start all services
docker compose up -d

# View running services
docker compose ps

# View logs
docker compose logs -f

# Stop all services
docker compose down

# Stop and remove volumes
docker compose down -v
```

---

## 🔄 Workflow — How Docker Works

```
👨‍💻 Write Code
      │
      ▼
📄 Create Dockerfile
      │
      ▼
🔨 Build Image
   docker build -t my-app .
      │
      ▼
🖼️  Docker Image Created
   (Immutable snapshot)
      │
      ▼
🚀 Run Container
   docker run -d -p 8080:80 my-app
      │
      ▼
🌐 App Running in Isolated Container
      │
      ▼
📤 Push to Docker Hub
   docker push yourusername/my-app
      │
      ▼
☁️  Deploy Anywhere (Cloud / Server / CI-CD)
```

---

## 📌 Use Cases

| 🏷️ Use Case | 📋 Description |
|---|---|
| 🛠️ **Dev Environments** | Consistent environments across all machines — no "works on my machine" issues |
| 🚀 **Deployment** | Package and ship apps with all dependencies bundled inside containers |
| 🔧 **Microservices** | Run each service independently in its own isolated container |
| 🧪 **Testing & CI/CD** | Spin up clean environments for automated testing pipelines |
| 🗄️ **Database Isolation** | Run multiple DB versions side-by-side without conflicts |
| 📦 **Portability** | Run the same container on Linux, Mac, Windows, or any cloud provider |

---

## 👨‍💻 Author

<p align="center">
  Made with ❤️ and 🐳 by <strong>Krishna prajapat</strong>
</p>

<p align="center">
  <a href="https://github.com/yourusername">
    <img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"/>
  </a>
  <a href="https://linkedin.com/in/yourprofile">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/>
  </a>
  <a href="https://hub.docker.com/u/yourusername">
    <img src="https://img.shields.io/badge/Docker%20Hub-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>
  </a>
</p>

---

<p align="center">
  ⭐ <strong>Star this repo</strong> if it helped you learn Docker!<br/>
  🐳 Happy Containerizing!
</p>
```