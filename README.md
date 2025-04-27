## 🧱 Containerization Systems
#### by Aditya Saxena

### 📘 Project Title: Multi-Platform Containerization Explorer

### 📝 Project Description
This project investigates, implements, and compares leading containerization platforms: Docker, Podman, and Containerd. Through structured modules, tutorials, and real-world examples, learners gain hands-on experience deploying and managing containers using different architectures and commands. The project includes theory, implementation, and a comparative evaluation to help developers, engineers, and DevOps professionals choose the best tool for their needs.

---

# 🧠 50 Short Answer Theory Questions on Containerization

---

### 1. What is a container?  
A container is a lightweight, standalone, executable package of software that includes everything needed to run it: code, runtime, system tools, libraries, and settings.

### 2. What is the main difference between VMs and containers?  
VMs virtualize hardware using a hypervisor, whereas containers virtualize the operating system kernel, making them more lightweight and faster.

### 3. What is Docker?  
Docker is a platform that enables developers to build, ship, and run containerized applications with consistency across environments.

### 4. What is Podman?  
Podman is a daemonless container engine compatible with Docker CLI, offering rootless containerization by default.

### 5. What is Containerd?  
Containerd is a high-performance container runtime used by Docker and Kubernetes to manage container lifecycle operations.

### 6. What is the OCI?  
The Open Container Initiative (OCI) defines industry standards for container image formats and runtimes.

### 7. What command builds a Docker image?  
`docker build -t image_name .`

### 8. What does `docker run` do?  
It starts a container instance from a previously built image.

### 9. What is rootless containerization?  
Running containers without root (admin) privileges, increasing security by limiting system-level access.

### 10. Which platform supports rootless containers by design?  
Podman.

### 11. Can Docker run rootless?  
Yes, but it requires additional configuration and is not enabled by default.

### 12. What is a container image?  
A container image is an immutable snapshot of a container's filesystem and metadata.

### 13. What is Docker Compose?  
A tool to define and manage multi-container applications using a `docker-compose.yml` file.

### 14. Does Podman support Compose?  
Yes, through a companion tool called `podman-compose`.

### 15. What is the purpose of Containerd?  
It serves as a core container runtime that manages the container lifecycle for Kubernetes and other systems.

### 16. Which platform is tightly integrated with Kubernetes?  
Containerd.

### 17. What is LXC?  
Linux Containers (LXC) is a low-level container technology offering lightweight virtualization similar to VMs.

### 18. What is LXD?  
LXD is a system container manager built on top of LXC to manage container environments more efficiently.

### 19. What is Nerdctl?  
A Docker-compatible CLI frontend for Containerd, supporting Docker-like workflows.

### 20. What is a volume in Docker?  
A volume is persistent storage mounted inside a container, used to store data outside the container lifecycle.

---

### 21. How do containers communicate?  
Through Docker networks, using virtual bridges, IP addressing, and port mapping.

### 22. Is Podman a daemon-based service?  
No, Podman is daemonless and uses fork/exec instead of a background service.

### 23. Can Docker and Podman coexist?  
Yes, but they manage separate container and image stores unless configured otherwise.

### 24. What is a Dockerfile?  
A script containing instructions to assemble a container image layer-by-layer.

### 25. Can Podman use Dockerfiles?  
Yes, Podman fully supports Dockerfile syntax.

### 26. What is a container runtime?  
A low-level engine that runs containers based on OCI specifications, e.g., Containerd or runc.

### 27. What is the difference between `build` and `run` in Docker?  
`build` creates a container image; `run` creates a live container from that image.

### 28. How do you list running containers in Docker?  
`docker ps`

### 29. How to remove all stopped containers?  
`docker container prune`

### 30. Is Containerd a CLI tool?  
No, it's a runtime. It is accessed using tools like `ctr` or `nerdctl`.

---

### 31. What is a container namespace?  
An OS-level feature that isolates system resources like process IDs, hostnames, and filesystems per container.

### 32. Which platform supports pods natively?  
Podman. It can group containers into pods similar to Kubernetes.

### 33. What are cgroups?  
Control groups used to limit, account for, and isolate resource usage (CPU, memory) of processes.

