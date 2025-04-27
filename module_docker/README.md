# 🐳 Docker: Introduction and Architecture

## 📘 What is Docker?

Docker is a containerization platform that allows developers to package applications and their dependencies into isolated environments called **containers**. These containers are portable, lightweight, and consistent across environments, making them ideal for DevOps and microservice architectures.

---

## 🏗️ Docker Architecture

Docker follows a client-server architecture:

- **Docker Client**: Sends commands to the Docker daemon (`docker` CLI).
- **Docker Daemon**: Runs on the host machine and manages containers.
- **Docker Images**: Read-only templates used to create containers.
- **Docker Registries**: Repositories to store and share images (e.g., Docker Hub).
- **Docker Containers**: Running instances of images.

```
[ CLI ] ---> [ Docker Daemon ] ---> [ Images | Containers | Volumes | Networks ]
```

---

## 🔄 Lifecycle of a Docker Container

1. Write a `Dockerfile`
2. Build an image: `docker build`
3. Run a container: `docker run`
4. Manage container state: `docker ps`, `docker stop`, etc.

---

## 🧰 Why Use Docker?

- **Portability**: Runs anywhere with Docker Engine
- **Isolation**: Containers are sandboxed
- **Consistency**: Eliminates “it works on my machine”
- **Efficiency**: Uses fewer resources than VMs

---

## 📌 Real-World Use Cases

- CI/CD Pipelines
- Microservices & APIs
- Application Sandboxing
- Data Science Environments

---

## 📚 Further Reading

- [Docker Docs](https://docs.docker.com/)
- [DockerHub](https://hub.docker.com/)