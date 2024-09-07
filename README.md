# MySQL and Apache as Containers

This project creates two containers using Podman: one for MySQL and another for Apache Web Server.

## Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/MySQL-Apache-Containers.git
   cd MySQL-Apache-Containers
   ```

2. Build and run the containers:
   ```bash
   docker-compose up --build
   ```

3. Access MySQL via port `3306` and Apache via `http://localhost:8080`.

## Systemd Service

To configure MySQL and Apache to start automatically as system services, copy the `.service` files to `/etc/systemd/system/`, and enable them:

```bash
sudo systemctl enable mysql-container.service
sudo systemctl enable apache-container.service
