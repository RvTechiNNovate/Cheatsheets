## **Dockerfile Cheat Sheet**

A **Dockerfile** defines the steps to create a Docker image.

### Basic Dockerfile Commands:
| Command      | Usage & Example                                                       | Description                                                 |
|--------------|-----------------------------------------------------------------------|-------------------------------------------------------------|
| **FROM**     | `FROM <image>:<tag>` <br> `FROM python:3.9`                           | Specifies the base image for the container.                  |
| **WORKDIR**  | `WORKDIR /app`                                                        | Sets the working directory inside the container.             |
| **COPY**     | `COPY <src> <dest>` <br> `COPY . /app`                                | Copies files from host to container.                         |
| **ADD**      | `ADD <src> <dest>` <br> `ADD https://example.com/file /file`          | Similar to `COPY`, but also supports URLs and extracting archives. |
| **RUN**      | `RUN <command>` <br> `RUN apt-get update && apt-get install -y curl`  | Runs a command during image build (e.g., install dependencies). |
| **CMD**      | `CMD ["<executable>", "<param>"]` <br> `CMD ["python", "app.py"]`     | Specifies the default command when the container starts.     |
| **ENTRYPOINT**  | `ENTRYPOINT ["<executable>", "<param>"]` <br> `ENTRYPOINT ["python"]` | Defines a fixed command to be run, even when additional arguments are provided. |
| **EXPOSE**        | `EXPOSE <port>` <br> `EXPOSE 5000`                                    | Exposes a port in the container (does not publish it on the host). |
| **ENV**      | `ENV <key>=<value>` <br> `ENV NODE_ENV=production`                    | Sets environment variables inside the container.             |
| **ARG**      | `ARG <name>=<default_value>` <br> `ARG VERSION=1.0`                   | Defines build-time arguments that can be overridden.         |
| **VOLUME**   | `VOLUME /data`                                                        | Creates a mount point for external data (persistent storage). |
| **USER**     | `USER <username>` <br> `USER nonroot`                                 | Specifies which user to run the container as.                |

### Dockerfile Example:
```Dockerfile
# Use a base image
FROM python:3.9-slim

# Set working directory
WORKDIR /app

# Copy local files to the container
COPY . /app

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Expose port 5000
EXPOSE 5000

# Default command to run the application
CMD ["python", "app.py"]
```

---
