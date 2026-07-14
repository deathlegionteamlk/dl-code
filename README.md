<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a1a2e,100:16213e&height=220&section=header&text=DL%20Code&fontSize=70&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=A%20free%20AI%20code%20editor%20that%20doesn't%20nag%20you%20for%20a%20subscription&descAlignY=55&descSize=18" width="100%"/>

<img src="https://readme-typing-svg.demolab.com/?lines=Claude+built+in.+Ollama+built+in.+No+API+key+required.;Describe+an+app,+watch+it+get+scaffolded.;Windows.+macOS.+Linux.+Pick+one.&font=Fira+Code&size=22&pause=1500&color=00D9FF&center=true&vCenter=true&width=700&height=50&duration=3000" alt="typing animation"/>

<br/>

[![Download](https://img.shields.io/badge/⬇️_Download-Free-brightgreen?style=for-the-badge)](https://github.com/deathlegionteamlk/dl-code/releases/latest)
[![Platforms](https://img.shields.io/badge/🖥️_Platforms-Win%20%7C%20Mac%20%7C%20Linux-blue?style=for-the-badge)](https://github.com/deathlegionteamlk/dl-code/releases/latest)
[![License](https://img.shields.io/badge/📄_License-MIT-yellow?style=for-the-badge)](LICENSE)
[![Version](https://img.shields.io/badge/🏷️_Version-1.0.0-orange?style=for-the-badge)](https://github.com/deathlegionteamlk/dl-code/releases/latest)

**[🌐 Website](https://deathlegionteamlk.github.io/dl-code/)** · **[📦 Download](https://github.com/deathlegionteamlk/dl-code/releases/latest)** · **[🐛 Report Bug](https://github.com/deathlegionteamlk/dl-code/issues)** · **[💡 Request Feature](https://github.com/deathlegionteamlk/dl-code/issues)**

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.gif" width="100%"/>

</div>

## 🤔 What is this thing?

DL Code is a code editor. We got tired of every "AI editor" on the market either locking the good models behind a subscription or shipping AI as a bolted-on sidebar that feels like an afterthought. So we built one where the AI is the point, and it costs nothing if you don't want it to.

Under the hood it's Monaco — the same editor VS Code uses — so your fingers already know where everything is. The look and feel borrows from JetBrains: dark, dense, no wasted pixels.

Run it with [Ollama](https://ollama.com) and you get a full AI coding assistant with zero API keys, zero rate limits, and zero recurring cost. It runs on your machine. Nobody's billing you per token.

<div align="center">
<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.gif" width="100%"/>
</div>

## ✨ What it actually does

- 🤖 **AI assistant, built in** — Claude sits inside the editor. Point it at a function, ask it to explain, refactor, write tests, kill a bug. It reads your open file, your selection, your workspace, not just whatever text you paste in.
- ⚡ **Agentic app builder** — Type "a todo app with React and TypeScript" and it scaffolds the whole thing: files, code, dependencies installed. Runs locally, no cloud round-trip required.
- 🆓 **Free AI via Ollama** — No API key. No rate limit. No usage cap. Works with the plane's wifi off. Supports Qwen 2.5 Coder, DeepSeek Coder v2, CodeLlama, Llama 3.2, and 50+ others.
- 🎨 **60+ languages highlighted** — TypeScript, Python, Rust, Go, Kotlin, Swift, SQL, Dockerfiles, Haskell, Elixir — if it's a real language, it's probably in there.
- 💻 **A terminal that's actually a terminal** — PTY-backed, bash/zsh/PowerShell/cmd, tabs, colors, clickable links. Not a fake text box pretending to be one.
- 🔄 **Git, without leaving the editor** — stage, unstage, commit, branch, diff, full history.
- 🔌 **Real extensions** — a proper extension host that loads from disk, VS Code-compatible API. Themes, linters, formatters, whatever you want to bolt on.
- 🔍 **Search that spans the whole workspace** — regex, case sensitivity, whole word, globs.
- ⌨️ **Command Palette + Quick Open** — `Ctrl+Shift+P` and `Ctrl+P` work exactly like you expect.
- 🌍 **Windows, macOS, Linux** — one codebase, three platforms, no "coming soon."

<div align="center">
<img src="https://media.giphy.com/media/13FrpeVH09Zrb2/giphy.gif" width="450" alt="demo placeholder — swap for a real screen recording"/>

*(swap this for an actual screen recording of the editor once you've got one — that sells it way better than any of these words)*
</div>

## 📦 Download

Grab a binary from the [Releases page](https://github.com/deathlegionteamlk/dl-code/releases/latest). No installer wizard, no account, no telemetry phoning home before you've even opened a file.

| Platform | File | Size | How to run |
|----------|------|------|------------|
| 🪟 **Windows** | `DL-Code-1.0.0-win-x64-portable.zip` | ~154 MB | Unzip, run `DL Code.exe` |
| 🍎 **macOS** | `DL-Code-1.0.0-macos-x64.zip` | ~345 MB | Unzip, drag to Applications, right-click → Open |
| 🐧 **Linux (AppImage)** | `DL-Code-1.0.0-linux-x86_64.AppImage` | ~144 MB | `chmod +x && ./DL-Code-*.AppImage` |
| 🐧 **Linux (.deb)** | `DL-Code_1.0.0_amd64.deb` | ~102 MB | `sudo dpkg -i DL-Code_*.deb` |
| 🐧 **Linux (tar.gz)** | `DL-Code-1.0.0-linux-x64.tar.gz` | ~143 MB | Extract, run `./dl-code` |

## 🤖 Setting up AI

Three providers. Switch between them anytime under **Settings → AI**.

### 1. Ollama — free, unlimited, runs on your machine (this is the one we'd pick)

```bash
# install Ollama from https://ollama.com
ollama pull qwen2.5-coder:32b

# that's it — DL Code finds it on localhost:11434 automatically
```

Models worth pulling:
- `qwen2.5-coder:32b` — the one we default to for a reason
- `deepseek-coder-v2` — a solid second opinion
- `codellama` — Meta's, does the job
- `llama3.2` — general purpose, not coding-specific

### 2. Claude Code Agent — when you need it to actually do things

The [Claude Code CLI](https://claude.ai/code) runs as an agent inside DL Code. It reads files, writes files, runs shell commands, edits code in place. This is the one for multi-step refactors you don't want to babysit line by line.

```bash
npm install -g @anthropic/claude-code
```

DL Code picks it up automatically once it's installed.

### 3. Anthropic API — no local setup, just a key

Fastest way to get inline suggestions if you don't want to install anything. Drop your key into **Settings → AI**. Keys come from [console.anthropic.com](https://console.anthropic.com).

<div align="center">
<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.gif" width="100%"/>
</div>

## ⚡ The agentic builder

Open it from the AI panel's **Builder** tab, or **AI → Run Claude Code Agent**.

1. Say what you want in plain English
2. Pick a template, or don't — it'll guess
3. Pick a provider: Ollama if you want it free, Claude Code if you want it powerful
4. Hit **Build My App**
5. Watch the files show up

**Prompts that work fine:**
- "A todo list app with React and TypeScript"
- "A REST API for a blog with Node.js and Express"
- "A Python script that scrapes weather data"
- "A CLI tool that converts JSON to YAML"
- "A static landing page for a coffee shop"
- "A Next.js blog with MDX"

Run it on Ollama and you can build as many of these as you want without ever touching a billing page.

## 🎨 Themes

Default is DL Dark, a Darcula-inspired theme. Change it in **Settings → General → Theme** or pull one from Extensions. Ships with DL Dark, DL Light, VS Dark, VS Light, High Contrast, plus 10 more in the bundled DL Theme Pack.

## 🔌 Extensions

Extensions live on disk, per platform:

- **Windows:** `%APPDATA%/dl-code/extensions/<publisher.name>/`
- **macOS:** `~/Library/Application Support/dl-code/extensions/<publisher.name>/`
- **Linux:** `~/.config/dl-code/extensions/<publisher.name>/`

Each one is a folder: `package.json` for the manifest, `main.js` as the entry point, `icon.png` for the icon. The API lines up with VS Code's, so a lot of existing extensions port over with minimal changes.

## ⌨️ Keyboard shortcuts

| Action | Windows/Linux | macOS |
|--------|---------------|-------|
| 🎛️ Command Palette | `Ctrl+Shift+P` | `Cmd+Shift+P` |
| 📂 Quick Open File | `Ctrl+P` | `Cmd+P` |
| 📑 Toggle Sidebar | `Ctrl+B` | `Cmd+B` |
| 📋 Toggle Panel | `Ctrl+J` | `Cmd+J` |
| 💻 Toggle Terminal | `` Ctrl+` `` | `` Cmd+` `` |
| 🔍 Search in Files | `Ctrl+Shift+F` | `Cmd+Shift+F` |
| 💬 Open AI Chat | `Ctrl+Shift+A` | `Cmd+Shift+A` |
| 💾 Save File | `Ctrl+S` | `Cmd+S` |
| 📄 New File | `Ctrl+N` | `Cmd+N` |
| 📁 Open Folder | `Ctrl+Shift+O` | `Cmd+Shift+O` |

## 🛠️ Built with

- **Electron 33** for the cross-platform shell
- **React 18** for the UI
- **TypeScript 5** everywhere
- **Monaco Editor** — same one VS Code runs
- **xterm.js** for the terminal
- **node-pty** for the actual PTY
- **simple-git** for git operations
- **Zustand** for state
- **Vite** for the build

Nothing exotic here. We picked things that work and stayed out of their way.

## 📊 What you need to run it

- Windows 10+ (64-bit), macOS 10.15+, or a Linux distro from the last few years
- 4 GB RAM minimum, 8 GB if you want it to feel good
- ~500 MB disk
- Running Ollama locally? Budget 8 GB+ RAM, 16 GB+ if you're pulling the bigger models

## 🗺️ What's next

- [ ] Debugger (DAP)
- [ ] Remote dev — SSH, containers, WSL
- [ ] Live Share-style collaborative editing
- [ ] More language servers (Python, Go, Rust, Java)
- [ ] Built-in formatters (Prettier, Black, gofmt, rustfmt)
- [ ] Built-in linters (ESLint, pylint, golangci-lint)
- [ ] Mobile companion app
- [ ] Settings/extension sync across machines

Missing something you actually want? [Open an issue](https://github.com/deathlegionteamlk/dl-code/issues) instead of just wishing for it.

## 🤝 Contributing

- ⭐ Star the repo, it's the cheapest way to help
- 🐛 [File bugs](https://github.com/deathlegionteamlk/dl-code/issues/new?labels=bug) when you hit them
- 💡 [Pitch features](https://github.com/deathlegionteamlk/dl-code/issues/new?labels=enhancement)
- 🌍 Tell someone who'd actually use this
- 🎨 Build an extension, share it

## 📜 License

MIT. Use it, fork it, ship it. See [LICENSE](LICENSE).

## 💬 Community

- 🐛 [GitHub Issues](https://github.com/deathlegionteamlk/dl-code/issues) — bugs and feature requests
- 💬 [GitHub Discussions](https://github.com/deathlegionteamlk/dl-code/discussions) — questions, general chat
- 🐦 [@deathlegionteam](https://twitter.com/deathlegionteam) — updates

## 🙏 Built on top of

- [Monaco Editor](https://microsoft.github.io/monaco-editor/) — Microsoft's editor, the one VS Code runs on
- [Electron](https://www.electronjs.org/) — the desktop shell
- [React](https://react.dev/) — UI
- [xterm.js](https://xtermjs.org/) — terminal emulator
- [Ollama](https://ollama.com/) — local AI, no strings
- [Anthropic](https://anthropic.com/) — Claude
- [simple-git](https://github.com/steveukx/git-js) — git for Node

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:16213e,100:1a1a2e&height=150&section=footer" width="100%"/>

**[⬇️ Download DL Code](https://github.com/deathlegionteamlk/dl-code/releases/latest)** · **[🌐 Visit Website](https://deathlegionteamlk.github.io/dl-code/)**

Made by [Death Legion Team](https://github.com/deathlegionteamlk) · Sri Lanka 🇱🇰

</div>
