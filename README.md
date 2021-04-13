# Magero
Data Monitoring tool for Data Engineers

# Setup
1. Create a .env file in the config folder named `timescaledb.env` with the following environment variable
```
POSTGRES_PASSWORD=<password of your timescale postgres database>
```

2. Create a .env file in the config folder named `promscale.env` with the following environment variables
```
PROMSCALE_LEADER_ELECTION_PG_ADVISORY_LOCK_ID=1
PROMSCALE_LEADER_ELECTION_PG_ADVISORY_LOCK_PROMETHEUS_TIMEOUT=30s
PROMSCALE_LOG_LEVEL=info
PROMSCALE_DB_CONNECT_RETRIES=10
PROMSCALE_WEB_TELEMETRY_PATH=/metrics-text
PROMSCALE_DB_HOST=magero-timescaledb
PROMSCALE_DB_NAME=<name of your timescale postgres database>
PROMSCALE_DB_PASSWORD=<password of your timescale postgres database>
PROMSCALE_DB_PORT=5432
PROMSCALE_DB_SSL_MODE=allow #change to `require` when in production
```

# Run
```
docker compose up --build -d
```
