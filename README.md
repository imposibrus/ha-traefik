Create `traefik` network:
```bash
docker network create traefik --driver=bridge
```

Use this network in other docker-compose files:
```yaml
# ...
network:
  traefik:
    external: true

services:
  app:
    # ...
    networks:
      - traefik
      - default
```

