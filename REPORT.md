# OS Lab 6: Multi-Container Application Deployment with Docker

**Docker Hub Username:** ziadmoh7

## Part 1: Docker Hub Images

Below are the links to the container images pushed to Docker Hub:

- **Database:** [ziadmoh7/mysql-custom](https://hub.docker.com/r/ziadmoh7/mysql-custom)
- **Backend:** [ziadmoh7/backend-app](https://hub.docker.com/r/ziadmoh7/backend-app)
- **Frontend:** [ziadmoh7/frontend-app](https://hub.docker.com/r/ziadmoh7/frontend-app)

## Part 2: Bonus (Docker Compose)

The `docker-compose.yml` file has been included in the root directory. It orchestrates the following services:
- **db:** MySQL 8.0 with a persistent volume (`mysql_vol`).
- **backend:** Node.js API connecting to the `db` service.
- **frontend:** React/Vite development server binding to the host.

### How to Run

1. Ensure the `./downloads` directory exists locally:
    ```bash
    mkdir downloads
    ```
2. Start the application stack:
    ```bash
    docker compose up -d
    ``` 
3. Access the application:
    - **Frontend:** http://localhost:5173

    - **Backend API:** http://localhost:3000

    - **CSV Export:** Files will appear in the `./downloads` folder.
4. Stop the application stack:
    ```bash
    docker compose down
    ```
    To also remove the persistent data volume, add `-v`
