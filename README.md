## 🧱 Containerization Systems
#### by Aditya Saxena

### 📘 Project Title: Multi-Platform Containerization Explorer

### 📝 Project Description
This project investigates, implements, and compares leading containerization platforms: Docker, Podman, and Containerd. Through structured modules, tutorials, and real-world examples, learners gain hands-on experience deploying and managing containers using different architectures and commands. The project includes theory, implementation, and a comparative evaluation to help developers, engineers, and DevOps professionals choose the best tool for their needs.

---

## 🧠 50 Short Answer Theory Questions with Answers

1. **What is a container?**
   A lightweight, portable unit for software that includes everything needed to run it.
2. **What is the main difference between VMs and containers?**
   VMs virtualize hardware; containers virtualize the OS.
3. **What is Docker?**
   A platform to develop, ship, and run applications in containers.
4. **What is Podman?**
   A daemonless container engine that is compatible with Docker CLI.
5. **What is Containerd?**
   A container runtime used as a core component in Docker and Kubernetes.
6. **What is the OCI?**
   Open Container Initiative: a standard for container formats and runtimes.
7. **What command builds a Docker image?**
   `docker build -t name .`
8. **What does `docker run` do?**
   It starts a container from an image.
9. **What is rootless containerization?**
   Running containers without root privileges.
10. **Which platform supports rootless containers by design?**
   Podman.
11. **Can Docker run rootless?**
   Yes, with configuration.
12. **What is a container image?**
   A static specification of a container, including code and dependencies.
13. **What is Docker Compose?**
   A tool for defining and running multi-container Docker applications.
14. **Does Podman support Compose?**
   Yes, via `podman-compose`.
15. **What is the purpose of `containerd`?**
   A low-level container runtime for Kubernetes.
16. **Which platform is tightly integrated with Kubernetes?**
   Containerd.
17. **What is LXC?**
   A low-level container technology closer to virtual machines.
18. **What is LXD?**
   A system container manager built on LXC.
19. **What is Nerdctl?**
   A Docker-compatible CLI for Containerd.
20. **What is a volume in Docker?**
   A persistent storage mechanism for containers.
21. **How do containers communicate?**
   Through networks and bridges.
22. **Is Podman a daemon-based service?**
   No.
23. **Can Docker and Podman coexist?**
   Yes, but care must be taken with networking and images.
24. **What is a Dockerfile?**
   A script to automate building container images.
25. **Can Podman use Dockerfiles?**
   Yes.
26. **What is a container runtime?**
   Software that runs containers according to OCI specifications.
27. **What is the difference between build and run in Docker?**
   Build creates an image; run executes it as a container.
28. **How do you list running containers in Docker?**
   `docker ps`
29. **How to remove all stopped containers?**
   `docker container prune`
30. **Is Containerd a CLI tool?**
   No, it's a runtime; CLI tools like `ctr` or `nerdctl` are used.
31. **What is a container namespace?**
   An isolated execution environment.
32. **Which platform supports pods natively?**
   Podman.
33. **What are cgroups?**
   Control groups for resource allocation.
34. **Does Docker use cgroups?**
   Yes.
35. **Is Podman more secure than Docker?**
   Yes, due to rootless architecture.
36. **What is a sandbox container?**
   A container used to enforce isolation policies.
37. **Can containers be used for CI/CD?**
   Absolutely.
38. **What is Docker Hub?**
   A cloud-based registry for container images.
39. **What is Podman’s image registry?**
   It uses the same registries as Docker by default.
40. **How are logs handled in containers?**
   Through logging drivers or output redirection.
41. **What is a multi-stage build?**
   Building images in multiple steps for efficiency.
42. **Do Podman and Docker share images?**
   Yes, if configured to use the same storage.
43. **What are containers good for?**
   Microservices, CI/CD, reproducibility, testing.
44. **Are containers faster than VMs?**
   Yes, they are lightweight and start faster.
45. **Is container networking customizable?**
   Yes.
46. **Can containers be run on Windows?**
   Yes, with Docker Desktop.
47. **What are bind mounts?**
   Mounting host paths into a container.
48. **What is `ctr` in Containerd?**
   A low-level CLI for Containerd.
49. **What is CRI?**
   Container Runtime Interface used by Kubernetes.
50. **Why study multiple platforms?**
   To choose the best-fit tool for your system and workload.

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
