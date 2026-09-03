# power-automate

Microsoft Power Automate 流存档目录。

## 存放内容

- 云流导出的包：`.zip`（Power Automate 网页端「导出 → 包」）
- 桌面流导出：`.msapp`（Power Automate 桌面版「导出」）
- 受限流（无法导出包）的文档化重建资料：`截图.png` + `步骤说明.md` + `导入说明.md`

## 子目录约定

每个流一个子目录，目录名用 `[功能]-[平台]`，例：

```
power-automate/
├─ invoice-approve/          # 可导出包
│  ├─ invoice-approve.zip
│  └─ README.md
├─ daily-report/             # 受限流：文档化重建
│  ├─ flow-overview.png
│  ├─ 步骤说明.md
│  ├─ 导入说明.md
│  └─ README.md
└─ README.md
```

## 导出步骤速查

1. 云流：Power Automate 网页端 → 我的流 → 目标流 → 导出 → 包(.zip) → 下载。
2. 桌面流：Power Automate 桌面版 → 我的流 → 目标流 → 导出 → 选择「带或不带连接」。

> 导出包优先；连接依赖云端账号导不出时，按根目录 README 的「受限时」策略用图文重建。