### 34. Does Docker use cgroups?  
Yes, Docker uses cgroups for resource control and management.

### 35. Is Podman more secure than Docker?  
Yes, mainly due to its rootless and daemonless design, reducing attack surface.

### 36. What is a sandbox container?  
A container used for isolation and security policy enforcement, often in Kubernetes.

### 37. Can containers be used for CI/CD?  
Absolutely. Containers enable reproducibility, fast builds, and isolated environments.

### 38. What is Docker Hub?  
A public container registry where users can publish and pull Docker images.

### 39. What is Podman’s image registry?  
Podman uses Docker-compatible registries by default, including Docker Hub and Quay.io.

### 40. How are logs handled in containers?  
Logs are streamed via stdout/stderr and can be collected using log drivers or log management tools.

---

### 41. What is a multi-stage build?  
A Docker build technique where multiple intermediate stages are used to produce optimized final images.

### 42. Do Podman and Docker share images?  
Not by default, but they can be configured to use the same storage backend.

### 43. What are containers good for?  
Microservices, reproducibility, testing, CI/CD, and simplifying dependency management.

### 44. Are containers faster than VMs?  
Yes, containers are lightweight and start almost instantly compared to VMs.

### 45. Is container networking customizable?  
Yes, users can define custom networks, IP ranges, and DNS settings.

### 46. Can containers be run on Windows?  
Yes, via Docker Desktop or Podman with WSL2 backend.

### 47. What are bind mounts?  
Mounting a host file or directory into a container's filesystem for real-time access.

### 48. What is `ctr` in Containerd?  
A low-level CLI to interact with Containerd directly (used mostly by advanced users).

### 49. What is CRI?  
Container Runtime Interface — an abstraction layer between Kubernetes and container runtimes.

### 50. Why study multiple platforms?  
To select the best tool for your use case, optimize security/performance, and increase platform flexibility.

---

## 🌍 Overview of Major Platforms

### 🔹 Docker
Docker is the most widely adopted containerization platform that simplifies the process of building, sharing, and running containers. It includes a daemon, CLI, and tools like Docker Compose. Its vast community and ecosystem make it ideal for beginners and enterprise adoption alike.

### 🔹 Podman
Podman is a daemonless container engine developed by RedHat. It allows rootless container management, making it more secure than Docker. Podman can run Dockerfiles and supports pods natively, similar to Kubernetes. It’s well-suited for security-focused environments.

### 🔹 Containerd
Containerd is a high-performance container runtime used by Kubernetes. It does not include a CLI by default but is used through tools like `ctr` or `nerdctl`. Its modular, low-level architecture makes it perfect for production orchestration at scale.

---

## 📊 Comparison Table

| Feature                 | Docker     | Podman     | Containerd |
|------------------------|------------|------------|------------|
| Daemonless             | ❌         | ✅         | ✅         |
| Rootless Support       | Partial    | Full       | Full       |
| Dockerfile Support     | ✅         | ✅         | ✅ (via Nerdctl) |
| Kubernetes Integration | ✅         | ✅         | ✅ (native) |
| CLI Availability       | ✅         | ✅         | ⚠️ `ctr`, `nerdctl` |
| Compose Support        | ✅         | ✅         | ❌         |
| Production Scale       | ✅         | ✅         | ✅         |
| Security               | Medium     | High       | High       |

---

## 📦 Module Structure

Each module contains:
- `README.md`: Platform overview and install guide
- `tutorial/`: Step-by-step setup and use
- `examples/`: Real-world examples (Dockerfile, pod config, etc.)
- `screenshots/`: Screenshots of execution and output

---

## 🔧 Module 1: Docker
- Installation and setup on Windows/Linux
- Build and run basic containers
- Use of Docker Compose
- Image layers and caching

## 🔧 Module 2: Podman
- Rootless install on Linux
- Running Dockerfiles using Podman
- Pod creation and inspection
- Comparison with Docker CLI

## 🔧 Module 3: Containerd
- Installation and runtime setup
- Using `ctr` and `nerdctl` commands
- Pull, run, stop containers
- Kubernetes readiness demo

---

## 📌 Final Report
All findings, screenshots, comparative notes, and performance observations are documented in `FINAL_REPORT.md`.# Containerization_Platforms
