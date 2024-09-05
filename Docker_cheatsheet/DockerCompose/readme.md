
## **Docker Compose Cheat Sheet**

A **Docker Compose file** is used to define and run multi-container applications.

### **Basic `docker-compose.yml` Structure:**
```yaml
version: '3'
services:
  <service_name>:
    image: <image>:<tag>
    build: <path_to_dockerfile>
    ports:
      - "<host_port>:<container_port>"
    environment:
      - <key>=<value>
    volumes:
      - <host_dir>:<container_dir>
    depends_on:
      - <another_service>
    networks:
      - <network_name>

volumes:
  <volume_name>:

networks:
  <network_name>:
```

### Common `docker-compose.yml` Commands:
| Command         | Usage & Example                                                         | Description                                                |
|-----------------|-------------------------------------------------------------------------|------------------------------------------------------------|
| **version**     | `version: '3'`                                                          | Defines the Docker Compose version.                        |
| **services**    | `services:`                                                             | Lists all the services (containers) to run.                |
| **build**       | `build: .`                                                              | Builds an image from a Dockerfile in the specified context. |
| **image**       | `image: redis:alpine`                                                   | Specifies an image from Docker Hub or a local image.       |
| **ports**       | `ports: ["5000:5000"]`                                                  | Maps container ports to host ports.                        |
| **volumes**     | `volumes: ["./data:/app/data"]`                                         | Mounts host directories or volumes inside the container.   |
| **environment** | `environment: <key>=<value>` <br> `environment: - NODE_ENV=production`  | Sets environment variables for the container.              |
| **depends_on**  | `depends_on: ["redis"]`                                                 | Specifies dependencies (starts the dependent service first). |
| **networks**    | `networks: - my_network`                                                | Defines custom networks for communication between services. |
| **volumes**     | `volumes: - redis_data`                                                 | Defines shared data volumes for persistence across containers. |
| **command**     | `command: ["python", "app.py"]`                                         | Overrides the default container start command.             |
| **restart**     | `restart: always`                                                       | Automatically restarts the container if it fails.          |
| **env_file**    | `env_file: .env`                                                        | Loads environment variables from a file.                   |
| **healthcheck** | `healthcheck:` <br> `test: ["CMD", "curl", "-f", "http://localhost"]`    | Defines health checks for the service.                     |

### Docker Compose Example:
```yaml
version: '3'
services:
  web:
    build: .
    ports:
      - "5000:5000"
    volumes:
      - .:/app
    environment:
      - FLASK_ENV=development
    depends_on:
      - redis
  redis:
    image: "redis:alpine"
    ports:
      - "6379:6379"

volumes:
  redis_data:

networks:
  my_network:
```

---
