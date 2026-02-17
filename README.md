Ah, got it! 😄 Shahmeer, the reason headings and formatting aren’t showing as **bold or proper headings** is because GitHub README files use **Markdown syntax**, not plain text. You need to add `#` for headings, `-` or `*` for lists, and triple backticks for code blocks.

Here’s your content converted to proper **Markdown** ready to paste in `README.md`:

---

````markdown
# OpenClaw Setup & Usage Guide

OpenClaw is a **headless AI agent framework**. It runs in the background (terminal/server) and lets you deploy AI agents that can work like **always-on employees**.

## Use it for:
- Persistent AI tasks
- Multi-channel monitoring & automation
- CLI/TUI-based control

## Supports:
- OpenAI GPT models (GPT-4, GPT-4o-mini, GPT-3.5)
- Claude (requires paid API key & credits)

---

## Requirements
- Windows 10/11 (WSL2) or Linux
- Node.js v20+
- npm latest
- Git
- OpenAI API Key (for testing, free trial works)
- Optional: Claude API key (paid)

---

## WSL Setup (Windows only)
Open PowerShell as admin:

```powershell
wsl --install
````

* Restart PC.
* Install Ubuntu from Microsoft Store.
* Open Ubuntu terminal and create a UNIX username when prompted.
* Update packages:

```bash
sudo apt update && sudo apt upgrade -y
```

---

## Node.js & npm

Install Node.js v20+:

```bash
curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash -
sudo apt install -y nodejs
```

Check versions:

```bash
node -v
npm -v
```

Upgrade npm (optional):

```bash
npm install -g npm@latest
```

---

## OpenClaw Installation

Clone the repo:

```bash
git clone https://github.com/openclaw/openclaw.git
cd openclaw
```

Install dependencies:

```bash
npm install
```

Install TUI daemon (optional):

```bash
openclaw onboard --install-daemon
```

---

## API Key Setup

OpenAI example:

```bash
export OPENAI_API_KEY="sk-your-openai-key"
```

Check key:

```bash
echo $OPENAI_API_KEY
```

⚠️ **Claude requires a paid API key and credits.**

---

## Running OpenClaw

**TUI mode (recommended):**

```bash
openclaw tui
```

**Hatch an agent:**

```bash
openclaw hatch
```

Inside TUI:

* Change model:

```bash
/model gpt-4o-mini
```

* Send message:

```bash
/say hello
```

---

## Optional Skills

During setup, OpenClaw may ask to install skills:

* 1password, blogwatcher, camsnap, clawhub, github, openai-whisper, etc.
* Skip any you don’t need
* Some skills require API keys (e.g., `GOOGLE_PLACES_API_KEY`)

---

## Troubleshooting

* No response in TUI → check API key, Node.js ≥20
* Network/npm issues:

```bash
npm config set registry https://registry.npmjs.org/
npm install
```

* Node.js version error → upgrade using NodeSource script
* Command not found → `npm install -g` or run `npx openclaw tui`

---

## Tips

* Test with OpenAI free trial first
* Persistent agents require paid API
* Export API key in terminal before running OpenClaw
* Keep dependencies updated:

```bash
npm update
```

---

## Example Commands

Set API key:

```bash
export OPENAI_API_KEY="sk-xxxx"
```

Start TUI:

```bash
openclaw tui
```

Hatch main agent:

```bash
openclaw hatch --agent main
```

Change model:

```bash
/model gpt-4o-mini
```

Send a message:

```bash
/say Hello OpenClaw!
```

```

---



Do you want me to do that too?
```
