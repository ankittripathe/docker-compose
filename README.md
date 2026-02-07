# Docker Compose
- A tool used to run multi-container applications using a single file called docker-compose.yml.

- Instead of running multiple docker run commands manually, you can define all services in one YAML file and start them together with one command.


```bash
# Key Commands
- 1️⃣ Start All Services
- docker compose -f fileName.yaml up -d
🔍 Explanation:
up → Create + Start all containers
-d → Run in Detached mode (background)
-f → Specify compose file
fileName.yaml → Example: mongodb.yaml, app.yaml
```

```bash
2️⃣ Stop & Remove All Services
docker compose -f fileName.yaml down
🔍 Explanation:

down → Stops and removes containers, networks, images (if created by compose)

⚡ Shortcuts (When File Name Is Default)
```

If your file is named docker-compose.yaml, you can run:

docker compose up -d
docker compose down
🗂️ Docker Compose File Example
version: '3.8'

services:
mongodb:
image: mongo
container_name: my-mongo
ports: - "27017:27017"
volumes: - mongo-data:/data/db

volumes:
mongo-data:
🧠 Remember

✔ Compose = Multi-container manager
✔ up = build + create + start
✔ down = stop + remove
✔ -d = background mode
✔ -f = use specific YAML file
