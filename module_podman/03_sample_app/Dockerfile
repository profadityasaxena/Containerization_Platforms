# Use an official Python image as base
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /app

# Copy dependency file and install
COPY requirements.txt .
RUN pip install -r requirements.txt

# Copy the application code
COPY app.py .

# Expose Flask port
EXPOSE 5000

# Default command
CMD ["python", "app.py"]
