# Curriculum expanded with Ansible, Logging, and GitOps

Added three advanced lessons (0017–0019) to close the most significant gaps identified in the course review: Ansible/配置管理 (0017) completes the IaC pillar alongside Terraform, 日志系统/Loki (0018) adds the logging half of observability next to Prometheus metrics, and GitOps/ArgoCD (0019) ties CI/CD + K8s + Git into a full automated deployment pipeline. Each lesson was designed for the user's 2GB VPS constraint — Ansible via SSH to existing server, Loki over ELK for memory efficiency, and ArgoCD on k3s. Total course now 19 lessons covering the full DevOps stack from Linux CLI through GitOps.

**Evidence:** Three new HTML lesson files written, index.html updated with Stage 4 section and flow chart, glossary expanded with ~20 new terms across Ansible, 日志系统, and GitOps domains.

**Implications:** User now has coverage across all DevOps interview domains. The remaining gap is cloud platform hands-on (AWS/阿里云), which requires a cloud account and is best addressed after the existing lessons are completed.
