# 🐳 Docker In One Shot

A simple Docker Compose setup to run **PostgreSQL** and **Redis** locally using containers.

---

## 📦 Services

| Service    | Image      | Port        |
|------------|------------|-------------|
| PostgreSQL | postgres   | 5432 → 5432 |
| Redis      | redis      | 6379 → 6379 |

---

## ⚙️ PostgreSQL Configuration

| Key               | Value      |
|-------------------|------------|
| POSTGRES_USER     | postgres   |
| POSTGRES_DB       | review     |
| POSTGRES_PASSWORD | password   |

---

## 🚀 Getting Started

### Prerequisites
- [Docker Desktop](https://www.docker.com/products/docker-desktop/) installed and running

### Run the Project

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/docker-project.git
cd docker-project

# Start all containers
docker compose up
```

To run in the background:
```bash
docker compose up -d
```

---

## ✅ Verify It's Running

```bash
docker ps
```

You should see both `postgres` and `redis` containers running.

---

## 🛑 Stop the Project

```bash
docker compose down
```

To stop and delete all data:
```bash
docker compose down -v
```

---

## 📁 Project Structure

```
docker-project/
├── docker-compose.yml   # Defines PostgreSQL and Redis services
└── Dockerfile           # Ubuntu-based Docker image setup
```

---

## 🔗 Connect to PostgreSQL

```bash
# Connect using psql inside the container
docker exec -it <postgres-container-id> psql -U postgres -d review
```

---

## 🔗 Connect to Redis

```bash
# Connect using redis-cli inside the container
docker exec -it <redis-container-id> redis-cli
```

---

## 📚 Useful Docker Commands

```bash
# View logs
docker compose logs

# Check running containers
docker ps

# View all containers (including stopped)
docker ps -a

# Remove all containers
docker compose down
```

---

## 🙌 Credits

Based on [Docker In One Shot](https://gist.github.com/piyushgarg-dev/ea8c5aa52de0496753b88cd938abd728) by [@piyushgarg-dev](https://github.com/piyushgarg-dev)
