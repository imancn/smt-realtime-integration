
# Instructions

This setup spins up a Flink CDC job to stream data from PostgreSQL to StarRocks using Debezium and StarRocks connectors.

## Requirements

- Docker
- Docker Compose

## How to Run

```bash
docker compose down -v --remove-orphans
docker compose build --no-cache
docker compose up --force-recreate
```

Once running, Flink should ingest data from PostgreSQL via CDC and stream it to StarRocks.
