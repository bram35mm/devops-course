# DevOps 从零到进阶

22 节中文 DevOps 课程，覆盖从 Linux 命令行到 Kubernetes 生产实践、云平台、DevSecOps、数据库运维。面向有开发经验、无运维经验的全栈/前端开发者。

**线上地址**: [devops-course-6ep.pages.dev](https://devops-course-6ep.pages.dev)

## 课程结构

```
阶段一（9 节）— 核心体系，广度优先
  0001  什么是 DevOps？
  0002  Linux 命令行基础
  0003  Git 进阶
  0004  Shell 脚本编程
  0005  Docker 入门
  0006  CI/CD：GitHub Actions
  0007  部署实战
  0008  IaC：Terraform
  0009  监控 & 可观测性

阶段二 · Stage 1-4（10 节）— 深入进阶，按需跳学
  0010  Linux 系统管理进阶
  0011  Linux 排错实战
  0012  网络协议基础
  0013  网络实战与负载均衡
  0014  K8s 核心概念
  0015  K8s 网络与配置
  0016  K8s 生产实践
  0017  Ansible 配置管理
  0018  日志系统：Loki + Promtail
  0019  GitOps：ArgoCD

阶段二 · Stage 5（3 节）— 云平台与运维实战
  0020  云平台实操（AWS 核心服务）
  0021  DevSecOps 安全基础
  0022  数据库运维基础

每节课包含：概念讲解 → 动手练习 → 小测验 → 推荐资源。

## 参考文档

- [术语表](https://devops-course-6ep.pages.dev/reference/glossary.html) — 100+ DevOps 核心术语，中英对照
- [Linux 命令速查表](https://devops-course-6ep.pages.dev/reference/linux-cheatsheet.html) — 按功能分类的高频命令

## 本地运行

纯静态 HTML，无需构建：

```bash
git clone git@github.com:bram35mm/devops-course.git
cd devops-course
python3 -m http.server 8000
# 打开 http://localhost:8000
```


## 学习目标

学完 22 节课后具备：

- 从零搭建 CI/CD 流水线（build → test → deploy）
- 用 Docker 容器化任意项目，Docker Compose 编排多服务
- 用 Terraform 声明式管理基础设施
- Linux 服务器排错（网络、进程、磁盘、权限）
- K8s 核心概念与生产实践（Helm、HPA、RBAC）
- 操作云平台核心服务（VPC/EC2/IAM/S3/RDS）
- DevSecOps 安全防线（SAST、密钥检测、镜像扫描、K8s 策略）
- 数据库备份恢复、连接池排错、Redis 缓存运维
- 通过 DevOps 初级/中级岗位的技术面试

## 笔记

- [MISSION.md](MISSION.md) — 学习目标与约束
- [NOTES.md](NOTES.md) — 教学偏好与实验环境配置
- [RESOURCES.md](RESOURCES.md) — 外部学习资源推荐
- [learning-records/](learning-records/) — 学习进度记录
