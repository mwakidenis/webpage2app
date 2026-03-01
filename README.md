<h1 align="center">webpg2app</h1>

<p align="center">
  <img src="https://res.cloudinary.com/dqv8dlj2s/image/upload/v1772326350/favicon_z20pgw.png" alt="favicon" width="64" />
</p>

<p align="center"><strong>Turn any webpage into a desktop app with one command, supports macOS, Windows, and Linux</strong></p>
<div align="center">
    <a href="https://twitter.com/Apro5550" target="_blank"> 
    <img alt="twitter" src="https://img.shields.io/badge/follow-Apro5550-red?style=flat-square&logo=Twitter"></a> 
    <a href="" target="_blank"> 
    <img alt="telegram" src="https://img.shields.io/badge/chat-telegram-blueviolet?style=flat-square&logo=Telegram"></a>
    <a href="https://github.com/mwakidenis/webpg2app/releases" target="_blank"> 
    <img alt="GitHub downloads" src="https://img.shields.io/github/downloads/mwakidenis/webpg2app/total.svg?style=flat-square"></a> 
    <a href="https://github.com/mwakidenis/webpg2app/commits" target="_blank"> 
    <img alt="GitHub commit" src="https://img.shields.io/github/commit-activity/m/tw93/Pake?style=flat-square"></a>
    <a href="https://github.com/mwakidenis/webpg2app/issues?q=is%3Aissue+is%3Aclosed" target="_blank"> 
    <img alt="GitHub closed issues" src="https://img.shields.io/github/issues-closed/mwakidenis/webpg2app.svg?style=flat-square"></a> 
</div>

## Features

- **Lightweight**: Nearly 20 times smaller than Electron packages, typically around 5MB
- **Fast**: Built with Rust Tauri, much faster than traditional JS frameworks with lower memory usage
- **Easy to use**: One-command packaging via CLI or online building, no complex configuration needed
- **Feature-rich**: Supports shortcuts, immersive windows, drag & drop, style customization, ad removal

## Getting Started

- **Beginners**: Download ready-made Popular Packages or use Online Building with no environment setup required
- **Developers**: Install CLI Tool for one-command packaging of any website with customizable icons, window settings, and more
- **Advanced Users**: Clone the project locally for Custom Development, or check Advanced Usage for style customization and feature enhancement
- **Troubleshooting**: Check FAQ for common issues and solutions

## Popular Packages

| Platform | Download                                                                                                                                                                          |
| -------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| WeRead   | [Mac](https://github.com/mwakidenis/webpg2app/releases) / [Windows](https://github.com/mwakidenis/webpg2app/releases) / [Linux](https://github.com/mwakidenis/webpg2app/releases) |
| Twitter  | [Mac](https://github.com/mwakidenis/webpg2app/releases) / [Windows](https://github.com/mwakidenis/webpg2app/releases) / [Linux](https://github.com/mwakidenis/webpg2app/releases) |
| ChatGPT  | [Mac](https://github.com/mwakidenis/webpg2app/releases) / [Windows](https://github.com/mwakidenis/webpg2app/releases) / [Linux](https://github.com/mwakidenis/webpg2app/releases) |
| YouTube  | [Mac](https://github.com/mwakidenis/webpg2app/releases) / [Windows](https://github.com/mwakidenis/webpg2app/releases) / [Linux](https://github.com/mwakidenis/webpg2app/releases) |

More applications available at [Releases](https://github.com/mwakidenis/webpg2app/releases).

## Keyboard Shortcuts

| Mac        | Windows/Linux | Function         |
| ---------- | ------------- | ---------------- |
| Cmd + [    | Ctrl + Left   | Previous page    |
| Cmd + ]    | Ctrl + Right  | Next page        |
| Cmd + Up   | Ctrl + Up     | Scroll to top    |
| Cmd + Down | Ctrl + Down   | Scroll to bottom |
| Cmd + r    | Ctrl + r      | Refresh          |
| Cmd + w    | Ctrl + w      | Hide window      |
| Cmd + -    | Ctrl + -      | Zoom out         |
| Cmd + =    | Ctrl + =      | Zoom in          |
| Cmd + 0    | Ctrl + 0      | Reset zoom       |
| Cmd + L    | Ctrl + L      | Copy URL         |

## Command-Line Packaging

```bash
# Install webpg2app CLI
pnpm install -g webpg2app-cli

# Basic usage
webpg2app https://github.com --name GitHub

# Advanced usage
webpg2app https://example.com --name MyApp --width 1200 --height 800 --hide-title-bar
Development

Requires Rust >=1.85 and Node >=22.

# Install dependencies
pnpm install

# Run in development mode
pnpm run dev

# Build application
pnpm run build
License

MIT License



███    ███ ██     ██  █████  ██   ██ ██ ██████  ███████ ███    ██ ██  ██████
████  ████ ██     ██ ██   ██ ██  ██  ██ ██   ██ ██      ████   ██ ██ ██
██ ████ ██ ██  █  ██ ███████ █████   ██ ██   ██ █████   ██ ██  ██ ██  ██████
██  ██  ██ ██ ███ ██ ██   ██ ██  ██  ██ ██   ██ ██      ██  ██ ██ ██       ██
██      ██  ███ ███  ██   ██ ██   ██ ██ ██████  ███████ ██   ████ ██  ██████

```
