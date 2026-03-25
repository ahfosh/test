# Git 基础命令练习项目

这个项目专门用于练习 Git 核心基础命令，帮助初学者熟悉 Git 的日常操作流程，掌握版本控制的核心思想和常用指令。

## 📋 项目目标
- 掌握 Git 本地仓库的初始化、提交、分支管理等核心命令
- 理解工作区、暂存区、版本库的概念及流转关系
- 熟悉远程仓库的关联、推送、拉取等操作
- 学会解决简单的分支冲突、版本回退等场景问题

## 🛠️ 环境准备
1. 安装 Git：前往 [Git 官方下载页](https://git-scm.com/downloads) 下载并安装对应系统的 Git 版本
2. 配置 Git 基础信息（首次使用必做）：
   ```bash
   # 配置用户名（替换为你的名称）
   git config --global user.name "Your Name"
   # 配置邮箱（替换为你的邮箱）
   git config --global user.email "your.email@example.com"
   # 查看配置是否生效
   git config --list
   ```

## 📖 核心练习内容
### 1. 本地仓库基础操作
| 命令 | 用途 | 示例 |
|------|------|------|
| `git init` | 初始化本地 Git 仓库 | `git init git-practice` |
| `git add` | 将文件添加到暂存区 | `git add README.md`（单个文件）<br>`git add .`（所有修改文件） |
| `git commit` | 提交暂存区文件到版本库 | `git commit -m "feat: 初始化README.md"` |
| `git status` | 查看工作区/暂存区状态 | `git status` |
| `git log` | 查看提交历史记录 | `git log`（完整日志）<br>`git log --oneline`（简洁日志） |
| `git reset` | 版本回退/撤销暂存 | `git reset --hard <commit-id>`（版本回退）<br>`git reset HEAD <file>`（撤销暂存） |
| `git checkout -- <file>` | 撤销工作区文件修改 | `git checkout -- README.md` |

### 2. 分支管理
| 命令 | 用途 | 示例 |
|------|------|------|
| `git branch` | 查看/创建分支 | `git branch`（查看分支）<br>`git branch feature/test`（创建分支） |
| `git checkout` | 切换分支 | `git checkout feature/test` |
| `git checkout -b` | 创建并切换分支 | `git checkout -b feature/test` |
| `git merge` | 合并分支到当前分支 | `git checkout main` <br> `git merge feature/test` |
| `git branch -d` | 删除本地分支 | `git branch -d feature/test` |

### 3. 远程仓库操作
> 前提：先在 GitHub/Gitee/GitLab 等平台创建空的远程仓库

| 命令 | 用途 | 示例 |
|------|------|------|
| `git remote add` | 关联远程仓库 | `git remote add origin https://github.com/your-username/git-practice.git` |
| `git push` | 推送本地分支到远程 | `git push -u origin main`（首次推送并关联）<br>`git push`（后续推送） |
| `git pull` | 拉取远程分支到本地 | `git pull origin main` |
| `git clone` | 克隆远程仓库到本地 | `git clone https://github.com/your-username/git-practice.git` |
| `git remote -v` | 查看远程仓库关联信息 | `git remote -v` |

## 📝 练习步骤建议
1. **初始化仓库**：本地创建文件夹，执行 `git init` 初始化
2. **基础提交**：创建/修改文件 → `git add` → `git commit`，重复多次熟悉提交流程
3. **版本回退**：用 `git log` 查看 commit-id，执行 `git reset` 回退，再尝试恢复
4. **分支练习**：创建功能分支 → 在分支上提交修改 → 合并到主分支 → 解决简单冲突
5. **远程联动**：关联远程仓库 → 推送本地代码 → 克隆到新目录 → 拉取更新 → 推送修改

## ❓ 常见问题
- **提交失败提示“身份未配置”**：检查 `git config --list`，确保配置了 user.name 和 user.email
- **push 失败提示“权限不足”**：确认远程仓库地址正确，且本地已配置 SSH 密钥/账号密码
- **分支合并冲突**：冲突文件会标注冲突区域，手动修改后重新 `git add` → `git commit` 即可

## 📚 拓展学习资源
- [Git 官方文档](https://git-scm.com/doc)
- [廖雪峰 Git 教程](https://www.liaoxuefeng.com/wiki/896043488029600)
- [GitHub Git 速查表](https://education.github.com/git-cheat-sheet-education.pdf)

## 🎯 练习完成标准
能独立完成「本地初始化 → 多分支开发 → 版本回退 → 远程推送/拉取 → 解决简单冲突」全流程，且能解释每个核心命令的作用和执行逻辑。
