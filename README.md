Homelab Stack

Docker-Compose collection that runs a small self-hosted stack over Tailscale with TLS termination handled by Traefik.

| Service           | Purpose                                                  | URL (default)          |
|-------------------|----------------------------------------------------------|------------------------|
| Tailscale         | Tailnet connectivity                                     | —                      |
| Traefik           | Reverse-proxy & ACME (dns-01 via Cloudflare)             | https://traefik.<DOMAIN> |
| PostgreSQL 16     | Shared database                                          | —                      |
| Speedtest-Tracker | Scheduled bandwidth tests                                | https://speed.<DOMAIN> |
| Gitea             | Lightweight Git server                                   | https://git.<DOMAIN>   |
| Actual-Budget     | Personal finance app                                     | https://actual.<DOMAIN> |
| Watchtower        | Automatic image updates                                  | —                      |

⸻

Prerequisites
	1.	Docker Engine + Compose plugin (or Docker Desktop)¹
	2.	Domain managed in Cloudflare (DNS API token with Zone - DNS:Edit)
	3.	Tailscale account & auth key (TS_AUTHKEY)
	4.	Server (Raspberry Pi) running a native Linux filesystem (ext4 / xfs / btrfs)

⸻

License

MIT — see LICENSE file.

⸻

Author

Yegor Stepanov · @ystepanoff
