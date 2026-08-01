<p align="center">
  <img src="./logo.png" width="96" height="96" alt="Shiori logo" />
</p>

<h1 align="center">Shiori 栞</h1>

<p align="center">
  A local-first reader for PDF, Markdown, and HTML documents.
</p>

<p align="center">
  <a href="./README.md">English</a>
  ·
  <a href="./README.zh-CN.md">简体中文</a>
  ·
  <a href="./README.ja.md">日本語</a>
</p>

<p align="center">
  <a href="https://shiori.nagi.fun">Website</a>
  ·
  <a href="https://github.com/Nagi-ovo/shiori-releases/releases/latest">Downloads</a>
</p>

![Shiori home screen](./assets/screenshots/home-en.jpg)

Shiori is a quiet document workspace for reading, marking up, and shipping
documents without turning them into somebody else's cloud data. PDF annotation is
the core workflow, and recent builds also support Markdown and HTML viewing with
tabs, per-document state, and session restore.

## Highlights

- **PDF reading and annotation**: highlights, markup tools, thumbnails, export,
  and local draft recovery.
- **Tabs for documents**: open multiple PDF, Markdown, and HTML files; each tab
  keeps its own view state and survives relaunch until you close it.
- **Markdown and HTML previews**: Markdown front matter is surfaced cleanly, and
  HTML can run in an isolated sandbox only when you choose to run it.
- **Desktop side tools**: keep an embedded browser or terminal next to a PDF,
  including local shells such as `cc` / Claude Code when they are installed.
- **Local-first storage**: documents, annotations, recent files, and preferences
  stay on your device.
- **Desktop and mobile targets**: macOS, Windows, Linux, Android direct install,
  with iOS / iPadOS and Google Play distribution handled through their stores.

## Screenshots

![PDF workspace with thumbnails, annotations, and side panel](./assets/screenshots/pdf-workspace.jpg)

![Tabbed workspace with PDF, Markdown, and HTML documents](./assets/screenshots/desktop-tabs.jpg)

![PDF workspace with the embedded browser open](./assets/screenshots/desktop-browser.jpg)

![PDF workspace with the embedded terminal running Claude Code through cc](./assets/screenshots/desktop-terminal-cc.jpg)

![Markdown document preview](./assets/screenshots/markdown-document.jpg)

![HTML document running in Shiori](./assets/screenshots/html-document.jpg)

## Downloads

Installers are published on the
[GitHub Releases](https://github.com/Nagi-ovo/shiori-releases/releases) page.

| Platform | Recommended package | Update path |
| --- | --- | --- |
| macOS Apple Silicon | `.dmg` | Signed in-app updater |
| macOS Intel | `.dmg` | Signed in-app updater |
| Windows | `.msi` | Signed in-app updater |
| Linux | `.AppImage`; `.deb` for Debian / Ubuntu | `.AppImage` updater or manual package update |
| Android direct install | `.apk` | In-app APK update flow |
| Google Play | Coming soon | Google Play |
| iOS / iPadOS | Coming soon | App Store / TestFlight |

Desktop and Android direct-install builds can update from inside Shiori. Android
direct-install builds download and verify the APK before handing it to the
Android package installer. Store builds are updated by their stores and are not
mirrored here as `.aab` or `.ipa` files.

## Agent skill

The open-source [Shiori CLI skill](./skills/shiori) teaches Codex, Claude Code,
and other compatible coding agents how to inspect the document open in Shiori,
find passages by text, add anchored annotations, and reply inside callout
threads. It expects the `shiori` CLI to be available on `PATH`.

> [!IMPORTANT]
> This skill is not usable yet because the Shiori CLI has not been released.
> Installing it now only prepares the agent integration for the future CLI.

<details>
<summary>Future installation instructions (after the CLI is released)</summary>

Install it globally with the cross-agent `skills` installer, then select the
coding agents that should receive it:

```sh
npx skills@latest add Nagi-ovo/shiori-releases --skill shiori --global
```

For local skill development, macOS and Linux contributors can instead clone
this repository and link the checkout into an agent's user-level skill
directory:

```sh
ln -s "$(pwd)/skills/shiori" "${CODEX_HOME:-$HOME/.codex}/skills/shiori"
ln -s "$(pwd)/skills/shiori" "$HOME/.claude/skills/shiori"
```

Use the line for the agent you are developing against.

</details>

The skill itself is independently available under the
[MIT License](./skills/shiori/LICENSE); that license does not apply to Shiori
application or CLI binaries.

## About This Repository

This repository hosts downloadable builds, updater signatures, localized
release notes, screenshots, and the open-source Shiori CLI agent skill. The
Shiori application source repository is private, and discussions, feature
requests, and bug reports are handled outside this repo.
