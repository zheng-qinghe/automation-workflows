# shortcuts

Apple 快捷指令（Shortcuts）存档目录。

## 存放内容

- 快捷指令文件：`.shortcut`（iPhone / iPad / Mac 通用，可在「快捷指令」App 跨设备同步）

## 子目录约定

每个指令单独存放，目录名用 `[功能]`：

```
shortcuts/
├─ log-mood/
│  ├─ log-mood.shortcut
│  └─ README.md
├─ wifi-toggle/
│  ├─ wifi-toggle.shortcut
│  └─ README.md
└─ README.md
```

## 导出 / 存入步骤

1. 「快捷指令」App → 打开目标指令 → 右上「…」→「分享」→「存储到文件」→ 导出 `.shortcut`。
2. 把 `.shortcut` 放进本目录对应子目录。
3. 在 `README.md` 写明用途、触发方式（Siri / 小组件 / 自动化）、依赖（需要的 App、权限）。

> 提示：`.shortcut` 是二进制 plist 封装，可直接双击导入「快捷指令」App 恢复。若 App 内已 iCloud 同步，导出文件主要用于版本备份与 GitHub 托管。
