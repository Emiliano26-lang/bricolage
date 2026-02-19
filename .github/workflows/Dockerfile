# Base image
FROM python:3.11-slim

# Set working directory
WORKDIR /app

# Copy requirements first (better caching)
COPY requirements.txt .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy project files
COPY . .

# Expose port if running a web server
EXPOSE 8000

# Default command
CMD ["python", "main.py"]

FROM ubuntu:20.04
RUN apt-get update && apt-get install -y curl
CMD ["echo", "Hello from Docker!"]
