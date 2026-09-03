# automator

macOS Automator 工作流 / 快速操作存档目录。

## 存放内容

- Automator 工作流：`.workflow`（本质是文件夹，git 可正常跟踪）
- 快速操作（Quick Action，macOS 11+ 称「快速操作」，旧称「服务」）：同样是 `.workflow` 格式

## 子目录约定

每个工作流单独存放，目录名用 `[功能]-[类型]`：

```
automator/
├─ rename-batch-workflow/
│  ├─ rename-batch.workflow
│  └─ README.md
├─ pdf-merge-quickaction/
│  ├─ pdf-merge.workflow
│  └─ README.md
└─ README.md
```

## 导出 / 存入步骤

1. Automator 中「文件 → 存储」（或新建时直接存到本目录）。
2. 快速操作存为 `.workflow` 后，可双击在 Automator 打开，或右键「快速操作」菜单调用。
3. 同步在 `README.md` 写明用途、触发方式（右键 / 菜单栏 / 文件夹操作）、依赖。

> 提示：`.workflow` 在 Finder 里显示为单个文件，但本质是包（文件夹），用 `git` 跟踪内容变化没问题。
