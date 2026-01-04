# webmap-stack

Docker-based stack for serving a web mapping application with a proxy and OpenResty overlay.

## Overview

This repository holds a lightweight stack composed with `compose.yaml` and supporting configuration in `proxy/` and `resty-overlay/`.

## Repository layout

- `compose.yaml` - docker compose definition for the services.
- `proxy/` - proxy configuration (virtual host and additive snippets).
- `resty-overlay/` - OpenResty overlay Dockerfile for custom Lua/Nginx logic.

## Quick start

1. Copy the environment example:

```bash
cp .env.example .env
```

2. Start the stack (builds images if needed):

```bash
docker compose up -d --build
```

3. Follow logs:

```bash
docker compose logs -f
```

## Development

- To rebuild the `resty-overlay` image manually:

```bash
docker build -t resty-overlay resty-overlay/
```

- Proxy configuration files are in `proxy/`. Adjust `virtualhost.conf` and `additive.main` as necessary.

## Notes

- This README contains a minimal usage guide. If you'd like, I can expand sections (examples, environment variable descriptions, or contribution notes).
