# ☁️ Personal Cloud Infrastructure: Nextcloud + MariaDB Deployment

## 🚀 Project Overview
This project demonstrates the architecture and deployment of a private, full-stack **Nextcloud** instance using **Docker Compose**. Moving beyond a simple "one-click" install, this infrastructure is built with a focus on security, data persistence, and professional networking standards.

## 🏗️ The Architecture
I designed this system with a two-tier architecture to ensure reliability and security:

* **Application Layer:** A Nextcloud container running Apache and PHP, serving the user interface.
* **Database Layer (The Vault):** A MariaDB 10.6 container storing all system metadata and user records.
* **Network Isolation:** Configured a dual-network setup (Public/Private) so the database is isolated from the open internet.
* **Healthchecks:** Implemented active health monitoring to ensure the application only attempts to connect once the database is fully operational.

## 🛠️ Tech Stack & Skills
* **Docker & Docker Compose:** Container orchestration and management.
* **MariaDB:** Relational database configuration.
* **Linux/Bash:** System administration and terminal-based troubleshooting.
* **Git/GitHub:** Version control and CI/CD foundations.
* **Networking:** Bridge networks, port mapping, and network isolation.

## 📂 Project Structure
```text
.
├── docker-compose.yml   # The "Blueprint" for the entire infrastructure
├── .gitignore           # Protecting private data/volumes from version control
├── db_data/             # Persistent storage for MariaDB (Local Volume)
└── cloud_data/          # Persistent storage for Nextcloud files (Local Volume)
