# 🐳 Docker CLI Tutorial – Explained with Flags and Syntax

This guide introduces the most essential Docker commands used in day-to-day container development. Every command is broken down into components, with full flag explanations.

KaTeX-compatible LaTeX is used for any conceptual representation.

---

## 🚧 1. Build Docker Image

```bash
docker build -t myapp .
```

### 🔍 Explanation

- `docker`: CLI command
- `build`: Subcommand to build an image from a Dockerfile
- `-t myapp`: Tags the resulting image as `myapp`
- `.`: Build context — current directory must contain Dockerfile

$$
\text{docker build -t <image-name> <context-path>}
$$

---

## 🚀 2. Run Docker Container

```bash
docker run -p 5000:5000 myapp
```

### 🔍 Explanation

- `run`: Subcommand to run a container from an image
- `-p 5000:5000`: Maps host port 5000 to container port 5000
- `myapp`: Name of the image to run

$$
\text{docker run -p <host-port>:<container-port> <image-name>}
$$

---

## 📋 3. List Running Containers

```bash
docker ps
```

- Lists all active containers
- Use `docker ps -a` to show **all containers** (even stopped ones)

---

## 🛑 4. Stop a Running Container

```bash
docker stop <container_id>
```

- Gracefully stops a running container by ID or name

---

## 🗑️ 5. Remove a Container

```bash
docker rm <container_id>
```

- Removes a stopped container
- Use `-f` to force remove a running container

---

## 🧼 6. Remove an Image

```bash
docker rmi <image_name>
```

- Deletes the Docker image from local cache

---

## 🧰 7. View Docker System Usage

```bash
docker system df
```

- Shows disk usage by images, containers, volumes, and build cache

---

## 📦 8. Docker Volumes

```bash
docker volume create mydata
docker volume ls
```

- Create and list Docker-managed volumes

---

## 🔁 9. Restart a Container

```bash
docker restart <container_id>
```

- Stops and restarts a container

---

## 🕵️ 10. View Container Logs

```bash
docker logs <container_id>
```

- Displays stdout/stderr output from a container

---

## 🔍 11. Inspect a Container

```bash
docker inspect <container_id>
```

- Returns low-level system data about the container in JSON

---

## 📦 12. Copy Files Between Host and Container

```bash
docker cp myfile.txt <container_id>:/app/myfile.txt
```

- Copies `myfile.txt` from host to container directory `/app/`

---

## 🧪 13. Run an Interactive Shell in Container

```bash
docker exec -it <container_id> /bin/bash
```

- `exec`: Execute a command in a running container
- `-it`: Interactive terminal

---

## ✅ Summary

Each Docker command follows this general form:

$$
\text{docker <subcommand> [options] [arguments]}
$$

---