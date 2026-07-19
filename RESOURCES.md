# DevOps 学习资源

## Knowledge（知识来源）

### 路线图 & 全景图

- [roadmap.sh/devops](https://roadmap.sh/devops)
  最权威的 DevOps 技能路线图，社区驱动，持续更新至 2026。涵盖从基础到高级的所有技能节点，每个节点附带学习资源链接。**用于：规划学习路径，确认当前所处阶段。**

- [milanm/DevOps-Roadmap (GitHub, 19.9k stars)](https://github.com/milanm/DevOps-Roadmap)
  以 roadmap.sh 为基础整理的资源合集，按主题分类（Git → 编程语言 → Linux → 网络 → 容器 → K8s → CI/CD → 云），附大量免费学习链接。**用于：按主题查找具体学习材料。**

### 书籍

- _The Phoenix Project_ — Gene Kim, Kevin Behr, George Spafford
  DevOps 入门必读小说。通过一家虚构公司的故事展示 DevOps 为什么重要、解决什么问题。不是技术书，但建立正确的思维框架。**用于：理解 DevOps 的「为什么」。**

- _The DevOps Handbook_ — Gene Kim, Jez Humble, Patrick Debois, John Willis
  《凤凰项目》的实操续作，讲如何在实际组织中落地 DevOps。**用于：学完基础工具后，理解它们如何拼在一起。**

- _Accelerate_ — Nicole Forsgren, Jez Humble, Gene Kim
  基于数据的 DevOps 效能研究。定义了衡量软件交付能力的四个关键指标（部署频率、变更前置时间、变更失败率、故障恢复时间）。**用于：理解 DevOps 的度量体系，面试常考题。**

### 在线课程

- [Linux Foundation: Introduction to DevOps and Site Reliability Engineering (edX)](https://www.edx.org/learn/devops/the-linux-foundation-introduction-to-devops-and-site-reliability-engineering)
  Linux 基金会官方出品，免费旁听。**用于：系统化入门。**

- [KodeKloud](https://kodekloud.com/)
  动手实操为主的 DevOps 学习平台，每个概念都配一个真实终端环境。覆盖 Docker、Kubernetes、Ansible、Terraform 等。付费但性价比极高。**用于：不想在自己机器上折腾环境时的替代方案。**

### 文档 & 教程

- [Docker 官方文档](https://docs.docker.com/get-started/)
  Docker 入门的最佳起点，有手把手的 getting started 指南。

- [Kubernetes 官方教程](https://kubernetes.io/docs/tutorials/)
  K8s 官方互动教程，从零部署一个集群。

- [Pro Git (免费在线书)](https://git-scm.com/book/zh/v2)
  Git 的权威参考书，有中文版。**用于：从「会用 Git 提交代码」升级到「理解 Git 内部原理」。**

- [The Missing Semester of Your CS Education (MIT)](https://missing.csail.mit.edu/)
  涵盖 Shell、Vim、Git、调试、元编程等「学校不教但工作必需」的技能。**用于：补全命令行和开发工具链的基础。**

## Wisdom（社区 & 实践）

- [r/devops (Reddit)](https://reddit.com/r/devops)
  DevOps 从业者社区，讨论工具选型、面试经验、职业发展。信噪比尚可。

- [DEV Community - DevOps tag](https://dev.to/t/devops)
  开发者社区的技术博文区，大量一手实操文章。

- [The New Stack](https://thenewstack.io/)
  DevOps / Cloud Native 领域的专业媒体，适合跟踪行业动态。

- [Cloud Native Computing Foundation (CNCF)](https://www.cncf.io/)
  云原生技术的大本营。Kubernetes、Prometheus、Helm 等项目都在这里。有免费的 [CNCF Landscape](https://landscape.cncf.io/) 全景图。


## GitHub 协作 & 项目管理

- [opensource.guide](https://opensource.guide/)
  GitHub 官方出品的开源指南，覆盖「如何创建开源项目」「如何维护」「如何建立社区」等全部主题。**用于：系统性学习开源项目维护的方方面面。**

- [semver.org](https://semver.org/)
  语义化版本规范（Semantic Versioning 2.0.0）。定义了 MAJOR.MINOR.PATCH 的精确含义和版本优先级规则。**用于：理解何时升 MAJOR、何时升 MINOR。**

- [keepachangelog.com](https://keepachangelog.com/)
  Changelog 最佳实践指南。定义了 CHANGELOG.md 的标准格式（Added/Changed/Deprecated/Removed/Fixed/Security）。**用于：写人能看懂的 Changelog。**

- [conventionalcommits.org](https://www.conventionalcommits.org/)
  约定式提交规范（Conventional Commits 1.0.0）。定义了 `feat:` `fix:` `BREAKING CHANGE:` 等标准化 commit message 格式。**用于：让机器能从 commit 历史自动判断版本号。**

- [common-changelog (vweevers)](https://github.com/vweevers/common-changelog)
  Changelog 风格指南，比 keepachangelog 更细致，覆盖多仓库、预发布版本等边缘情况。**用于：写生产级 Changelog 的参考。**

- [The Open Source Way 2.0](https://github.com/theopensourceway/guidebook)
  Red Hat 社区架构师编写的开源社区管理指南，有中文版。覆盖用户→贡献者转化、治理模型、导师制。**用于：深度理解开源社区治理。**

- [Linux Foundation: Recommended Practices for Hosting OSS on GitHub](https://www.linuxfoundation.org/research/hosting-os-projects-on-github)
  Linux 基金会官方报告，系统总结在 GitHub 上托管开源项目的最佳实践。**用于：从机构角度理解 GitHub 项目管理的完整图景。**
## Gaps（待填补的空白）

- 目前缺少中文社区/资源推荐。如用户偏好中文内容，后续补充。
- 云服务商（AWS/阿里云）的 free tier 实操路径需要专门调研。
- 面试专项资源（DevOps 面试题、模拟面试）尚未收录。
