# Curriculum expanded with Cloud Platform, DevSecOps, and Database Ops

Added three lessons (0020–0022) to close the three biggest gaps identified in the course review: Cloud Platform (0020) fills the "what do these tools actually manage" blind spot, DevSecOps (0021) adds the security dimension that's now JD-required, and Database Ops (0022) covers the most common DevOps production incidents.

## Lessons Added

### 0020: Cloud Platform (AWS Core Services)
- VPC networking model (public/private subnets, Security Groups, NACLs)
- EC2 instance lifecycle and types
- IAM (Users/Roles/Policies, Least Privilege principle)
- S3 object storage (versioning, lifecycle policies, static hosting)
- RDS managed databases (Multi-AZ, Read Replicas, PITR)
- Hands-on: AWS CLI + Terraform to create/destroy S3 + EC2
- **Why this matters:** JD "familiar with at least one cloud platform" appears in ~100% of DevOps listings. The existing 19 lessons taught tools but not the resources those tools manage.

### 0021: DevSecOps Security Fundamentals
- Four defense lines: SAST (Semgrep) → Secret Detection (gitleaks) → Image Scanning (Trivy) → K8s Policies (OPA/Gatekeeper)
- Pre-commit hooks to block secret leaks before they reach Git
- Docker security hardening: non-root USER, read-only FS, distroless images, fixed digests
- Incident response: what to do when a secret leaks (revoke first, clean history second)
- **Why this matters:** Security has shifted from nice-to-have to JD-required. Every DevOps engineer needs to know gitleaks + Trivy at minimum.

### 0022: Database Operations
- Migration management (golang-migrate, up/down files, CI/CD integration)
- Backup & recovery (pg_dump, WAL archiving, PITR, RPO vs RTO)
- Connection pooling (PgBouncer, transaction pooling, troubleshooting idle-in-transaction)
- Redis operations (cache avalanche/penetration/breakdown, maxmemory-policy, persistence)
- **Why this matters:** Database incidents are the #1 cause of DevOps on-call pages. Not DBA depth, but enough to be the database person in a small team.

## Evidence
- Three new HTML lesson files created: `lessons/0020-cloud-platform.html`, `lessons/0021-devsecops.html`, `lessons/0022-database-ops.html`
- `index.html` updated: 22 lessons, 5 stages, new pill classes (cloud/security/database), flow chart extended
- `README.md` updated: expanded course structure and learning objectives

## Implications
- Course now covers ALL major DevOps interview domains. From 19 to 22 lessons, 5 stages total.
- Remaining gaps (out of scope for now): advanced SRE (chaos engineering, SLI/SLO design), cloud certifications (CKA/AWS SA), large distributed system architecture. These are explicitly mid-to-senior level.
- The course is now positioned to pass virtually all junior and most mid-level DevOps technical interviews.
