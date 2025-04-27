# 🐳 Docker Module – Python Flask App

## 📘 Overview

This module demonstrates how to containerize a simple Python Flask application using Docker. It covers setup, Dockerfile creation, container execution, and key observations.

---

## ⚙️ Step 1: Setup Python Flask App

### 📁 `03_sample_app/app.py`
```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def home():
    return "Hello from Dockerized Flask App!"

if __name__ == '__main__':
    app.run(host='0.0.0.0', port=5000)
```

### 📁 `03_sample_app/requirements.txt`
```text
flask
```

---

## 📦 Step 2: Create Dockerfile

### 📁 `03_sample_app/Dockerfile`
```Dockerfile
# Use Python base image
FROM python:3.9-slim

# Set working directory
WORKDIR /app

# Copy files
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY app.py .

# Expose port
EXPOSE 5000

# Command to run app
CMD ["python", "app.py"]
```

---

## 🚀 Step 3: Build and Run

### 🔧 Build Docker Image
```bash
docker build -t flask-app ./03_sample_app
```

### ▶️ Run the Container
```bash
docker run -p 5000:5000 flask-app
```

Access the app at: [http://localhost:5000](http://localhost:5000)

---

## 📌 Key Learnings

- Docker simplifies app packaging and distribution
- Flask works well with lightweight images like `python:3.9-slim`
- Use `.dockerignore` to reduce image size (not shown here)

---