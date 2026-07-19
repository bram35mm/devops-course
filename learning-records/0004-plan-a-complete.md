# Plan A 深入课程扩展完成

在 9 节核心课的基础上，新增了 7 节深入课程（0010-0016），分为三个阶段：

**Stage 1: Linux 深入 (0010-0011)**
- 0010: 系统管理进阶 — 用户/组管理、sudo 配置、systemd unit 文件编写、cron、logrotate、ufw 防火墙、磁盘挂载
- 0011: 排错实战 — strace/lsof/tcpdump/性能分析套件、5 个经典故障场景（磁盘满、OOM、端口占用、进程死亡、响应慢）

**Stage 2: 网络深入 (0012-0013)**
- 0012: 网络协议基础 — TCP 三次握手/四次挥手、DNS 解析链、TLS 握手/证书链、HTTP 状态码、面试题覆盖
- 0013: 网络实战 — Nginx 生产配置（限流、健康检查、超时）、负载均衡算法、CDN 原理、真实排错场景（慢/502/端口不通）

**Stage 3: Kubernetes (0014-0016)**
- 0014: 核心概念 — 架构、Pod、Deployment、Service、Namespace、kubectl
- 0015: 网络与配置 — Ingress、ConfigMap、Secret、PVC、资源限制、Probes（liveness/readiness/startup）
- 0016: 生产实践 — Helm、HPA 自动扩缩容、RBAC 权限、K8s 监控集成、安全清单

**Evidence:** 全部 16 节课的 HTML 文件已生成，每节课包含测验和动手练习。
