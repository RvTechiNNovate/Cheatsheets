
## **Docker Compose Commands (CLI)**

### **Start/Stop/Manage Services**:
| Command                                 | Usage & Example                                                    | Description                                                     |
|-----------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------|
| **docker-compose up**                   | `docker-compose up` <br> `docker-compose up -d`                    | Starts the services defined in the `docker-compose.yml`. <br> `-d` runs in detached mode. |
| **docker-compose down**                 | `docker-compose down`                                              | Stops and removes containers, networks, and volumes.            |
| **docker-compose build**                | `docker-compose build`                                              | Builds the images defined in the `docker-compose.yml`.          |
| **docker-compose stop**                 | `docker-compose stop`                                              | Stops running containers without removing them.                 |
| **docker-compose restart**              | `docker-compose restart`                                           | Restarts all services.                                          |
| **docker-compose logs**                 | `docker-compose logs`                                              | Shows logs from all running services.                           |
| **docker-compose logs -f**              | `docker-compose logs -f`                                           | Follows live log output (like `tail -f`).                       |
| **docker-compose exec**                 | `docker-compose exec <service> <command>` <br> `docker-compose exec web bash` | Runs a command inside a running container (like SSH into a container). |
| **docker-compose ps**                   | `docker-compose ps`                                                | Lists all running containers/services managed by Compose.        |
| **docker-compose rm**                   | `docker-compose rm`                                                | Removes stopped containers.                                     |

### **Volumes and Networks**:
| Command                                 | Usage & Example                                                    | Description                                                     |
|-----------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------|
| **docker-compose up -d --build**        | `docker-compose up -d --build`                                     | Rebuilds images before starting containers.                     |
| **docker-compose run**                  | `docker-compose run <service> <command>`                           | Runs a one-time command in a new container.                     |
| **docker-compose config**               | `docker-compose config`                                            | Validates and displays the Docker Compose file configuration.   |
| **docker-compose down -v**              | `docker-compose down -v`                                           | Removes the containers and associated volumes.                  |
| **docker-compose down --rmi all**       | `docker-compose down --rmi all`                                    | Stops containers and removes images as well.                    |

---

### **Docker Compose Networking**:
| Command                                  | Usage & Example                                                    | Description                                                     |
|------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------|
| **networks**                             | `networks:`                                                        | Defines custom networks in Docker Compose.                      |
| **external networks**                    | `external: true`                                                   | Use existing external Docker networks.                          |
| **docker network ls**                    | `docker network ls`                                                | Lists all Docker networks.                                      |
| **docker network create**                | `docker network create <name>`                                     | Creates a new Docker network.                                   |

---

### **Example Full Flow**:

1. **Build and Start Services**:
   ```bash
   docker-compose up --build
   ```

2. **Check Running Services**:
   ```bash
   docker-compose ps
   ```

3. **View Logs**:
   ```bash
   docker-compose logs
   ```

4. **Execute a Command in a Running Container**:
   ```bash
   docker-compose exec web bash
   ```

5. **Stop and Remove All Services**

:
   ```bash
   docker-compose down
   ```
