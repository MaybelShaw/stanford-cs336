# Stanford-CS336-Language-Modeling-from-Scratch-Spring-2025

## 仓库结构

本仓库使用 **git subtree** 管理两个独立的 assignment 仓库：

```
stanford-cs336/ (主仓库)
├── assignment1-basics/     → 同步到 MaybelShaw/assignment1-basics
├── assignment2-systems/    → 同步到 MaybelShaw/assignment2-systems
└── 其他文件
```

## 提交和推送指南

### 1. 添加和提交更改

```bash
# 添加所有更改
git add .

# 提交到本地主仓库
git commit -m "你的提交信息"
```

### 2. 推送到主仓库 (GitHub - stanford-cs336)

```bash
git push origin main
```

### 3. 同步到独立的 assignment 仓库

```bash
# 同步 assignment1 到独立仓库
git subtree push --prefix=assignment1-basics assignment1-remote main

# 同步 assignment2 到独立仓库
git subtree push --prefix=assignment2-systems assignment2-remote main
```

### 完整工作流程示例

```bash
# 修改了 assignment2-systems/ 下的文件后
git add .
git commit -m "fix: 修复 attention 实现"
git push origin main                                    # 推送到主仓库
git subtree push --prefix=assignment2-systems assignment2-remote main  # 同步到独立仓库
```

### 从独立仓库拉取更新

```bash
# 从 assignment1 独立仓库拉取
git subtree pull --prefix=assignment1-basics assignment1-remote main

# 从 assignment2 独立仓库拉取
git subtree pull --prefix=assignment2-systems assignment2-remote main
```

---