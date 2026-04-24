<img src="logo.png" align="right" width="120" alt="Shiori 标志" />

[English](README.md) · 中文

# Shiori 栞

一个更安静的 PDF 阅读与批注工具。此页面供受邀测试者下载。

目前处于**封闭内测**阶段。每个版本会在发布七天后自动失效，避免旧版里的
遗留问题积累。

---

## 最新版本

→ **[前往发布页](https://github.com/Nagi-ovo/shiori-releases/releases/latest)**

| 平台 | 文件 |
|---|---|
| macOS（Apple Silicon） | `Shiori_<版本号>_aarch64.dmg` |
| Windows（x64） | `Shiori_<版本号>_x64_en-US.msi` |

内测阶段不支持 Intel Mac。

每个版本的更新说明都挂在对应 release 下。你也可以在 app 内点击 Landing
页右下角的版本号查看完整 changelog。

---

## 首次启动

内测阶段 Shiori 未做签名，所以系统第一次启动它时会弹出提示。属于正常
现象。

### macOS

Gatekeeper 会提示*"无法打开 'Shiori'，因为 Apple 无法检查其中是否存在
恶意软件"*。

1. 挂载 DMG，把 **Shiori** 拖进 Applications。
2. 双击 Shiori，点击警告框里的**"取消"**。
3. 打开**系统设置 → 隐私与安全性**，拉到最底部，找到*"Shiori 已被阻止…"*
   一行，点击**"仍要打开"**。
4. 回到 Launchpad 或 Applications，再次双击 Shiori，在最后一次确认中
   点**"打开"**。

之后启动就是正常行为。

### Windows

SmartScreen 会提示*"Windows 已保护你的电脑"*。

- 点击**"更多信息"**
- 点击**"仍要运行"**

---

## 有效期

每个版本会在发布七天后失效。到期时 Shiori 会弹出提示并指引你回到这里
下载最新版本。

**你的草稿会跨版本保留。** 升级到新版不会丢失已经打开、批注或编辑过
的内容。

---

## 报告问题

请通过给你这个版本的渠道反馈。提 bug 时请附上日志文件：

- **macOS** — `~/Library/Logs/fun.nagi.shiori/Shiori.log`
- **Windows** — `%APPDATA%\fun.nagi.shiori\logs\`

---

## 隐私

Shiori 本地优先。所有 PDF、批注和偏好设置只存在你自己的设备上。无
账号，无遥测，无云同步。
