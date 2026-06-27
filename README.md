# Microservices Containerization Assessment

## Project Overview

This project demonstrates the containerization of a Node.js-based microservices application using Docker and Docker Compose.

The application consists of four microservices:

* **User Service** (Port 3000)
* **Product Service** (Port 3001)
* **Order Service** (Port 3002)
* **Gateway Service** (Port 3003)

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

<img width="1326" height="87" alt="image" src="https://github.com/user-attachments/assets/a20d443f-4219-40c1-ad17-cff379bca09d" />

<img width="1207" height="462" alt="image" src="https://github.com/user-attachments/assets/b88f7d1a-201d-4cc9-a0f4-abe0cb647f4d" />

```bash
docker compose logs
```

<img width="850" height="134" alt="image" src="https://github.com/user-attachments/assets/5a0b6be9-17fb-4975-8430-6efe0866b213" />

---

## API Endpoints

### User Service

```
GET http://localhost:3000/health
```

```
GET http://localhost:3000/users
```
<img width="452" height="117" alt="image" src="https://github.com/user-attachments/assets/6a4d8c18-2ac6-43ef-ad35-13ec80fa6f52" />

### Product Service

```
GET http://localhost:3001/health
```

```
GET http://localhost:3001/products
```
<img width="1198" height="210" alt="image" src="https://github.com/user-attachments/assets/e1ef3489-9d8e-4fd4-8895-9994a169067d" />

### Order Service

```
GET http://localhost:3002/health
```

```
GET http://localhost:3002/orders
```
<img width="388" height="118" alt="image" src="https://github.com/user-attachments/assets/63fb08b5-c855-4282-ad74-72793328e84b" />

### Gateway Service

```
GET http://localhost:3003/health
```
<img width="433" height="129" alt="image" src="https://github.com/user-attachments/assets/e6d2d1ed-31f2-4530-b4f5-63c5bb35ecd2" />

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

## GitHub Repository

Repository Link:

```
https://github.com/<your-username>/Microservices-cloud-n-container
```

---

## Author

**Vinamra Parashar**

Microservices Containerization Assessment
