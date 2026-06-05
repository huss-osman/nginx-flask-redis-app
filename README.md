# NGINX Flask Redis App

![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?logo=flask&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?logo=redis&logoColor=white)
![NGINX](https://img.shields.io/badge/NGINX-009639?logo=nginx&logoColor=white)

<p align="center">
  <img width="1000" alt="Architecture Diagram" src="images/Architecture_Diagram.png" />
</p>

---

## Overview

This project brings together containerisation, reverse proxying, service communication, load balancing, and multi-container workflows.

The objective is to deploy a scalable Flask application using Docker, NGINX, and Redis across connected container services securely.

By completing this project, the setup simulates how modern containerised applications are orchestrated across infrastructure environments.

---

## Objective

The goal of this project was to:

- Build and containerise a Flask web application
- Use Redis as a key-value store for persistent counting
- Configure NGINX as a reverse proxy and load balancer
- Use Docker Compose to orchestrate multiple services
- Validate communication between containers
- Configure persistent storage using Docker volumes
- Manage Redis connection details using environment variables
- Practice real-world container networking and troubleshooting workflows

---

## Architecture

<p align="center">
  <img width="1000" alt="Architecture Diagram" src="images/Architecture_Diagram.png" />
</p>

> [!NOTE]
> The application is built as a multi-container environment using Docker Compose.
>
> NGINX routes incoming traffic to Flask application containers, while Redis stores and retrieves the visit count data.

> [!IMPORTANT]
> Docker Compose manages:
>
> - Flask application containers
> - Redis service
> - NGINX reverse proxy
> - Container networking
> - Service communication
> - Persistent Redis storage

---

## How It Works

1. A user visits the application through the exposed NGINX service  
2. NGINX receives the request and forwards traffic to the Flask application  
3. The Flask application handles the request and communicates with Redis  
4. Redis stores and retrieves the visit count data  
5. Docker Compose keeps the services connected through a shared container network  
