## 👋 Welcome to budibase 🚀

Low-code platform for building internal apps

## 📋 Description

Low-code platform for building internal apps

## 🚀 Services

- **proxy**: budibase.docker.scarf.sh/budibase/proxy:latest
- **app**: budibase.docker.scarf.sh/budibase/apps:latest
- **worker**: budibase.docker.scarf.sh/budibase/worker:latest
- **couchdb**: budibase/couchdb:latest
- **minio**: minio/minio:latest

### Infrastructure Components

- **redis**: Redis database


## 📦 Installation

### Option 1: Quick Install
```bash
curl -q -LSsf "https://raw.githubusercontent.com/composemgr/budibase/main/docker-compose.yaml" -o compose.yml
```

### Option 2: Git Clone
```bash
git clone "https://github.com/composemgr/budibase" ~/.local/srv/docker/budibase
cd ~/.local/srv/docker/budibase
docker compose up -d
```

### Option 3: Using composemgr
```bash
composemgr install budibase
```

## 🔧 Configuration

### Environment Variables

```shell
TZ=America/New_York
```

See `docker-compose.yaml` for complete list of configurable options.

## 🌐 Access

- **Web Interface**: http://172.17.0.1:59061

## 📂 Volumes

- `./volumes/data/db/couchdb/budibase` - Data storage
- `./volumes/data/db/redis/budibase` - Data storage
- `./volumes/data/minio` - Data storage

## 🔐 Security

- Change all default passwords before deploying to production
- Use strong secrets for all authentication tokens
- Configure HTTPS using a reverse proxy (nginx, traefik, caddy)
- Regularly update Docker images for security patches
- Backup your data regularly

## 🔍 Logging

```shell
docker compose logs -f proxy
```

## 🛠️ Management

```bash
# Start services
docker compose up -d

# Stop services
docker compose down

# Update to latest images
docker compose pull && docker compose up -d

# View logs
docker compose logs -f

# Restart services
docker compose restart
```

## 📋 Requirements

- Docker Engine 20.10+
- Docker Compose V2+

## 🤝 Author

🤖 casjay: [Github](https://github.com/casjay) 🤖  
🦄 composemgr: [Github](https://github.com/composemgr) 🦄
