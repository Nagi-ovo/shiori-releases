<p align="center">
  <img src="./logo.png" width="96" height="96" alt="Shiori logo" />
</p>

<h1 align="center">Shiori 栞</h1>

<p align="center">
  PDF、Markdown、HTML のためのローカルファーストな文書リーダー。
</p>

<p align="center">
  <a href="./README.md">English</a>
  ·
  <a href="./README.zh-CN.md">简体中文</a>
  ·
  <a href="./README.ja.md">日本語</a>
</p>

<p align="center">
  <a href="https://shiori.nagi.fun">Web サイト</a>
  ·
  <a href="https://github.com/Nagi-ovo/shiori-releases/releases/latest">ダウンロード</a>
</p>

![Shiori Japanese home screen](./assets/screenshots/home-ja.jpg)

Shiori は、文書をクラウドに預けず、静かに読み、書き込み、書き出すための
文書ワークスペースです。中心となるのは PDF 注釈ですが、最近のビルドでは
Markdown と HTML のプレビュー、文書ごとのタブ状態、次回起動時の復元にも対応しています。

## 主な機能

- **PDF の閲覧と注釈**：ハイライト、マークアップ、サムネイル、書き出し、
  ローカル草稿の復元。
- **文書タブ**：PDF、Markdown、HTML を複数開けます。各タブは表示位置や状態を保持し、
  閉じない限り次回起動時にも復元されます。
- **Markdown / HTML プレビュー**：Markdown の front matter を読みやすく表示し、
  HTML は明示的に実行したときだけ隔離サンドボックスで動きます。
- **デスクトップ用サイドツール**：PDF の横に内蔵ブラウザやターミナルを置けます。
  `cc` / Claude Code がローカルに入っていれば、Shiori の内蔵ターミナルから起動できます。
- **ローカルファースト**：文書、注釈、最近使ったファイル、設定はあなたの端末に残ります。
- **デスクトップとモバイル**：macOS、Windows、Linux、Android 直接インストール版。
  iOS / iPadOS と Google Play は各ストア経由で配布します。

## スクリーンショット

![サムネイル、注釈、サイドパネルを開いた PDF ワークスペース](./assets/screenshots/pdf-workspace.jpg)

![PDF、Markdown、HTML を同時に開いたタブ付きワークスペース](./assets/screenshots/desktop-tabs.jpg)

![内蔵ブラウザを横に開いた PDF ワークスペース](./assets/screenshots/desktop-browser.jpg)

![内蔵ターミナルで cc から Claude Code を起動している PDF ワークスペース](./assets/screenshots/desktop-terminal-cc.jpg)

![Shiori の Markdown プレビュー](./assets/screenshots/markdown-document.jpg)

![Shiori で実行中の HTML 文書](./assets/screenshots/html-document.jpg)

## ダウンロード

インストーラーは
[GitHub Releases](https://github.com/Nagi-ovo/shiori-releases/releases) で公開しています。

| プラットフォーム | 推奨パッケージ | 更新方法 |
| --- | --- | --- |
| macOS Apple Silicon | `.dmg` | 署名付きアプリ内アップデート |
| macOS Intel | `.dmg` | 署名付きアプリ内アップデート |
| Windows | `.msi` | 署名付きアプリ内アップデート |
| Linux | `.AppImage`；Debian / Ubuntu は `.deb` | `.AppImage` updater または手動更新 |
| Android 直接インストール版 | `.apk` | アプリ内 APK 更新フロー |
| Google Play | 近日公開 | Google Play |
| iOS / iPadOS | 近日公開 | App Store / TestFlight |

デスクトップ版と Android の直接インストール版は、Shiori 内から更新できます。
Android 直接インストール版は APK をアプリ内でダウンロードして検証したあと、
Android のパッケージインストーラーへ渡します。ストア版は各ストアで更新されるため、
このリポジトリには `.aab` や `.ipa` としてミラーしません。

## Agent skill

オープンソースの [Shiori CLI skill](./skills/shiori) は、Codex、Claude Code、
その他の対応 coding agent に、Shiori で開いている文書の読み取り、本文検索、
テキストに結び付いた注釈の追加、callout thread への返信方法を伝えます。
利用するには `shiori` CLI が `PATH` に含まれている必要があります。

このリポジトリを clone したあと、macOS / Linux では使用する Agent の
ユーザーレベル skill ディレクトリへリンクできます。

```sh
ln -s "$(pwd)/skills/shiori" "${CODEX_HOME:-$HOME/.codex}/skills/shiori"
ln -s "$(pwd)/skills/shiori" "$HOME/.claude/skills/shiori"
```

利用する Agent に対応する一行だけを実行してください。この skill は独立して
[MIT License](./skills/shiori/LICENSE) で公開されます。このライセンスは Shiori
アプリケーションおよび CLI バイナリには適用されません。

## このリポジトリについて

このリポジトリは、Shiori のインストーラー、更新署名、ローカライズされた
リリースノート、スクリーンショット、およびオープンソースの Shiori CLI Agent
skill をホストしています。Shiori アプリケーションのソースリポジトリは非公開で、
議論・機能要望・不具合報告はこのリポジトリでは扱いません。
