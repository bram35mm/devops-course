# 理解了 Linux 文件权限

用户通过 `ls -l` 的实际输出理解了 Linux 权限模型：10 字符权限段（类型 + owner + group + others）、r/w/x 含义、目录 x 权限的特殊含义（能否 cd 进入）、数字权限计算方式（r=4, w=2, x=1）。

**Evidence:** 用户贴出了 `ls -l ~/code/podcast` 的实际输出并提问。从提问内容看，用户已经理解了 `ls -l` 命令本身，卡在权限字符的解读上。经过解释后，用户表示理解并继续下一课。

**Implications:**
- 权限概念是 Linux 基础中的关键节点，理解了 rwx 模型后，chmod、chown 操作就不会再困惑
- 用户现在可以独立排查「Permission denied」类问题
- 后续 Docker（容器内用户权限）、SSH key 权限（必须 600）等课程可以直接引用这个概念
