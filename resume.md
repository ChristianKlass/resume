# Mark Christian Klass

**Software Engineer | DevOps | AI/ML Infrastructure**

- 📞 +65 9226 8757
- 📧 [klass.mark.christian@gmail.com](mailto:klass.mark.christian@gmail.com)
- 🐙 [github.com/ChristianKlass](https://github.com/ChristianKlass)
- 💼 [linkedin.com/in/mark-klass-681262ba](https://www.linkedin.com/in/mark-klass-681262ba)
- 📍 Based in Singapore. Willing to travel.
- 📄 [Download PDF](https://resume.markklass.dev/resume_mark_klass.pdf)

DevOps and Platform Engineer with 8+ years of experience in infrastructure automation, containerization, and cloud operations. Increasingly focused on AI/ML infrastructure and intelligent automation — building self-optimizing pipelines that integrate AI APIs, automated content generation, and data-driven feedback loops. Combines deep Linux systems expertise with a practical, ship-it approach to solving operational problems at scale.

## Work Experience

### Software Engineer — WizVision Pte Ltd _(Nov 2021 – Present)_

- Hardened security across 11 production and UAT systems by performing RHEL9 upgrades and vulnerability patching, resolving VMS scan findings and mitigating critical risks.
- Diagnosed and resolved AWS infrastructure issues including EC2 connectivity failures and CloudWatch log forwarding malfunctions, restoring stable cloud operations.
- Automated 50+ batch processes using JobScheduler, cutting manual intervention by 40% and freeing the team for higher-value work.
- Identified and resolved performance bottlenecks through JMeter load testing, improving application response times by 20%.
- Resolved 100+ production issues across the stack, directly improving system uptime and reliability.
- Created the team's first formal documentation for RHEL9 patching, upgrades, and repository configuration, enabling clean handover to Day 2 operations.

**EKS Platform Hardening**

- Rebuilt EKS worker node images as CIS Level 1 hardened AL2023 AMIs across two UAT clusters, bringing container hosts onto the same hardening baseline already applied to the RHEL fleet.
- Designed the security agent delivery model for endpoint protection, vulnerability scanning, and log forwarding, choosing host-baked or DaemonSet deployment per agent based on which needed host OS visibility.
- Built a deferred-activation pattern so agents ship inside the AMI but register at first boot via Secrets Manager and IRSA, clearing agent identity state pre-bake to prevent GUID collisions across autoscaled nodes.
- Built an offline RPM transfer pipeline (repotrack, archive, jumphost transfer) to bake packages in an environment with no direct repository access.

### DevOps Engineer — Z Turing _(Aug 2021 – Oct 2021)_

- Cut node provisioning time by 50% by containerizing setup and configuration workflows with Docker for Bitcoin, Filecoin, Ethereum, and TRON.
- Designed and deployed a monitoring solution with automated alerting via Telegram, Discord, and WhatsApp, reducing mean time to resolution by 25%.
- Evaluated infrastructure requirements for high-compute workloads, ensuring technical feasibility and performance targets were met.

### DevOps Engineer — ST Engineering: Mission Software & Services _(Jan 2021 – Aug 2021)_

- Streamlined deployment workflows by implementing Docker Compose automation, reducing deployment friction and configuration drift.
- Introduced Kubernetes for container orchestration, enabling horizontal scaling and improving fault tolerance for production services.
- Integrated observability and auth tooling: Prometheus, Grafana, Loki, Vector, KrakenD, and Keycloak.

### Software Engineer — ST Engineering Electronics _(Apr 2019 – Dec 2020)_

- Built and demonstrated a real-time monitoring and alerting solution using Prometheus, Grafana, and VictoriaMetrics, enabling proactive system health management.
- Pioneered containerization of the monitoring stack with Docker and Kubernetes (Istio, KrakenD, Keycloak), improving deployment portability across client environments.

### Identity Specialist — Azimuth Labs _(Apr 2018 – Jan 2019)_

- Managed CA Identity Management and Governance for a major client, handling 20–30 tickets per day independently while maintaining identity governance compliance.
- Built API and back-end services for authentication and authorization using OAuth2 and OIDC.
- Automated user provisioning and identity lifecycle management, reducing administrative overhead.

## Projects

### Homelab Infrastructure _(Personal Project)_

- Run a production-grade homelab: a two-node Kubernetes cluster on Proxmox VMs, fully GitOps-managed — Flux reconciles 17 namespaces from a self-hosted GitLab, with image automation rolling out new container builds.
- Manage guest infrastructure as code with Terraform (bpg/proxmox provider) covering 13 of 14 VM/LXC definitions; Ansible handles monitoring agents and watchdogs.
- Keep all secrets encrypted at rest with SOPS + age, decrypted in-cluster by sops-secrets-operator.
- Operate a four-tier GitLab backup chain ending age-encrypted in Cloudflare R2, plus CloudNativePG PostgreSQL clusters with continuous barman backups to R2.
- Run Frigate NVR with Coral USB EdgeTPU passthrough (~7.5 ms inference) and Intel iGPU Quick Sync decode over mergerfs union storage.
- Expose services with zero inbound ports: Cloudflare Tunnels fronted by Authentik SSO.

### AI Video Pipeline _(Personal Project)_

- Built and operated a fully automated content pipeline: Reddit story discovery → AI script generation (Claude) → voice synthesis (Fish Speech) → captioning (Whisper) → video assembly (ffmpeg) → YouTube/TikTok upload, which ran 3x daily.
- Built a self-optimization loop that pulled YouTube Analytics data, used AI to analyze trends, rewrote underperforming titles, removed dead content, and produced weekly strategy reports — closing the feedback loop between performance metrics and content selection.

### pvewatch _([Open Source — GitHub](https://github.com/ChristianKlass/pvewatch))_

- Built pvewatch, an open-source Proxmox backup and VM monitoring tool, shipped through its own GitLab CI pipeline with linting, tests, and SonarQube quality gates.

### The Kopi Log _(Personal Project)_

- Built an unattended tech-news pipeline that ingests RSS feeds, clusters related stories with TF-IDF, and synthesizes original analysis articles with an LLM — published as a static Astro site by a Kubernetes CronJob three times weekly.
- Engineered for zero metered API spend — subscription LLM credentials via a local proxy, free Pexels image API with graceful degradation — with idempotent runs and a half-hourly freshness probe.

### NRIC Generator/Validator _([Open Source — GitHub](https://github.com/ChristianKlass/nric-generator-validator))_

- Built a utility to generate and validate Singaporean NRIC numbers based on the official checksum algorithm, used for creating realistic test data in UAT environments.

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
