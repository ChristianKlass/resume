# Mark Christian Klass

**Software Engineer | DevOps | AI/ML Infrastructure**

- 📞 +65 9226 8757
- 📧 [klass.mark.christian@gmail.com](mailto:klass.mark.christian@gmail.com)
- 🐙 [github.com/ChristianKlass](https://github.com/ChristianKlass)
- 💼 [linkedin.com/in/mark-klass-681262ba](https://www.linkedin.com/in/mark-klass-681262ba)
- 📍 Based in Singapore. Willing to travel.
- 📄 [Download PDF](https://resume.markklass.dev/resume_mark_klass.pdf)

DevOps and platform engineer, 8+ years, mostly on Linux, AWS, and Kubernetes. Most of the work is making operations run without a human: patching, provisioning, deployments, monitoring. Recent projects apply LLMs to the same idea — content pipelines that run unattended.

## Work Experience

### Software Engineer — WizVision Pte Ltd _(Nov 2021 – Present)_

- RHEL9 upgrades and vulnerability patching across 11 production and UAT systems, clearing VMS scan findings.
- Debugged and fixed AWS issues: EC2 connectivity failures, CloudWatch log forwarding.
- Automated 50+ batch processes with JobScheduler, cutting manual intervention by 40%.
- JMeter load testing found the bottlenecks; fixing them improved application response times by 20%.
- Resolved 100+ production issues.
- Wrote the team's first formal documentation for RHEL9 patching, upgrades, and repository configuration.

**EKS Platform Hardening**

- Rebuilt EKS worker node images as CIS Level 1 hardened AL2023 AMIs across two UAT clusters, bringing container hosts onto the same hardening baseline already applied to the RHEL fleet.
- Designed the security agent delivery model for endpoint protection, vulnerability scanning, and log forwarding, choosing host-baked or DaemonSet deployment per agent based on which needed host OS visibility.
- Built a deferred-activation pattern so agents ship inside the AMI but register at first boot via Secrets Manager and IRSA, clearing agent identity state pre-bake to prevent GUID collisions across autoscaled nodes.
- Built an offline RPM transfer pipeline (repotrack, archive, jumphost transfer) to bake packages in an environment with no direct repository access.

### DevOps Engineer — Z Turing _(Aug 2021 – Oct 2021)_

- Node provisioning for Bitcoin, Filecoin, Ethereum, and TRON was manual; containerizing it with Docker cut setup time by 50%.
- Built monitoring with alerting into Telegram, Discord, and WhatsApp — mean time to resolution dropped 25%.
- Sized infrastructure for high-compute workloads.

### DevOps Engineer — ST Engineering: Mission Software & Services _(Jan 2021 – Aug 2021)_

- Moved deployments onto Docker Compose to curb configuration drift.
- Introduced Kubernetes for orchestration and horizontal scaling.
- Observability and auth tooling: Prometheus, Grafana, Loki, Vector, KrakenD, Keycloak.

### Software Engineer — ST Engineering Electronics _(Apr 2019 – Dec 2020)_

- Built and demoed real-time monitoring on Prometheus, Grafana, and VictoriaMetrics.
- Containerized the monitoring stack (Docker, Kubernetes, Istio, KrakenD, Keycloak) so it could move between client environments.

### Identity Specialist — Azimuth Labs _(Apr 2018 – Jan 2019)_

- Ran CA Identity Management and Governance for a major client — 20–30 tickets a day, handled independently.
- API and back-end services for authentication and authorization, on OAuth2 and OIDC.
- Automated user provisioning and identity lifecycle management.

## Projects

### Homelab Infrastructure _(Personal Project)_

- A two-node Kubernetes cluster on Proxmox VMs, fully GitOps-managed: Flux reconciles 17 namespaces from a self-hosted GitLab, and image automation rolls out new container builds.
- Terraform (bpg/proxmox) defines 13 of the 14 VMs and LXCs; Ansible handles monitoring agents and watchdogs.
- Secrets are SOPS + age encrypted at rest, decrypted in-cluster by sops-secrets-operator.
- GitLab backups run through a four-tier chain, ending age-encrypted in Cloudflare R2. CloudNativePG PostgreSQL clusters take continuous barman backups to R2 as well.
- Frigate NVR detects on a Coral USB EdgeTPU (~7.5 ms inference), decodes on Intel Quick Sync, and records to mergerfs union storage.
- No inbound ports open: external access goes through Cloudflare Tunnels with Authentik SSO in front.

### AI Video Pipeline _(Personal Project)_

- A fully automated content pipeline that ran 3x daily: Reddit story discovery → script generation (Claude) → voice synthesis (Fish Speech) → captioning (Whisper) → video assembly (ffmpeg) → YouTube/TikTok upload.
- A second loop pulled YouTube Analytics, used AI to analyze trends, rewrote underperforming titles, and removed dead content. Weekly strategy reports came out of the same loop.

### pvewatch _([Open Source — GitHub](https://github.com/ChristianKlass/pvewatch))_

- An open-source Proxmox backup and VM monitor. Ships through its own GitLab CI pipeline: lint, tests, SonarQube quality gates.

### The Kopi Log _(Personal Project)_

- An unattended tech-news pipeline: RSS ingestion, TF-IDF clustering of related stories, LLM-written analysis articles, published as a static Astro site by a Kubernetes CronJob three times a week.
- Zero metered API spend — subscription LLM credentials through a local proxy, images from the free Pexels API. Runs are idempotent, and a half-hourly probe checks that the site hasn't gone stale.

### NRIC Generator/Validator _([Open Source — GitHub](https://github.com/ChristianKlass/nric-generator-validator))_

- Generates and validates Singaporean NRIC numbers with the official checksum algorithm — written for realistic UAT test data.

## Skills

**Cloud & Infrastructure:** AWS (EC2, EKS, CloudWatch, IAM) · AMI Pipelines · Docker / Kubernetes / LXC · Proxmox VE / Linux / NFS · Ansible / CI/CD · Prometheus / Grafana / Loki

**AI & Automation:** LLM APIs (Claude, Gemini) · OpenAI Whisper · Event-driven Workflow Automation

**Security & Languages:** IAM / SSO (Authentik) · Cloudflare Tunnels · RHEL / CIS Hardening · Python / Bash / PowerShell · Git / REST APIs / OAuth2

## Education

- **BSc in Computer Science (Digital Systems Security)** — University of Wollongong – SIM _(2015 – 2018)_
- **Diploma in Interactive Media Informatics** — Temasek Polytechnic _(2009 – 2012)_
- **Higher NITEC in Information Technology (Networking)** — Institute of Technical Education _(2007 – 2009)_

## Certifications

- **Software Design Guidelines for Safety-Critical Systems** — Critical Systems Labs _(October 2019)_
- **Government Commercial Cloud – Foundation** — Government Technology Agency _(April 2022)_

## Languages

- English _(Native)_

## Interests

Cooking · Reading · Learning (about anything, really) · Home Improvement
