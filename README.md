# DL Code

<div align="center">

![DL Code](https://deathlegionteamlk.github.io/dl-code/og-image.png)

**A free AI-powered code editor for Windows, macOS, and Linux.**

Built with a built-in Claude AI assistant, an agentic app builder, and unlimited free AI via Ollama.

[![Download](https://img.shields.io/badge/Download-Free-brightgreen?style=for-the-badge)](https://github.com/deathlegionteamlk/dl-code/releases/latest)
[![Platforms](https://img.shields.io/badge/Platforms-Win%20%7C%20Mac%20%7C%20Linux-blue?style=for-the-badge)](https://github.com/deathlegionteamlk/dl-code/releases/latest)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)
[![Version](https://img.shields.io/badge/Version-1.0.0-orange?style=for-the-badge)](https://github.com/deathlegionteamlk/dl-code/releases/latest)

[🌐 Website](https://deathlegionteamlk.github.io/dl-code/) · [📦 Download](https://github.com/deathlegionteamlk/dl-code/releases/latest) · [🐛 Report Bug](https://github.com/deathlegionteamlk/dl-code/issues) · [💡 Request Feature](https://github.com/deathlegionteamlk/dl-code/issues)

</div>

---

## What is DL Code?

DL Code is a modern, cross-platform code editor that puts AI at the center of your workflow. It's not just a text editor with an AI plugin bolted on — AI is built in from the ground up. Describe an app in plain English, and DL Code's agentic builder scaffolds the project, writes every file, and installs the dependencies for you.

It uses the same Monaco editor that powers VS Code, so the editing experience feels instantly familiar. The UI is inspired by JetBrains IDEs — dark, dense, focused, and built for long coding sessions.

**Best of all: it's completely free.** The AI features work with local models via [Ollama](https://ollama.com), so you get unlimited AI assistance with no API keys, no rate limits, and no usage caps. Forever.

## ✨ Key Features

- **🤖 Built-in AI Assistant** — Chat with Claude right inside the editor. Ask it to explain code, refactor functions, generate tests, or fix bugs. The AI sees your file context, your selection, and your workspace.
- **⚡ Agentic App Builder** — Describe an app in plain English and DL Code's AI agent builds the entire project: scaffolds files, writes code, installs dependencies. A real Cursor-style builder that runs on your machine.
- **🆓 Free Unlimited AI (Ollama)** — Run AI models locally with Ollama. No API key, no rate limits, no usage caps. Works offline. Supports Qwen 2.5 Coder, DeepSeek Coder v2, CodeLlama, Llama 3.2, and 50+ more.
- **🎨 Syntax Highlighting for 60+ Languages** — TypeScript, JavaScript, Python, Rust, Go, Java, C++, C#, Ruby, PHP, Swift, Kotlin, Scala, HTML, CSS, JSON, YAML, SQL, Docker, Lua, Haskell, Elixir, Erlang, Clojure, Perl, Dart, R, Julia, OCaml, and many more.
- **💻 Real Integrated Terminal** — A PTY-backed terminal running bash, zsh, PowerShell, or cmd.exe. Multiple tabs, full color support, web links, and search.
- **🔄 Git Integration** — Source control panel with staged/unstaged changes, one-click stage/unstage, commit, branch switching, diff viewer, and full history.
- **🔌 Plugin & Extension System** — A real extension host that dynamically loads extensions from disk. VS Code-compatible API for themes, language packs, formatters, linters, and tools.
- **🔍 Cross-File Search** — Find anything across your entire workspace with regex support, case sensitivity, whole word matching, and file globs.
- **⌨️ Command Palette & Quick Open** — Press `Ctrl+Shift+P` for commands, `Ctrl+P` to jump to any file. All your muscle memory from VS Code and JetBrains works here.
- **🌍 Cross-Platform** — One editor, three platforms. Windows 10+, macOS (Intel and Apple Silicon via Rosetta), and Linux (AppImage, .deb, and tarball).

## 📦 Download

Pre-built binaries for every platform are available on the [Releases page](https://github.com/deathlegionteamlk/dl-code/releases/latest). Just download and run — no installers, no signup, no tracking.

| Platform | File | Size | How to run |
|----------|------|------|------------|
| **Windows** | `DL-Code-1.0.0-win-x64-portable.zip` | ~154 MB | Unzip, run `DL Code.exe` |
| **macOS** | `DL-Code-1.0.0-macos-x64.zip` | ~345 MB | Unzip, drag to Applications, right-click → Open |
| **Linux (AppImage)** | `DL-Code-1.0.0-linux-x86_64.AppImage` | ~144 MB | `chmod +x && ./DL-Code-*.AppImage` |
| **Linux (.deb)** | `DL-Code_1.0.0_amd64.deb` | ~102 MB | `sudo dpkg -i DL-Code_*.deb` |
| **Linux (tar.gz)** | `DL-Code-1.0.0-linux-x64.tar.gz` | ~143 MB | Extract, run `./dl-code` |

## 🤖 AI Setup

DL Code supports three AI providers. Pick whichever fits your needs — you can switch between them anytime in **Settings → AI**.

### Option 1: Ollama (Free, Unlimited, Local) — Recommended

[Ollama](https://ollama.com) runs AI models directly on your machine. No API key, no rate limits, no usage caps — completely free forever. Works offline.

```bash
# 1. Install Ollama from https://ollama.com
# 2. Pull a coding model
ollama pull qwen2.5-coder:32b

# 3. That's it. DL Code auto-detects Ollama on localhost:11434.
```

**Recommended models for coding:**
- `qwen2.5-coder:32b` — Best overall (recommended)
- `deepseek-coder-v2` — Strong alternative
- `codellama` — Meta's Code Llama
- `llama3.2` — General purpose

### Option 2: Claude Code Agent (Most Powerful)

The [Claude Code CLI](https://claude.ai/code) runs as an autonomous agent inside DL Code. It can read and write files, run shell commands, and edit code in place — perfect for complex multi-step refactors.

```bash
npm install -g @anthropic/claude-code
```

DL Code automatically detects Claude Code and uses it for full agent mode.

### Option 3: Anthropic API (Direct)

For quick inline suggestions without installing anything locally. Add your API key in **Settings → AI**. Get a key from [console.anthropic.com](https://console.anthropic.com).

## ⚡ Agentic Builder

The agentic builder turns natural language into real, runnable code. Open it from the AI panel → Builder tab, or from the menu: **AI → Run Claude Code Agent**.

**How it works:**
1. Describe what you want to build in plain English
2. Pick a template (or let DL Code auto-detect)
3. Pick an AI provider (Ollama for free, Claude Code for power, API for direct)
4. Click **Build My App**
5. Watch as the AI scaffolds the project, writes every file, and installs dependencies

**Example prompts:**
- "A todo list app with React and TypeScript"
- "A REST API for a blog with Node.js and Express"
- "A Python script that scrapes weather data"
- "A CLI tool that converts JSON to YAML"
- "A static landing page for a coffee shop"
- "A Next.js blog with MDX"

The builder works with all three AI providers — so you can build unlimited apps for free using Ollama.

## 🎨 Theming

DL Code ships with a beautiful dark theme inspired by JetBrains Darcula. Want a different look? Switch themes in **Settings → General → Theme**, or install a theme pack from the Extensions panel.

Built-in themes: DL Dark (default), DL Light, VS Dark, VS Light, High Contrast. Plus 10 more via the bundled DL Theme Pack extension.

## 🔌 Extensions

DL Code has a real extension host. Extensions live in:

- **Windows:** `%APPDATA%/dl-code/extensions/<publisher.name>/`
- **macOS:** `~/Library/Application Support/dl-code/extensions/<publisher.name>/`
- **Linux:** `~/.config/dl-code/extensions/<publisher.name>/`

Each extension is a folder containing:
- `package.json` — manifest with activation events and contributions
- `main.js` — compiled JavaScript entry point
- `icon.png` — extension icon

The extension API is compatible with VS Code's, so many VS Code extensions can be ported with minimal changes.

## ⌨️ Keyboard Shortcuts

DL Code respects your muscle memory. Most VS Code and JetBrains shortcuts work out of the box.

| Action | Windows/Linux | macOS |
|--------|---------------|-------|
| Command Palette | `Ctrl+Shift+P` | `Cmd+Shift+P` |
| Quick Open File | `Ctrl+P` | `Cmd+P` |
| Toggle Sidebar | `Ctrl+B` | `Cmd+B` |
| Toggle Panel | `Ctrl+J` | `Cmd+J` |
| Toggle Terminal | `` Ctrl+` `` | `` Cmd+` `` |
| Search in Files | `Ctrl+Shift+F` | `Cmd+Shift+F` |
| Open AI Chat | `Ctrl+Shift+A` | `Cmd+Shift+A` |
| Save File | `Ctrl+S` | `Cmd+S` |
| New File | `Ctrl+N` | `Cmd+N` |
| Open Folder | `Ctrl+Shift+O` | `Cmd+Shift+O` |

## 🛠️ Tech Stack

DL Code is built with proven, reliable technologies:

- **Electron 33** — Cross-platform desktop framework
- **React 18** — UI library
- **TypeScript 5** — Type safety throughout
- **Monaco Editor** — The same editor that powers VS Code
- **xterm.js** — Terminal emulator
- **node-pty** — Real PTY for terminals
- **simple-git** — Git operations
- **Zustand** — State management
- **Vite** — Build tooling

## 📊 System Requirements

- **OS:** Windows 10+ (64-bit), macOS 10.15+, or any modern Linux distro
- **RAM:** 4 GB minimum (8 GB recommended)
- **Disk:** ~500 MB free space
- **For local AI (Ollama):** 8 GB RAM minimum (16 GB+ for larger models)

## 🗺️ Roadmap

- [ ] Code debugger (DAP - Debug Adapter Protocol)
- [ ] Remote development (SSH, Containers, WSL)
- [ ] Collaborative editing (Live Share)
- [ ] More language servers (Python, Go, Rust, Java)
- [ ] Built-in formatters (Prettier, Black, gofmt, rustfmt)
- [ ] Built-in linters (ESLint, pylint, golangci-lint)
- [ ] Mobile companion app
- [ ] Cloud sync for settings and extensions

Have an idea? [Open an issue](https://github.com/deathlegionteamlk/dl-code/issues) and let us know!

## 🤝 Contributing

We love contributions! Here's how to help:

1. ⭐ Star this repo — it helps others discover DL Code
2. 🐛 [Report bugs](https://github.com/deathlegionteamlk/dl-code/issues/new?labels=bug) you find
3. 💡 [Suggest features](https://github.com/deathlegionteamlk/dl-code/issues/new?labels=enhancement) you'd love to see
4. 🌍 Spread the word — tell a friend, share on social media
5. 🎨 Build extensions and share them with the community

## 📜 License

MIT — DL Code is free to use, modify, and distribute. See [LICENSE](LICENSE) for details.

## 💬 Community

- 🐛 [GitHub Issues](https://github.com/deathlegionteamlk/dl-code/issues) — Bug reports and feature requests
- 💬 [GitHub Discussions](https://github.com/deathlegionteamlk/dl-code/discussions) — Questions and community chat
- 🐦 [@deathlegionteam](https://twitter.com/deathlegionteam) — Updates and news

## 🙏 Acknowledgments

DL Code stands on the shoulders of giants:

- **[Monaco Editor](https://microsoft.github.io/monaco-editor/)** by Microsoft — the editor that powers VS Code
- **[Electron](https://www.electronjs.org/)** — cross-platform desktop apps with web tech
- **[React](https://react.dev/)** — UI library by Meta
- **[xterm.js](https://xtermjs.org/)** — terminal emulator
- **[Ollama](https://ollama.com/)** — local AI for everyone
- **[Anthropic](https://anthropic.com/)** — Claude AI
- **[simple-git](https://github.com/steveukx/git-js)** — Git for Node.js

---

<div align="center">

**[Download DL Code](https://github.com/deathlegionteamlk/dl-code/releases/latest)** · **[Visit Website](https://deathlegionteamlk.github.io/dl-code/)**

Made with ❤️ by [Death Legion Team](https://github.com/deathlegionteamlk) · Sri Lanka 🇱🇰

</div>
