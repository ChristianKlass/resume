# Mark Christian Klass

**Software Engineer | DevOps | AI/ML Infrastructure**

- Phone: +65 9226 8757
- Email: [klass.mark.christian@gmail.com](mailto:klass.mark.christian@gmail.com)
- GitHub: [github.com/ChristianKlass](https://github.com/ChristianKlass)
- LinkedIn: [linkedin.com/in/mark-klass-681262ba](https://www.linkedin.com/in/mark-klass-681262ba)
- Portfolio: [Portfolio](https://demo.markklass.dev)
- Location: Based in Singapore. Hybrid or remote preferred.
- PDF: [resume.markklass.dev/resume_mark_klass.pdf](https://resume.markklass.dev/resume_mark_klass.pdf)

DevOps and platform engineer, 8+ years, mostly on Linux, AWS, and Kubernetes. Most of the work is making operations run without a human, whether that's patching, provisioning, deployments, or monitoring. Recent projects use LLMs for content pipelines that run unattended.

## Work Experience

### Software Engineer | WizVision Pte Ltd _(Nov 2021 - Present)_

**EKS Platform Hardening**

- Rebuilt worker-node images as CIS Level 1 hardened AL2023 AMIs across two UAT clusters, bringing them up to the RHEL fleet's baseline.
- Each security agent, whether endpoint protection, vulnerability scanning, or log forwarding, went host-baked or DaemonSet depending on whether it needed host OS visibility; agents ship inside the AMI but activate at first boot, registering through Secrets Manager and IRSA.
- The build environment had no direct repository access, so packages came in through an offline RPM pipeline using repotrack, archives, and a jumphost.

**Incident Response & Networking**

- Traced a cluster-wide loss of kubectl logs and exec on production EKS to a security agent kernel module silently dropping inbound TCP 10250.
- Diagnosed Pod Identity Agent credential timeouts on two UAT clusters to a Private DNS change on the eks-auth VPC endpoint, working from logs alone. Proposed a Route 53 Resolver forwarding rule after testing showed the AD servers could not resolve local names.
- Migrated Lambda functions from Python 3.9 to 3.13, including a rebuilt paramiko layer for AL2023, and wrote the change instructions for the operations team.
- Wrote the Kubernetes node patching SOP, including microservice redeployment and pre-redeployment log capture.

**RHEL & AWS Operations**

- RHEL9 upgrades and vulnerability patching across 11 production and UAT systems, clearing VMS scan findings.
- Debugged and fixed AWS issues like EC2 connectivity failures and broken CloudWatch log forwarding.
- Automated 50+ batch processes with JobScheduler, cutting manual intervention by 40%.
- JMeter load testing found the bottlenecks; fixing them improved application response times by 20%.

### DevOps Engineer | Z Turing _(Aug 2021 - Oct 2021)_

- Node provisioning for Bitcoin, Filecoin, Ethereum, and TRON was manual; containerizing it with Docker cut setup time by 50%.
- Monitoring and alerting went to Telegram, Discord, and WhatsApp, and mean time to resolution dropped 25%.

### DevOps Engineer | ST Engineering: Mission Software & Services _(Jan 2021 - Aug 2021)_

- Moved deployments onto Docker Compose to curb configuration drift.
- Introduced Kubernetes for orchestration and horizontal scaling.
- Integrated Prometheus, Grafana, Loki, Vector, KrakenD, and Keycloak for observability and auth.

### Software Engineer | ST Engineering Electronics _(Apr 2019 - Dec 2020)_

- Stood up real-time monitoring on Prometheus, Grafana, and VictoriaMetrics as a working demo.

### Identity Specialist | Azimuth Labs _(Apr 2018 - Jan 2019)_

- Ran CA Identity Management and Governance for a major client and independently handled 20-30 tickets a day.
- API and back-end services for authentication and authorization, on OAuth2 and OIDC.

## Projects

### Homelab Infrastructure _(Personal Project)_

- A four-node Kubernetes cluster (two Proxmox VMs, two bare-metal workers including an RTX 3070 node for local LLM inference), managed entirely through GitOps. Flux reconciles 44 Kustomizations from self-hosted Forgejo and image automation rolls out new container builds.
- Terraform on the bpg/proxmox provider defines the Proxmox VMs and LXCs it owns, and Ansible handles monitoring agents and watchdogs.
- Secrets are SOPS + age encrypted at rest, decrypted in-cluster by sops-secrets-operator.
- Git server dumps and NAS shares go off-site nightly as encrypted restic snapshots on Google Drive, and CloudNativePG PostgreSQL clusters take daily barman backups to Cloudflare R2.
- No inbound ports are open. External access goes through Cloudflare Tunnels with Authentik SSO in front.

### Agentic Tooling & Guardrails _(Personal Project)_

- Claude Code setup with PreToolUse and PostToolUse hooks for secret blocking and output redaction, deny/allow/ask permission tiers, and SOPS + age secrets.
- Custom parallel subagent skill with exclusive scopes, JSON contracts and deterministic merge, plus an MCP server exposing Proxmox, Docker and Home Assistant APIs and a Telegram bridge to Claude Code.

### pvewatch _([Open Source - GitHub](https://github.com/ChristianKlass/pvewatch))_

- An open-source Proxmox backup and VM monitor. It ships through its own Forgejo Actions pipeline with lint, tests, and SonarQube quality gates. MIT licensed. v0.2.0 adds a heartbeat dead-man's switch.

### The Kopi Log _(Personal Project)_

- An unattended tech-news pipeline that ingests RSS feeds, clusters related stories with TF-IDF, has an LLM write the analysis articles, and publishes them as a static Astro site three times a week from a Kubernetes CronJob. 276 articles published unattended since June 18, and still running.
- It operates at zero marginal API cost and uses free images from Pexels. Runs are idempotent, and a half-hourly probe checks that the site hasn't gone stale.

## Skills

**Cloud & Infrastructure:** AWS (EC2, EKS, CloudWatch, IAM), Terraform, AMI Pipelines, Kubernetes, Docker, LXC, GitLab CI, Forgejo Actions, Flux, GitOps, Helm, Ansible, SOPS, Proxmox VE, Linux, NFS, Prometheus, Grafana, Loki

**AI & Automation:** LLM APIs (Claude, Gemini), OpenAI Whisper, Event-driven Workflow Automation, MCP, Claude Code, Ollama, local LLM serving, n8n

**Security & Languages:** IAM, SSO (Authentik), Cloudflare Tunnels, RHEL Hardening, CIS Benchmarks, Python, Bash, PowerShell, Git, REST APIs, OAuth2

## Education & Certifications

- **BSc in Computer Science (Digital Systems Security)** | University of Wollongong - SIM _(2015 - 2018)_
- **Diploma in Interactive Media Informatics** | Temasek Polytechnic _(2009 - 2012)_
- **Claude API, MCP (introduction and advanced), Agent Skills, Subagents** | Anthropic Academy
- **Government Commercial Cloud - Foundation** | Government Technology Agency _(Apr 2022)_

## Languages & Interests

**Languages:** English _(Native)_ | **Interests:** Cooking · Reading · Learning · Home Improvement
