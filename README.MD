# Local AI Service Setup Guide

This comprehensive guide walks you through setting up and running the Local AI service using Docker. Aimed at ensuring privacy and efficiency, this service processes AI tasks locally on your machine.

## Prerequisites

Before you start, ensure that Docker is installed on your system. If Docker is not yet installed, refer to the [official Docker installation guide](https://docs.docker.com/get-docker/).

## Installation Steps

### Step 1: Pull the Docker Image

Initiate by pulling the latest version of the Local AI service Docker image:

```bash
docker pull quay.io/go-skynet/local-ai:latest

### Step 2: Change to models directory

cd path/to/your/models

### Step 3: Run  the Docker Image
docker run -p 8080:8080 -v $PWD:/models -ti --rm quay.io/go-skynet/local-ai:latest --models-path /models --context-size 700 --threads 16

