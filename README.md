<h1 align="center">webpg2app</h1>

<p align="center">
  <img src="https://res.cloudinary.com/dqv8dlj2s/image/upload/v1772326350/favicon_z20pgw.png" alt="favicon" width="64" />
</p>

<p align="center"><strong>Turn any webpage into a desktop app with one command, supports macOS, Windows, and Linux</strong></p>

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
