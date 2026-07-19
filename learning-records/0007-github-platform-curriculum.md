# GitHub 平台系统性教学——新增子课程

用户明确提出需要 GitHub 的系统性教学，包括开源项目维护、发布 release 等知识。

现有课程已覆盖 Git 进阶操作（0003）和 GitHub Actions CI/CD（0006），但 GitHub 作为**协作平台**的系统性知识是空白的——包括项目管理（Issues/Projects）、版本发布（SemVer/Releases/Changelog）、开源社区维护（模板/治理/Pages）。

## 新增 3 节课程

### 0023: GitHub 协作——Issues、PR、Code Review
- GitHub Issues 项目管理（Labels/Milestones/Assignees）
- Pull Request 工作流（Draft/Review/Suggested changes）
- Branch Protection（审批 + CI 检查门禁）
- CODEOWNERS 自动指派 Reviewer
- **DevOps 关联**：分支保护 → CI 门禁 → 代码质量自动化

### 0024: 版本发布——SemVer、Tags、Releases、Changelog
- Semantic Versioning（MAJOR.MINOR.PATCH）
- git tag（lightweight vs annotated——永远用 annotated）
- GitHub Releases（auto-generated notes/assets/pre-release）
- CHANGELOG.md（keepachangelog.com 格式）
- Conventional Commits + semantic-release 自动化
- **DevOps 关联**：Tag push → CI/CD 触发 → 自动构建+发布+部署

### 0025: 开源项目维护——社区治理、模板、Pages
- Community health files（CONTRIBUTING/CODE_OF_CONDUCT/SECURITY/SUPPORT）
- Issue/PR 模板（.github/ISSUE_TEMPLATE/）
- .github 仓库（org-wide defaults）
- 许可证选择（MIT/Apache 2.0/GPL 的区别）
- GitHub Discussions / Wiki / Pages
- 治理模型（BDFL → Maintainer Team → TSC）

## Resources Added
- opensource.guide（GitHub 官方开源指南）
- semver.org（语义化版本规范）
- keepachangelog.com（Changelog 最佳实践）
- conventionalcommits.org（约定式提交）
- common-changelog（Changelog 风格指南）

## Implications
- GitHub 协作技能是 DevOps 日常工作的高频技能——code review、PR 流程、release 管理
- 分支保护 + CI/CD 门禁是 DevOps 的核心职责之一
- 课程数从 22 → 25，新增 GitHub 协作领域 pill
