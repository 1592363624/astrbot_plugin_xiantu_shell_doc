# 仙途 · 玩家文档

AstrBot 修仙文字游戏插件 `astrbot_plugin_xiantu_shell` 的玩家向文档仓库。

本仓库以 **git submodule** 形式挂在主项目 `wiki/` 目录下：在主仓库里可以直接看到这些文档，也可以单独推送更新到 GitHub。

## 目录规划

| 文档 | 内容 |
|------|------|
| [项目介绍.md](./项目介绍.md) | 这是什么游戏、适合谁玩、怎么接入 |
| [快速开始.md](./快速开始.md) | 新玩家第一局怎么玩 |
| [指令手册.md](./指令手册.md) | 全部指令、参数、权限、示例 |
| [玩法指南.md](./玩法指南.md) | 境界、功法、炼丹炼器、渡劫、组队、活动等系统说明 |
| [wiki/](./wiki/) | 进阶条目、名词表、FAQ、版本备忘 |

## 在主仓库中查看

```bash
git submodule update --init
# 然后打开 wiki/ 目录
```

## 更新本文档并推送到 GitHub

```bash
cd wiki
# 1. 编辑 / 新增 markdown
git add .
git commit -m "docs: 更新指令手册"
git push origin main

# 2. 回到主仓库，记录子模块指针并推送
cd ..
git add wiki
git commit -m "chore: 同步玩家文档子模块"
git push origin master
```

先推子仓库，再推主仓库；否则主仓库指针会指向本地未发布的提交。
