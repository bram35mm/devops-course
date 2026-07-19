# Teaching Notes

## User Preferences
- 中文授课（用户使用中文交流）
- 混合风格：讲一点理论马上跟一个练习
- 每周 5–8 小时，课程应控制在单次 30–60 分钟内完成

## Style Notes
- 使用简体中文撰写课程内容
- 术语保留英文原文并附中文解释，避免翻译歧义
- 每个 Lesson 结尾提醒用户可以向 agent 追问

## Infrastructure
- VPS: RackNerd, 2 vCPU / 2GB RAM. Provider IP and OS TBD.
- 用途：Docker 部署、Nginx、监控（0010-0013 练习）
- K8s 学习：本机用 kind（不占 VPS 资源），VPS 可额外装 k3s 做轻量体验
- 本机环境：Ubuntu 22.04, Docker 29.6.2, Bash, SSH key (ed25519)
