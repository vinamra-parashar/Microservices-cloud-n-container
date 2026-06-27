# Microservices Containerization Assessment

## Project Overview

This project demonstrates the containerization of a Node.js-based microservices application using Docker and Docker Compose.

The application consists of four microservices:

* **User Service** (Port 3000)
* **Product Service** (Port 3001)
* **Order Service** (Port 3002)
* **Gateway Service** (Port 3003)

The Gateway Service acts as the entry point and communicates with the other services over a shared Docker bridge network.

---

## Technologies Used

* Node.js
* Express.js
* Docker
* Docker Compose

---

## Project Structure

```text
Microservices-cloud-n-container/
├── docker-compose.yml
├── README.md
└── Microservices/
    ├── gateway-service/
    │   ├── app.js
    │   ├── package.json
    │   ├── Dockerfile
    │   └── .dockerignore
    ├── order-service/
    │   ├── app.js
    │   ├── package.json
    │   ├── Dockerfile
    │   └── .dockerignore
    ├── product-service/
    │   ├── app.js
    │   ├── package.json
    │   ├── Dockerfile
    │   └── .dockerignore
    └── user-service/
        ├── app.js
        ├── package.json
        ├── Dockerfile
        └── .dockerignore
```

---

## Prerequisites

Ensure the following are installed:

* Docker Desktop
* Docker Compose

Verify installation:

```bash
docker --version
docker compose version
```

---

## Setup Instructions

### 1. Clone the Repository

```bash
git clone <YOUR_FORKED_REPOSITORY_URL>
cd Microservices-cloud-n-container
```

### 2. Build Docker Images

```bash
docker compose build
```

### 3. Start All Services

```bash
docker compose up
```

Or run in detached mode:

```bash
docker compose up -d
```

### 4. Verify Running Containers

```bash
docker compose ps
```

---

## API Endpoints

### User Service

```
GET http://localhost:3000/users
```

### Product Service

```
GET http://localhost:3001/products
```

### Order Service

```
GET http://localhost:3002/orders
```

### Gateway Service

Health Check

```
GET http://localhost:3003/health
```

Users

```
GET http://localhost:3003/api/users
```

Products

```
GET http://localhost:3003/api/products
```

Orders

```
GET http://localhost:3003/api/orders
```

Create Order

```
POST http://localhost:3003/api/orders
```

---

## Docker Network

All services communicate through a shared Docker bridge network defined in `docker-compose.yml`.

Service-to-service communication uses Docker service names:

* user-service
* product-service
* order-service

This enables the Gateway Service to communicate internally without using localhost.

---

## Useful Docker Commands

Build images

```bash
docker compose build
```

Start containers

```bash
docker compose up
```

Run in background

```bash
docker compose up -d
```

View running containers

```bash
docker compose ps
```

View logs

```bash
docker compose logs
```

Stop containers

```bash
docker compose down
```

---

## Troubleshooting

### Port Already in Use

If a port is already occupied, stop the conflicting process or modify the port mapping in `docker-compose.yml`.

### Container Fails to Start

Check logs:

```bash
docker compose logs
```

### Rebuild Images

```bash
docker compose down
docker compose build --no-cache
docker compose up
```

---

## Screenshots

Include the following screenshots:

* Docker Desktop showing all four containers running
* Output of `docker compose ps`
* Successful API responses from browser or Postman
* Terminal showing `docker compose up`

---

## GitHub Repository

Repository Link:

```
https://github.com/<your-username>/Microservices-cloud-n-container
```

---

## Author

**Vinamra Parashar**

Microservices Containerization Assessment
