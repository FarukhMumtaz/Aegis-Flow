🛡️ Aegis Flow

**High-Performance Security Gateway & Containerized Backend Infrastructure**

[![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)](https://nodejs.org/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![Express.js](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)](https://expressjs.com/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/FarukhMumtaz)

---

🚀 The Problem & The Solution

Many developers build functional APIs that collapse under load or suffer from major security gaps. Aegis Flow is a high-performance Security-First API Gateway and Backend System. Built for production, it isolates critical infrastructure to ensure data integrity, prevent unauthorized access, and handle high concurrency.

🏗️ Architectural Excellence
1. Zero-Drift Deployment (IaC)

Forget manual configurations. The entire system is orchestrated via Docker Compose. A single command spins up a containerized environment that is immutable and consistent from development to production.

2. High-Performance Resilience

Integrated Database Connection Pooling (pg-pool) allows the gateway to handle massive request spikes without crashing, ensuring reliable service availability.

3. Persistent Data Layer

Strategically implemented Docker Volumes keep the PostgreSQL data independent of the container lifecycle. Containers can be destroyed or updated without losing database state.

🔒 Security-First Logic
1. Custom Auth Middleware

Acting as the primary gatekeeper, a custom authentication layer validates every request before it even reaches the core business logic.

2. Zero-Exposure Secrets

No credentials are hardcoded. Sensistive data like API_KEY and database credentials are obfuscated and injected via environment variables (.env).

🛠️ Tech Stack & Directory Structure

Runtime: Node.js (Express Framework)

Database: PostgreSQL (Production Optimized)

DevOps: Docker & Docker Compose (Container Orchestration)

    Bash

    aegis-flow/
    ├── src/                        # Gateway Source Code
    │   ├── middleware/             # Security & Auth Logic
    │   ├── routes/                 # Express API Endpoints
    │   ├── db.js                   # Connection Pooling Logic
    │   └── app.js                  # Application Entry Point
    ├── docker-compose.yml          # Infrastructure Orchestration (IaC)
    ├── Dockerfile                  # Node.js Container Definition
    ├── .env.example                # Secrets Template
    └── README.md                   # System Documentation

⚡ Quick Start (Deploy in < 2 mins)
1. Configuration

Create a .env file in the root directory by copying the template:
    Bash

    DATABASE_USER=your_secure_user
    DATABASE_PASSWORD=your_secure_password
    DATABASE_NAME=aegis_db
    DATABASE_HOST=db
    DATABASE_PORT=5432
    API_KEY=your_secret_access_key

2. Build & Launch

Run the entire infrastructure in detached mode:
    Bash

    docker compose up --build -d

Note: The first run initializes a Docker Volume for database persistence.

👨‍💻 Developed By

Farukh Mumtaz

Aspiring DevSecOps Engineer.
