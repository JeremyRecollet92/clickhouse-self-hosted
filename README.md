# ClickHouse Self-Hosted with Docker

This repository provides a `docker compose` setup for running a self-hosted [ClickHouse](https://clickhouse.com/) server.

It is pre-configured to join a shared Docker network, which simplifies connecting to other services like [n8n](https://github.com/AiratTop/n8n-self-hosted).

## Features

-   Uses the official ClickHouse server Docker image.
-   Persists data in a local volume.
-   Configured for a shared network for easy integration.
-   Includes scripts for easy management.
-   Telemetry is disabled by default.
-   Pre-configured to query data directly from MySQL and PostgreSQL sources.

## Getting Started

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/AiratTop/clickhouse-self-hosted.git
    cd clickhouse-self-hosted
    ```

2.  **Create the shared network:**
    If it doesn't exist yet, create the shared Docker network:
    ```bash
    docker network create shared_network
    ```

3.  **Configure environment variables:**
    Update a `.env` file and specify your database credentials.


4.  **Start the service:**
    ```bash
    docker compose up -d
    ```

## Usage

-   **Start:** `docker compose up -d`
-   **Restart:** `./restart-docker.sh`
-   **Update:** `./update-docker.sh` (Pulls the latest image and restarts)

## Connecting with n8n

This setup is designed to work with the [n8n-self-hosted](https://github.com/AiratTop/n8n-self-hosted) configuration. Since both services are on the `shared_network`, you can connect to ClickHouse from n8n using `clickhouse` as the host. 

- Use port `8123` for the native ClickHouse HTTP interface.
- Use port `9004` for the MySQL compatible endpoint.
- Use port `9005` for the PostgreSQL compatible endpoint.

## See Also

Check out other self-hosted solutions:

-   [postgresql-self-hosted](https://github.com/AiratTop/postgresql-self-hosted)
-   [mysql-self-hosted](https://github.com/AiratTop/mysql-self-hosted)
-   [qdrant-self-hosted](https://github.com/AiratTop/qdrant-self-hosted)
-   [n8n-self-hosted](https://github.com/AiratTop/n8n-self-hosted)
-   [caddy-self-hosted](https://github.com/AiratTop/caddy-self-hosted)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Author

**Airat Halitov**

- Website: [airat.top](https://airat.top)
- GitHub: [@AiratTop](https://github.com/AiratTop)
- Repository: [clickhouse-self-hosted](https://github.com/AiratTop/clickhouse-self-hosted)