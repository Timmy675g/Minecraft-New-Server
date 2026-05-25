# Infrastructure Documentation

This document contains the infrastructure overview and operational setup for the SurvivalKendy Minecraft server.

---

# Server Architecture

Current infrastructure is based around a Dockerized Fabric Minecraft server deployment hosted on a VPS environment.

Main components:
- Minecraft Fabric Server
- Docker Containerization
- Cloudflare Proxying
- NGINX Reverse Proxy
- Geyser + Floodgate Bedrock Support
- Automated Backups
- Monitoring and Profiling Systems

Funfact : This server moved to another provider when 1 Free Trial ends 
Server 1 - 2 : GCP ( Google Cloud Platform )
Server 3 : DO ( DigitalOcean )
The Server is planning to move to a Paid VPS Provider. 
Looking for a viable options right now :>.
---

# Current Stack

## Core Server
- Minecraft Fabric `26.1.2` ( 1.21.11 Before the New Server )
- Fabric Loader `0.19.2`
- Java 25

## Infrastructure
- Docker
- Docker Compose
- Linux VPS ( Debian 12 )
- NGINX
- Cloudflare

## Monitoring
- Spark Profiler
- Uptime Monitoring
- Status Page ( View it in : status.survivalkendy.systems )

## Crossplay
- Geyser
- Floodgate

---

# Directory Structure

```txt
/srv/minecraft
├── compose.yaml
├── mods/
├── config/
├── world/
├── logs/
├── backups/
```

---

# Docker

The Minecraft server runs inside a Docker container.

Main container:
```txt
minecraft-docker-new
```

Useful commands:

## Restart Server
```bash
docker restart minecraft-docker-new
```

## Server Console via RCON
```bash
docker exec -it minecraft-docker-new rcon-cli list
```

## TPS Check
```bash
docker exec -it minecraft-docker-new rcon-cli spark tps
```

## Spark Profiling
```bash
docker exec -it minecraft-docker-new rcon-cli spark profiler start
docker exec -it minecraft-docker-new rcon-cli spark profiler stop
```

---

# Networking

Cloudflare is used for:
- DNS management
- SSL/TLS handling
- Reverse proxying for website infrastructure

NGINX handles:
- Reverse proxying
- API routing
- SSL integration
- Website forwarding

---

# Backup System

Automated backups run every 6 hours.

Backups include:
- World data
- Configurations
- Docker related server files

Important:
- Always verify backups before major migrations or mod changes.
- Maintain off server backup copies whenever possible.

---

# Bedrock Support

Bedrock support is handled using:
- Geyser
- Floodgate

Important:
- Preserve `key.pem`
- Do not change Floodgate username prefix without migration planning.

---

# Operational Notes

## Daily Maintenance
- Monitor TPS
- Review logs
- Check backup completion
- Monitor Bedrock compatibility issues

## Recommended Practices
- Avoid live mod changes while players are online
- Always create backups before infrastructure changes
- Test mod compatibility carefully after updates
- Keep documentation updated after major incidents

---

# Future Goals

- VPS migration preparation
- Better Bedrock compatibility
- Infrastructure automation improvements
- Improved monitoring systems
- Cleaner logging and diagnostics