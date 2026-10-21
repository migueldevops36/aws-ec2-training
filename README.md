# AWS EC2 DevOps Monitoring Project

## Overview

This project runs a monitoring stack on an AWS EC2 Ubuntu server using Docker Compose.

The goal is to practice Linux administration, containerization, monitoring, Git, GitHub, and Continuous Integration (CI).

## Architecture

The project includes four services:

| Service | Purpose | Port |
|---|---|---|
| Grafana | Monitoring dashboards and visualization | 3000 |
| Prometheus | Metrics collection and storage | 9090 |
| Node Exporter | Linux server metrics | 9100 |
| Nginx | Web server | 80 |

## Technologies

- AWS EC2
- Ubuntu Linux
- Docker
- Docker Compose
- Prometheus
- Grafana
- Node Exporter
- Nginx
- Git and GitHub
- GitHub Actions

## Project Structure

```text
firstproject/
├── .github/
│   └── workflows/
│       └── deploy.yml
├── prometheus/
│   └── prometheus.yml
├── docker-compose.yml
└── README.md
```

## Start the Services

```bash
sudo docker compose up -d
```

## Check Service Status

```bash
sudo docker compose ps
```

## Validate Docker Compose Configuration

```bash
sudo docker compose config -q
```

## CI Pipeline

GitHub Actions automatically validates the Docker Compose configuration and checks for required project files when changes are pushed to the `main` branch.

The current workflow performs validation only. It does not automatically deploy changes to EC2.

## Learning Objectives

- Manage an Ubuntu server on AWS EC2.
- Run multiple services using Docker Compose.
- Collect server metrics with Prometheus and Node Exporter.
- Visualize monitoring data with Grafana.
- Track project changes with Git and GitHub.
- Validate project configuration using GitHub Actions.

## Current Status

- Docker Compose configuration validated.
- Four containers running with version-specific image tags.
- GitHub Actions validation workflow passing.
