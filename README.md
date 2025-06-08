Homelab Stack

Docker-Compose collection that runs a small self-hosted stack over Tailscale with TLS termination handled by Traefik.

| Service           | Purpose                             | URL (default)              |
|-------------------|-------------------------------------|----------------------------|
| Tailscale         | Tailnet connectivity                | —                          |
| Traefik           | Reverse-proxy & ACME (dns-01 via Cloudflare) | https://traefik.${DOMAIN} |
| Portainer         | Docker management UI                | https://portainer.${DOMAIN} |
| PostgreSQL 16     | Shared database                     | —                          |
| Speedtest-Tracker | Scheduled bandwidth tests           | https://speed.${DOMAIN}    |
| Gitea             | Lightweight Git server              | https://git.${DOMAIN}      |
| Actual-Budget     | Personal finance app                | https://actual.${DOMAIN}   |
| Duplicati         | Encrypted backups to OneDrive       | https://bkp.${DOMAIN}      |
| Pi-hole           | Network-wide ad-blocking DNS        | https://pihole.${DOMAIN}   |
| Glance            | Self-hosted dashboard               | https://glance.${DOMAIN}   |
| Uptime-Kuma       | Service uptime monitoring           | https://uptime.${DOMAIN}   |
| Watchtower        | Automatic image updates             | —                          |
| The Lounge         | Web IRC client                      | https://irc.${DOMAIN}     |
| Netdata            | System metrics & monitoring         | https://netdata.${DOMAIN} |
| Unbound            | Recursive DNS resolver              | -                         |
| Grafana            | Metrics visualization               | https://grafana.${DOMAIN} |
| Prometheus         | Metrics collection                  | https://prometheus.${DOMAIN}    |

⸻

Prerequisites

- Docker Engine + Compose plugin (or Docker Desktop)
- Domain managed in Cloudflare (DNS API token with Zone - DNS:Edit)
- Tailscale account & auth key (TS_AUTHKEY)
- Server (Raspberry Pi) running a native Linux filesystem (ext4 / xfs / btrfs)

⸻

License

MIT — see LICENSE file.

⸻

Author

Yegor Stepanov · @ystepanoff
