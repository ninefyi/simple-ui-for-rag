# Use the official Python image as a base
FROM python:3.12-slim

# Set the working directory in the container
WORKDIR /app

# Install any required packages
# For a simple chat UI with streamlit, we need a few things
# First, install some system dependencies
RUN apt-get update && apt-get install -y --no-install-recommends \
    build-essential \
    git \
    && rm -rf /var/lib/apt/lists/*

COPY requirements.txt .

# Install Python dependencies
RUN pip install --no-cache-dir -r requirements.txt