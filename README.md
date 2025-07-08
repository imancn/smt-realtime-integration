# Real-Time Data Sync Pipeline: PostgreSQL → Flink → StarRocks

This project provides a containerized real-time data synchronization pipeline using PostgreSQL, Apache Flink, and StarRocks.

## Architecture
```
+-------------+       +-------------+       +------------+
| PostgreSQL  |  -->  |   Flink     |  -->  | StarRocks  |
+-------------+       +-------------+       +------------+
     Source            Stream Engine        Destination Lake
```

## Components

- **PostgreSQL**: Source database
- **Apache Flink**: Stream processing engine
- **StarRocks**: Real-time analytical database (data lake)
- **SMT (StarRocks Sync Tool)**: Flink job that syncs data from PostgreSQL to StarRocks

## Setup Instructions

```bash
# Start entire pipeline
docker compose up -d
```

## Directory Structure
- `postgres/`: Contains init SQL for PostgreSQL
- `starrocks/`: Configuration and metadata for StarRocks
- `flink/`: Flink JobManager and TaskManager
- `smt/`: SMT job files (Flink job, configs)
