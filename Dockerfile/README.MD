📌 Overview

This repository contains a Dockerfile used to build a containerized environment for running the application. Docker enables consistent development, testing, and deployment across different systems by packaging the application along with its dependencies.

🚀 What is a Dockerfile?

A Dockerfile is a script that contains a series of instructions to automatically build a Docker image. It defines:

Base image
Environment setup
Dependencies installation
Application code execution

Example Dockerfile:

# Use official Python runtime as base image
FROM python:3.10-slim

# Set working directory
WORKDIR /app

# Copy requirements file
COPY app/requirements.txt .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy application code
COPY app/ .

# Expose port
EXPOSE 5000

# Run the application
CMD ["python", "main.py"]
🔍 Breakdown
FROM → Defines base image
WORKDIR → Sets working directory inside container
COPY → Copies files into container
RUN → Installs dependencies
EXPOSE → Opens port for communication
CMD → Runs the application