<img src="logo.png" align="right" width="120" alt="Shiori logo" />

English · [中文](README.zh.md)

# Shiori 栞

A quieter place to read, annotate, and organize your PDFs. This is
the download page for invited testers.

Everything here is **closed-alpha**. Builds expire seven days after
release so stale bugs don't linger in the wild.

---

## Latest build

→ **[Releases](https://github.com/Nagi-ovo/shiori-releases/releases/latest)**

| Platform | File |
|---|---|
| macOS (Apple Silicon) | `Shiori_<version>_aarch64.dmg` |
| Windows (x64) | `Shiori_<version>_x64_en-US.msi` |

Intel Mac is not supported during the alpha.

Release notes are attached to each build on the releases page. You
can also open the in-app changelog by clicking the version number on
the Landing screen.

---

## First launch

Shiori is unsigned during the alpha, so your OS will pause the first
time you open it. This is expected.

### macOS

Gatekeeper will say *"Apple cannot check it for malicious software."*

1. Mount the DMG and drag **Shiori** into Applications.
2. Double-click Shiori. Click **Cancel** on the warning.
3. Open **System Settings → Privacy & Security**, scroll to the
   bottom, and click **Open Anyway** next to *"Shiori was blocked…"*.
4. Return to Launchpad / Applications and open Shiori again. Click
   **Open** on the final dialog.

Every launch after that is normal.

### Windows

SmartScreen will say *"Windows protected your PC."*

- Click **More info**
- Click **Run anyway**

---

## Expiry

Each build stops working seven days after its release date. When
that happens, Shiori will point you here for the next build.

**Your drafts carry over.** Upgrading to a new build keeps
everything you've opened, annotated, or drafted in place.

---

## Reporting bugs

Use whichever channel you received this build from. Please attach
the log file when filing:

- **macOS** — `~/Library/Logs/fun.nagi.shiori/Shiori.log`
- **Windows** — `%APPDATA%\fun.nagi.shiori\logs\`

---

## Privacy

Shiori is local-first. Your PDFs, notes, and preferences live only
on your machine. No accounts, no telemetry, no cloud sync.
