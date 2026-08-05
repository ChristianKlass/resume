# Mark Christian Klass

**Software Engineer | DevOps | AI/ML Infrastructure**

- 📞 +65 9226 8757
- 📧 [klass.mark.christian@gmail.com](mailto:klass.mark.christian@gmail.com)
- 🐙 [github.com/ChristianKlass](https://github.com/ChristianKlass)
- 💼 [linkedin.com/in/mark-klass-681262ba](https://www.linkedin.com/in/mark-klass-681262ba)
- 📍 Based in Singapore. Willing to travel.
- 📄 [Download PDF](https://resume.markklass.dev/resume_mark_klass.pdf)

DevOps and platform engineer, 8+ years, mostly on Linux, AWS, and Kubernetes. Most of the work is making operations run without a human, whether that's patching, provisioning, deployments, or monitoring. Recent projects use LLMs for content pipelines that run unattended.

## Work Experience

### Software Engineer — WizVision Pte Ltd _(Nov 2021 – Present)_

- RHEL9 upgrades and vulnerability patching across 11 production and UAT systems, clearing VMS scan findings.
- Debugged and fixed AWS issues like EC2 connectivity failures and broken CloudWatch log forwarding.
- Automated 50+ batch processes with JobScheduler, cutting manual intervention by 40%.
- JMeter load testing found the bottlenecks; fixing them improved application response times by 20%.
- Resolved 100+ production issues.
- Wrote the team's first formal documentation for RHEL9 patching, upgrades, and repository configuration.

**EKS Platform Hardening**

- Worker nodes lagged the RHEL fleet's hardening baseline. Rebuilt their images as CIS Level 1 hardened AL2023 AMIs across two UAT clusters.
- Each security agent, whether endpoint protection, vulnerability scanning, or log forwarding, went host-baked or DaemonSet depending on whether it needed host OS visibility.
- Agents ship inside the AMI but activate at first boot, registering through Secrets Manager and IRSA. Identity state is cleared pre-bake so autoscaled nodes don't collide on GUIDs.
- The build environment had no direct repository access, so packages came in through an offline RPM pipeline using repotrack, archives, and a jumphost.

### DevOps Engineer — Z Turing _(Aug 2021 – Oct 2021)_

- Node provisioning for Bitcoin, Filecoin, Ethereum, and TRON was manual; containerizing it with Docker cut setup time by 50%.
- Monitoring and alerting went to Telegram, Discord, and WhatsApp, and mean time to resolution dropped 25%.
- Sized infrastructure for high-compute workloads.

### DevOps Engineer — ST Engineering: Mission Software & Services _(Jan 2021 – Aug 2021)_

- Moved deployments onto Docker Compose to curb configuration drift.
- Introduced Kubernetes for orchestration and horizontal scaling.
- Integrated Prometheus, Grafana, Loki, Vector, KrakenD, and Keycloak for observability and auth.

### Software Engineer — ST Engineering Electronics _(Apr 2019 – Dec 2020)_

- Stood up real-time monitoring on Prometheus, Grafana, and VictoriaMetrics as a working demo.
- Containerized the monitoring stack (Docker, Kubernetes, Istio, KrakenD, Keycloak) so it could move between client environments.

### Identity Specialist — Azimuth Labs _(Apr 2018 – Jan 2019)_

- Ran CA Identity Management and Governance for a major client and independently handled 20–30 tickets a day.
- API and back-end services for authentication and authorization, on OAuth2 and OIDC.
- Automated user provisioning and identity lifecycle management.

## Projects

### Homelab Infrastructure _(Personal Project)_

- A two-node Kubernetes cluster on Proxmox VMs, managed entirely through GitOps. Flux reconciles 17 namespaces from a self-hosted GitLab and image automation rolls out new container builds.
- Terraform on the bpg/proxmox provider defines 13 of the 14 VMs and LXCs, and Ansible handles monitoring agents and watchdogs.
- Secrets are SOPS + age encrypted at rest, decrypted in-cluster by sops-secrets-operator.
- GitLab backups run through a four-tier chain, ending age-encrypted in Cloudflare R2. CloudNativePG PostgreSQL clusters take continuous barman backups to R2 as well.
- Frigate NVR detects on a Coral USB EdgeTPU at around 7.5 ms per inference, decodes on Intel Quick Sync, and records to mergerfs union storage.
- No inbound ports are open. External access goes through Cloudflare Tunnels with Authentik SSO in front.

### Absurd Vault _(Personal Project)_

- A fully automated content pipeline that ran three times a day. It found stories on Reddit, wrote scripts with Claude, synthesized voice-over with Fish Speech, captioned with Whisper, assembled video with ffmpeg, and uploaded to YouTube and TikTok.
- A second loop pulled YouTube Analytics and analyzed trends with Claude, with a local Gemma model handling the daily pulses. It rewrote underperforming titles, removed dead content, and produced weekly strategy reports.

### pvewatch _([Open Source — GitHub](https://github.com/ChristianKlass/pvewatch))_

- An open-source Proxmox backup and VM monitor. It ships through its own GitLab CI pipeline with lint, tests, and SonarQube quality gates.

### The Kopi Log _(Personal Project)_

- An unattended tech-news pipeline that ingests RSS feeds, clusters related stories with TF-IDF, has an LLM write the analysis articles, and publishes them as a static Astro site three times a week from a Kubernetes CronJob.
- It costs nothing in metered API fees, running on subscription LLM credentials through a local proxy and free images from Pexels. Runs are idempotent, and a half-hourly probe checks that the site hasn't gone stale.

### NRIC Generator/Validator _([Open Source — GitHub](https://github.com/ChristianKlass/nric-generator-validator))_

- Generates and validates Singaporean NRIC numbers with the official checksum algorithm, written for realistic UAT test data.

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
