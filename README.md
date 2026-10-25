<h1 align="center">Hi, I'm Josef 👋</h1>
<p align="center">
  CS student at <b>Masaryk University</b> (FI, Brno)<br>
  I like infrastructure that runs itself: automated, monitored and locked down.
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/TODO"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:jcrhonek@proton.me"><img src="https://img.shields.io/badge/Email-333?style=flat&logo=maildotru&logoColor=white" alt="Email"></a>
  <img src="https://img.shields.io/badge/open%20to%20internship%20(from%20Feb%202027)-2ea44f?style=flat" alt="Open to internship">
</p>

---

### 🏠 Homelab: my main project

One Proxmox server, everything defined as code. Rebuilding it from scratch is a single Ansible run.

```mermaid
flowchart LR
  user((Internet)) --> cf[Cloudflare Tunnel<br/>zero open ports]
  cf --> edge[NGINX edge]
  edge --> sso[Authentik SSO<br/>OIDC + forward auth]
  edge --> apps[Apps in LXC / VMs]
  apps --> mon[Prometheus · Grafana<br/>Alertmanager → ntfy]
  agent[AI agent VM] --> fw[OpenWrt firewall<br/>egress allowlist + DNS sinkhole]
```

- **8 LXC containers / VMs**, provisioned by **21 custom Ansible roles** (Vault for secrets, idempotent reruns)
- **No open ports**: Cloudflare Tunnel → NGINX, every service behind central SSO
- **Monitoring and alerting** with Prometheus, Grafana, Alertmanager and Uptime Kuma, plus nightly backups
- **Sandboxed AI coding agent** in an isolated VM with SNI-based egress allowlist and DNS sinkhole
- Scale-to-zero apps and defense in depth (per-host firewalls, unprivileged containers, Docker socket proxy)

### 🚀 Other projects

| Project | What it is |
|---|---|
| **[health-coach](https://github.com/diamond447/health-coach)** | Self-hosted MCP servers that let an AI assistant coach me from my own health and training data. Runs daily in the homelab behind Authentik. |
| **[mapy-gpx-exporter](https://github.com/diamond447/mapy-gpx-exporter)** | Python library + CLI for exporting GPX from Mapy.com, [published on PyPI](https://pypi.org/project/mapy-gpx-exporter/). Reverse-engineered the export flow from browser devtools. |
| **[BikeMapy](https://github.com/diamond447/BikeMapy)** | Map of cycling routes shared on BikeForum.cz. An experiment in spec-driven development: I write specs and review PRs, AI agents write the code. |

> 🤖 **About AI:** I build my app projects with AI coding agents. I design the system, write the spec,
> review every change and own the infrastructure it runs on. The homelab is my own hands-on work.
> 🧩 **Without AI:** I learned to code by solving algorithmic problems by hand in
> [KSI](https://ksi.fi.muni.cz/profil/5468), the Correspondence Seminar in Informatics at Masaryk University,
> which I completed as a successful graduate in the 2024/2025 year.

### 🛠️ Tools I actually use

![Proxmox](https://img.shields.io/badge/Proxmox-E57000?style=flat&logo=proxmox&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-EE0000?style=flat&logo=ansible&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![NGINX](https://img.shields.io/badge/NGINX-009639?style=flat&logo=nginx&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat&logo=cloudflare&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat&logo=grafana&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat&logo=gnubash&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat&logo=githubactions&logoColor=white)

### 🌱 Right now

- 2nd year of Bc. *Programming and Application Development* at FI MUNI
- 4th year of using Manjaro btw 
- Other hobbies: fitness, cycling, martial arts, bouldering 🚴
