### Check Docker Version
```bash
docker --version
````

### Get Help

```bash
docker help
docker <command> --help
```

---

## 🔹 Image Related Commands

### Pull an Image

```bash
docker pull <image_name>
```

Example:

```bash
docker pull nginx
```

### List All Images

```bash
docker images
```

### Remove an Image

```bash
docker rmi <image_id>
```

### Force Remove Image

```bash
docker rmi -f <image_id>
```

---

## 🔹 Container Related Commands

### Run a Container (Interactive Mode)

```bash
docker run -it <image_name>
```

Example:

```bash
docker run -it ubuntu
```

### Run Container in Detached Mode (Background)

```bash
docker run -d <image_name>
```

### Run Container with Name

```bash
docker run --name <container_name> <image_name>
```

### List Running Containers

```bash
docker ps
```

### List All Containers (Running + Stopped)

```bash
docker ps -a
```

### Start a Stopped Container

```bash
docker start <container_id>
```

### Stop a Running Container

```bash
docker stop <container_id>
```

### Restart a Container

```bash
docker restart <container_id>
```

### Remove a Container

```bash
docker rm <container_id>
```

### Force Remove Running Container

```bash
docker rm -f <container_id>
```

---

## 🔹 Environment Variable (-e flag)

### Pass Environment Variable

```bash
docker run -e VAR_NAME=value <image_name>
```

Example:

```bash
docker run -e MYSQL_ROOT_PASSWORD=root mysql
```

---

## 🔹 Port Binding Commands

### Bind Container Port to Host Port

```bash
docker run -p <host_port>:<container_port> <image_name>
```

Example:

```bash
docker run -p 8080:80 nginx
```

### Run in Background with Port Binding

```bash
docker run -d -p 8080:80 nginx
```

---

## 🔹 Volume / Data Persistence (Basic)

### Bind Mount

```bash
docker run -v <host_path>:<container_path> <image_name>
```

---

## 🔹 Docker Logs & Inspect (Troubleshooting)

### View Container Logs

```bash
docker logs <container_id>
```

### Follow Logs Live

```bash
docker logs -f <container_id>
```

### Inspect Container Details

```bash
docker inspect <container_id>
```

### Check Running Processes Inside Container

```bash
docker top <container_id>
```

---

## 🔹 Execute Commands Inside Container

### Enter Running Container

```bash
docker exec -it <container_id> /bin/bash
```

or

```bash
docker exec -it <container_id> sh
```

---

## 🔹 Docker Network Commands

### List Networks

```bash
docker network ls
```

### Create a Network

```bash
docker network create <network_name>
```

### Inspect Network

```bash
docker network inspect <network_name>
```

### Connect Container to Network

```bash
docker network connect <network_name> <container_name>
```

### Disconnect Container from Network

```bash
docker network disconnect <network_name> <container_name>
```

---

## 🔹 System & Cleanup Commands (Troubleshooting)

### Show Disk Usage

```bash
docker system df
```

### Remove Unused Containers, Images, Networks

```bash
docker system prune
```

### Remove Everything (Force)

```bash
docker system prune -a
```

---

## 🔹 Common Troubleshooting Commands

### Check Docker Service Status (Linux)

```bash
systemctl status docker
```

### Start Docker Service

```bash
systemctl start docker
```

### Restart Docker Service

```bash
systemctl restart docker
```