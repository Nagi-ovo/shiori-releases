# Shiori 栞 — closed-alpha releases

Binary host for [**Shiori**](https://shiori.nagi.fun), a local-first
PDF reader and editor. This repository exists so invited testers have
a single URL to pull from; the source is kept in a separate private
repo.

Everything here is **closed-alpha**. Builds self-destruct 7 days after
compile time — see **Expiry** below.

---

## Latest build

→ **[Releases](https://github.com/Nagi-ovo/shiori-release/releases/latest)**

Each release ships three artifacts:

| Platform | File |
|---|---|
| macOS (Apple Silicon) | `Shiori_<version>_aarch64.dmg` |
| Windows (x64) | `Shiori_<version>_x64-setup.exe` (NSIS) |
| Windows (x64) | `Shiori_<version>_x64_en-US.msi` (Windows Installer) |

Intel Mac is not supported during the alpha.

In-app release notes are available by clicking the version number in
the Landing corner. The latest notes are also pinned to each GitHub
release above.

---

## First launch

Builds are unsigned during the alpha, so the OS will warn you.

### macOS

Gatekeeper will say *"Apple cannot check it for malicious software."*
This is expected.

1. Mount the DMG and drag **Shiori** into Applications.
2. Double-click Shiori. Click **Cancel** on the Gatekeeper warning.
3. Open **System Settings → Privacy & Security**. Scroll to the
   bottom — you'll see *"Shiori was blocked…"*. Click **Open Anyway**.
4. Return to Launchpad / Applications and open Shiori again. Click
   **Open** on the final dialog.

Subsequent launches are normal.

中文速通：双击被拦 → System Settings → Privacy & Security 拉到底
→ Open Anyway → 回去再打开一次 → Open。之后正常。

### Windows

SmartScreen will say *"Windows protected your PC."*

- Click **More info**
- Click **Run anyway**

---

## Expiry

Each build carries a `__BUILD_TIMESTAMP__` injected at compile time
and refuses to start more than **7 days** after that moment. When the
app expires it shows an expiry screen linking back to
[the latest release](https://github.com/Nagi-ovo/shiori-release/releases/latest).

**Your drafts carry over across upgrades.** They live in IndexedDB
scoped to the `fun.nagi.shiori` bundle identifier, so installing a
newer build keeps everything in place.

---

## Reporting bugs

Use whichever channel you got this build from. Please attach the log
file when filing:

- **macOS** — `~/Library/Logs/fun.nagi.shiori/Shiori.log`
- **Windows** — `%APPDATA%\fun.nagi.shiori\logs\`

---

## What's here vs. what's not

- **Here** — compiled binaries only (`.dmg`, `.msi`, `.exe`) and
  these release notes.
- **Not here** — source, issues, PRs. The source repo is private for
  the alpha.

---

## Privacy

Shiori is local-first. No accounts, no telemetry, no cloud sync.
Drafts, thumbnails, and preferences all live on your machine —
IndexedDB + OS-standard application-support paths.
