# Personal Media Services

This repository contains a Docker Compose setup for personal media management. It makes use of images from the excellent [linuxserver.io](https://linuxserver.io/) project, which provides well-maintained Docker images for various media services.

## Services Included

- **Plex**: Media server for streaming your personal media collection.
- **Sonarr**: TV series management and automation.
- **Radarr**: Movie management and automation.
- **Lidarr**: Music management and automation.
- **Sabnzbd**: Usenet download manager.
- **qBittorrent**: Torrent download manager.

## Requirements

- Docker and Docker Compose installed on your system.

## Environment Variables

The `.env` file contains environment variables used to configure the services. Create a `.env` file in the root directory with the following variables and modify them as needed:

```ini
# System specifics
PUID=1000 # Host Linux User ID to use for the services
PGID=1000 # Host Linux Group ID for the services
TZ="Etc/UTC" # Your timezone, e.g., "Asia/Singapore"

# Host directories
HOST_DOWNLOADS="/share/downloads"
HOST_MEDIA="/share/media"
HOST_BACKUP="/share/backup"

# Administrator credentials
ADMIN_EMAIL="admin@example.com"
ADMIN_PASSWORD="change_ME!123"
```

## Usage

1. Clone the repository:

   ```bash
   git clone https://github.com/frasermclean/personal-media-services.git
   cd personal-media-services
   ```

2. Create and populate the `.env` file.:

   ```bash
   nano .env
   ```

3. Start the services:

   ```bash
   docker compose up -d
   ```

4. Access the services via their respective ports (see compose.yml)
