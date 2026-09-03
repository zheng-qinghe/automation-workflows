# automation-workflows

跨生态自动化工作流仓库。统一管理三类个人自动化资产：

- **Microsoft Power Automate** —— 云流（Cloud flows）/ 桌面流（Desktop flows）
- **macOS Automator** —— 工作流（Workflow）/ 快速操作（Quick Action）
- **Apple Shortcuts** —— 快捷指令（iPhone / iPad / Mac 通用）

目标：让每个流都能**被检索、被重建、被复用**，而不是散落在各账号里。

---

## 目录结构

```
automation-workflows/
├─ power-automate/   # 微软 Power Automate 流存档
├─ automator/        # macOS Automator .workflow
├─ shortcuts/        # Apple 快捷指令 .shortcut
└─ README.md         # 本文件：索引 + 规范
```

每个子目录下的 `README.md` 说明该类资产的存放约定与命名格式。

---

## 提交规范（所有流通用）

每个流 **单独一个子目录或单独一个文件**，并配套一份说明，字段至少包含：

| 字段 | 说明 |
|------|------|
| 名称 | 流的中文 + 英文简称 |
| 用途 | 一句话解决什么问题 |
| 触发条件 | 手动 / 定时 / 收到邮件 / 文件变更 等 |
| 依赖 | 需要的账号、App、连接器、权限 |
| 导入方式 | 如何在本机恢复这个流 |
| 备注 | 已知限制、坑、维护记录 |

**命名约定**：`[工具]-[功能]-[平台]`
例：`powerautomate-invoice-approve`、`automator-rename-batch`、`shortcut-log-mood`

---

## Power Automate 存档策略（关键）

Power Automate 的流绑在微软账号上，能否离线导出取决于类型：

1. **优先——完整导出（可重新导入）**
   - 云流：在 Power Automate 网页端「导出 → 包(.zip)」，包含流定义与连接引用。
   - 桌面流：在 Power Automate 桌面版「导出」为 `.msapp`。
   - 把 `.zip` / `.msapp` 直接放进 `power-automate/` 对应子目录。

2. **受限时——文档化重建（截图 + 步骤文本 + 导入说明）**
   - 当连接依赖云端账号、无法导出包时，**不要只放截图**。
   - 采用：`流程图全景截图.png` + `步骤说明.md`（逐一列出每个动作、字段值、表达式）+ `导入说明.md`（连接如何配置）。
   - 这样别人（或未来的你）能照着重建，且文本可被 GitHub 检索。

> 原则：**能导出包就导出包；导不出就用「图 + 文」双保险**，绝不只丢一张截图。

---

## Shortcuts / Automator 存档

- `shortcuts/`：在「快捷指令」App 里「分享 → 存储到文件」导出 `.shortcut`，直接放进目录。
- `automator/`：在 Automator 里「文件 → 存储」，生成 `.workflow` 包（本质是文件夹，git 可正常跟踪），直接放进目录。

---

## 初始化记录

- 仓库名：`automation-workflows`
- 创建：2026-09-03
- 状态：骨架已建（README + 三个分类目录 + .gitignore），尚未推送远程。
